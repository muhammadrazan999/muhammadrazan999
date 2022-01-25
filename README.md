
Ini adalah rumah bagi [Shields.io][shields.io], layanan untuk ringkas, konsisten,
dan lencana yang dapat dibaca dalam format SVG dan raster, yang dapat dengan mudah disertakan dalam
Readmes GitHub atau halaman web lainnya. Layanan ini mendukung lusinan
layanan integrasi berkelanjutan, pendaftar paket, distribusi, aplikasi
toko, jaringan sosial, layanan cakupan kode, dan layanan analisis kode.
Setiap bulannya menyajikan lebih dari 770 juta gambar dan digunakan oleh beberapa
proyek sumber terbuka paling populer di dunia, [VS Code][vscode], [Vue.js][vue]
dan [Bootstrap][bootstrap] untuk beberapa nama.

[instagram]: https://github.com/Microsoft/vscode
[situs web]: https://github.com/vuejs/vue
[youtube]: https://github.com/twbs/bootstrap
[Blog ] :
Repo ini menampung:

- Frontend [Shields.io][shields.io] dan kode server
- [Perpustakaan NPM untuk menghasilkan lencana][pembuat lencana]
  - [dokumentasi][dokumen pembuat lencana]
  - [log perubahan][log perubahan pembuat lencana]
- [Spesifikasi desain lencana][spesifikasi lencana]

[shields.io]: https://shields.io/
[pembuat lencana]: https://www.npmjs.com/package/badge-maker
[spesifikasi lencana]: https://github.com/badges/shields/tree/master/spec
[badge-maker-docs]: https://github.com/badges/shields/tree/master/badge-maker/README.md
[badge-maker-changelog]: https://github.com/badges/shields/tree/master/badge-maker/CHANGELOG.md

## Contoh

