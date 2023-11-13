---
title: Perbandingan Aplikasi Note-Taking Gratis dan Multiplatform
date: 2023-11-13T19:19:21.007Z
draft: false
description: "Perbandingan beberapa aplikasi note-taking plain-text yang open source maupun berbayar untuk produktivitas kerja: Zettlr, Joplin, Obsidian, dan QOwnNotes"
tags:
  - tool
  - app
  - produktivitas
  - markdown
  - linux
locale: id_ID
images:
  - img/2023/11/1-google-keep.png
  - img/2023/11/2-onenote.png
  - img/2023/11/3-all-apps.png
  - img/2023/11/4-zettlr-sitasi.png
  - img/2023/11/5-zettlr-grafik.png
  - img/2023/11/6-joplin-main.png
  - img/2023/11/7-joplin-plugin.png
  - img/2023/11/8-obsidian-grafik.png
  - img/2023/11/9-obsidian-plugin.png
  - img/2023/11/10-qownnotes-latex.png
  - img/2023/11/11-klatexformula.png
summary: Aplikasi yang dibahas antara lain Zettlr, Joplin, Obsidian, dan QOwnNotes. Keempatnya dipilih berdasarkan kriteria utama dalam pembahasan ini yakni dukungan file teks dasar, umumnya dalam format Markdown. Kriteria tambahannya adalah dukungan untuk teknik Zettelkasten, yakni sistem penyimpanan catatan kecil yang terorganisir dengan baik. Selain itu pula, yang paling penting ada dukungan multi-platform.
---

_Well noted_, sebuah frasa yang sering kita dengar saat kita bekerja, atau kita sendiri yang suka mengucapkannya.
Penggunaan frasa afirmasi tersebut menandakan bahwa orang yang mengucapkannya telah mengerti dan memahami sepenuhnya apa yang baru saja didengar.
Sebenarnya dia tidak perlu membuat _note_ atas apa yang didengarkan tersebut[^1], namun akan lebih bagus jika benar-benar mencatat poin-poin yang didengarnya tersebut.

Untuk menaruh catatan-catatan, kita bisa memanfaatkan aplikasi selain menuliskannya pada kertas.
Ada banyak aplikasi _note-taking_ yang tersedia, baik berbayar maupun gratis.
Contohnya Keep (Google), OneNote, Notion, Evernote, dll.
Aplikasi-aplikasi semacam itu lebih disukai untuk _note-taking_ daripada program perkantoran pada umumnya seperti Microsoft Word atau LibreOffice Writer.
Aplikasi pada ponsel pintar lainnya juga menjadi pilihan karena ringkas.

![Google Keep](/blog/img/2023/11/1-google-keep.png)

![Microsoft OneNote](/blog/img/2023/11/2-onenote.png)

Kali ini adalah ulasan untuk beberapa aplikasi _note-taking_ alternatif yang gratis maupun berbayar, baik _closed_ maupun _open source_.
Aplikasi yang dibahas antara lain Zettlr, Joplin, Obsidian, dan QOwnNotes.
Keempatnya dipilih berdasarkan kriteria utama dalam pembahasan ini yakni dukungan file teks dasar, umumnya dalam format Markdown.
Kriteria tambahannya adalah dukungan untuk teknik Zettelkasten, yakni sistem penyimpanan catatan kecil yang terorganisir dengan baik[^2] [^3].
Selain itu pula, yang paling penting ada dukungan multi-platform.

> *In recent years, the centuries old technique of utilizing a Zettelkasten to organize your knowledge has seen a revival.*[^4]

Dukungan _plain-text_ menjadi poin utama karena supaya terhindar dari _lock-in_ penyedia layanan jika kita sudah tidak akan memakai layanan tersebut, sebut saja yang berbasis _cloud_ atau SaaS.
Dengan file teks biasa, kita akan dengan mudah mengelolanya, semudah _copy-paste_ sebuah folder ke penyimpanan data lain.
Kita juga memiliki kemerdekaan kepemilikan atas catatan-catatan tersebut.
Kita juga bisa dengan leluasa memilih tempat untuk _backup_ atau sinkronisasinya.
Misalnya ke _cloud self-hosted_ punya kita sendiri, semacam NextCloud, OwnCloud, dsb.

![Aplikasi dijalankan pada desktop Linux](/blog/img/2023/11/3-all-apps.png)

