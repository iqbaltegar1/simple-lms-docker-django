# 🚀 Simple LMS - Docker & Django Foundation

## 📌 Deskripsi

Project ini merupakan implementasi **Django Web Framework** yang dijalankan menggunakan **Docker Compose** dengan **PostgreSQL** sebagai database.

Tujuan dari project ini adalah untuk memahami:

- Containerization menggunakan Docker
- Multi-container dengan Docker Compose
- Integrasi Django dengan PostgreSQL
- Penggunaan environment variables

---

## 🏗️ Project Structure

```
simple-lms/
├── docker-compose.yml
├── Dockerfile
├── .env.example
├── requirements.txt
├── manage.py
├── config/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── README.md
```

---

## 🐳 Teknologi yang Digunakan

- Python 3.11
- Django
- PostgreSQL
- Docker & Docker Compose

---

## ⚙️ Environment Variables

Buat file `.env` berdasarkan `.env.example`

Contoh:

```
DEBUG=True
SECRET_KEY=your-secret-key

DB_NAME=lms_db
DB_USER=lms_user
DB_PASSWORD=lms_pass
DB_HOST=db
DB_PORT=5432
```

---

## 🚀 Cara Menjalankan Project

### 1. Clone Repository

```
git clone <URL_REPOSITORY>
cd simple-lms
```

---

### 2. Copy Environment File

```
cp .env.example .env
```

_(Windows bisa pakai: `copy .env.example .env`)_

---

### 3. Build & Run Docker

```
docker-compose up --build
```

---

### 4. Akses Aplikasi

Buka browser:

```
http://localhost:8000
```

Jika berhasil, akan muncul halaman **Django Welcome Page** 🎉

---

## 🧪 Testing Database (PostgreSQL)

Untuk memastikan koneksi database berjalan dengan baik, jalankan:

```
docker-compose exec web python manage.py migrate
```

Jika berhasil, akan muncul output:

```
Applying admin... OK
Applying auth... OK
Applying sessions... OK
```

✔️ Ini menandakan Django sudah terhubung dengan PostgreSQL

---

## 📸 Screenshot (Lampirkan)

Tambahkan screenshot berikut di repository:

1. Halaman Django (http://localhost:8000)
2. Hasil `docker ps` (3 container berjalan)
3. Hasil perintah migrate (berhasil)

---

## 📦 Docker Services

### 🔹 Web (Django)

- Menjalankan aplikasi Django
- Port: 8000

### 🔹 Database (PostgreSQL)

- Menyimpan data aplikasi
- Menggunakan volume untuk persistence

---

## 💾 Data Persistence

Database menggunakan Docker Volume:

```
postgres_data:/var/lib/postgresql/data
```

✔️ Data tetap aman meskipun container dihentikan

---

## ✅ Hasil Akhir

- ✔️ Django berjalan di Docker
- ✔️ PostgreSQL terhubung dengan baik
- ✔️ Environment variables digunakan
- ✔️ Multi-container berjalan dengan Docker Compose
- ✔️ Project structure sesuai best practice

---

## 🧠 Pembelajaran

Dari project ini, dipelajari:

- Cara membuat Dockerfile
- Cara menggunakan Docker Compose
- Cara menghubungkan Django dengan PostgreSQL
- Konsep container networking
- Environment configuration

---


## 👨‍💻 Author

- Nama: Iqbal Tegar Pratama  
- NIM: A11.2023.14969  
- Project: Simple LMS - Docker & Django Foundation  

---
