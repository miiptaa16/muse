# Website Muse

Struktur proyek:

```
muse-project/
├── index.html
└── css/
    └── style.css
```

Buka `index.html` di browser (lewat Live Server) untuk melihat website-nya.
Semua styling ada di `css/style.css`. Warna brand Muse diatur di bagian
`:root` paling atas file CSS, jadi kalau mau ganti warna cukup ubah di satu
tempat itu saja.

## Struktur halaman (single page)

Sekarang cuma ada 1 halaman dengan 4 section utama yang dihubungkan lewat
navigasi anchor:

- `#home` — hero / perkenalan singkat
- `#about` — tentang Muse, kenapa beda dari agensi lain, dan untuk siapa
  Muse dibuat (dulunya 3 section terpisah, sekarang digabung jadi satu
  section About dengan beberapa sub-bagian)
- `#services` — daftar layanan
- `#contact` — info kontak (WhatsApp, email, Instagram) + form kontak

## Yang perlu kamu ganti

- Nomor WhatsApp: cari `wa.me/6281234567890` di `index.html`
- Email: cari `hello@musedigital.id`
- Instagram: cari `instagram.com/muse.digital`
- Form kontak (`#contact-form`) saat ini masih statis (tampil pesan "Terima
  kasih" lewat JavaScript). Kalau mau pesan beneran masuk ke email/WhatsApp
  kamu, hubungkan lewat layanan seperti Formspree, Getform, atau backend
  sendiri, lalu ganti bagian `form.addEventListener('submit', ...)` di
  `index.html`.

## Yang berubah dari versi sebelumnya

- Nav disederhanakan jadi 4 link: Home, About, Services, Contact. Sticky,
  ada highlight link aktif sesuai scroll, dan menu mobile (hamburger) di
  layar kecil
- Section "Kenapa Beda" dan "Untuk Siapa" digabung ke dalam About sebagai
  sub-bagian, bukan section terpisah
- Section "Kolaborasi" (CTA) diganti jadi section Contact yang punya info
  kontak + form

## Perombakan tampilan (v3 — desain ulang total)

Versi ini dirombak dari nol dengan konsep "meja pasar thrift / editorial",
bukan sekadar mengganti warna dari versi sebelumnya:

- **Warna**: ink coklat gelap hampir hitam (`--ink`), clay/terracotta yang
  lebih dalam (`--clay`), moss green (`--moss`) untuk sentuhan
  "berkelanjutan", dan mustard (`--sand`) sebagai aksen tag. Kombinasi ini
  lebih spesifik ke tema thrift & sustainable fashion, bukan palet cream-
  oranye generik
- **Hero**: headline sekarang satu warna penuh (tidak ada trik "satu kata
  dikasih warna beda" yang terasa template), dan visualnya pakai gantungan
  tag harga (`.hang-tag`) yang nempel di kartu baju preloved — motif yang
  memang relevan ke bisnis thrift, bukan ikon roket/lingkaran generik
- **Label eyebrow dihapus**: label kecil di atas tiap judul section
  ("Tentang Muse", "Layanan", dst) dihapus karena itu pola template yang
  paling gampang ketahuan hasil AI. Sekarang judul section langsung
  menyampaikan pesannya sendiri
- **"Kenapa Beda"**: diganti dari tabel/kartu perbandingan jadi gaya
  "coretan editor" — teks lama dicoret, teks baru ditulis ulang dengan
  warna clay & font italic, seperti draft yang sedang direvisi. Ini pas
  karena Muse juga jualan jasa copywriting
- **Services**: sekarang jadi section gelap (invert warna) supaya section
  ini jadi titik paling menonjol di halaman — seperti rak baju di bawah
  lampu toko malam hari — dan section lain di sekitarnya dibuat tenang
- **Kontak**: tombol kirim pesan pakai warna moss (bukan clay) supaya
  warna moss punya fungsi jelas, bukan cuma dekorasi
- Semua daftar (perbandingan, layanan, channel kontak) memakai motif garis
  tipis (hairline) yang sama supaya terasa satu sistem desain, bukan
  campuran kartu-kartu dengan gaya berbeda-beda