---
title: "Materi 6: Pengantar API Testing"
date: 2025-10-24 22:00:00 +0800
categories: [Software Testing]
tags: [API Testing, Postman, Software Quality]
image: /assets/image/pengantar-api-testing.jpg
---

## 🔍 Pengantar API Testing

### 📘 Definisi
**API Testing** adalah proses pengujian antarmuka pemrograman aplikasi (Application Programming Interface) untuk memastikan bahwa setiap endpoint bekerja sesuai spesifikasi.  
Berbeda dengan *UI Testing* yang berfokus pada tampilan, **API Testing** langsung menguji komunikasi antar komponen atau sistem melalui request dan response data.

API Testing membantu memverifikasi:
- Integrasi antar modul berjalan baik  
- Data yang dikirim dan diterima sudah benar  
- Kinerja, keamanan, dan keandalan API  

---

### 🎯 Keunggulan API Testing
Beberapa alasan kenapa pengujian API sangat penting:
1. **Deteksi kesalahan lebih awal** — karena API diujikan sebelum UI selesai dibangun.  
2. **Pengujian cepat & efisien** — tidak bergantung pada tampilan antarmuka.  
3. **Meningkatkan reliabilitas sistem** — memastikan komunikasi antar layanan berjalan konsisten.  
4. **Mendukung otomatisasi** — mudah diintegrasikan dengan CI/CD pipeline.

---

### 🧰 Tools API Testing
Berikut beberapa tools populer untuk melakukan API Testing:

| Tool | Deskripsi Singkat |
|------|--------------------|
| **Postman** | Tool paling populer untuk mengirim, mengelola, dan menguji request API. |
| **SoapUI** | Digunakan untuk pengujian layanan berbasis SOAP dan REST dengan antarmuka lengkap. |
| **cURL** | Command line tool sederhana untuk mengirim request HTTP secara manual. |
| **Newman** | CLI Postman untuk menjalankan koleksi API secara otomatis. |

Pada materi ini, fokus kita menggunakan **Postman**.

---

### 🧩 Konsep Dasar: Anatomi Request & Response API

#### Request
Sebuah **request** terdiri dari beberapa elemen penting:
- **Method**: Jenis operasi (GET, POST, PUT, DELETE)
- **URL/Endpoint**: Alamat API (misal: `https://jsonplaceholder.typicode.com/posts`)
- **Headers**: Informasi tambahan seperti format data (`Content-Type: application/json`)
- **Body**: Data yang dikirim (biasanya dalam format JSON)

#### Response
Response dari API biasanya terdiri dari:
- **Status Code** (misal: 200 OK, 404 Not Found, 500 Server Error)
- **Headers**
- **Body** berisi data hasil request (biasanya JSON)

---

### ⚙️ Operasi Dasar di Postman

1. **Membuka Postman**
   - Klik tombol **New → HTTP Request**
   - Pilih method (GET/POST)
   - Masukkan URL endpoint API

2. **Menjalankan Request GET**
   - Method: `GET`  
   - URL: `https://jsonplaceholder.typicode.com/posts/1`  
   - Klik tombol **Send**  
   - Lihat hasil di tab *Response* (kode status, waktu, dan data JSON)

3. **Menjalankan Request POST**
   - Method: `POST`  
   - URL: `https://jsonplaceholder.typicode.com/posts`  
   - Tab **Body → Raw → JSON**  
   - Masukkan contoh data berikut:
     ```json
     {
       "title": "Belajar API Testing",
       "body": "API testing dengan Postman sangat menyenangkan!",
       "userId": 1
     }
     ```
   - Klik **Send**, lalu perhatikan response `id` baru yang dihasilkan.

---

### 💡 Studi Kasus: API Publik JSONPlaceholder

#### Contoh GET Request menggunakan Python (requests)
```python
import requests

url = "https://jsonplaceholder.typicode.com/posts/1"
response = requests.get(url)

print("Status Code:", response.status_code)
print("Response JSON:", response.json())
