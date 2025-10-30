---
title: "Materi 4: Test Scenario, Test Case, and Bug Report"
date: 2025-10-24 10:00:00 +0800
categories: [Software Testing, QA]
tags: [Test Scenario, Test Case, Bug Report, QA, SDLC]
image:
  path: /assets/image/test-scenario.jpg
  alt: "Test Scenario and Bug Report"
---

# 🧩 Materi 4: Test Scenario, Test Case, and Bug Report

---

## 1. Pengantar
Dalam proses **Software Testing**, pembuatan *Test Scenario* dan *Test Case* merupakan langkah penting untuk memastikan bahwa seluruh fungsi perangkat lunak telah diuji secara menyeluruh dan sistematis.  
Selain itu, apabila ditemukan kesalahan (*bug*), maka perlu dibuat **Bug Report** agar tim pengembang dapat memperbaikinya dengan cepat dan tepat.

---

## 2. Test Scenario dan Test Case

### 2.1. Apa itu Test Scenario?
**Test Scenario** adalah **kondisi atau situasi pengujian tingkat tinggi** yang menggambarkan **apa** yang akan diuji pada suatu fitur aplikasi.  
Test scenario biasanya ditulis dari perspektif pengguna dan membantu mengidentifikasi area utama yang perlu diuji.

🧩 **Contoh:**  
> Verifikasi bahwa sistem dapat menghitung Body Mass Index (BMI) berdasarkan input berat dan tinggi pengguna.

---

### 2.2. Apa itu Test Case?
**Test Case** adalah **rangkaian langkah-langkah pengujian** yang lebih detail, digunakan untuk memverifikasi skenario tertentu.  
Setiap test case mencakup:
- **ID Test Case**
- **Deskripsi**
- **Langkah-langkah pengujian**
- **Data uji (test data)**
- **Hasil yang diharapkan**
- **Hasil aktual**
- **Status (PASS/FAIL)**

🧠 **Perbedaan singkat:**
| Aspek | Test Scenario | Test Case |
|--------|----------------|------------|
| Fokus | Apa yang diuji | Bagaimana cara menguji |
| Detail | Umum | Spesifik |
| Tujuan | Menentukan area uji | Menentukan langkah uji |

---

## 3. Template Sederhana

### 🧾 Template Test Scenario
| No | Test Scenario ID | Deskripsi Skenario | Modul | Prioritas |
|----|------------------|--------------------|--------|------------|
| 1 | TS001 | Verifikasi perhitungan BMI berdasarkan berat dan tinggi pengguna | BMI Calculator | Tinggi |
| 2 | TS002 | Verifikasi tampilan hasil BMI dan kategori kesehatan | BMI Calculator | Menengah |

---

### 🧾 Template Test Case
| No | Test Case ID | Skenario ID | Langkah Uji | Data Uji | Hasil yang Diharapkan | Hasil Aktual | Status |
|----|---------------|-------------|-------------|-----------|------------------------|---------------|---------|
| 1 | TC001 | TS001 | 1. Masukkan berat 60 kg dan tinggi 165 cm. <br> 2. Tekan tombol "Hitung BMI". | Berat: 60, Tinggi: 165 | BMI tampil dan hasilnya sesuai rumus (≈22.0) | Sesuai | PASS |
| 2 | TC002 | TS001 | 1. Masukkan berat kosong, tekan "Hitung BMI". | Berat: -, Tinggi: 170 | Tampil pesan error “Masukkan berat badan.” | Sesuai | PASS |
| 3 | TC003 | TS002 | 1. Hitung BMI 22. <br> 2. Periksa kategori hasil. | BMI = 22 | Tampil kategori “Normal” | Tidak tampil kategori | FAIL |

---

## 4. Contoh Test Scenario dan Test Case untuk Aplikasi BMI

### 📱 Deskripsi Aplikasi BMI
Aplikasi BMI digunakan untuk menghitung indeks massa tubuh pengguna berdasarkan **berat (kg)** dan **tinggi (cm)**, serta menampilkan **kategori kesehatan** seperti:  
- Kurus  
- Normal  
- Kelebihan berat badan  
- Obesitas  

---

### 🧩 Test Scenario
| No | Test Scenario ID | Deskripsi Skenario | Modul | Prioritas |
|----|------------------|--------------------|--------|------------|
| 1 | TS001 | Verifikasi perhitungan BMI berdasarkan input berat dan tinggi | Perhitungan | Tinggi |
| 2 | TS002 | Verifikasi validasi input kosong atau tidak valid | Input Validation | Tinggi |
| 3 | TS003 | Verifikasi tampilan kategori hasil BMI (Kurus, Normal, Gemuk, Obesitas) | Output Display | Menengah |
| 4 | TS004 | Verifikasi tampilan pesan kesalahan pada input negatif atau nol | Input Validation | Rendah |

