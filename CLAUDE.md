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
Hero (tagline "I explain the unexplainable") → **Start here** → **Empat lensa,
satu pertanyaan** (Evolution · Psychology · Philosophy · Society) → **Kenapa
isinya bisa dipegang**.

## Catatan kerja
- Nama brand ditulis `NYCHO` + `THESIS`, bagian **THESIS** berwarna emas.
- Motif kubus dipakai sebagai cap air di kanan hero, dimatikan di tablet ke bawah.
- Kalau ganti judul/deskripsi, cek juga tag `og:` dan `twitter:` di `<head>`
  biar preview link ga ketinggalan.
