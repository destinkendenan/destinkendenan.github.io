---
title: "Materi 3: Testing Plan"
date: 2025-10-24 10:00:00 +0800
categories: [Software Testing, QA]
tags: [Testing Plan, IEEE 829, QA, SDLC]
image:
  path: /assets/image/testing-plan.jpg
  alt: "Testing Plan Document"
---

# 🧩 Materi 3: Testing Plan

## 1. Review Testing Plan
Testing Plan (Rencana Pengujian) adalah dokumen yang berfungsi sebagai **panduan utama** dalam melaksanakan kegiatan pengujian perangkat lunak. Dokumen ini menjelaskan **strategi, ruang lingkup, pendekatan, sumber daya, jadwal, serta kriteria keberhasilan** dari proses testing.  
Testing plan sangat penting agar pengujian berjalan sistematis, terukur, dan sesuai tujuan proyek.

---

## 2. Apa itu Testing Plan?
**Testing Plan** adalah dokumen formal yang disusun oleh tim QA atau tester untuk menjelaskan bagaimana proses pengujian perangkat lunak akan dilakukan.  
Testing plan mencakup:  
- Apa yang akan diuji  
- Tujuan pengujian  
- Siapa yang akan melakukan pengujian  
- Sumber daya yang dibutuhkan  
- Kapan pengujian dilakukan  
- Kriteria keberhasilan dan penghentian pengujian  

> **Referensi:** IEEE Standard for Software Test Documentation (IEEE 829-2008)

---

## 3. Tujuan Testing Plan
Tujuan utama dari penyusunan Testing Plan meliputi:
- 📋 **Memberikan panduan terstruktur** bagi tim QA dan developer.  
- 🧠 **Menjamin bahwa semua fungsi sistem diuji secara menyeluruh.**  
- 💬 **Meningkatkan komunikasi** antar anggota tim proyek.  
- 💰 **Mengoptimalkan sumber daya dan waktu pengujian.**  
- 🛠️ **Mengurangi risiko bug besar** muncul setelah implementasi.  

---

## 4. Komponen Testing Plan (berdasarkan IEEE 829)
Menurut standar **IEEE 829**, komponen utama dari sebuah *Software Test Plan (STP)* meliputi bagian-bagian berikut:

### 4.1. Test Plan Identifier
Nomor atau kode unik yang mengidentifikasi dokumen rencana pengujian ini, misalnya:  
`STP-001/2025`

---

### 4.2. Introduction
Menjelaskan **tujuan dan ruang lingkup pengujian**, sistem yang akan diuji, serta konteks proyek.  
Contoh:
> Pengujian dilakukan terhadap modul login, register, dan dashboard pada sistem manajemen tugas berbasis web.

---

### 4.3. Test Items
Daftar item atau modul yang akan diuji.  
Contoh:
- Modul Login  
- Modul Registrasi  
- Modul Dashboard  

---

### 4.4. Features to be Tested
Menjelaskan fitur-fitur yang termasuk dalam ruang lingkup pengujian.  
Contoh:
- Validasi input login (username & password)  
- Autentikasi token JWT  
- Respons halaman dashboard  

---

### 4.5. Features Not to be Tested
Fitur yang **tidak termasuk** dalam pengujian.  
Contoh:
- Fitur chat internal (karena masih dalam pengembangan)  

---

### 4.6. Approach (Pendekatan Pengujian)
Menjelaskan strategi pengujian yang akan digunakan, misalnya:
- **Black Box Testing** untuk fungsionalitas.  
- **White Box Testing** untuk logika internal modul.  
- **Manual Testing** untuk antarmuka pengguna (UI).  
- **Automated Testing** untuk regression test.  

---

### 4.7. Item Pass/Fail Criteria
Menetapkan **kriteria kelulusan** setiap test case.  
Contoh:
> Test case dinyatakan *PASS* jika hasil aktual sesuai dengan hasil yang diharapkan tanpa error.

---

### 4.8. Suspension Criteria and Resumption Requirements
Menjelaskan kondisi kapan pengujian dihentikan sementara dan bagaimana dilanjutkan.  
Contoh:
> Pengujian dihentikan jika 40% test case gagal karena bug kritikal. Pengujian dilanjutkan setelah bug diperbaiki.

