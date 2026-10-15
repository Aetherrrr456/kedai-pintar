# Kedai Pintar - Membuat file APK (aplikasi Android)

GitHub akan membangun APK-nya otomatis di cloud (gratis). Anda tidak perlu menginstal apa pun di komputer.

## Langkah
1. Buat repository baru di GitHub (Public), mis. `kedai-pintar-apk`.
2. Klik **uploading an existing file**, lalu tarik SEMUA isi folder ini:
   `.github`, `www`, `assets`, `package.json`, `capacitor.config.json`.
   - Jika folder `.github` tidak ikut terunggah: klik **Add file > Create new file**, ketik nama
     `.github/workflows/build-apk.yml`, lalu tempel isi file `build-apk.yml` dan Commit.
3. Klik tab **Actions**. Jika muncul tombol untuk mengaktifkan workflow, klik. Pilih **Build APK**
   lalu **Run workflow**. (Otomatis berjalan juga setiap ada perubahan.)
4. Tunggu 5-10 menit sampai muncul tanda centang hijau.
5. Klik proses (run) yang berhasil, gulir ke **Artifacts**, unduh **KedaiPintar-APK**, ekstrak zip-nya,
   dan Anda mendapat file **app-debug.apk**.
6. Kirim APK ke HP Android (WhatsApp/Drive/kabel), buka, dan izinkan "Install dari sumber tidak dikenal".

## Mengganti logo/nama
- Nama: ubah `appName` di `capacitor.config.json`.
- Ikon: ganti 3 file di folder `assets` (icon-only.png, icon-foreground.png, icon-background.png), ukuran 1024x1024.

## Catatan
- Hanya untuk Android. iPhone tidak bisa memasang APK (gunakan Add to Home Screen).
- Data di APK tersimpan terpisah dari versi web. Pindahkan via Laporan > Backup data / Pulihkan data.
- Tombol Cetak struk memakai fitur cetak browser dan belum didukung di APK.
