SGRP98 RACEBOX — Android Studio project
========================================
Fitur versi awal:
- GPS speed real-time (KM/J)
- Drag timer otomatis mulai saat GPS speed >= 3 km/j
- Checkpoint 50 ft, 100 m, 201 m, 402 m
- Stop & simpan run ke penyimpanan lokal
- Riwayat run dan ekspor CSV

CARA MEMBUAT APK:
1. Ekstrak ZIP ini.
2. Buka folder SGRP98_Racebox melalui Android Studio (versi terbaru).
3. Tunggu Gradle Sync selesai; pastikan Android SDK 35 terpasang.
4. Pilih Build > Build Bundle(s) / APK(s) > Build APK(s).
5. APK debug akan muncul di app/build/outputs/apk/debug/app-debug.apk.

CATATAN:
- Ini project sumber Android, bukan APK yang sudah dikompilasi.
- GPS memerlukan izin lokasi dan sinyal terbuka; akurasi bergantung perangkat/lingkungan.
- Jalankan tes hanya di area tertutup/aman, jangan mengoperasikan ponsel saat berkendara.
- Versi awal menghitung jarak dari koordinat GPS berturut-turut; bukan alat ukur tersertifikasi.


CARA BUILD HANYA DENGAN HP (GitHub Actions):
1. Buat akun/login di https://github.com lewat browser HP.
2. Buat repository baru bernama SGRP98-Racebox (Public atau Private).
3. Upload seluruh isi folder project ZIP ini ke repository, termasuk folder .github.
   Pastikan file android-build.yml ada di .github/workflows/.
4. Buka tab Actions pada repository. Jika diminta, aktifkan Actions.
5. Pilih workflow "Build SGRP98 APK", tekan Run workflow.
6. Tunggu sampai proses selesai (tanda centang hijau).
7. Buka hasil run, cari bagian Artifacts, lalu download SGRP98-debug-APK.
8. Ekstrak ZIP artifact dan install app-debug.apk di HP. Izinkan instalasi dari sumber tersebut bila Android memintanya.

Jika upload lewat tampilan HP menyembunyikan folder .github, buat folder dan file workflow itu lewat fitur Add file > Create new file di GitHub dengan path:
.github/workflows/android-build.yml
Lalu tempel isi workflow yang ada pada file tersebut.
