# LAPORAN PRAKTIKUM CLOUD COMPUTING
## Deployment Website MyFinance pada Microsoft Azure Static Web Apps

### 1. Tujuan
Membuat dan melakukan deployment website statis menggunakan Microsoft Azure Static Web Apps, serta memahami proses Continuous Deployment melalui GitHub.

### 2. Deskripsi Project
MyFinance merupakan website pencatatan keuangan harian sederhana. Website dapat mencatat pemasukan dan pengeluaran, menghitung saldo, menampilkan riwayat transaksi, serta menghapus transaksi. Website dibuat menggunakan HTML, CSS, dan JavaScript. Data disimpan pada localStorage browser sehingga tidak memerlukan server database.

### 3. Tools
- Visual Studio Code / editor teks
- Browser
- GitHub
- Microsoft Azure Static Web Apps

### 4. Langkah Pengerjaan dan Deployment
1. Membuat file `index.html` berisi struktur, desain, dan fungsi website MyFinance.
2. Membuka file `index.html` pada browser untuk memastikan website berjalan secara lokal.
   **[Masukkan Screenshot 1 – Website berjalan lokal]**
3. Membuat repository baru di GitHub dengan nama `myfinance-cloud`.
   **[Masukkan Screenshot 2 – Repository GitHub]**
4. Mengunggah file `index.html` ke root repository dan melakukan commit.
   **[Masukkan Screenshot 3 – File index.html di GitHub]**
5. Membuka Microsoft Azure Portal, mencari Static Web Apps, lalu memilih Create.
   **[Masukkan Screenshot 4 – Pembuatan Static Web App]**
6. Mengisi subscription dan resource group yang tersedia, nama aplikasi `myfinance-web`, serta memilih paket Free jika tersedia.
   **[Masukkan Screenshot 5 – Konfigurasi dasar Azure]**
7. Memilih GitHub sebagai sumber deployment, menghubungkan akun GitHub, lalu memilih repository `myfinance-cloud` dan branch `main`.
   **[Masukkan Screenshot 6 – Konfigurasi repository]**
8. Mengatur konfigurasi build untuk website HTML statis: App location `/`, API location kosong, dan Output location kosong. Lanjutkan proses Review + create dan Create.
   **[Masukkan Screenshot 7 – Konfigurasi deployment]**
9. Menunggu proses deployment selesai, kemudian membuka URL yang disediakan Azure.
   **[Masukkan Screenshot 8 – Website berhasil dibuka melalui Azure]**

### 5. Modifikasi Website dan Continuous Deployment
Setelah website berhasil di-deploy, lakukan perubahan pada file `index.html` di GitHub. Contoh perubahan:
- Mengubah judul website menjadi `MyFinance – Versi 2`.
- Mengubah teks footer menjadi `Website ini telah diperbarui melalui GitHub`.

Simpan perubahan dengan Commit changes. GitHub Actions akan menjalankan workflow deployment yang terhubung dengan Azure Static Web Apps. Setelah workflow berhasil, buka kembali URL Azure dan refresh halaman untuk melihat perubahan.
**[Masukkan Screenshot 9 – Perubahan file di GitHub]**
**[Masukkan Screenshot 10 – Workflow GitHub Actions berhasil]**
**[Masukkan Screenshot 11 – Website Azure setelah dimodifikasi]**

### 6. Penanganan Error
Jika deployment gagal, beberapa pemeriksaan yang dapat dilakukan:
1. Pastikan file `index.html` berada di root repository.
2. Pastikan Azure terhubung ke repository dan branch yang benar.
3. Periksa tab Actions pada GitHub untuk melihat detail workflow yang gagal.
4. Pastikan App location diisi `/` untuk file yang berada di root.
5. Periksa kembali konfigurasi build dan jalankan ulang deployment setelah memperbaiki kesalahan.

**[Masukkan screenshot error dan screenshot setelah berhasil diperbaiki jika terjadi error.]**

### 7. Kesimpulan
Melalui praktikum ini, website statis MyFinance dibuat menggunakan HTML, CSS, dan JavaScript, kemudian dipublikasikan melalui Microsoft Azure Static Web Apps dengan source code yang disimpan di GitHub. Integrasi GitHub memungkinkan perubahan pada source code memicu proses deployment kembali secara otomatis (Continuous Deployment). Dengan demikian, website dapat diperbarui tanpa mengunggah file secara manual ke hosting setiap kali terjadi perubahan.

---
Catatan: Lengkapi laporan dengan screenshot asli dari akun GitHub dan Azure yang digunakan saat praktikum. Jangan menyatakan deployment berhasil sebelum website benar-benar dapat diakses melalui URL Azure.
