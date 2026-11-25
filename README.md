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

Login admin memakai **username + password**.
- **Pertama kali:** buka halaman admin, buat username & password (min. 10 karakter), lalu tempel **GitHub fine-grained token** sekali saja (buat di https://github.com/settings/personal-access-tokens/new → *Only select repositories*: `Portofolio-Upgrade` → *Contents: Read and write*).
- Token disimpan **terenkripsi** di `admin-auth.json` (AES-GCM, kunci dari PBKDF2 600.000 putaran atas username+password). Tanpa password yang benar, file itu tidak bisa dipakai. Gunakan password yang panjang dan tidak dipakai di tempat lain.
- **Lupa password / token kedaluwarsa:** di halaman login klik *Atur ulang login*, lalu buat username, password, dan token baru.
- Ganti username/password: menu **Akun** di bar admin.

Setiap klik **Simpan** di admin membuat 1 commit ke `content.js` (foto baru masuk ke `assets/`). Tamu melihat perubahan sekitar 1–2 menit kemudian.

Catatan: statistik pengunjung dan tombol like hanya ada di versi Claude Artifact. Karena repo publik, file yang disembunyikan dari tamu tetap bisa ditemukan di repo.
