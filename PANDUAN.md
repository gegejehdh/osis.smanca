# Panduan Website OSIS + Aplikasi Admin

Isi folder:
- `public/index.html`  → website publik OSIS
- `admin/`             → aplikasi admin (index.html, manifest.json, sw.js, ikon)
- `firestore.rules`    → aturan keamanan database

## 1. Siapkan Firebase (gratis)
1. Buka https://console.firebase.google.com → **Add project**.
2. **Build → Firestore Database → Create database** (mode production).
3. **Build → Authentication → Get started → Email/Password → Enable**. Lalu tab *Users → Add user*: buat email + kata sandi admin.
4. **Project settings → Your apps → Web (</>)** → daftarkan app, salin objek `firebaseConfig`.
5. **Firestore → Rules**: tempel isi `firestore.rules`, ganti `GANTI_DENGAN_EMAIL_ADMIN@gmail.com` dengan email admin tadi, lalu **Publish**.

## 2. Isi konfigurasi
Di `public/index.html` dan `admin/index.html`, ganti objek `FIREBASE_CONFIG` (cari tulisan `ISI_API_KEY`) dengan konfigurasi dari langkah 4.

## 3. Pasang di hosting
Pakai Firebase Hosting, GitHub Pages, atau Netlify (gratis):
- Website publik: unggah `public/index.html`
- Aplikasi admin: unggah isi folder `admin/` di alamat terpisah (harus HTTPS)

## 4. Jadikan APK
Buka https://www.pwabuilder.com → masukkan alamat aplikasi admin → **Package for stores → Android** → unduh APK dan pasang di HP.
(Tanpa APK pun bisa: buka alamat admin di Chrome HP → menu ⋮ → **Tambahkan ke layar utama**.)

## Catatan
- Sebelum Firebase diisi, website publik tetap jalan dengan data contoh (aspirasi hanya tersimpan di perangkat).
- Berita, program, kegiatan, galeri, pengurus, dan anggota diatur dari aplikasi admin dan langsung tampil di website publik.
