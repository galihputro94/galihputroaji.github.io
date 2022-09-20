---
layout: post
title: Cara Deploy Jekyll Ke Github Pages
date: 2022-09-20 21:45
category: [Tutorial, Jekyll]
author: Galih Putro Aji
tags: [how to, tutorial, jekyll, github, github pages, deploy]
---

Di tutorial sebelumnya, kita sudah membahas tentang cara instalasi dan setup, serta menambahkan post di blog jekyll kita. Selanjutnya di tutorial kali ini kita akan membahas cara agar blog kita bisa di akses dan tulisan kita bisa di baca oleh semua orang.

## Proses Deploy

Pertama silahkan kalian pastikan sudah memasang `Github Desktop` di komputer kalian. Jika belum ada, silahkan download melalui [Link Ini](https://desktop.github.com/) dan lakukan instalasi. Jika sudah, silahkan buka Github desktop kalian, dan buka menu `File > Options...`

![Github Desktop Login!](/assets/img/deploy-jekyll/git-desktop.png)

Lalu silahkan klik tombol `sign in` di bagian _Github.com_ (atas), dan lanjut klik pilihan `Continue with browser`

![Git Desktop 2!](/assets/img/deploy-jekyll/git-desktop2.png)

Silahkan ikuti perintah yang keluar di browser kalian, hingga proses login berhasil. Sampai sini harusnya kalian sudah bisa melihat daftar repository yang kalian punya

![Git Desktop 3!](/assets/img/deploy-jekyll/git-desktop3.png)

Klik menu `Add an Existing Repository from your hard drive...`
lalu pilih `Choose...` dan arahkan ke folder Blog Jekyll kalian. Perlu di catat, folder blog Jekyll yang berada di komputer kita itu disebut repositori lokal dan tugas kita adalah untuk sinkronisasi dengan repositori online yang ada di `Github.com`.

Jika sebelumnya kalian sudah melakukan basic setup dan menambahkan post di blog Jekyll kalian, kalian pasti akan menemukan tampilan berikut di Github Desktop kalian:

![Github Desktop 4!](/assets/img/deploy-jekyll/git-desktop4.png)

Seperti yang sudah disebutkan diatas, itu semua adalah perubahan yang sudah kalian lakukan di folder repositori kalian.
Sebelum melakukan sinkronisasi dengan online repo di Github.com, kita akan melakukan beberapa langkah untuk menyiapkan proses `deploy` di `Github Pages`. Caranya silahkan kalian buka online repo kalian dengan mengakses `https://github.com` lalu klik di pojok kanan atas (avatar) dan pilih `Your Repository` dan buka repository yang kalian gunakan di tutorial awal [Tutorial Membuat Blog Menggunakan Jekyll](/posts/Tutorial-Jekyll/), pergi ke tab `Settings` lalu di bagian kiri pilih menu `Pages`. Pada bagian source, silahkan pilih `Deploy from a branch` sementara arahkan ke branch `main` lalu silahkan tekan Save.

![Github 2!](/assets/img/deploy-jekyll/github2.png)

## Edit file \_config.yml

Sampai sini silahkan kalian tinggalkan browser kalian dan kembali ke aplikasi editor, kemudian edit file `_config.yml` dari root folder jekyll kalian dan cari baris `url:` dan masukan alamat url github pages kalian, contoh:

```yml
# fill in the protocol & hostname for your site, e.g., 'https://username.github.io'

url: "https://username.github.io"

# Contoh milik saya:

url: "https://galihputroaji.github.io"
```

Jika sudah, silahkan simpan dengan menekan `Ctrl + S`. Lanjut silahkan kalian buka console / terminal / cmd / powershell di folder Jekyll seperti biasa dengan menahan tombol `shift` lalu `klik kanan` pada folder tersebut dan pilih `open command window here` jika sudah silahkan jalankan perintah berikut:

```console
bundle lock --add-platform x86_64-linux
```

## Melakukan Push Repo

Selanjutnya kita akan lakukan sinkronisasi atau **_push_** repositori lokal kita dengan repositori online di [Github.com](https://github.com) dengan cara buka aplikasi `Github Desktop` kalian, dibagian kiri bawah pada form `commit`

![form commit!](/assets/img/deploy-jekyll/commit-form.png)

Pada input judul commit (Paling Atas) silahkan kalian isi bebas, misalnya `Persiapan Deploy` atau apapun, di bagian `Description` boleh di kosongi, atau kalian bisa isi dengan menambahkan detail apa saja yang kalian lakukan di repo tersebut. Selanjutnya klik `Commit to **main**` kalau sudah, silahkan kalian perhatikan tampilan di sebelah kanan aplikasi Github Desktop kalian, akan muncul tampilan berikut:

![Push Repo!](/assets/img/deploy-jekyll/push-repo.png)

Silahkan kalian klik `Push origin`. Sampai sini kalian sudah berhasil melakukan `push` repo dari lokal ke online.

Selanjutnya silahkan buka halaman online repo kalian di https://github.com/nama-repo-kalian lalu kita kembali pergi ke `Settings > Pages` di bagian `Branch` silahkan kalian klik dan akan muncul branch baru bernama `gh-pages` silahkan kalian pilih `gh-pages` dan klik `Save`. Tunggu beberapa saat dan seharusnya kalian sudah bisa melihat alamat url github pages kalian di bagian atas Branch tadi, seperti `username.github.io`. Selanjutnya kalian klik tombol `Visit Site` untuk melihat Blog Kalian. Jika tampilan blog kalian masih kosong silahkan tunggu saja sampai proses workflow action repo kalian berhasil di eksekusi, atau kalian bisa kembali ke halaman repo kalian dan pergi ke bagian tab `Actions`.

## Penutup

Sampai sini seharusnya kalian sudah memiliki sebuah blog tanpa harus membayar biaya sewa hosting dll.

> ### **Penting !**
>
> _Kalian harus selalu melakukan **Push Repo** Setiap kalian selesai menambahkan post atau melakukan perubahan apapun di lokal repo kalian. Jika tidak, maka semua perubahan yang kalian lakukan akan sia-sia dan dan online blog kalian tidak akan ter-update. Intinya Blog yang kalian install di github pages hanya akan ter-update ketika kalian melakukan push repo. Selama proses eksekusi `workflow` di tab `Actions` berjalan lancar tanpa terjadi error, maka Online Blog kalian akan selalu ter-update_

Demikian tutorial untuk deploy Jekyll di Github Pages. Mohon maaf jika terlalu panjang dan ada kesalahan dalam penyampaian saya. Saya usahakan untuk menjelaskan lebih detail supaya mudah dipahami. Jangan lupa tinggalkan komentar jika kalian mengalami kesulitan dalam proses deploying. Terimakasih..