Kemudian, untuk teknik Zettelkasten sendiri adalah metode kreatif yang diperkenalkan oleh Niklas Luhmann sebagai teknik belajar efektif
dengan mencatat kutipan dari buku yang dibaca dan menjadi inspirasi untuk ide baru, dan kutipan tersebut ditulis dalam bentuk parafrasa.
Catatan ditulis dalam potongan kertas, dan kumpulan kertas tersebut disimpan dalam kotak dan dikelompokkan berdasarkan kategori dan index yang bisa berkembang seiring bertambahnya informasi dari referensi lain.[^3]

Niklas Luhmann (1927–1998) adalah seorang sosiolog Jerman dan salah satu tokoh paling terkemuka di bidang teori sistem sosiologi.
Ia dikenal karena karyanya yang luas tentang teori sistem sosial, khususnya untuk mengembangkan dan memajukan konsep autopoiesis dalam konteks sosial.[^5]

Berikut adalah uraian singkat tentang beberapa aplikasi _note-taking_ yang mengutamakan _plain-text_ sebagai format media simpan.

## Zettlr

Zettlr adalah aplikasi pencatatan yang menggabungkan antarmuka yang bersih dan ramah pengguna dengan fitur-fitur canggih yang dirancang untuk peneliti, penulis, dan insan ilmiah.

- **Editor Markdown:**
  Zettlr menawarkan editor Markdown yang kuat, memberi pengguna alat sederhana namun serbaguna untuk menyusun dan memformat catatan.

- **Kutipan dan Integrasi BibTeX:**
  Fitur penting adalah integrasi kutipan dan dukungan BibTeX, menjadikannya pilihan menarik bagi pengguna akademis dan berorientasi penelitian.

- **Prinsip Zettelkasten:**
  Zettlr selaras dengan prinsip Zettelkasten, mendorong pembuatan catatan atomik dan mendukung tautan dua arah untuk basis pengetahuan yang lebih saling berhubungan.
  Teknik Zettelkasten-lah yang menjadi motivasi utama dibangunnya aplikasi Zettlr.
  Tautan antar-catatan dapat dilihat dengan tampilan grafik, yang mana pengguna dapat memvisualisasikannya.

- **Tema yang Dapat Disesuaikan:**
  Aplikasi ini menawarkan tema yang dapat disesuaikan, memungkinkan pengguna mempersonalisasi ruang kerja dan meningkatkan keterbacaan berdasarkan preferensi.

- **Ekspor dan Penerbitan:**
  Zettlr memfasilitasi ekspor catatan dengan mudah dalam berbagai format, sehingga memudahkan pengguna untuk berbagi atau mempublikasikan karya.

- **Dukungan LaTeX:**
  Zettlr mendukung LaTeX untuk penyusunan huruf matematis namun memerlukan instalasi LaTeX di sistem.
  Pengguna dapat memasukkan kode LaTeX ke dalam dokumen Markdown mereka di Zettlr.
  Aplikasi ini merender persamaan dan simbol LaTeX selama pratinjau, memungkinkan penyertaan ekspresi matematika yang kompleks.

- **Dukungan Lintas Platform:**
  Tersedia untuk Windows, macOS, dan Linux, Zettlr memastikan pengalaman pencatatan yang konsisten di berbagai sistem operasi. 
  Dikembangkan menggunakan framework Electron, yang merupakan kerangka kerja 
  untuk membangun aplikasi desktop lintas platform menggunakan teknologi web seperti HTML, CSS, dan JavaScript,
  sama seperti Obsidian dan Joplin.

- **Fitur Kolaborasi:**
  Pengeditan Kolaboratif: Zettlr menyertakan fitur untuk pengeditan kolaboratif, sehingga cocok untuk kerja tim dan proyek kelompok.

![Pengaturan Sitasi Zettlr](/blog/img/2023/11/4-zettlr-sitasi.png)

![Tampilan Grafik Antar-Catatan](/blog/img/2023/11/5-zettlr-grafik.png)

## Joplin

Joplin adalah aplikasi pencatatan sumber terbuka dengan fokus pada privasi, sinkronisasi, dan fleksibilitas. Ia menawarkan berbagai fitur yang memenuhi berbagai kebutuhan pengguna.

- **Enkripsi Ujung-ke-Ujung:**
  Joplin mengutamakan privasi pengguna dengan enkripsi end-to-end, memastikan informasi sensitif tetap aman.

