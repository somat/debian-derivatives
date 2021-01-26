# debian-derivatives

Source: https://wiki.debian.org/Derivatives/Guidelines

Halaman ini menguraikan aspek-aspek yang harus diperhatikan saat membuat distribusi turunan Debian.
Untuk saat ini hal ini hanyalah uraian garis besar untuk mengumpulkan informasi yang relevan yang nantinya dapat diformalkan dalam bentuk Spesifikasi.

## Intro

Distribusi turunan Debian bervariasi dalam domain spesialisasi, basis pengguna, dan skala modifikasi/ekstensi yang dibawa oleh distribusi Vanilla Debian. Oleh karena itu, mungkin tidak ada aturan deterministik yang ketat, dan lebih tepatnya seperangkat pedoman yang dapat membantu untuk memutuskan tindakan mana yang harus diambil oleh pengembang turunan agar tidak menimbulkan kerugian bagi Debian, dan terlebih lagi agar mendapat keuntungan dari infrastruktur Debian/sumber daya/framework jika memungkinkan.

## Infrastruktur

Kami mendorong distribusi turunan untuk menyebutkan dan menjelaskan hubungannya dengan Debian di halaman web yang memberikan informasi tentang distro turunan (biasanya halaman about).
Kami mendorong distribusi turunan untuk menggunakan infrastruktur Debian dan perangkat lunak yang mendukung infrastruktur Debian jika memungkinkan.

## Lumbung/Repositori

Bagi turunan Debian yang menggunakan paket biner, tambahkan paket kode sumber dan modifikasi paket kode sumber, jika memungkinkan kami mendorong untuk menggunakan cermin debian standar dan menambahkan lumbung ke dua yang mengandung hanya sumber dan paket binari yang sudah ditambahkan atau dimodifikasi.

Bagi turunan Debian yang membangun ulang paket sumber Debian, tambahkan paket sumber dan modifikasi paket sumber, jika memungkinkan kami mendorong untuk menggunakan cermin standar Debian untuk paket sumber dan menambahkan lumbung ke dua yang mengandung hanya paket sumber dan paket binari yang sudah ditambahkan atau dimodifikasi. Rekomendasi ini kemungkinan sulit untuk dilaksanakan, untuk itu sinkronisasi paket sumber reguler merupakan rekomendasi alternatif.

Tentu saja untuk ke dua kasus tersebut merupakan ide yang baik untuk menjalankan cermin Debian untuk memastikan ketersediaan kode sumber dan binari. Mirror yang sama persis dari kode sumber Debian dan atau paket biner harus didaftarkan ke daftar mirror Debian.

Jika Anda menyalin kode sumber Debian ke repositori Anda tanpa melakukan modifikasi, harap membiarkan tanda tangan apa adanya di berkas .dsc, jangan menanda-tangani ulang dengan kunci tanda tangan Anda.

## *Keyring*

Harap membuat paket *keyring* Anda sendiri, alih-alih menambal/memodifikasi paket *keyring* Debian.

## Rilis

Jika turunan yang Anda buat merupakan turunan yang berdasarkan rilis stabil Debian, harap memulai proses pengujian rilis minimal pada saat terjadi pembekuan Debian, atau lakukan pengujian rilis reguler selama seluruh siklus rilis Debian.

Saat Anda membuat rilis menjadi usang dan tidak lagi didukung, harap pindahkan dari repositori apt reguler dan tempatkan di *hostname* yang berbeda (contohnya seperti arsip.example.org) atau URL (contohnya seperti ftp.example.org/arsip).

Jika Anda memiliki konstanta nomor rilis, harap memberikan nama yang merujuk/dihubungkan dengan nama kode. Di Debian kami menggunakan oldstable, stable, testing, unstable dan experimental, yang mana merujuk kepada nama rilis seperti lenny, squeeze, wheezy, sid dan rc-buggy.
