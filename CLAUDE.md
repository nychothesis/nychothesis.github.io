# Homepage Nychothesis

Landing page utama brand. Halaman publik pertama yang dilihat orang.

> Profil brand, gaya bahasa, dan preferensi visual ada di `CLAUDE.md` root
> (`Vibe Code/CLAUDE.md`) — berlaku juga di sini, ga perlu diulang.

## Fakta repo
- Folder lokal: `homepage/` — **beda dari nama repo**, disengaja.
- Repo: `nychothesis/nychothesis.github.io` (publik). Nama repo **wajib** persis
  begitu karena ini GitHub Pages *user site*. Jangan pernah di-rename — situsnya mati.
- Live: **https://nychothesis.com** (custom domain via file `CNAME`).
- Deploy: push ke `main`, Pages auto-update. Ga ada build step.

## Isi
- `index.html` — seluruh halaman, satu file, CSS inline. Ga ada dependency.
- `CNAME` — isinya `nychothesis.com`. **Jangan dihapus** atau custom domain-nya lepas.
- `assets/logo.svg`, `assets/og.png` — og.png dipakai buat preview link
  (og:image + twitter card).

## Struktur halaman
Hero → **01 Start here** (course, PDF gratis, Discord) → **02 Buktinya**
(foto + satu klaim dibedah bertingkat + dua aturan main) → penutup WhatsApp.

Dua bagian lama, **Empat lensa** dan **Cara Kerja**, udah dibubarin 2026-08-09.
Empat lensa dibuang karena namanya udah kesebut di hero dan tiap pertanyaan di
hero udah mewakili satu lensa, jadi kartunya cuma ngulang. Cara Kerja diperes
masuk ke Buktinya. Hasilnya halaman turun dari 434 kata jadi 358 kata **sambil**
nambah bukti dan foto.

## Catatan kerja
- **Isi hero berurutan**: kicker nama → empat pertanyaan (kecil, abu-abu) →
  kalimat besar → baris empat pilar → tombol.
- **Prinsipnya: pertanyaan mancing, kalimat besar yang bayar.** Makanya yang
  digedein kalimatnya, bukan pertanyaannya. Sempat dicoba kebalik dan gagal
  sendiri: pertanyaan yang bagus itu spesifik, spesifik itu panjang, dan panjang
  ga bisa dipasang gede. Diputusin 2026-08-09.
- **Tagline Inggris udah ga ada di hero.** "I explain the unexplainable"
  itu kalimat sikap, bukan kalimat isi, dan kalimat besar yang sekarang
  ngelakuin tugasnya dengan lebih konkret. Taglinenya masih idup di lynk.id dan
  di tag `og:`/`twitter:`.
- **Pertanyaan hero jangan yang nyalahin siapa-siapa.** "Kenapa yang tulus malah
  jadi cadangan" itu keluhan yang dikasih tanda tanya, dan itu bahasa red pill,
  kategori yang justru lagi dijauhin. Pertanyaan yang bener nunjuk ke
  **mekanisme**, bukan ke pihak. Satu dari tiga segmen audiens itu cewe, dan
  pertanyaan model nuduh ngusir mereka di baris pertama.
- **Tiap pertanyaan mewakili satu pilar**, urut: psychology, evolution, society,
  philosophy. Itu yang bikin baris pilar di bawahnya jadi keterangan, bukan
  hiasan.
- **Ukuran huruf di hero jangan dikira-kira, diukur.** Lebar tiap huruf bisa
  diambil dari `assets/fonts/poppins-900.woff2` pakai fontTools. Kolom kiri hero
  paling sempit **581px** (kejadiannya pas layar 861px, waktu kubus baru muncul
  dan mulai makan tempat). Pernah kejadian judul disetel 2.5rem tanpa diukur dan
  baris terakhirnya kelipet.
- **Selisih ukuran pertanyaan vs kalimat besar harus dijaga sekitar 1,7x di
  semua lebar.** Pernah kejadian di HP tinggal 1,29x karena pertanyaannya
  ukurannya mati sementara judulnya ikut ngecil. HP itu tampilan utama, bukan
  kasus pinggiran, soalnya trafiknya dari bio sosmed.
- **Baris tingkatan (`.tiers li`) itu grid dua kolom.** Keterangannya WAJIB
  dibungkus satu `<span class="d">`. Kalau ditulis teks polos terus di dalemnya
  ada `<i>` atau `<b>`, tag itu kehitung jadi kotak grid sendiri dan nyasar ke
  kolom label baris bawahnya.
- **JS pemecah kata cuma ngegarap h1 PERTAMA di halaman**, dan tiap potongan
  dibungkus `<span class="w">`. Jangan pernah bikin aturan `.w { display: block }`
  lagi, itu bikin satu kata jadi satu baris.
- Poppins buat judul, tombol, dan label. **Badan teks Atkinson.** Pernah kejadian
  daftar tingkatan balik ke Poppins gara-gara dipindah keluar dari `.rigor dd`.
- Foto `assets/nicho.jpg` cuma dipakai di bagian Buktinya, **bukan di hero**. Di
  hero dia rebutan mata sama pertanyaan. Foto mentahnya di-gitignore.
- Ejaan halaman ini konsisten `cowo`/`cewe` tanpa k, dan `ga` bukan `gak`.
- Nama brand ditulis `NYCHO` + `THESIS`, bagian **THESIS** berwarna emas.
- Motif kubus dipakai sebagai cap air di kanan hero, dimatikan di tablet ke bawah.
- Kalau ganti judul/deskripsi, cek juga tag `og:` dan `twitter:` di `<head>`
  biar preview link ga ketinggalan.
