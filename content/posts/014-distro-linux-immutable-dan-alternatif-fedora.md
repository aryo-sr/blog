---
title: "Distro Linux Immutable dan Alternatif Fedora"
date: 2023-07-09T17:02:12+07:00
draft: false
description: "Mengikuti tren perkembangan model OS distro linux dengan konsep immutable"
tags: ["linux", "fedora", "opensuse", "ubuntu", "immutable-os"]
images:
    - img/2023/07/opensusemicroos_1.png
    - img/2023/07/opensusemicroos_2.png
    - img/2023/07/opensusemicroos_3.png
    - img/2023/07/opensusemicroos_4.png
    - img/2023/07/opensusemicroos_5.png
    - img/2023/07/opensusemicroos_6.png
summary: "Tren OS distro linux terus berganti seiring waktu. Saat ini konsep *immutable system* semakin jamak diusung oleh distro-distro mainstream. Fedora termasuk yang terdepan dalam implementasi konsep ini sejak versi 31 melalui CoreOS untuk ranah server. Kemudian dikembangkan lagi untuk desktop melalui spin Silverblue yang menggunakan GNOME, Kinoite menggunakan KDE dan Sericea menggunakan Sway tiling window manager."
---

Tren OS distro linux terus berganti seiring waktu.
Saat ini konsep *immutable system* semakin jamak diusung oleh distro-distro mainstream.
Fedora termasuk yang terdepan dalam implementasi konsep ini sejak versi 31 melalui CoreOS untuk ranah server[^1].
Kemudian dikembangkan lagi untuk desktop melalui spin Silverblue yang menggunakan GNOME, Kinoite menggunakan KDE dan Sericea menggunakan Sway tiling window manager.

Konsep immutable ini sebenarnya sudah lebih lama dipakai oleh distro NixOS yang pertama kali muncul tahun 2003[^2].
MacOS juga mengusung konsep ini melalui SIP (System Integrity Protection).
Beberapa waktu lalu, Ubuntu mengumumkan akan mengusung konsep ini melalui Ubuntu Core[^3].

Saat ini saya sedang mempersiapkan untuk beralih ke sistem immutable OS ini untuk *daily driver*.
Bersamaan dengan itu, saya merasa perlu mengganti distro juga karena lanskap per-distro-an linux sudah mencapai titik jenuh.
Seperti yang dikatakan Nick juga[^4], konsep distro linux sudah *broken*.
Segmentasi alias banyaknya jumlah distro sudah tak terbendung.
Meskipun ini menunjukkan *true freedom* dari semangat *free software*, ada sisi yang cenderung negatif.
Yakni bisa memunculkan FOMO dan FOBO[^5] bagi user baru.

Selain itu, semakin ke sini, semangat komunitas *open source* pada distro linux bisa dikatakan sudah cenderung berorientasi profit.
Tak dapat dipungkiri bahwa kebanyakan distro mainstream adalah produk *open* dari korporasi besar, semacam Red Hat, Canonical.
Sejak Red Hat "dibeli" oleh IBM, langkah-langkah korporasinya sangat tidak bersahabat bagi komunitas open source.
Dalam hal ini adalah berakhirnya CentOS yang *free* yang mendorong komunitas untuk membuat *fork*-nya menjadi distro baru.
Walaupun sebenarnya bukan benar-benar karena akuisisi, karena Red Hat sudah sejak lama bergantung pada "komunitas" untuk mencari profit.[^6]

Sampai saat ini, saya sudah cukup lama menjadikan Fedora (produk Red Hat) sebagai OS utama untuk *daily driver*.
Dengan perkembangan saat ini, rasanya sudah saatnya saya mengganti OS.
Setelah melakukan riset singkat, saya rasa akan beralih ke openSUSE MicroOS.
Dia mengusung konsep immutable, sama seperti CoreOS Fedora.
Metode instalasi aplikasi / program menggunakan Flatpak, yang juga dipakai Fedora.
Sandboxing menggunakan `toolbox` yang juga memakai `podman`, serupa yang ada di Fedora Silverblue.
Jadi, saya tidak perlu banyak *re-learning* untuk terbiasa pada sistem operasi baru ini.
Apalagi, saya sempat menjadikan openSUSE tumbleweed sebagai *daily driver*.

Karena saya lebih memilih KDE sebagai *desktop environment*, maka saya pilih varian MicroOS Kalpa.

![openSUSE MicroOS](/blog/img/2023/07/opensusemicroos_1.png "Screenshot openSUSE microOS booting")
![openSUSE MicroOS install](/blog/img/2023/07/opensusemicroos_2.png "Screenshot openSUSE microOS install")
![openSUSE MicroOS kalpa screen](/blog/img/2023/07/opensusemicroos_3.png "Screenshot openSUSE microOS kalpa first time login")
![openSUSE MicroOS kde system](/blog/img/2023/07/opensusemicroos_4.png "Screenshot openSUSE microOS kde system information")
![openSUSE MicroOS kde monitor](/blog/img/2023/07/opensusemicroos_5.png "Screenshot openSUSE microOS kde system monitor")
![openSUSE MicroOS kde discover](/blog/img/2023/07/opensusemicroos_6.png "Screenshot openSUSE microOS installing app")

Sementara ini masih dicoba pada *virtual machine*, karena perlu waktu untuk migrasi data-data dari komputer utama.

[^1]: https://fedoramagazine.org/introducing-fedora-coreos/
[^2]: https://en.wikipedia.org/wiki/NixOS
[^3]: https://ubuntu.com/blog/ubuntu-core-an-immutable-linux-desktop
[^4]: https://www.youtube.com/watch?v=8yAo9Bc6iOI
[^5]: *fear of missing out, fear of better options*
[^6]: https://dissociatedpress.net/2023/07/03/red-hat-and-the-clone-wars-iii-the-dawn-of-centos/