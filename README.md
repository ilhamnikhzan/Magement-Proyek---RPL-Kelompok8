# 📘 Panduan Instalasi Aplikasi Absensi Guru (Laravel)

Langkah‑langkah menyiapkan dan menjalankan aplikasi **Absensi Guru** di lingkungan lokal.

---

## 🛠️ 1. Clone Repository

    git clone https://github.com/username/aplikasi-absensi-guru.git
    cd aplikasi-absensi-guru

## 📦 2. Install Dependency

    composer install
    npm install        # jalankan jika proyek memakai Vite/front‑end JS

## ⚙️ 3. Salin & Konfigurasi `.env`

    cp .env.example .env

Buka `.env` lalu sesuaikan nilai berikut:

    APP_NAME=AbsensiGuru
    APP_URL=http://localhost:8000

    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=absensi_guru
    DB_USERNAME=root
    DB_PASSWORD=

## 🔑 4. Generate App Key

    php artisan key:generate

## 🧬 5. Migrasi & Seeder (opsional)

    php artisan migrate --seed

## 🚀 6. Jalankan Aplikasi

    php artisan serve

Akses di browser: <http://localhost:8000>

---

## 📝 Catatan

- Pastikan MySQL/MariaDB aktif dan database `absensi_guru` sudah dibuat.
- Jika aplikasi memerlukan upload file, beri izin tulis pada `storage/` lalu jalankan:

      php artisan storage:link

Selamat mencoba! 🎉
