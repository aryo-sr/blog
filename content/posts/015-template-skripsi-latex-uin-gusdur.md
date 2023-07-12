---
title: "Template (Xe)LaTeX untuk Skripsi atau Tesis"
date: 2023-07-12T15:20:05+07:00
draft: false
description: "Template XeLaTeX untuk tugas akhir kuliah di UIN Gus Dur Pekalongan"
tags: ["karya-ilmiah","penelitian","skripsi","latex","pdf","typesetting"]
---

~~Dengan terbitnya blog tentang template (Xe)LaTeX untuk tugas akhir ini,
artinya penulis sudah menyelesaikan seluruh tugasnya sebagai mahasiswa.~~
~~Seharusnya *sih* seperti itu, tetapi saat itu penulis sedang *stuck* mengerjakan revisi.~~
~~Sebagai penyela untuk meringankan *pressure*, penulis merasa lebih baik merapikan 
repository template latex dan mempublikasikannya.~~<!--more-->

Sejak awal kuliah, saya sudah punya rencana untuk membuat skripsi menggunakan format $ \LaTeX $.
LaTeX adalah bahasa markup atau sistem penyiapan dokumen untuk peranti lunak TeX. 
Tex merupakan program komputer yang digunakan untuk membuat *typesetting* suatu dokumen, atau membuat formula matematika. 
LaTeX memungkinkan penulis/penggunanya untuk melakukan *typesetting* dan mencetak hasil kerjanya dalam bentuk tipografi yang terbaik. 
Oleh karenanya LaTeX paling banyak digunakan oleh para matematikawan, ilmuwan, insinyur, akademisi, dan profesional lainnya.
Pada awalnya LaTeX ditulis pada awal 1980-an oleh Leslie Lamport di SRI International.[^1] 
Sedangkan $ \TeX $ sendiri adalah program buatan Donald E. Knuth yang dirilis pada tahun 1978.

*Typesetting* atau tata cetak adalah komposisi teks menggunakan huruf logam.[^2]
Yakni proses pengaturan huruf teks sebelum dicetak, merujuk pada proses percetakan tradisional.
Seiring berjalannya waktu, istilah *typesetting* juga digunakan untuk proses desain karya cetak digital.
TeX merupakan perangkat lunak *free* untuk *typesetting* yang masih banyak dipakai sampai sekarang.
TeX dirancang dengan dua tujuan utama: untuk memungkinkan siapa pun menghasilkan buku berkualitas tinggi dengan usaha yang minimal, 
dan untuk menyediakan sistem yang akan memberikan hasil yang persis sama di semua komputer kapanpun.

Salah satu kekurangan $ \LaTeX $ adalah *learning curve* yang lumayan curam untuk mempelajarinya.
Kita perlu menuliskan kode-kode untuk menghasilkan dokumen yang akan dicetak.
Walaupun ini menjadikannya sangat fleksibel, di sisi lainnya itu tidak praktis bagi yang terbiasa mengoperasikan program WYSIWYG[^3].
Alternatifnya, ada program *typesetting* dengan GUI yang juga populer seperti Adobe InDesign.
Saya pernah belajar menggunakannya untuk membuat semacam *flyer* dan majalah.
Program *open source* yang setara adalah Scribus.

Saya bersikukuh menggunakan $ \LaTeX $, lebih tepatnya XeLaTeX, untuk skripsi karena menurut saya sangat sesuai dengan fungsinya,
yakni untuk membuat dokumen karya ilmiah akademik. Beberapa keuntungan yang saya pikirkan antara lain:

1. menghasilkan tata letak yang sangat rapi
2. mempermudah memasukkan dan mengelola referensi sitasi (daftar pustaka / bibliografi)
3. dapat menggambar grafik atau rumus-rumus matematika rumit secara langsung di dokumen (misalnya dengan *package* TikZ)
4. mengurangi upaya repetitif dalam memformat teks, misalnya huruf miring (*italic*), penomoran, indentasi, dll. sebagaimana yang biasa kita lakukan pada program perkantoran seperti MS Word
5. LaTeX sudah menjadi standar de facto untuk tata letak rumus matematika bahkan pada halaman web[^4]
6. tidak perlu *re-learning* karena saya pernah mempelajari $ \LaTeX $

Untuk yang terakhir, saya pernah membuat ulang (lebih tepatnya membajak) sebuah buku dalam $ \LaTeX $ dengan tata letak yang dibuat semirip mungkin.
Buku cetaknya masih ada, tetapi file projeknya entah di mana.
Jadi, dengan ini saya sudah punya dasar dalam mengkode $ \LaTeX $.