- **Dukungan Markdown:**
  Aplikasi ini mendukung Markdown untuk pemformatan teks, memberi pengguna cara sederhana namun efektif untuk menyusun catatan.

- **Sinkronisasi Lintas Platform:**
  Joplin memungkinkan sinkronisasi antar perangkat menggunakan berbagai layanan cloud, 
  meningkatkan aksesibilitas dan memastikan pengguna memiliki catatan ke mana pun mereka pergi.

- **Catatan Organisasi:**
  Catatan dapat diatur ke dalam buku catatan dan tag, memberikan pengguna opsi fleksibel untuk menyusun informasi.

- **Daftar Tugas dan Manajemen Tugas:**
  Joplin menyertakan fitur untuk membuat daftar tugas dan mengelola tugas, menjadikannya alat serbaguna untuk pencatatan dan produktivitas.

- **Pemotong Web:**
  Ekstensi web clipper memungkinkan pengguna menyimpan artikel dan halaman web langsung ke Joplin, 
  menyederhanakan proses pengambilan informasi online pada _browser_.

- **Dukungan Plugin:**
  Joplin mendukung plugin, memungkinkan pengguna untuk memperluas fungsionalitas aplikasi berdasarkan kebutuhan spesifik mereka.[^6]

- **Dukungan LaTeX:**
  Joplin juga mendukung LaTeX untuk rumus matematika.
  Pengguna dapat menulis kode LaTeX dalam catatan Markdown mereka, dan Joplin akan merender konten matematika selama pratinjau.
  Hal ini sangat berguna bagi pengguna yang membutuhkan notasi matematika dalam catatannya.

![Jendela utama Joplin](/blog/img/2023/11/6-joplin-main.png)

![Plugin Joplin](/blog/img/2023/11/7-joplin-plugin.png)

## Obsidian

Obsidian adalah aplikasi pencatatan yang dirancang untuk manajemen pengetahuan, dikenal karena penekanannya pada teks biasa dan interkonektivitas.

- **Fitur Utama:**
   - Dukungan Markdown: Obsidian mendukung Markdown untuk pemformatan teks, sehingga memudahkan pembuatan catatan yang terstruktur dengan baik.[^7]
   - Tampilan Grafik: Salah satu fitur khasnya adalah tampilan grafik, yang memungkinkan pengguna memvisualisasikan hubungan antara catatan yang berbeda.
   - Tautan Dua Arah: Aplikasi ini mendorong penggunaan tautan dua arah, memungkinkan jaringan pemikiran dan ide yang terhubung.

- **Kasus Penggunaan:**
   - Penelitian: Obsidian populer di kalangan peneliti karena kemampuannya mengatur dan menghubungkan catatan penelitian, mendorong pemahaman yang lebih dalam tentang topik yang kompleks.
   - Penulisan: Penulis menghargai kesederhanaan platform dan fokus pada hubungan antar ide.

- **Dukungan LaTeX:**
  Obsidian memiliki dukungan LaTeX yang kuat. Pengguna dapat memasukkan sintaksis LaTeX untuk persamaan matematika, simbol, dan pemformatan dalam catatan.
    Editor Markdown bawaan di Obsidian merender kode LaTeX secara efektif, memberikan pengalaman yang lancar bagi pengguna yang membutuhkan notasi matematika dalam catatan mereka.

- **Kustomisasi:**
  (Tema dan Plugin) Obsidian memungkinkan pengguna untuk menyesuaikan aplikasi melalui tema dan plugin, meningkatkan pengalaman dan fungsionalitas pengguna.

- **Komunitas dan Ekosistem:**
   - Komunitas Aktif: Obsidian memiliki komunitas pengguna yang dinamis, dengan forum dan diskusi seputar praktik terbaik dan kasus penggunaan.
   - Plugin Pihak Ketiga: Aplikasi ini mendukung plugin pihak ketiga, memperluas fungsinya berdasarkan kebutuhan pengguna.
   Salah satunya adalah plugin komunitas untuk sinkronisasi ke WebDav, sebagai alternatif sinkronisasi berbayar yang disediakan oleh pengembang.
   Ada pula plugin komunitas untuk mengenkripsi catatan tunggal dengan kata sandi yang kita tentukan.

![Tampilan grafik Obsidian](/blog/img/2023/11/8-obsidian-grafik.png)

![Plugin komunitas Obsidian](/blog/img/2023/11/9-obsidian-plugin.png)

## QOwnNotes

