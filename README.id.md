# SWG bar

[English](README.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Français](README.fr.md) · [Italiano](README.it.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Português (BR)](README.pt-BR.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · **Bahasa Indonesia**

**Ketahui saat HTTPS Anda diinspeksi. Lewati SWG dengan sekali klik.**

[Situs resmi](https://swgbar.com/id/) · [Unduh untuk Mac](https://swgbar.com/id/#pricing) · [Panduan](https://swgbar.com/id/guides/) · [CLI](https://swgbar.com/id/cli/) · [MCP](https://swgbar.com/id/mcp/)

SWG bar adalah aplikasi native di bar menu macOS untuk mendeteksi **inspeksi HTTPS/SSL (break-and-inspect)** oleh secure web gateway (SWG) perusahaan—seperti Zscaler, Netskope, dan Cloudflare Gateway—serta mengelola **bypass SWG per domain dalam sekali klik**. Periksa hasil domain dan bukti sertifikat di Mac, lihat hasil lokal yang tercatat melalui ekstensi pendamping Chrome, atau kelola pemeriksaan dan aturan domain dari Terminal maupun agen pengodean AI.

## Fitur

- **Inspeksi HTTPS/SSL & bukti sertifikat:** kenali domain yang diinspeksi, periksa penerbit, masa berlaku, sidik jari SHA-256, serta nama host terkait, dan bandingkan evaluasi kepercayaan Rantai Kunci macOS (termasuk CA akar dari MDM) dengan pemeriksaan independen sertifikat akar publik.
- **Bypass SWG per domain sekali klik:** arahkan nama host terpilih di macOS tanpa dekripsi HTTPS oleh gateway pada jaringan yang diizinkan, melalui bar menu, CLI, atau MCP.
- **Ekstensi pendamping Chrome (`2.1.13`):** lihat hasil lokal yang sudah dicatat aplikasi Mac untuk domain aktif langsung dari bilah alat browser.
- **CLI `swgbar` native & server MCP:** periksa telemetri inspeksi, jalankan probe TLS sesuai permintaan, dan atur bypass per domain dari Terminal ([panduan CLI](https://swgbar.com/id/cli/)) atau klien AI yang mendukung MCP seperti Claude Desktop, Cursor, Windsurf, dan Claude Code ([panduan MCP](https://swgbar.com/id/mcp/)).

Data deteksi dianalisis dan disimpan secara lokal di Mac. Pemeriksaan membuka koneksi TLS IPv4 terpisah; ekstensi Chrome bersifat baca-saja melalui Chrome Native Messaging untuk menampilkan hasil lokal yang ada. Lihat [cara kerja SWG bar](https://swgbar.com/id/how-it-works/), [pemberitahuan privasi](https://swgbar.com/id/privacy/), dan [privasi ekstensi](https://swgbar.com/id/extension-privacy/).

## Mulai menggunakan

Memerlukan **macOS 14 atau lebih baru dan Apple silicon** (`arm64`). Uji coba gratis mencakup **14 hari penggunaan aktual** tanpa kartu kredit; paket Personal dan Tim terkini tersedia di [situs resmi](https://swgbar.com/id/#pricing).

1. Unduh penginstal `.pkg` resmi yang telah ditandatangani dan dinotarisasi (`2.4.12`, build `42`) dari [situs resmi](https://swgbar.com/id/#pricing) dan ikuti [panduan instalasi](https://swgbar.com/id/install/).
2. Buka SWG bar dari bar menu untuk memeriksa nama host, CA akar, dan kontrol bypass SWG per domain.
3. Jika diperlukan, hubungkan [ekstensi Chrome](https://swgbar.com/id/chrome-extension/), siapkan [`swgbar` CLI](https://swgbar.com/id/cli/), atau daftarkan [server MCP](https://swgbar.com/id/mcp/) pada klien AI Anda.

Aplikasi Mac `2.4.12` beserta ekstensi Chrome `2.1.13` yang disertakan mendukung seluruh 12 bahasa situs web. Pembaruan di Chrome Web Store diterbitkan secara terpisah setelah peninjauan; periksa versi yang tercantum di toko.

## Panduan: inspeksi HTTPS, bypass SWG, dan error sertifikat CLI/AI

Saat menelusuri inspeksi HTTPS di macOS, pisahkan **perutean jaringan** dari **dekripsi TLS**. Melewati SWG berarti mengarahkan koneksi nama host ke jalur di luar dekripsi gateway; pengecualian inspeksi TLS dapat tetap melewatkan lalu lintas melalui gateway tanpa mendekripsinya, sehingga rantai sertifikat publik saja tidak membuktikan adanya perubahan jalur.

- [Cara mendeteksi inspeksi HTTPS & SSL di Mac](https://swgbar.com/id/guides/detect-https-inspection/) — periksa rantai sertifikat dan CA akar lokal di macOS.
- [Inspeksi HTTPS SWG perusahaan & MDM di Mac](https://swgbar.com/id/guides/enterprise-swg-https-inspection-macos/) — mengapa Zscaler, Netskope, dan Cloudflare Gateway tetap menampilkan ikon gembok normal di browser melalui CA akar MDM.
- [Cara melewati SWG di Mac](https://swgbar.com/id/guides/how-to-bypass-swg/) — langkah demi langkah pengaturan bypass per domain, persetujuan ekstensi jaringan macOS, perilaku mulai ulang, dan batas jaringan.
- [Bypass SWG vs. pengecualian inspeksi TLS (break-and-inspect)](https://swgbar.com/id/guides/swg-bypass-vs-tls-exception/) — perbedaan antara perutean per domain dan pengecualian dekripsi di gateway.
- [Atasi error sertifikat TLS & SSL SWG di CLI dan alat AI di Mac](https://swgbar.com/id/guides/swg-tls-certificate-errors-macos/) — atasi `CERTIFICATE_VERIFY_FAILED` dan error penerbit lokal pada `git`, `npm`, `Python`, `Claude Code`, dan `Cursor`.

**Status rilis, diperiksa pada 18 November 2026:** versi resmi saat ini adalah **SWG bar 2.4.12** (build `42`), mencakup ekstensi jaringan native bertanda tangan untuk bypass SWG per domain, CLI `swgbar` dan server MCP, serta ekstensi pendamping Chrome `2.1.13`. Checksum SHA-256, tanda tangan Apple, dan notarisasi paket telah diverifikasi. Lihat [informasi rilis](https://swgbar.com/id/releases/) dan [panduan resmi](https://swgbar.com/id/guides/).

## Pertanyaan dan masukan

Ini adalah repositori resmi untuk pengenalan publik proyek. Gunakan [Issues](https://github.com/nonbutAworker/swg-bar/issues) untuk pertanyaan publik dan saran dokumentasi. Untuk instalasi, pesanan, atau dukungan pribadi, hubungi [support@swgbar.com](mailto:support@swgbar.com). Jangan memublikasikan kunci lisensi atau riwayat penjelajahan.

[Tentang SWG bar](https://swgbar.com/id/about/) · [Privasi](https://swgbar.com/id/privacy/) · [Privasi ekstensi](https://swgbar.com/id/extension-privacy/) · [Ketentuan](https://swgbar.com/id/terms/)
