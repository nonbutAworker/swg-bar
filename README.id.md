# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · **Bahasa Indonesia**

[Situs resmi](https://swgbar.com/id/) · [Unduh untuk Mac](https://swgbar.com/id/#pricing) · [Panduan](https://swgbar.com/id/guides/)

SWG bar adalah aplikasi native di bar menu macOS untuk memeriksa inspeksi HTTPS oleh secure web gateway (SWG). Periksa hasil domain dan bukti sertifikat di Mac, lalu lihat hasil lokal yang tersedia melalui ekstensi pendamping Chrome.

## Fitur

- Cari domain yang teramati dan lihat hasil pemeriksaan terbarunya.
- Periksa penerbit, masa berlaku, sidik jari, dan domain yang terkait dengan sertifikat.
- Bandingkan evaluasi kepercayaan sertifikat macOS dengan pemeriksaan independen menggunakan sertifikat akar publik.
- Lihat hasil domain yang sudah tersimpan di aplikasi Mac melalui toolbar Chrome.

Data deteksi dianalisis dan disimpan di Mac. Pemeriksaan membuka koneksi TLS terpisah; ekstensi membaca hasil lokal yang sudah ada. Lihat [cara kerja](https://swgbar.com/id/how-it-works/) dan [pemberitahuan privasi](https://swgbar.com/id/privacy/).

## Mulai menggunakan

Memerlukan **macOS 14 atau lebih baru dan Apple silicon**. Uji coba mencakup **14 hari penggunaan aktual**; paket terkini tersedia di situs resmi.

1. Unduh penginstal dari [situs resmi](https://swgbar.com/id/#pricing) dan ikuti [panduan instalasi](https://swgbar.com/id/install/).
2. Buka SWG bar dari bar menu dan periksa domain beserta sertifikatnya.
3. Jika diperlukan, atur [ekstensi Chrome](https://swgbar.com/id/chrome-extension/).

Aplikasi Mac mendukung bahasa Inggris, Mandarin sederhana dan tradisional, Jepang, serta Korea. Ekstensi Chrome 2.1.13 yang disertakan dalam aplikasi Mac 2.3.7 mendukung seluruh 12 bahasa situs web. Pembaruan Chrome Web Store diterbitkan secara terpisah setelah peninjauan; periksa versi yang tercantum di toko.

## Cara melewati SWG dan pengecualian inspeksi TLS

Melewati SWG berarti mengubah jalur jaringan suatu koneksi. Pengecualian inspeksi TLS dapat tetap melewatkan lalu lintas melalui gateway tanpa mendekripsinya. Rantai sertifikat publik saja tidak membuktikan bahwa jalur jaringan telah berubah.

Baca [perbandingan bypass SWG dan pengecualian TLS](https://swgbar.com/id/guides/swg-bypass-vs-tls-exception/) serta [panduan mendeteksi inspeksi HTTPS](https://swgbar.com/id/guides/detect-https-inspection/).

**Diperiksa pada 24 Oktober 2026:** versi penginstal yang diterbitkan adalah 2.3.7. Bypass domain dengan satu klik direncanakan untuk versi 2.4.0. Lihat [informasi rilis](https://swgbar.com/id/releases/) dan [panduan resmi](https://swgbar.com/id/guides/) untuk langkah yang telah diverifikasi.

## Pengukuran dan bantuan

[Studi pemeriksaan sertifikat](https://swgbar.com/id/guides/certificate-check-case-study/) mencatat pengukuran bertanggal untuk `swgbar.com:443`, perintah OpenSSL yang dapat diulang, hasil evaluasi macOS, serta pengamatan terpisah menggunakan kode pemeriksaan SWG bar. Hasil tersebut hanya menjelaskan koneksi yang diukur dan tidak membuktikan bahwa gateway telah dilewati.

Ini adalah repositori resmi untuk pengenalan publik proyek. Gunakan [Issues](https://github.com/nonbutAworker/swg-bar/issues) untuk pertanyaan publik dan saran dokumentasi. Untuk urusan pribadi, hubungi [support@swgbar.com](mailto:support@swgbar.com). Jangan memublikasikan kunci lisensi atau riwayat penjelajahan.

[Tentang SWG bar](https://swgbar.com/id/about/) · [Privasi](https://swgbar.com/id/privacy/) · [Ketentuan](https://swgbar.com/id/terms/)
