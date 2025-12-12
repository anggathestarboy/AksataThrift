# 🛍️ Thrift Malang – Fullstack Laravel + Tailwind (Vite)

Thrift Malang adalah aplikasi web fullstack untuk mengelola penjualan produk thrift. Aplikasi ini mendukung fitur CRUD, pencarian produk, sistem transaksi, serta memiliki dua role utama: **Admin** dan **User**. Dibangun menggunakan **Laravel**, **TailwindCSS**, dan **Vite**.

---

## ✨ **Fitur Utama**

### 🔐 **Role & Auth**

* **Admin**

  * CRUD produk (create, read, update, delete)
  * Mengelola transaksi
  * Melihat daftar seluruh user
* **User**

  * Melihat dan mencari produk
  * Melakukan transaksi pembelian

### 🧩 **Fitur Aplikasi**

* CRUD Produk
* Search Produk
* Manajemen Transaksi
* Role Admin & User
* UI menggunakan **TailwindCSS**
* Build system menggunakan **Vite**

---

## 🚀 **Tech Stack**

* **Laravel 11+** (Backend API & Frontend Blade)
* **TailwindCSS** (UI Styling)
* **Vite** (Bundler & Asset Management)
* **MySQL** (Database)

---

## 🛠️ **Instalasi & Setup Project**

Ikuti langkah-langkah berikut untuk menjalankan project di lokal Anda:

### **1️⃣ Clone Repository**

```bash
git clone https://github.com/username/thrift-malang.git
cd thrift-malang
```

### **2️⃣ Install Dependencies Laravel**

```bash
composer install
```

### **3️⃣ Install Dependencies Frontend (Vite + Tailwind)**

```bash
npm install
```

---

## ⚙️ **Konfigurasi Environment**

### **4️⃣ Buat file `.env`**

```bash
cp .env.example .env
```

### **5️⃣ Generate Key Laravel**

```bash
php artisan key:generate
```

### **6️⃣ Setup Database di `.env`**

Sesuaikan bagian berikut:

```env
DB_DATABASE=thrift_malang
DB_USERNAME=root
DB_PASSWORD=
```

---

## 🗄️ **Migration & Seeding**

### **7️⃣ Jalankan Migration**

```bash
php artisan migrate
```

### (Opsional) Seeder jika tersedia:

```bash
php artisan db:seed
```

---

## 🏃 **Menjalankan Project**

### **8️⃣ Jalankan server Laravel**

```bash
php artisan serve
```

### **9️⃣ Jalankan Vite**

```bash
npm run dev
```

Akses aplikasi melalui:

```
http://localhost:8000
```

---

## 📁 **Struktur Folder Penting**

```
app/
 ├── Models/        → Model Laravel
 ├── Http/Controllers/
resources/
 ├── views/         → Blade Templates
 ├── css/           → Tailwind Input
 ├── js/            → Vite Config JS
routes/
 ├── web.php        → Route UI
 ├── api.php        → Route API (jika digunakan)
```

---

## 🎨 **TailwindCSS + Vite Setup**

### File: `tailwind.config.js`

```js
module.exports = {
  content: [
    './resources/**/*.blade.php',
    './resources/**/*.js',
    './resources/**/*.vue',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

### File: `vite.config.js`

```js
import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';

export default defineConfig({
    plugins: [
        laravel({
            input: ['resources/css/app.css', 'resources/js/app.js'],
            refresh: true,
        }),
    ],
});
```

---

## 💳 **Fitur Transaksi**

### Admin

* Melihat daftar transaksi
* Mengubah status transaksi

### User

* Membeli produk
* Melihat riwayat transaksi

---

## 🧪 **Testing (Opsional)**

```bash
php artisan test
```

---

## 🏁 **Penutup**

Aplikasi Thrift Malang dibangun untuk menyediakan pengalaman jual beli produk thrift dengan fitur lengkap dan tampilan modern.

Jika ingin menambahkan fitur, memperbaiki bug, atau berkontribusi, silakan buat **issue** atau **pull request**.

Terima kasih telah menggunakan Thrift Malang! 🎉
