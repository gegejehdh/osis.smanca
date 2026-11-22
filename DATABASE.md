# Struktur Database (Cloud Firestore)

| Koleksi | Isi dokumen | Dibaca | Diubah |
|---|---|---|---|
| `settings/main` | name, school, desc, addr, email, ig, wa, sec, vision, mission, history, values | Publik | Admin |
| `members` | name, role, grp (`Pembina` / `Inti` / `Anggota`), desc | Publik | Admin |
| `programs` | name, field, desc, goal, pic, time, status | Publik | Admin |
| `activities` | name, date, time, place, desc, status | Publik | Admin |
| `news` | title, type (`Berita`/`Pengumuman`), cat, date, body | Publik | Admin |
| `gallery` | title, kind (`Foto`/`Video`), cat | Publik | Admin |
| `aspirations` | kelas, kat, sub, isi, status, at, nama (opsional), resp (tanggapan) | Admin | Siswa hanya bisa mengirim |
| `stats/asp` | n (jumlah aspirasi) | Publik | Otomatis |

## Cara mengisi data awal
**Termudah:** login ke aplikasi admin → tab **Ringkasan** → tombol **Isi data awal ke database**.

Alternatif: file `database-seed.json` berisi data yang sama (format koleksi → id dokumen → isi).
