---
layout: post
title: Menambahkan Post Di Jekyll
date: 2022-09-19 01:34
category: [Tutorial, Jekyll]
author: Galih Putro Aji
tags: [jekyll, blog, tutorial, how to, add, post]
---

Pada tutorial sebelumnya, kita sudah belajar untuk [membuat sebuah blog menggunakan platform Jekyll](https://galihputroaji.github.io/posts/Tutorial-Jekyll/). Salah satu fitur yang membuat banyak konten kreator atau developer memilih [Jekyll](https://jekyllrb.com/), salah satunya adalah sederhananya memulai projek baru. Cukup dengan membuat satu file di folder `_post` kita sudah bisa membuat post baru. Berikut adalah sedikit tutorial untuk [membuat post di Jekyl](https://jekyllrb.com/docs/posts/).

## Daftar Isi

- Menyiapkan Aplikasi Editor
- Mempelajari Syntax [Markdown](https://www.markdownguide.org/)
- Membuat file posting
- Menulis konten
- Publish konten
- Kesimpulan

## Menyiapkan Aplikasi Editor

Di Jekyll untuk membuat sebuah konten berbentuk post, menggunakan file ber format [Markdown](https://www.markdownguide.org/) (.md), jadi untuk menulis post kita membutuhkan aplikasi text editor yang mendukung format `.md`. Salah satu nya saya merekomendasikan `Visual Studio Code` , `Sublime` , atau `Notepad++`.
Kalian bisa cari sendiri di [Google](https://google.com) untuk menginstall aplikasi nya.

## Mempelajari Syntax Markdown

Karena format tulisan untuk post di [Jekyll](https://jekyllrb.com/) ini berformat [Markdown](https://www.markdownguide.org/) (.md) maka kita harus tahu dulu basic syntax dalam penulisan nya. Untuk tutorial lengkap mengenai syntax penulisan file [Markdown](https://www.markdownguide.org/) ini, kalian bisa kunjungi [Official Documentation](https://www.markdownguide.org/basic-syntax/) dari [Markdown Guide](https://www.markdownguide.org), atau saya akan membuat tutorial lanjutannya di postingan lain.

## Membuat File posting

Untuk mulai menulis post, langkah pertama yang harus dilakukan adalah membuat sebuah file di folder `_post` yang sudah tersedia di `root folder` blog [Jekyll](https://jekyllrb.com/) kita.

![add file!](/assets/img/menambah-post-jekyll/add-file.png)

Pastikan nama file menggunakan format seperti berikut:

```yml
YYYY-MM-DD-nama-post.md

YYYY-MM-DD # waktu post di publish / dibuat
YYYY #Tahun
MM #Bulan
DD #Tanggal

# Contoh
2022-09-20-Tutorial-Jekyll.md
```

Setelah membuat file [Markdown](https://www.markdownguide.org/)nya, silahkan edit file tersebut dan tambahkan kode berikut untuk template awal post nya.

```yaml
---
layout: post # Jenis Layout
title: Judul Post # Judul Post
date: 2022-09-19 22:04 # Tanggal Pembuatan Post
category: [tutorial] # Kategori Post
author: Galih # Nama Pembuat / Author
tags: [how to, create, post] # Tag Post
---
```

Selanjutnya kalian bisa menuliskan isi dari postingan kalian di bawah kode tersebut menggunakan syntax [Markdown](https://www.markdownguide.org/) yang sudah kalian pelajari sebelumnya.

## Publish konten

Post di [Jekyll](https://jekyllrb.com/) ini sudah otomatis terpublish ketika kita menyimpan file postnya. Jadi kita bisa langsung melihat hasil nya dengan cara _running lokal server_ menggunakan perintah berikut di terminal / cmd:

```console
jekyll serve
```

Perintah di atas berguna untuk menjalankan blog kita di server lokal. Jadi setiap kita ingin melihat perubahan pada blog kita, perintah tersebut harus di eksekusi. Untuk menghentikan servernya, tekan tombol `CTRL + C`.

## Kesimpulan

Untuk kalian yang mungkin sebelumnya terbiasa dengan platform [Wordpress](https://wordpress.com) pasti akan merasa asing, dan pastinya butuh penyesuaian karena [Jekyll](https://jekyllrb.com/) ini sedikit berbeda. Tapi dengan beberapa hari membiasakan menulis di platform [Jekyll](https://jekyllrb.com/) ini, kalian pasti akan terbiasa dengan mekanismenya.  
Tips dari saya, perbanyak pengetahuan dengan membaca [Jekyll Documentation](https://jekyllrb.com/docs/) dan tutorial di [blog ini](https://galihputroaji.github.io). Semoga [tulisan ini](https://galihputroaji.github.io/posts/Menambahkan-Post-Di-Jekyll/) bermanfaat, terimakasih.
