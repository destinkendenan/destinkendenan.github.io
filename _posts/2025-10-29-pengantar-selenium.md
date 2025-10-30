---
title: "Materi 7: Pengantar Selenium WebDriver"
date: 2025-10-24 23:00:00 +0800
categories: [Software Testing]
tags: [Selenium, Automation Testing, Python]
image: /assets/image/pengantar-selenium.jpg
---

## 🧠 Pengantar Selenium WebDriver

### 📘 Apa itu Selenium?
**Selenium** adalah sebuah framework open-source yang digunakan untuk mengotomatisasi pengujian aplikasi web di berbagai browser.  
Dengan Selenium, pengujian dapat dilakukan tanpa interaksi manual terhadap antarmuka pengguna.

Selenium memiliki beberapa komponen utama:
1. **Selenium IDE** – alat perekam dan pemutaran (*record & playback*) sederhana untuk membuat skrip otomatis.
2. **Selenium WebDriver** – API untuk berinteraksi langsung dengan browser melalui kode.
3. **Selenium Grid** – digunakan untuk menjalankan pengujian paralel di berbagai browser dan mesin.

---

### ⚙️ Apa itu Selenium WebDriver?
**Selenium WebDriver** adalah komponen utama Selenium yang memungkinkan pengujian otomatis berbasis kode.  
WebDriver bertindak sebagai jembatan antara *script automation* dengan browser, seperti Chrome, Firefox, Edge, atau Safari.

Dengan WebDriver, kita bisa:
- Membuka dan menutup browser secara otomatis  
- Mengisi form, klik tombol, scroll halaman  
- Mengambil data dari elemen HTML  
- Melakukan validasi hasil uji

---

### 💡 Kenapa Harus Selenium?
Beberapa alasan kenapa Selenium banyak digunakan:
- ✅ **Open-source & gratis**
- 🌍 **Mendukung banyak browser dan platform** (Chrome, Firefox, Edge, Safari)
- 🐍 **Mendukung berbagai bahasa pemrograman** (Python, Java, C#, Ruby, JavaScript)
- 🤖 **Dapat diintegrasikan dengan CI/CD tools** seperti Jenkins, GitHub Actions, atau GitLab CI
- 🔄 **Mendukung automation testing end-to-end**

---

### 🧰 Instalasi Selenium dengan Python

Langkah-langkah instalasi:

1. **Pastikan Python sudah terinstal**  
   Cek dengan perintah:
   ```bash
   python --version
