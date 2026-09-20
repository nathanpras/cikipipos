# CiKiPi POS — Deploy ke Vercel

Isi folder ini cuma 2 berkas: `index.html` dan `bundle.js`. Ini situs statis
biasa (tidak perlu proses build apa pun), jadi upload-nya simpel — tidak
perlu install apa-apa di komputer, semua lewat browser.

Versi ini sama seperti yang dipasang di APK Android kemarin: data tersimpan
lokal di browser (IndexedDB), tidak ada cloud, tidak ada login.

## Langkah 1 — Bikin repo GitHub (lewat browser, tanpa install apa pun)

1. Buka https://github.com, login atau daftar akun dulu kalau belum punya
2. Klik tombol hijau **"New"** (atau ikon **+** di pojok kanan atas → **New repository**)
3. Nama repo: `cikipi-pos` (bebas, tapi ini yang gampang diingat)
4. Pilih **Public**
5. Klik **Create repository**
6. Di halaman repo yang baru dibuat, klik link **"uploading an existing file"**
7. **Drag & drop** kedua berkas (`index.html` dan `bundle.js`) dari folder
   hasil ekstrak zip ini ke kotak upload di situ
8. Scroll ke bawah, klik **"Commit changes"**

## Langkah 2 — Sambungkan ke Vercel

1. Buka https://vercel.com, klik **Sign Up**, pilih **Continue with GitHub**
   (pakai akun GitHub yang sama dari Langkah 1)
2. Setelah masuk, klik **"Add New..."** → **"Project"**
3. Cari repo `cikipi-pos` yang tadi dibuat, klik **Import**
4. Semua pengaturan biarkan default (Vercel otomatis kenali ini situs
   statis biasa) — langsung klik **Deploy**
5. Tunggu 30-60 detik, muncul halaman "Congratulations" dengan tautan
   seperti `cikipi-pos-xxxx.vercel.app` — itu alamat CiKiPi POS Anda yang
   baru, bisa dibuka dari HP atau komputer mana saja, tanpa login apa pun.

## Setelah online

- Buka tautan `.vercel.app` itu di Chrome/Safari HP Anda, tombol **Cetak**
  akan berfungsi normal (tidak perlu jalan memutar seperti sebelumnya)
- Bisa **"Add to Home Screen"** di iPhone/Android seperti sebelumnya
- Bisa juga dicoba lagi lewat **PWABuilder.com** untuk bikin APK — kali ini
  kemungkinan besar berhasil, karena halamannya publik, tidak terkunci
  login lagi

## Kalau nanti mau update aplikasinya

Setiap kali saya kasih `bundle.js` atau `index.html` versi baru, tinggal:
1. Buka repo `cikipi-pos` di GitHub
2. Klik berkas yang mau diganti → ikon pensil (Edit) → atau hapus & upload
   ulang yang baru
3. Commit changes

Vercel otomatis re-deploy sendiri setiap kali ada perubahan di GitHub —
tidak perlu buka Vercel sama sekali untuk update.
