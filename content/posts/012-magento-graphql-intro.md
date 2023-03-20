---
title: "Magento GraphQL Intro"
date: 2023-03-20T16:30:07+07:00
draft: false
description: "Pengenalan pengembangan API dengan GraphQL di Magento"
tags: ["magento","graphql","api"]
---

Baiklah, untuk menghidupkan kembali blog ini, kali ini saya kembali membahas tentang Magento.
Sejak medio 2021 lalu, saya kembali bekerja 9-5 dan masih berfokus dengan spesialisasi Magento.
Sebagian *task* yang saya kerjakan berkaitan dengan *frontend* terpisah dan berkomunikasi dengan *backend* menggunakan API, yakni GraphQL.
Oleh karena itu, untuk memulai lagi posting secara rutin --semoga konsisten, sebaiknya saya menulis tentang GraphQL.

Dukungan GraphQL di Magento mulai dimasukkan ke *core framework* kira-kira sejak versi 2.3.4, atau sekitar tiga tahun lalu.
Kemudian Magento merilis *framework* untuk *frontend* terpisah berbasis React bernama PWA Studio.
Dan *framework* ini sangat bergantung pada GraphQL untuk berkomunikasi dengan *headless* Magento.

### Struktur File

Berikut adalah struktur minimum skrip-skrip untuk membuat *custom endpoint* GraphQL.

```
etc
|- module.xml
|- schema.graphqls
Model
|- Resolver
   |- QueryResolver.php
registration.php
```

`Model/Resolver` adalah lokasi yang disarankan untuk class yang menangani value keluaran GraphQL.

Berikut adalah contoh isi dari `schema.graphqls`

```
type Query {
    customer: Customer @resolver(class: "Magento\\CustomerGraphQl\\Model\\Resolver\\Customer")
}

type Customer @doc(description: "Defines the customer name, addresses, and other details.") {
    group_id: Int @deprecated(reason: "Customer group should not be exposed in the storefront scenarios.")
    prefix: String @doc(description: "An honorific, such as Dr., Mr., or Mrs.")
    firstname: String @doc(description: "The customer's first name.")
    middlename: String @doc(description: "The customer's middle name.")
    lastname: String @doc(description: "The customer's family name.")
    suffix: String @doc(description: "A value such as Sr., Jr., or III.")
    email: String @doc(description: "The customer's email address. Required.")
    ...
}
```

Berikut adalah contoh class resolver dari custom query di atas:

```
<?php
/**
 * Copyright © Magento, Inc. All rights reserved.
 * See COPYING.txt for license details.
 */
declare(strict_types=1);

namespace Magento\CustomerGraphQl\Model\Resolver;

use ...

/**
 * Customers field resolver, used for GraphQL request processing.
 */
class Customer implements ResolverInterface
{
    ...

    /** 
     * @inheritdoc
     */
    public function resolve(
        Field $field,
        $context,
        ResolveInfo $info,
        array $value = null,
        array $args = null
    ) { 
        /** @var ContextInterface $context */
        if (false === $context->getExtensionAttributes()->getIsCustomer()) {
            throw new GraphQlAuthorizationException(__('The current customer isn\'t authorized.'));
        }   

        $customer = $this->getCustomer->execute($context);
        return $this->extractCustomerData->execute($customer);
    }   
}

```

### Calling Endpoint

Untuk memanggil *endpoint* pada contoh di atas, berikut adalah contoh payloadnya:

```
query {
    customer {
       firstname
       lastname
       email
       group_id
    }
}
```

URL *endpoint* GraphQL defaultnya adalah `<base_url>/graphql`.

Untuk *payload* di atas, perlu *token bearer* pada *request header*. Contoh lengkap dengan cURL:

```
curl -L 'https://magento.localhost/graphql' \
    -H 'Authorization: Bearer eyJraWQiOiIxIiwiYWxnIjoiSFMyNTYifQ.eyJ1aWQiOjEsInV0eXBpZCI6MywiaWF0IjoxNjc5MzA3NjQ4LCJleHAiOjE2NzkzMTEyNDh9.k4vrVTDT7py-eLoFptF3al4FIkYRzNQM4jS6nJEECKM' \
    -H 'Content-Type: application/json' \
    -d '{"query":"{\n  customer {\n    firstname\n    lastname\n    email\n    group_id\n  }\n}","variables":{}}'
```

Return datanya sebagai berikut:

```
{
    "data": {
        "customer": {
            "firstname": "test",
            "lastname": "first",
            "email": "quauteullaujuno-8138@yopmail.com",
            "group_id": null
        }
    }
}
```

Bearer token bisa diambil dengan mutation GraphQL lainnya, yakni `generateCustomerToken`[^1]


[^1]: [Laman dokumentasi Magento](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/generate-token/).