# Portofolio — Wisnu Pandu Hidayat

Website portofolio statis, siap tampil di **GitHub Pages**.

## Struktur
- `index.html` — tampilan dan logika halaman.
- `content.js` — **semua isi website** (profil, pengalaman, pendidikan, sertifikasi, keahlian, project, kontak). Ubah teks di sini lalu commit.
- `assets/img/` — foto; `assets/docs/` — PDF (CV dan sertifikat).
- `favicon.svg`, `.nojekyll` — ikon tab dan pengaturan GitHub Pages.

## Menambah project atau foto
1. Upload foto ke `assets/img/` (mis. `proyek-baru-1.jpg`).
2. Di `content.js`, tambahkan nama file itu ke `window.SITE_ASSETS` (mis. `"proyek-baru-1": "assets/img/proyek-baru-1.jpg"`).
3. Tambahkan project baru di `projects` dengan `cover` dan `photos` memakai kunci yang sama.

## Mengaktifkan GitHub Pages
Settings → Pages → Source: *Deploy from a branch* → pilih branch dan folder `/ (root)` → Save.

Catatan: mode admin (`#admin`), statistik pengunjung, dan tombol like hanya ada di versi Claude Artifact. Di GitHub Pages, isi diubah lewat `content.js`.