---

### 🧩 Test Case
| No | Test Case ID | Skenario ID | Langkah Uji | Data Uji | Hasil yang Diharapkan | Hasil Aktual | Status |
|----|---------------|-------------|-------------|-----------|------------------------|---------------|---------|
| 1 | TC001 | TS001 | Masukkan berat 60, tinggi 165, tekan "Hitung BMI" | 60 / 165 | BMI = 22.0 | Sesuai | PASS |
| 2 | TC002 | TS002 | Masukkan berat kosong, tekan "Hitung BMI" | - / 170 | Pesan error “Masukkan berat badan” | Sesuai | PASS |
| 3 | TC003 | TS002 | Masukkan tinggi 0, tekan "Hitung BMI" | 70 / 0 | Pesan error “Tinggi tidak boleh nol” | Sesuai | PASS |
| 4 | TC004 | TS003 | Masukkan berat 80, tinggi 165, tekan "Hitung BMI" | 80 / 165 | BMI ≈ 29.4, kategori “Kelebihan berat badan” | Tidak tampil kategori | FAIL |
| 5 | TC005 | TS004 | Masukkan berat -50, tinggi 160, tekan "Hitung BMI" | -50 / 160 | Pesan error “Input tidak valid” | Sesuai | PASS |

---

## 5. Bug Report

### 5.1. Apa itu Bug Report?
**Bug Report** adalah laporan formal yang digunakan oleh tester untuk mendokumentasikan kesalahan atau cacat (*defect*) yang ditemukan selama pengujian.  
Tujuannya adalah membantu **developer memahami, mereproduksi, dan memperbaiki bug tersebut**.

---

### 5.2. Komponen Utama Bug Report
1. **Bug ID** – Nomor unik untuk identifikasi.  
2. **Judul Bug** – Ringkasan singkat masalah.  
3. **Deskripsi Bug** – Penjelasan lengkap kondisi error.  
4. **Langkah Reproduksi** – Langkah-langkah untuk menimbulkan bug.  
5. **Hasil Aktual** – Apa yang terjadi saat bug muncul.  
6. **Hasil yang Diharapkan** – Seharusnya apa yang terjadi.  
7. **Lingkungan Uji** – Informasi versi sistem, browser, atau OS.  
8. **Prioritas & Severity** – Tingkat penting dan dampak bug.  
9. **Status** – (New, Assigned, Fixed, Closed)

---

### 5.3. Contoh Format Bug Report (Kasus Aplikasi BMI)

| Field | Deskripsi |
|--------|------------|
| **Bug ID** | BUG-001 |
| **Judul Bug** | Kategori hasil BMI tidak muncul pada hasil perhitungan |
| **Modul** | Output Display |
| **Langkah Reproduksi** | 1. Buka aplikasi BMI <br> 2. Masukkan berat: 80, tinggi: 165 <br> 3. Tekan “Hitung BMI” |
| **Hasil Aktual** | Nilai BMI muncul (29.4), namun kategori kesehatan tidak tampil. |
| **Hasil yang Diharapkan** | Kategori “Kelebihan berat badan” seharusnya tampil bersama nilai BMI. |
| **Lingkungan Uji** | Android 14, BMI App v1.0, Pixel 6 |
| **Severity** | Major |
| **Prioritas** | High |
| **Status** | New |
| **Dilaporkan oleh** | QA Tester - Destin K. |
| **Tanggal Ditemukan** | 24 Oktober 2025 |

---

## 💡 Kesimpulan
- **Test Scenario** menggambarkan *apa* yang diuji.  
- **Test Case** menjelaskan *bagaimana* pengujian dilakukan.  
- **Bug Report** berfungsi sebagai sarana komunikasi antara tester dan developer.  
Ketiganya adalah bagian penting dari siklus pengujian perangkat lunak untuk memastikan sistem berfungsi sesuai kebutuhan pengguna.

---

> 📚 **Referensi:**
> - IEEE Std 829-2008: *Standard for Software and System Test Documentation*  
> - ISTQB Foundation Level Syllabus (2018)  
> - Pressman, R. S. (2015). *Software Engineering: A Practitioner’s Approach.*
