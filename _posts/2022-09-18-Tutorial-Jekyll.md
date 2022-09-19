---
layout: post
title: Tutorial Membuat Blog Menggunakan Jekyll
date: 2022-09-18 12:21
category: [Tutorial, Jekyll]
author: Galih Putro Aji
tags: [how to, build, install, jekyll, blog, github]
---

## Persyaratan

- Memiliki Akun Github.
- Memiliki Komputer / Laptop
- Sudah Menginstall Ruby & Gem
- Memiliki Koneksi Internet
- Menginstall GIT di Komputer.

## Daftar Isi

1. Apa Itu Jekyll.
2. Pilih Tema Blog.
3. Fork / Generate Github Repo.
4. Clone Repo Ke Lokal.
5. Test Run Lokal.
6. Edit Config.

## Apa itu Jekyll ?

[Jekyll](https://jekyllrb.com/), sesuai tagline-nya “a simple, blog-aware, static site generator” adalah software untuk membuat blog statis. Untuk menghasilkan sebuah blog, Jekyll hanya membutuhkan template, file-file artikel yang ditulis dengan format [Markdown](https://www.markdownguide.org/) dan sebuah file konfigurasi. Kemudian hasilnya kita upload ke server. Itulah blog kita. Sesederhana itu. Mungkin terdengar seperti alternatif yang hanya cocok untuk para [“geek”](https://id.wikipedia.org/wiki/Geek), tapi sebenernya Jekyll (dan juga static blog lainnya) mempunyai banyak kelebihan dibandingkan Wordpress dkk.

Sejatinya [Wordpress](https://wordpress.com) itu terlalu overkill jika penggunaannya hanya untuk blogging. Terlalu banyak junk fitur dan "resource waste" untuk pemula.  
Maka dari itu, di tahun 2022 ini memang dirasa paling cocok menggunakan platform semacam [Jekyll](https://jekyllrb.com/) ini.

## Memilih Tema

Layaknya Platform Blogging / CMS lain, [Jekyll](https://jekyllrb.com) Juga dilengkapi dengan [Tema](http://jekyllthemes.org/) untuk mempercatik tampilan blog kita nantinya. Untuk tutorial kali ini, kita akan menggunakan [Tema](http://jekyllthemes.org/) bernama [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy/).

Kalian bisa langsung mengunjungi github repo nya [**Disini**](https://github.com/cotes2020/jekyll-theme-chirpy/).

## Fork / Generate Github Repo

Untuk memulai membuat blog, kalian bisa mengikuti [Official Documentation](https://chirpy.cotes.page/posts/getting-started/) dari [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy/) atau dari artikel ini. Langkah pertama, kita harus clone atau menyalin semua file yang ada di github repo dari [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy/) ke komputer / lokal dengan klik [**Disini**](https://github.com/cotes2020/chirpy-starter/generate).  
Sebelumnya kalian harus sudah menginstall **`Ruby`**, **`Ruby Gems`**, **`Jekyll`**. Jika belum silahkan menginstall nya terlebih dahulu, ikuti tutorial dari [Jekyll Documentation](https://jekyllrb.com/docs/installation/).  
Jika Sudah, Silahkan kalian generate repo melalui [**Link ini**](https://github.com/cotes2020/chirpy-starter/generate).
silahkan beri nama repo kalian dengan `(username_github).github.io`.

![Generate Repo!](/assets/img/tutorial-jekyll/generate-repo.png)

Jika Sudah, pergi ke halaman repo yang kalian buat tadi, copy url repo tersebut. Sekarang kita beralih ke lokal komputer kita, buat folder untuk project kita.
Buka terminal / cmd / powershell di folder tersebut, dan ketikan perintah berikut

```console
git clone https://<url-github-repo-kalian> .
```

Contohnya:

```console
git clone https://github.com/galihdjx/galihdjx.github.io .
```

Tunggu hingga proses selesai, lalu ketikan perintah berikut:

```console
Bundle
```

![Console!](/assets/img/tutorial-jekyll/console.png)

Tunggu hingga bundle menginstall semua yang diperlukan.

## Test Run Lokal

Sampai sini blog kita sudah bisa di gunakan. Kalian bisa mencobanya dengan mengetikan perintah:

```console
bundle exec jekyll s
```

Selanjutnya buka browser kalian dan kunjungi `http://localhost:4000`

![local-test!](/assets/img/tutorial-jekyll/local-test.png)

Itu adalah tampilan awal blog kita, selanjutnya kita edit file `_config.yml` untuk menyesuaikan blog kita. Kalian bisa edit sesuai kemauan, beberapa line yang wajib di edit diantaranya:

```yml
lang: en # kalian bisa ganti ke id-ID untuk bahasa Indonesia
timezone: Asia/Jakarta # Format Timezone standard Indonesia
title: GVerse # Judul Blog Kalian
tagline: # Sub Judul Blog
description: # Deskripsi Blog untuk SEO
url: # url Blog
```

Sisa nya seperti `github username` , `twitter` , `facebook` kalian sesuaikan dengan url / username kalian. Didalamnya juga ada konfigurasi untuk google analythics, silahkan disesuaikan. Sampai sini kita sudah mengubah informasi blog kita.
Blog ini bisa di deploy / install ke dalam `github pages` jadi kita tidak perlu membayar sewa hosting dll.

Untuk tutorial deploying, membuat post, dll akan saya buat next time. Terimakasih.
