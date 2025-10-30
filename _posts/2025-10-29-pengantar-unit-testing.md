---
title: "Materi 5: Pengantar Unit Testing"
date: 2025-10-24 10:00:00 +0800
categories: [Software Testing, QA]
tags: [Unit Testing, Pytest, JUnit, Jest, Software QA]
image:
  path: /assets/image/pengantar-unit-testing.jpg
  alt: "Unit Testing Frameworks"
---

# 🧩 Materi 5: Pengantar Unit Testing

---

## 1. Definisi: Apa Itu Unit Testing?

**Unit Testing** adalah proses pengujian yang dilakukan pada **bagian terkecil dari program (unit)** — biasanya berupa fungsi, metode, atau kelas — untuk memastikan bahwa bagian tersebut bekerja sesuai yang diharapkan.

Unit testing merupakan **lapisan pertama** dalam *software testing pyramid* dan biasanya dilakukan oleh **developer** secara otomatis menggunakan framework pengujian.

🧠 **Tujuan utamanya:**  
- Memastikan setiap komponen kode berfungsi dengan benar.  
- Mendeteksi bug lebih awal sebelum proses integrasi.  
- Menjaga stabilitas sistem saat melakukan perubahan kode (*refactoring*).  

---

## 2. Keunggulan Unit Testing

Berikut alasan mengapa unit testing sangat penting dalam siklus pengembangan perangkat lunak:

| Keunggulan | Penjelasan |
|-------------|------------|
| 🔍 **Deteksi Dini Bug** | Kesalahan ditemukan lebih cepat saat tahap pengembangan awal. |
| ⚙️ **Meningkatkan Keandalan** | Setiap unit diuji terpisah, sehingga fungsi sistem lebih stabil. |
| 🧩 **Mempermudah Refactoring** | Perubahan kode tidak menimbulkan efek samping karena tes otomatis akan mendeteksinya. |
| 💬 **Dokumentasi Hidup** | Unit test berfungsi sebagai dokumentasi cara kerja kode. |
| 🚀 **Meningkatkan Kecepatan Deployment** | Dengan test otomatis, QA tidak perlu mengulang pengujian manual untuk fungsi dasar. |

> Dengan kata lain, **unit testing = keamanan bagi developer** saat melakukan perubahan kode.

---

## 3. Framework & Tools Populer

Beberapa framework yang paling sering digunakan untuk melakukan unit testing antara lain:

| Bahasa | Framework | Keterangan |
|---------|------------|------------|
| **Java** | [JUnit](https://junit.org/junit5/) | Framework paling populer untuk pengujian unit di Java. |
| **Python** | [Pytest](https://docs.pytest.org/en/stable/) | Framework ringan dengan sintaks sederhana dan dukungan assert bawaan. |
| **JavaScript** | [Jest](https://jestjs.io/) | Digunakan untuk menguji aplikasi React, Node.js, atau proyek JS modern. |
| **C#** | [NUnit](https://nunit.org/) | Framework testing serbaguna untuk .NET. |
| **PHP** | [PHPUnit](https://phpunit.de/) | Framework standar untuk pengujian aplikasi PHP. |

---

## 4. Struktur Tes: Pola AAA (Arrange, Act, Assert)

Pola dasar dalam unit testing disebut **AAA Pattern**:

| Langkah | Deskripsi |
|----------|------------|
| 🧱 **Arrange** | Menyiapkan semua data dan objek yang diperlukan untuk pengujian. |
| ⚙️ **Act** | Menjalankan fungsi atau metode yang ingin diuji. |
| ✅ **Assert** | Memverifikasi bahwa hasil yang diperoleh sesuai dengan yang diharapkan. |

📘 **Contoh logika AAA:**

```python
# Arrange
nilai = [80, 90, 100]

# Act
rata_rata = sum(nilai) / len(nilai)

# Assert
assert rata_rata == 90