---

### 4.9. Test Deliverables
Dokumen atau artefak yang dihasilkan selama dan setelah proses testing, seperti:
- Test Case Document  
- Test Script  
- Test Report  
- Bug Report  

---

### 4.10. Testing Tasks
Daftar tugas atau aktivitas yang perlu dilakukan selama pengujian.  
Contoh:
1. Menulis test case  
2. Melakukan eksekusi testing  
3. Mencatat bug  
4. Menyusun laporan hasil  

---

### 4.11. Environmental Needs
Menjelaskan **kebutuhan lingkungan pengujian**, seperti:
- Perangkat keras (hardware)
- Perangkat lunak (software)
- Jaringan
- Database  

Contoh:
> - OS: Windows 11  
> - Browser: Chrome v110+  
> - Database: MySQL 8.0  
> - Server: Localhost  

---

### 4.12. Responsibilities
Menentukan siapa yang bertanggung jawab terhadap tiap aktivitas.  
Contoh:
| Peran | Tanggung Jawab |
|-------|-----------------|
| QA Lead | Menyusun dan memvalidasi test plan |
| Tester | Menulis dan menjalankan test case |
| Developer | Memperbaiki bug yang ditemukan |

---

### 4.13. Schedule
Menentukan **jadwal pengujian** dalam bentuk timeline atau tabel.

| Aktivitas | Durasi | Tanggal Mulai | Tanggal Selesai |
|------------|--------|----------------|----------------|
| Menulis test plan | 2 hari | 25 Okt 2025 | 26 Okt 2025 |
| Eksekusi test case | 5 hari | 27 Okt 2025 | 31 Okt 2025 |
| Pelaporan hasil | 2 hari | 1 Nov 2025 | 2 Nov 2025 |

---

### 4.14. Risks and Contingencies
Menjelaskan risiko yang mungkin muncul selama testing dan bagaimana mengatasinya.

| Risiko | Dampak | Mitigasi |
|--------|---------|-----------|
| Server down | Menunda eksekusi testing | Gunakan server backup |
| Tester sakit | Mengurangi waktu testing | Siapkan tester cadangan |

---

### 4.15. Approvals
Bagian tanda tangan persetujuan dari pihak terkait (Project Manager, QA Lead, Developer Lead).

---

## 5. Contoh Template Testing Plan IEEE 829 (disederhanakan)

| No | Komponen | Deskripsi |
|----|-----------|-----------|
| 1 | Test Plan Identifier | STP-001/2025 |
| 2 | Introduction | Rencana pengujian sistem manajemen tugas |
| 3 | Test Items | Modul Login, Register, Dashboard |
| 4 | Features to be Tested | Validasi input, Autentikasi |
| 5 | Features not to be Tested | Modul Chat |
| 6 | Approach | Black box, White box |
| 7 | Item Pass/Fail Criteria | Hasil aktual sesuai hasil ekspektasi |
| 8 | Suspension Criteria | >40% gagal karena bug kritikal |
| 9 | Test Deliverables | Test Case, Bug Report, Test Summary |
| 10 | Testing Tasks | Menulis, Menjalankan, Melaporkan |
| 11 | Environmental Needs | Windows 11, MySQL 8, Chrome |
| 12 | Responsibilities | QA Lead, Tester, Developer |
| 13 | Schedule | 25 Okt–2 Nov 2025 |
| 14 | Risks | Server down, Tester unavailable |
| 15 | Approvals | Ditandatangani oleh QA Lead dan PM |

---

## 💡 Kesimpulan
Testing Plan adalah **fondasi dari proses pengujian perangkat lunak**.  
Dengan mengikuti standar seperti **IEEE 829**, proses testing menjadi lebih terstruktur, terdokumentasi dengan baik, dan mudah dievaluasi untuk perbaikan di masa mendatang.

---

> 📚 **Referensi:**
> - IEEE Std 829-2008: Standard for Software and System Test Documentation  
> - ISTQB Foundation Level Syllabus (2018)  
> - Pressman, R. S. (2015). *Software Engineering: A Practitioner's Approach.*
