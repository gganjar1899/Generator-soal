# BuatSoal Pro - Hybrid Server Mode

Aplikasi generator soal yang bisa dipakai guru tanpa memasukkan API key.
API key Gemini disimpan di server Vercel melalui Environment Variables.

## Isi Folder

- `public/index.html` = aplikasi utama
- `api/generate.js` = backend proxy Gemini
- `vercel.json` = konfigurasi Vercel
- `package.json` = konfigurasi project

## Cara Pasang di Vercel

1. Buat akun/login di Vercel.
2. Buat project baru.
3. Upload folder ini ke GitHub, lalu import ke Vercel.
4. Buka menu Project Settings > Environment Variables.
5. Tambahkan:
   - Name: `GEMINI_API_KEY`
   - Value: isi API key Gemini Bapak
6. Opsional tambahkan:
   - Name: `GEMINI_MODEL`
   - Value: `gemini-2.5-flash`
7. Deploy ulang.
8. Buka link Vercel. Guru cukup pilih **Server Gemini - Tanpa API Key Guru**.

## Cara Pakai Guru

- Buka link aplikasi.
- Pilih mode `Server Gemini - Tanpa API Key Guru`.
- Isi mapel, kelas, materi, jumlah soal.
- Klik Generate.

Jika server belum dikonfigurasi, guru bisa pilih `Offline Template`.

## Catatan Keamanan

Jangan menaruh API key Gemini di file HTML. Simpan hanya di Environment Variables Vercel.