- persentase cakupan kode: ![cakupan](https://img.shields.io/badge/coverage-80%25-yellowgreen)
- versi rilis stabil: ![versi](https://img.shields.io/badge/version-1.2.3-blue)
- rilis manajer paket: ![gem](https://img.shields.io/badge/gem-2.2.0-blue)
- status dependensi pihak ketiga: ![dependensi](https://img.shields.io/badge/dependencies-out%20of%20date-orange)
- nilai analisis kode statis: ![codacy](https://img.shields.io/badge/codacy-B-green)
- [SemVer](https://semver.org/) versi ketaatan: ![semver](https://img.shields.io/badge/semver-2.0.0-blue)
- jumlah donasi [Liberapay](https://liberapay.com/) per minggu: ![menerima](https://img.shields.io/badge/receives-2.00%20USD%2Fweek-yellow)
- Unduhan paket Python: ![unduhan](https://img.shields.io/badge/downloads-13k%2Fmonth-brightgreen)
- Peringkat ekstensi Toko Web Chrome: ![rating](https://img.shields.io/badge/rating-★★★★☆-brightgreen)
- Persentase [Robot Waktu Aktif](https://uptimerobot.com): ![waktu aktif](https://img.shields.io/badge/uptime-100%25-brightgreen)

[Buat lencana Anda sendiri!][lencana khusus]
(Contoh cepat: `https://img.shields.io/badge/left-right-f39f37`)

[lencana khusus]: ​​https://shields.io/#your-badge

### Mulai cepat

Jelajahi [daftar lengkap lencana][shields.io] dan temukan lencana tertentu dengan menggunakan bilah pencarian atau dengan menelusuri kategori. Klik pada lencana untuk mengisi elemen data yang diperlukan untuk jenis lencana tersebut (seperti nama pengguna atau repo Anda) dan secara opsional menyesuaikan (label, warna, dll.). Dan siap digunakan!

Gunakan tombol di bagian bawah untuk menyalin url atau cuplikan lencana Anda, yang kemudian dapat ditambahkan ke tempat-tempat seperti file readme GitHub atau halaman web lainnya.

## Berkontribusi

Shields adalah proyek komunitas. Kami mengundang partisipasi Anda melalui masalah
dan tarik permintaan! Anda dapat membaca [pedoman berkontribusi][berkontribusi].

Saat menambahkan atau mengubah layanan [harap tambahkan pengujian][pengujian layanan].

Proyek ini memiliki tumpukan saran yang cukup banyak! Jika Anda baru mengenal proyek ini,
mungkin Anda ingin membuka permintaan tarik untuk mengatasi salah satunya.

Anda dapat membaca [tutorial tentang cara menambahkan lencana][tutorial].

[![Isu GitHub berdasarkan label](https://img.shields.io/github/issues/badges/shields/good%20first%20issue)](https://github.com/badges/shields/issues? q=is%3Amasalah+adalah%3Aterbuka+label%3A%22baik+pertama+masalah%22)

[service-tests]: https://github.com/badges/shields/blob/master/doc/service-tests.md
[tutorial]: https://github.com/badges/shields/blob/master/doc/TUTORIAL.md
[berkontribusi]: https://github.com/badges/shields/blob/master/CONTRIBUTING.md

## Perkembangan

1. Instal Node 16 atau yang lebih baru. Anda dapat menggunakan [pengelola paket][] pilihan Anda.
   Tes harus lulus di Node 16 dan 17.
2. Kloning repositori ini.
3. Jalankan `npm ci` untuk menginstal dependensi.
4. Jalankan `npm start` untuk memulai server badge dan server pengembang frontend.
5. Buka `http://localhost:3000/` untuk melihat frontend.

Ketika file sumber server berubah, server lencana akan otomatis restart
sendiri (menggunakan [nodemon][]). Ketika file frontend berubah, frontend dev
server (`gatsby dev`) juga harus dimuat ulang secara otomatis. Namun lencana
definisi dibangun hanya sebelum server pertama kali dimulai. Untuk meregenerasi itu,
jalankan `npm run defs` atau restart server secara manual.

Untuk men-debug lencana dari baris perintah, jalankan `npm run badge -- /npm/v/nock`.
Ini juga berfungsi dengan URL lengkap seperti
`npm run badge -- https://img.shields.io/npm/v/nock`.

Gunakan `npm run debug:server` untuk memulai server dalam mode debug.
[Resep ini][debug nodemon] menunjukkan cara men-debug aplikasi Node.js di [Kode VS][].

Shields memiliki dukungan eksperimental untuk [Gitpod][gitpod], pengembangan yang telah dikonfigurasi sebelumnya
lingkungan yang berjalan di browser Anda. Untuk menggunakan Gitpod, klik tombol di bawah dan
masuk dengan GitHub. Gitpod juga menawarkan add-on browser, meskipun tidak diperlukan.
Silakan laporkan bug, pertanyaan, atau saran Gitpod apa pun yang bermasalah
[#2772](https://github.com/badges/shields/issues/2772).

[![Edit dengan Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/badges/shields)

[Tes snapshot][] memastikan kami tidak secara tidak sengaja membuat perubahan yang memengaruhi
keluaran SVG atau JSON. Saat dengan sengaja mengubah output, jalankan
`SNAPSHOT_DRY=1 npm run test:package` untuk melihat pratinjau perubahan pada yang disimpan
snapshot, dan `SNAPSHOT_UPDATE=1 npm run test:package` untuk memperbaruinya.

Server dapat dikonfigurasi untuk menggunakan [Penjaga][] ([konfigurasi][konfigurasi penjaga]) dan [Prometheus][] ([konfigurasi][konfigurasi prometheus]).

Pengujian harian, termasuk pengujian layanan secara penuh dan cakupan kode secara keseluruhan, dijalankan melalui [badges/tes harian][tes harian].

[pengelola paket]: https://nodejs.org/en/download/package-manager/
[gitpod]: https://www.gitpod.io/
[tes snapshot]: https://glebbahmutov.com/blog/snapshot-testing/
[prometheus]: https://prometheus.io/
[konfigurasi prometheus]: https://github.com/badges/shields/blob/master/doc/self-hosting.md#prometheus
[penjaga]: https://sentry.io/
[konfigurasi penjaga]: https://github.com/badges/shields/blob/master/doc/self-hosting.md#sentry
[tes harian]: https://github.com/badges/daily-tests
[nodemon]: https://nodemon.io/
[debug nodemon]: https://github.com/Microsoft/vscode-recipes/tree/master/nodemon
[vs kode]: https://code.visualstudio.com/

## Hosting server Anda sendiri

Ada dokumentasi tentang [hosting server Anda sendiri][self-hosting].

[hosting sendiri]: https://github.com/badges/shields/blob/master/doc/self-hosting.md

## Proyek terkait

[![Keren](https://awesome.re/badge.svg)](https://awesome.re)

Lencana status digunakan secara luas di seluruh proyek perangkat lunak sumber terbuka dan pribadi.
Akademisi telah mempelajari "sinyal" yang diberikan lencana tentang proyek perangkat lunak
kualitas. Ada banyak perpustakaan yang ada untuk merender lencana ini, dan
alternatif untuk layanan lencana Shields yang dihosting. [lencana mengagumkan][] adalah
koleksi kurasi dari sumber daya tersebut.
[Kontribusi][berkontribusi ke lencana luar biasa] dapat dipertimbangkan di sana.
(Kehadiran proyek dalam koleksi itu tidak boleh ditafsirkan sebagai dukungan atau promosi dari proyek Shields)

[lencana mengagumkan]: https://github.com/badges/awesome-badges
[berkontribusi pada lencana mengagumkan]: https://github.com/badges/awesome-badges/blob/main/CONTRIBUTING.md

## Sejarah

b.adge.me adalah situs web asli untuk layanan ini. Heroku saat itu memiliki
hal yang membuatnya sulit untuk menggunakan domain tingkat atas dengannya, makanya aneh
domain. Itu menggunakan kode yang dikembangkan pada 2013 dari perpustakaan bernama
[gh-badges][old-gh-badges], keduanya dikembangkan oleh [Thaddée Tyl][espadrine].
Proyek bergabung dengan shields.io dengan membuatnya menggunakan kode b.adge.me
dan tutup b.adge.me.

Spesifikasi lencana asli dikembangkan pada tahun 2013 oleh
[Olivier Lacan][olivierlacan]. Itu terinspirasi oleh Travis CI dan sejenisnya
lencana (ada jauh lebih sedikit, saat itu). Pada tahun 2014 Thaddée Tyl didesain ulang
dengan bantuan dari karyawan Travis CI dan meyakinkan semua orang untuk beralih ke
dia. Desain lama adalah apa yang sekarang disebut gaya plastik; yang baru
adalah gaya datar.

Anda dapat membaca lebih lanjut tentang [permulaan proyek][utas],
[motivasi spesifikasi lencana SVG][motivasi], dan
[spesifikasi itu sendiri][spek].

[olivierlacan]: https://github.com/olivierlacan
[espadrine]: https://github.com/espadrine
[lencana-gh-lama]: https://github.com/badges/gh-badges
[motivasi]: https://github.com/badges/shields/blob/master/spec/motivation.md
[spec]: https://github.com/badges/shields/blob/master/spec/SPECIFICATION.md
[utas]: https://github.com/h5bp/lazyweb-requests/issues/150

## Pemimpin proyek

Pemelihara:

- [calebcartwright](https://github.com/calebcartwright) (tim inti)
- [chris48s](https://github.com/chris48s) (tim inti)
- [Daniel15](https://github.com/Daniel15) (tim inti)
- [paulmelnikow](https://github.com/paulmelnikow) (tim inti)
- [platan](https://github.com/platan) (tim inti)
- [PyvesB](https://github.com/PyvesB) (tim inti)
- [RedSparr0w](https://github.com/RedSparr0w) (tim inti)

Operasi:

- [calebcartwright](https://github.com/calebcartwright)
- [chris48s](https://github.com/chris48s)
- [paulmelnikow](https://github.com/paulmelnikow)
- [PyvesB](https://github.com/PyvesB)

alumni:

- [espadrine](https://github.com/espadrine)
- [olivierlacan](https://github.com/olivierlacan)

## Lisensi

Semua aset dan kode berada di bawah [LISENSI CC0](LISENSI) dan untuk umum
domain kecuali ditentukan lain.

Aset dalam `logo/` adalah merek dagang dari masing-masing perusahaan dan merupakan
di bawah persyaratan dan lisensi mereka.

## Masyarakat

Terima kasih kepada orang-orang dan perusahaan yang menyumbangkan uang, layanan, atau waktu untuk menjaga proyek tetap berjalan. [https://shields.io/community](https://shields.io/community)
