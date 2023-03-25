---
title: "KDE Plasma Widget Boilerplate (QML)"
date: 2023-03-25T12:11:59+07:00
draft: false
description: "How to develop a simple KDE plasma 5 applet"
tags: ["linux","kde","plasma5","plasma-applet","qml"]
---

Saya adalah pehobi Linux untuk desktop. Khusus *desktop environment* KDE, saya sudah cukup setia sebagai penggunanya sejak masa transisi KDE Plasma 4 menjadi Plasma 5, yaitu sekitar tahun 2015.
Pada Plasma 4, ada satu *applet* yang saya suka, namanya [Mawakit](https://store.kde.org/p/998939 "Mawakit - KDE Store").
Dia berfungsi sebagai pengingat waktu sholat dan menampilkan jadwalnya.

Setelah *update* ke Plasma 5 dan saya semakin suka karena *image* bahwa KDE 4 itu berat sudah tidak relevan, ternyata widget itu tidak bisa diinstall karena secara kode memang spesifik menggunakan API Plasma 4.
Ternyata saat itu pun kode sumber sudah cukup lama tidak dirawat.

Sampai akhirnya beberapa tahun belakangan saya kembali teringat pada widget tersebut setelah menunggu lama dan sampai lupa.
Lupa kalau salah satunya dari dia lah saya menjadi pengguna setia KDE.

Dari situ saya menginisiasi untuk membuat widget serupa karena belum menemukan penggantinya.
Eksekusinya sudah saya mulai sekitar tiga tahun yang lalu.
Dan akhirnya sekarang sudah bisa digunakan walaupun fiturnya tidak sebanyak Mawakit.

![Plasma widget Usalli](/blog/img/2023/03/screen_101402.png "Screenshot plasma applet usalli")

Kode sumber *applet* tersebut ada di [repo Github ini](https://github.com/aryo-sr/plasma-applet-usalli).

Pada tulisan ini saya akan *share* template untuk membuat sebuah *applet/widget/plasmoid* di KDE Plasma.

### Struktur file

Berikut adalah struktur minimal file widget. `<namespace>` adalah nama ID yang juga didefinisikan pada `metadata.json`.

```
<namespace>
|- contents
   |- ui
      |- main.qml
   |- icons
      |- custom-icon.svg
|- metadata.json
```

Folder `<namespace>` akan diinstall di `~/.local/share/plasma/plasmoids/`.
Folder `icons` tidak wajib, kecuali kita ingin menampilkan ikon *custom*.
File `custom-icon.svg` perlu di-copy ke `./local/share/icons/` karena saat tulisan ini dibuat, sepertinya masih implementasi awal.
Karena pada standar sebelumnya, tampilan ikon didefinisikan pada file `metadata.desktop`, bukan json.

### File metadata.json

```
{
    "KPlugin": {
        "Authors": [
            {
                "Email": "valid@email.address",
                "Name": "Your Name"
            }
        ],
        "Category": "Date and Time",
        "Description": "A short description shown on about window",
        "Icon": "custom-icon.svg",
        "Id": "<namespace>",
        "Name": "Fancy Name",
        "ServiceTypes": [
            "Plasma/Applet"
        ],
        "Version": "0.0.1",
        "Website": "https://github.com/johndoe/simple-kde-widget"
    },
    "X-Plasma-API": "declarativeappletscript",
    "X-Plasma-MainScript": "ui/main.qml"
}
```

*Category* bisa mengacu pada halaman dokumentasi KDE[^1]. *Id* harus sesuai dengan nama folder `<namespace>` di atas. *X-Plasma-MainScript* merujuk pada file QML utama, pada contoh di atas hanya ada satu file yakni di dalam folder `contents/ui/main.qml`.

### File `main.qml`

```
import QtQuick 2.0
import org.kde.plasma.plasmoid 2.0
import org.kde.plasma.core 2.0 as PlasmaCore

// Item - the most basic plasmoid component, an empty container.
Item {
    
    // IconItem - a simple item to display an icon
    PlasmaCore.IconItem {
        
        // source - the icon to be displayed
        source: "face-smile"
        
        // height & width set to equal the size of the parent item (the empty "Item" above)
        width: parent.width
        height: parent.width
    }
}
```

Kode di atas akan menghasilkan widget yang menampilkan icon `face-smile`. 
Kode merupakan contoh pada halaman dokumentasi KDE yang lama.
Untuk panduan terbaru, silakan menuju halaman dokumentasi KDE[^2].
Untuk sampel kode lebih lengkap bisa merujuk ke repo Githubnya[^3].


[^1]: [Plasmoid Guidelines](https://community.kde.org/Plasma/PlasmoidGuidelines#Category_Names)
[^2]: [Plasma Widget Tutorial](https://develop.kde.org/docs/plasma/widget/)
[^3]: [plasma-framework - Github](https://github.com/KDE/plasma-framework/tree/master/templates/qml-plasmoid)