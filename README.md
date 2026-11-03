# Resep Warm

Aplikasi web resep makanan berbasis Laravel. Pengguna dapat mencari resep dari Spoonacular API, mendapatkan rekomendasi resep dari bahan yang dimiliki, mengubah foto makanan atau minuman menjadi resep dengan Gemini API, serta membuat dan menyimpan resep sendiri.

## Fitur Utama

- **Pencarian resep**: cari resep berdasarkan nama makanan melalui Spoonacular API.
- **Rekomendasi dari bahan**: masukkan bahan yang dimiliki, aplikasi menampilkan resep yang memakai bahan tersebut.
- **Resep dari foto (AI)**: unggah foto makanan atau minuman, Gemini API menghasilkan nama hidangan, jenis hidangan, waktu memasak, porsi, bahan, dan langkah memasak.
- **Resep favorit**: simpan resep dari Spoonacular maupun resep hasil AI ke daftar favorit, lalu lihat, ubah, dan hapus.
- **Resep Saya**: buat, lihat, ubah, dan hapus resep buatan sendiri.
- **Autentikasi pengguna**: registrasi, login, verifikasi email, reset password.
- **Dashboard**: ringkasan jumlah favorit dan resep pribadi, resep favorit terbaru, dan rekomendasi resep.

## Teknologi

- Backend: PHP 8.2+, Laravel 11
- Frontend: Blade, Tailwind CSS, Alpine.js, Vite
- Basis data: MySQL 
- Autentikasi: Laravel Breeze
- API eksternal: Spoonacular API, Google Gemini API


## Instalasi

1. Clone repository dan masuk ke foldernya.
   ```bash
   git clone https://github.com/LouisJonathan88/resep_warm.git
   cd resep_warm
   ```
2. Pasang dependency.
   ```bash
   composer install
   npm install
   ```
3. Salin file environment dan buat application key.
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
4. Buat database MySQL, lalu atur koneksi di `.env`.
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=resep_fix
   DB_USERNAME=root
   DB_PASSWORD=
   ```
5. Tambahkan API key di `.env`.
   ```env
   SPOONACULAR_API_KEY=isi_api_key_spoonacular
   GEMINI_API_KEY=isi_api_key_gemini
   ```
6. Jalankan migration dan buat symbolic link untuk penyimpanan gambar.
   ```bash
   php artisan migrate
   php artisan storage:link
   ```

## Menjalankan Aplikasi

Jalankan dua perintah ini di terminal terpisah:

```bash
php artisan serve
npm run dev
```