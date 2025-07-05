# 📘 Panduan Instalasi Aplikasi Absensi Guru (Laravel)

Langkah‑langkah menyiapkan dan menjalankan aplikasi Absensi Guru di lingkungan lokal.

---

## 👥 Kelompok

- Ilham Nurul Ikhsan
- Nailan Shafa
- Rohimat

---

## 📦 0. Unduh & Ekstrak Berkas ZIP

1. Unduh rilis ZIP proyek (mis. aplikasi-absensi-guru.zip) dari GitHub atau sumber lain.
2. Ekstrak semua isinya ke folder pilihan di komputer Anda.

Setelah diekstrak, buka terminal / Command Prompt di dalam folder hasil ekstraksi, lalu lanjut ke langkah berikut.

---

## 🛠️ 1. Clone Repository *(opsional jika sudah ekstrak ZIP)*

    git clone https://github.com/username/aplikasi-absensi-guru.git
    cd aplikasi-absensi-guru

Lewati langkah ini jika Anda sudah mengekstrak ZIP di langkah 0.

---

## 📦 2. Install Dependency

    composer install
    npm install        # jalankan jika proyek memakai Vite / front-end JS

---

## ⚙️ 3. Salin & Konfigurasi .env

    cp .env.example .env

Buka file .env lalu sesuaikan konfigurasi berikut:

    APP_NAME=AbsensiGuru
    APP_URL=http://localhost:8000

    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=absensi_guru
    DB_USERNAME=root
    DB_PASSWORD=

---

## 🔑 4. Generate App Key

    php artisan key:generate

---

## 🧬 5. Migrasi & Seeder (opsional)

    php artisan migrate --seed

---

## 🚀 6. Jalankan Aplikasi

    php artisan serve

Buka di browser:

    http://localhost:8000

---

## 📝 Catatan

- Pastikan MySQL/MariaDB aktif dan database `absensi_guru` sudah dibuat.
- Jika aplikasi memerlukan upload file, beri izin tulis pada folder storage/ lalu jalankan:

      php artisan storage:link

Selamat mencoba! 🎉