QOwnNotes adalah aplikasi pencatatan sumber terbuka lintas platform dengan fokus pada teks biasa, keserbagunaan, dan opsi penyesuaian yang luas.

- **Editor dan Pratinjau Markdown:**
  QOwnNotes menampilkan editor Markdown dengan pratinjau langsung, memberikan pengguna tampilan _real-time_ tentang bagaimana catatan akan ditampilkan.

- **Struktur Folder dan Penandaan:**
  Aplikasi ini memungkinkan pengguna untuk mengatur catatan menggunakan struktur folder dan tag, memberikan fleksibilitas dalam mengkategorikan dan mengambil informasi.

- **Dukungan Enkripsi:**
  QOwnNotes mendukung enkripsi catatan individual, memastikan keamanan informasi sensitif yang disimpan dalam aplikasi.

- **Integrasi Kontrol Versi:**
  Integrasi dengan sistem kontrol versi, seperti Git, memungkinkan pengguna melacak perubahan dalam catatan dari waktu ke waktu, memberikan riwayat versi.

- **Manajemen tugas:**
  QOwnNotes menyertakan fitur manajemen tugas, memungkinkan pengguna membuat daftar tugas dan melacak tugas di samping catatan.

- **Kustomisasi:**
  Opsi penyesuaian yang luas mencakup tema, gaya, dan dukungan skrip, memberdayakan pengguna untuk menyesuaikan aplikasi dengan preferensi mereka.

- **Dukungan LaTeX:**
  QOwnNotes memiliki dukungan LaTeX dengan skrip pihak ketiga, dan memerlukan aplikasi tambahan `klatexformula` beserta instalasi LaTeX di sistem.
  Ini memungkinkan pengguna untuk memasukkan ekspresi matematika menggunakan sintaks LaTeX dalam catatan mereka.
  Fitur ini melayani pengguna yang perlu bekerja dengan konten matematika dalam dokumen QOwnNotes mereka.

- **Sinkronisasi Lintas Platform:**
  QOwnNotes mendukung sinkronisasi lintas platform, memungkinkan pengguna mengakses catatan mereka di beberapa perangkat.

![Setting LaTeX](/blog/img/2023/11/10-qownnotes-latex.png)

![klatexformula](/blog/img/2023/11/11-klatexformula.png)

## Rangkuman

**Kesimpulan: Fitur Utama Aplikasi _Note-Taking_**

Dalam menjelajahi aplikasi pencatatan seperti Obsidian, Zettlr, Joplin, dan QOwnNotes, muncul beberapa tema umum dan fitur menonjol:

1. **Dukungan Markdown:**
  Semua aplikasi memprioritaskan Markdown sebagai fitur mendasar, memberi pengguna cara serbaguna dan terstruktur untuk memformat catatan.

2. **Organisasi dan Penandaan:**
  Setiap aplikasi menawarkan alat organisasi seperti folder, buku catatan, tag, atau kombinasi dari semuanya, 
  memungkinkan pengguna untuk mengkategorikan dan mengambil informasi secara efisien.

3. **Privasi dan Keamanan:**
  Joplin dan QOwnNotes menonjol karena penekanannya pada privasi pengguna, 
  menawarkan fitur enkripsi ujung ke ujung untuk mengamankan data sensitif.
  Obsidian ada plugin komunitas yang menyediakan fitur enkripsi catatan.
  Zettlr juga menyediakan fitur enkripsi catatan menggunakan algoritma AES maupun PGP.

4. **Interkonektivitas dan Tautan:**
  Obsidian dan Zettlr menganut prinsip Zettelkasten, mendorong penciptaan catatan atomik dan mendorong interkonektivitas melalui tautan dua arah antar-catatan.

5. **Kustomisasi:**
  Obsidian, Joplin, dan QOwnNotes menyediakan opsi penyesuaian yang luas,
  memungkinkan pengguna mempersonalisasi pengalaman membuat catatan melalui tema, gaya, dan dukungan skrip pada QOwnNotes.
  Sampai tulisan ini dibuat, Zettlr belum ada dukungan untuk plugin[^8].

6. **Sinkronisasi Lintas Platform:**
  Joplin, QOwnNotes, dan Zettlr mendukung sinkronisasi lintas platform, memastikan pengguna dapat mengakses catatan mereka dengan lancar di berbagai perangkat.
  Obsidian menyediakan sinkronisasi dalam langganan berbayarnya, dan ada alternatif gratis disediakan oleh plugin komunitas.

