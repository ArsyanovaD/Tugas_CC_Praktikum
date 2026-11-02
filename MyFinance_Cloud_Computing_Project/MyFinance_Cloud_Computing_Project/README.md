# MyFinance – Catatan Keuangan Harian

Project website statis sederhana untuk praktikum Cloud Computing. Dibuat menggunakan HTML, CSS, dan JavaScript tanpa backend atau database. Data transaksi disimpan di browser menggunakan `localStorage`.

## Menjalankan secara lokal
1. Ekstrak folder project.
2. Buka `index.html` menggunakan browser.
3. Tambahkan transaksi pemasukan dan pengeluaran untuk mencoba fitur.

## Deployment ke Azure Static Web Apps
1. Login ke GitHub dan buat repository baru, misalnya `myfinance-cloud`.
2. Upload `index.html` ke root repository, lalu commit.
3. Login ke portal Azure: https://portal.azure.com/
4. Cari **Static Web Apps** lalu pilih **Create**.
5. Pilih subscription yang tersedia (misalnya Azure for Students jika akun mendapatkannya), buat/pilih Resource Group, dan isi nama aplikasi `myfinance-web`.
6. Hosting plan pilih **Free** (jika tersedia). Deployment source pilih **GitHub**.
7. Authorize Azure untuk mengakses GitHub, lalu pilih Organization, Repository `myfinance-cloud`, dan Branch `main`.
8. Pada Build Details, pilih **Custom** atau konfigurasi yang sesuai untuk static HTML. Isi App location `/`, API location kosong, dan Output location kosong. Untuk file HTML statis tanpa proses build, konfigurasi dapat berbeda menurut tampilan portal yang digunakan.
9. Pilih region terdekat yang tersedia, lanjutkan **Review + create**, kemudian **Create**.
10. Buka resource Static Web App dan tunggu deployment selesai. Buka URL yang diberikan Azure untuk menguji website.

> Catatan: Nama menu dan pilihan di portal Azure dapat berubah. Ikuti pilihan yang tersedia pada akun/portal saat deployment. Azure for Students juga bergantung pada kelayakan akun mahasiswa.

## Continuous Deployment melalui GitHub
1. Setelah website berhasil online, buka repository GitHub.
2. Edit `index.html`, misalnya ubah teks footer menjadi `MyFinance – Praktikum Cloud Computing 2026`.
3. Klik **Commit changes** (atau push perubahan melalui Git).
4. Buka tab **Actions** pada repository untuk melihat workflow deployment.
5. Tunggu workflow selesai dengan status berhasil, lalu refresh URL Azure. Perubahan akan tampil otomatis karena Azure Static Web Apps terhubung ke repository.

## Ide modifikasi untuk bukti tugas
- Ubah judul header dari `MyFinance` menjadi `MyFinance – Versi 2`.
- Ubah teks footer menjadi `Website ini telah diperbarui melalui GitHub`.
- Commit perubahan dan ambil screenshot halaman GitHub, workflow Actions yang sukses, serta website Azure setelah diperbarui.

## Screenshot yang perlu diambil sendiri
Screenshot harus berasal dari proses akun dan deployment milik mahasiswa:
1. Website berjalan secara lokal.
2. Repository GitHub berisi `index.html`.
3. Konfigurasi Azure Static Web Apps.
4. Proses deployment / workflow GitHub Actions berhasil.
5. Website terbuka melalui URL Azure.
6. Perubahan `index.html` setelah commit.
7. Website Azure setelah perubahan tampil.

Jangan gunakan screenshot contoh sebagai bukti deployment pribadi.