Kali pertama saya mengetahui dan terpapar pada $ \LaTeX $ adalah saat awal-awal menjadi *user* linux desktop.
Di komunitas, ada yang berbagi mengenai $ \LaTeX $ sebagai format dokumen.
Dia digunakan sebagai alternatif aplikasi perkantoran *proprietary* yang normalnya tidak bisa dijalankan di linux.
Selain itu, dokumen $ \LaTeX $ juga banyak dipakai oleh pengembang program *open source* untuk dokumentasi atau manual *offline*.
Saya tertarik untuk berkontribusi pada pengembangan program *open source*, sehingga mempelajari $ \LaTeX $ adalah salah satu cara 
yang paling memungkinkan untuk dapat bergabung dalam tim pengembangan, yakni dengan membantu dalam dokumentasi program.

Contoh kode $ \LaTeX $ dan hasil akhirnya:

```
\begin{aligned} 
 CV & = \left\{
 \begin{array}{cccccc}
     8 & 12 & 16 & 20 & 24 & 28  \\
     8 & 12 & 16 & 20 & 24 & 28  \\
     \vdots & \vdots & \vdots & \vdots & \vdots  & \vdots \\
     8 & 12 & 16 & 20 & 24 & 28  \\
   \end{array}
   \right\} \\
   & \\
 \%Diff & = \left\{
 \begin{array}{ccccc}
     5 & 5 & 5 & 5 & 5  \\
     10 & 10 & 10 & 10 & 10 \\
     \vdots & \vdots & \vdots & \vdots & \vdots \\
     25 & 25 & 25 & 25 & 25 \\
   \end{array}
   \right\}
\end{aligned} 
```

$$
\\begin{aligned} 
 CV & = \\left\\{
 \\begin{array}{cccccc}
     8 & 12 & 16 & 20 & 24 & 28  \\\\
     8 & 12 & 16 & 20 & 24 & 28  \\\\
     \\vdots & \\vdots & \\vdots & \\vdots & \\vdots  & \\vdots \\\\
     8 & 12 & 16 & 20 & 24 & 28  \\\\
   \\end{array}
   \\right\\} \\\\
   & \\\\
 \\%Diff & = \\left\\{
 \\begin{array}{ccccc}
     5 & 5 & 5 & 5 & 5  \\\\
     10 & 10 & 10 & 10 & 10 \\\\
     \\vdots & \\vdots & \\vdots & \\vdots & \\vdots \\\\
     25 & 25 & 25 & 25 & 25 \\\\
   \\end{array}
   \\right\\}
\\end{aligned}
$$

