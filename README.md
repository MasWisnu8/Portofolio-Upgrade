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

## Halaman admin dan guest
- **Guest (tamu):** `https://maswisnu8.github.io/Portofolio-Upgrade/`
- **Admin:** `https://maswisnu8.github.io/Portofolio-Upgrade/admin.html` (atau tambahkan `#admin` di akhir alamat).

Login admin memakai **GitHub fine-grained token** milik pemilik repo:
1. Buka https://github.com/settings/personal-access-tokens/new
2. Isi nama (mis. "Admin Portofolio") dan masa berlaku (mis. 1 tahun).
3. *Repository access* → **Only select repositories** → pilih `Portofolio-Upgrade`.
4. *Permissions* → *Repository permissions* → **Contents: Read and write**.
5. Klik **Generate token**, salin, lalu tempel di halaman login admin.

Setiap klik **Simpan** di admin membuat 1 commit ke `content.js` (foto baru masuk ke `assets/`). Tamu melihat perubahan sekitar 1–2 menit kemudian. Token hanya disimpan di browser, tidak pernah ditulis ke repo.

Catatan: statistik pengunjung dan tombol like hanya ada di versi Claude Artifact. Karena repo publik, file yang disembunyikan dari tamu tetap bisa ditemukan di repo.
