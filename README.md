#  CRUD PHP API (Laragon + MySQL)

Proyek ini merupakan **REST API CRUD sederhana** yang dibuat menggunakan **PHP Native** dan **MySQL**, serta dijalankan menggunakan **Laragon** sebagai local server.  
API ini digunakan untuk mengelola data pengguna (user) — seperti menambah, menampilkan, memperbarui, dan menghapus data.

---

## Fitur CRUD
| Metode | Deskripsi | Endpoint | Body (JSON) |
|---------|------------|-----------|--------------|
| **GET** | Menampilkan semua data user | `/index.php` | - |
| **GET** | Menampilkan 1 user berdasarkan ID | `/index.php/{id}` | - |
| **POST** | Menambah user baru | `/index.php` | `{ "username": "budi", "email": "budi@gmail.com", "password": "12345" }` |
| **PUT** | Memperbarui data user | `/index.php/{id}` | `{ "email": "budi_update@gmail.com" }` |
| **DELETE** | Menghapus user | `/index.php/{id}` | - |

---

## ⚙️ Teknologi yang Digunakan
-  PHP Native  
-  MySQL Database  
- Laragon (Local Server)  
-  Postman (Testing API)

---

##  Struktur Folder Proyek
CRUD/
│
├── index.php # File utama API (handle semua request)
├── database.sql # (Opsional) File SQL untuk import tabel
└── README.md # Dokumentasi proyek


---

##  Struktur Tabel Database
Gunakan database bernama **`my_app`**, lalu buat tabel `users` dengan struktur berikut:

```sql
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(100) NOT NULL,
  email VARCHAR(100) NOT NULL,
  password VARCHAR(255) NOT NULL
);

