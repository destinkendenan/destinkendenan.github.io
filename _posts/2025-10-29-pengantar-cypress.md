---
title: "Materi 8: Pengantar Cypress"
date: 2025-10-24 23:00:00 +0800
categories: [Software Testing, Cypress]
tags: [Testing, Cypress, Automation, JavaScript]
image:
  path: /assets/image/pengantar-cypress.jpg
  alt: "Pengantar Cypress"
---

# 🧪 Materi 8: Pengantar Cypress

---

## 📘 Definisi

**Cypress** adalah framework **End-to-End Testing** berbasis **JavaScript** yang dirancang untuk melakukan pengujian aplikasi web secara langsung di browser.  
Berbeda dengan alat lain seperti **Selenium**, Cypress berjalan **di dalam browser yang sama dengan aplikasi yang diuji**, sehingga hasil pengujian lebih **akurat, cepat, dan stabil**.

### 🔹 Posisi Cypress dalam Testing
Cypress digunakan terutama untuk:
- **End-to-End Testing (E2E):** Menguji seluruh alur kerja dari sisi pengguna.
- **Integration Testing:** Menguji interaksi antar komponen aplikasi.
- **Component Testing:** Menguji komponen individual (khususnya untuk framework seperti React, Vue, atau Angular).

Cypress ditulis sepenuhnya dalam **JavaScript** dan sangat cocok digunakan pada **pengujian aplikasi web modern berbasis front-end framework**.

---

## ⚡ Keunggulan Cypress

Cypress memiliki beberapa keunggulan utama yang membuatnya berbeda dari framework testing lainnya seperti Selenium atau Puppeteer.  
Berikut adalah tiga fitur utama yang menjadikan Cypress populer di kalangan developer front-end.

---

### 🧱 1. Arsitektur Modern
Cypress memiliki arsitektur yang unik karena berjalan **langsung di dalam browser** yang sama dengan aplikasi yang diuji.  
Artinya, Cypress dapat:
- Mengakses DOM secara langsung.
- Menjalankan perintah dan mendeteksi event di browser **dalam waktu nyata**.
- Tidak bergantung pada server eksternal seperti Selenium WebDriver.

> 🔍 Hasilnya: Tes berjalan lebih **cepat, stabil,** dan **minim flakiness** (ketidakstabilan hasil tes).

---

### 🧭 2. Test Runner Interaktif
Cypress menyediakan **GUI Test Runner** yang sangat interaktif dan mudah digunakan.  
Dengan Test Runner ini, kita bisa:
- Melihat setiap langkah pengujian secara visual di browser.
- Menyaksikan hasil dan status setiap perintah secara langsung.
- Men-debug kesalahan tanpa perlu membuka console browser.

> 💡 Contoh: Saat test dijalankan, kamu bisa melihat elemen yang sedang diuji akan disorot langsung di halaman.

---

### ⏪ 3. Time Travel
Fitur **Time Travel** adalah salah satu keunggulan khas Cypress.  
Setiap kali perintah dijalankan (`cy.visit`, `cy.get`, `cy.click`, dll), Cypress mengambil **snapshot** dari DOM.

Dengan fitur ini, pengguna dapat:
- Melihat keadaan DOM pada setiap langkah test.
- Mengarahkan kursor ke langkah tertentu di Test Runner untuk melihat tampilan halaman saat itu.

> 🕰️ Keuntungan: Debugging menjadi jauh lebih mudah karena kamu bisa “kembali ke masa lalu” untuk melihat kondisi saat error terjadi.

---

## ⚙️ Instalasi Cypress

Sebelum menggunakan Cypress, pastikan kamu sudah menginstal **Node.js** dan **npm (Node Package Manager)** di sistem kamu.  
Cypress dijalankan sebagai dependensi pengembangan (development dependency) di dalam proyek JavaScript.

---

### 🪜 Langkah 1: Inisialisasi Project

Jika kamu belum memiliki project Node.js, buat project baru dengan perintah berikut:

```bash
npm init -y