Diambil dari [Stackoverflow](https://stackoverflow.com/questions/57651944/how-to-write-formula-in-md-file-for-hugo-website "How to write formula in .md file for hugo website").

---

Dokumen $ \LaTeX $ skripsi saya adalah *fork* atau turunan dari *source code* template skripsi yang dibuat kali pertama oleh fasilkom UI.
Ini sekaligus bisa menjadi salah satu contoh nyata bagaimana $ \LaTeX $ dapat digunakan dalam berkolaborasi untuk mengerjakan karya ilmiah.
Yakni dengan memanfaatkan Git yang menyimpan informasi perubahan setiap file dengan transparan oleh setiap individu yang terlibat.
Perubahan sekecil apapun dapat dilihat karena file $ \LaTeX $ adalah murni *plain text* yang relatif mudah untuk diperbandingkan perbedaan sebelum dan sesudah perubahan.
Proses seperti itu agaknya akan sulit dilakukan pada file dokumen populer seperti DOCX, karena pada dasarnya dia adalah file zip yang memuat sejumlah file berupa dokumen itu sendiri dan metadatanya.
Tetapi mungkin saja *tracking* perubahan versi file sama seperti git akan bisa dilakukan di masa mendatang.
Dan perlu diperhatikan, kekurangan dari git adalah terkadang cukup menyusahkan jika terjadi konflik dalam file yang dikerjakan bersama.

Kekurangan dari $ \LaTeX $ adalah setup atau instalasi program dan pemilihan *engine* serta kompatibilitas *package* yang akan digunakan.
Setidaknya itu yang pernah saya alami di Windows, yakni kesulitan saat instalasi distribusi MikTex karena kendala koneksi internet.
Tetapi di Linux tidak mengalami kesulitan, karena *source code* `texlive` didukung dan disediakan program binernya oleh distro linux, jadi bisa langsung diinstall.
Di sini saya tidak akan menjelaskan bagaimana setupnya, dan mungkin akan dibahas pada tulisan yang akan datang.

Untuk template yang akan saya bagikan ini pun, saya lebih memaksimalkan untuk dikerjakan pada layanan daring yang 
menyediakan tempat untuk menulis dokumen $ \LaTeX $ tanpa harus berurusan dengan setupnya, yakni di **Overleaf**[^5].
Disediakan layanan gratis yang dibatasi waktu *compile* dokumen.
Jadi, kode-kode $ \LaTeX $ yang kita buat perlu di-*compile* menjadi PDF, dan itu membutuhkan waktu.
Semakin kompleks dokumennya, semakin lama proses *compile*.
Batasan yang diberikan Overleaf adalah 1 menit untuk yang gratis, dan 4 menit bagi yang berbayar.
Untuk dokumen skripsi saya masih memungkinkan di-*compile* dalam semenit karena tidak terlalu kompleks.
Dengan Overleaf, saya bahkan bisa mengerjakan dokumen menggunakan ponsel Android di mana saja selama ada koneksi internet.

Sebenarnya saya menambah banyak perubahan pada template asal dari UI untuk dokumen ini.
Itu karena adanya perbedaan kebutuhan, di mana kampus saya adalah perguruan tinggi Islam, 
jadi membutuhkan pemrosesan teks bahasa Arab, misalnya untuk menulis ayat Al-Quran dan hadits.
Oleh karena itu, dibutuhkan makro tambahan yang tidak dapat diproses oleh $ \LaTeX $ (pdfLaTeX hanya memproses teks ASCII),
sehingga saya memilih *engine* XeTeX untuk *compiler* dokumen XeLaTeX.
Engine XeTeX mendukung pemrosesan karakter UTF-8 dan juga ada dukungan untuk font Arab dan RTL (right-to-left)[^6].
Selain itu juga karena memerlukan dukungan *hyphenation* untuk bahasa Indonesia, yang menggunakan *package* Polyglossia.
Package ini dipilih karena sempat ada konflik pada *package* `biblatex` yang digunakan untuk pemformatan sitasi APA[^7].

![Pedoman Penyusunan Skripsi](/blog/img/2023/07/pedoman2023.png "Pedoman Penyusunan Skripsi FEBI 2023")

**Unduh Template Skripsi dari Github: [aryo-sr/template-skripsi-2022-latex](https://github.com/aryo-sr/template-skripsi-2022-latex)**

Template skripsi ini dimaksudkan sebagai *boilerplate* bagi mahasiswa FEBI UIN K.H. Abdurrahmah Wahid Pekalongan 
yang ingin membuat skripsi dengan $ \LaTeX $.
Format penulisan sudah disesuaikan dengan Pedoman Penyusunan Skripsi terbaru dari fakultas.
Yang disediakan antara lain:

1. frontmatter: halaman judul, pernyataan keaslian, nota pembimbing, pengesahan sidang, halaman persembahan, abstrak, kata pengantar dan pedoman transliterasi Arab-Latin
2. pemformatan halaman: batas tepi (margin), indentasi, font, hierarki bab-subbab
3. pemformatan teks: dalil ayat atau hadits dan terjemahannya, teks kutipan wawancara, daftar isi
4. manajemen sitasi menggunakan bibtex, format daftar pustaka dengan standar APA 7
5. daftar gambar dan tabel, contoh bagan metode analisis data
6. custom appendices sebagai daftar lampiran, riwayat hidup penulis
7. dukungan format dokumen standar PDF/A-2b[^8]

_**Catatan**_: Jika ingin menggunakan templat ini, perlu diperhatikan bahwa masih **diperlukan format dokumen DOCX** dalam beberapa *step*
pada proses administrasi skripsi.
Antara lain saat cek plagiarisme dan unggah mandiri ke perpustakaan.
Kenyataan bahwa masih ada ketergantungan pada format dokumen word bagi saya cukup disayangkan dan tidak dapat berbuat banyak.
Oleh karena itu, bisa dibilang penggunaan $ \LaTeX $ untuk skripsi ini adalah upaya yang *overkill*.
Jadi, harap dipertimbangkan dengan bijak sebelum melangkah lebih jauh.
Konversi format $ \LaTeX $ ke DOCX sebenarnya dimungkinkan menggunakan Pandoc[^9] atau `mk4ht`, tetapi untuk XeLaTeX masih belum sempurna dan masih diupayakan dalam template ini.
Saya sendiri sudah mencoba konversi dari PDF ke DOCX menggunakan MS Word (365) dan Adobe Acrobat (23).
Keduanya menghasilkan file DOCX yang mendekati sempurna, dan hasil Acrobat lebih bagus daripada Word.

![Adobe Acrobat export pdf to word](/blog/img/2023/07/acrobat2023.png "Adobe acrobat convert pdf to docx")

[^1]: https://id.wikipedia.org/wiki/LaTeX
[^2]: https://id.wikipedia.org/wiki/Tata_cetak
[^3]: what you see is what you get
[^4]: https://en.wikipedia.org/wiki/LaTeX#Compatibility_and_converters
[^5]: https://www.overleaf.com/
[^6]: https://en.wikipedia.org/wiki/XeTeX#Arabic_support
[^7]: American Psychological Association
[^8]: https://en.wikipedia.org/wiki/PDF/A
[^9]: https://github.com/jgm/pandoc