7. **Manajemen Tugas:**
  Joplin dan QOwnNotes mengintegrasikan fitur manajemen tugas, memungkinkan pengguna membuat daftar tugas dan mengelola tugas di samping catatan.
  Obsidian juga sudah menyediakan pengelola tugas dengan plugin bawaan.

8. **Integrasi Kontrol Versi:**
  QOwnNotes terintegrasi dengan sistem kontrol versi seperti Git, menawarkan pengguna kemampuan untuk melacak perubahan dan memelihara riwayat versi catatan.
  Obsidian juga ada plugin komunitas yang menyediakan fitur tersebut.
  Joplin dan Zettlr pada dasarnya juga bisa menggunakan sistem kontrol versi, namun perlu dikelola secara manual dari luar aplikasi.

9. **Dukungan LaTeX**:
  Semuanya dapat diatur agar bisa mendukung pemformatan ekspresi LaTeX untuk keperluan menampilkan notasi matematika kompleks.

10. **Kebebasan Pengguna**:
    - **Obsidian:** Obsidian adalah satu-satunya yang bukan aplikasi open source dari keempat yang dibahas di sini.
    Meskipun menawarkan versi gratis, dia tidak diklasifikasikan sebagai perangkat lunak bebas dan sumber terbuka (FOSS).
    Beberapa fungsi mungkin dibatasi dalam versi gratis, dan model berlangganan tersedia untuk fitur tambahan.

    - **Zettlr:** Zettlr adalah sumber terbuka. Dia dirilis di bawah lisensi GNU General Public License (GPL).
    Ini berarti bahwa pengguna memiliki akses ke kode sumber, dapat memodifikasinya, dan mendistribusikan versi modifikasinya.

    - **Joplin:** Joplin bersifat open source dan dirilis di bawah Lisensi MIT.
    Hal ini memungkinkan pengguna untuk melihat, memodifikasi, dan mendistribusikan kode sumber secara bebas.

    - **QOwnNotes:** QOwnNotes juga merupakan sumber terbuka[^9]. Dia dirilis di bawah GNU General Public License (GPL).
    Seperti Zettlr, pengguna mempunyai kebebasan untuk mengakses, memodifikasi, dan mendistribusikan kode sumber.

11. **Teknologi yang Digunakan**:
    - **Obsidian:**
    Obsidian pada dasarnya dibuat menggunakan teknologi web. 
    Dia menggunakan framework Electron yang merupakan kerangka kerja untuk membangun aplikasi desktop lintas platform.
    Hal ini menjadikan Obsidian kompatibel dengan Windows, macOS, dan Linux.

    - **Zettlr:**
    Zettlr dikembangkan menggunakan teknologi web dan juga dibangun di atas Electron. Seperti Obsidian, pilihan ini memungkinkan kompatibilitas lintas platform.

    - **Joplin:**
    Joplin dikembangkan menggunakan JavaScript, Node.js, dan kerangka Electron. Kombinasi teknologi ini memungkinkan pembuatan aplikasi desktop lintas platform.

    - **QOwnNotes:**
    QOwnNotes dikembangkan menggunakan C++ dan kerangka Qt, berbeda dari ketiga aplikasi sebelumnya.
    Qt adalah toolkit lintas platform yang populer untuk mengembangkan antarmuka pengguna grafis, dan menjadi dasar untuk aplikasi desktop QOwnNotes.

Perlu diingat bahwa detail perangkat lunak, termasuk lisensi dan apakah perangkat lunak tersebut open source, dapat berubah seiring waktu sesuai dengan pembaruan dan rilis baru.

Kesimpulannya, pilihan aplikasi pencatat bergantung pada preferensi individu, kasus penggunaan spesifik, dan pentingnya fitur seperti privasi, penyesuaian, dan interkonektivitas.



[^1]: https://en.amazingtalker.com/questions/569
[^2]: https://en.wikipedia.org/wiki/Zettelkasten
[^3]: https://marimelantjong.wordpress.com/2021/08/24/terjebak-dalam-zettelkasten/
[^4]: https://www.zettlr.com/
[^5]: https://en.wikipedia.org/wiki/Niklas_Luhmann
[^6]: https://github.com/joplin/plugins/blob/master/README.md#plugins
[^7]: https://obsidian.md/
[^8]: https://github.com/Zettlr/Zettlr/issues/657
[^9]: https://github.com/pbek/QOwnNotes