# 9Score

<div align="center">

![9Score Logo](assets/images/MentariLogo-Dark.png)

### Asisten Cerdas & Otomatisasi Alur Pembelajaran LMS Mentari UNPAM
**Created by 009's Core.**

[![Version](https://img.shields.io/badge/version-v1.3.0%20Beta-38bdf8.svg?style=flat-square)](manifest.json)
[![Platform](https://img.shields.io/badge/platform-Chrome%20%7C%20Edge%20%7C%20Brave-30d158.svg?style=flat-square)](manifest.json)
[![Manifest](https://img.shields.io/badge/manifest-V3-f59e0b.svg?style=flat-square)](manifest.json)
[![License](https://img.shields.io/badge/license-MIT-64748b.svg?style=flat-square)](LICENSE)

</div>

---

## 📌 Tentang 9Score

**9Score** adalah ekstensi browser modern berbasis AI yang dirancang khusus untuk mempermudah, mempercepat, dan mengotomatiskan seluruh alur aktivitas belajar mahasiswa di portal **LMS Mentari Universitas Pamulang** (`mentari.unpam.ac.id`).

Mulai dari pengerjaan kuis (Pre-Test & Post-Test) secara terukur, simulasi membaca modul materi agar presensi tercatat di log LMS, perumusan argumen diskusi cerdas berbasis Gemini AI, hingga pengisian survei/kuesioner pembelajaran secara otomatis dalam satu klik.

---

## ✨ Fitur Utama

### 1. 🚀 9Score Runner (Alur Otomatisasi Pertemuan)
* **Alur Presensi Lengkap (End-to-End)**:
  $$\text{Pre-Test} \longrightarrow \text{Materi PPT/PDF} \longrightarrow \text{Forum Diskusi (2 Balasan)} \longrightarrow \text{Post-Test} \longrightarrow \text{Kuesioner}$$
* **Multi-Meeting & Batch Runner**: Jalankan otomatisasi untuk 1 pertemuan, beberapa pertemuan pilihan, atau seluruh pertemuan mata kuliah sekaligus.
* **Multi-Task Dashboard**: Mendukung antrean tugas lintas mata kuliah (*cross-course queue*) secara berurutan tanpa perlu mengklik manual satu per satu.
* **Simulasi Membaca Materi**: Membuka dokumen dan mensimulasikan waktu membaca (countdown natural) agar akses materi resmi tercatat di log sistem LMS Mentari.
* **Smart Skip Protection**: Sistem cerdas yang mendeteksi instruksi tugas manual/fisik pada forum (seperti tugas video YouTube, makalah PDF, tugas kelompok, atau resume tulis tangan). Jika terdeteksi, topik akan dilewati secara otomatis dan aman agar nilai mahasiswa tidak terancam.
* **Live Progress Log (Monokrom Silver)**: Panel log berdesain *Apple Dark Glassmorphism* dengan indikator hijau berdenyut (*pulse glow*) dan hierarki teks silver bertingkat yang rapi saat digulir.

### 2. 🧠 Smart Quiz Engine (Pre-Test, Post-Test & Ujian)
* **3 Mode Pengerjaan Kuis**:
  * **Humanis (Direkomendasikan)**: Tingkat akurasi terukur (85%–95%) dengan jeda acak manusiawi (600–1200ms) untuk menyerupai pola pengerjaan mahasiswa asli.
  * **Ambis**: Akurasi 100% dengan jeda natural (150–300ms).
  * **Turbo**: Menjawab seluruh soal pilihan ganda secara instan.
* **Auto-Submit & Validasi**: Otomatis menyimpan setiap jawaban ke server LMS dan mengakhiri kuis saat seluruh soal selesai dijawab.

### 3. 💬 Asisten Diskusi Forum AI
* Menganalisis konteks topik diskusi dosen secara mendalam.
* Merumuskan **2 balasan tanggapan argumentatif** yang berbobot, akademis, dan relevan dengan materi.
* Integrasi langsung dengan editor CKEditor dan REST API Mentari UNPAM.

### 4. 📝 Otomatisasi Kuesioner Pembelajaran
* Deteksi kuesioner pintar pasca Post-Test (hanya berjalan jika pertemuan tersebut memang memiliki silabus kuesioner).
* Mengisi seluruh instrumen survei pembelajaran secara otomatis dan melakukan submit tuntas.

### 5. ⚡ Dua Metode Provider AI (Fleksibel)
* **Route Bersama (API Key Resmi)**: *Plug & Play* langsung aktif tanpa perlu registrasi atau membuat API Key sendiri. Menggunakan engine server relay teroptimasi khusus format Mentari UNPAM.
* **Gemini API Key Pribadi**: Kuota bebas antrean langsung dari Google AI Studio dengan kebebasan memilih beragam varian model Google Gemini (`gemini-flash-lite-latest`, `gemini-2.5-flash`, `gemini-2.5-pro`, `gemini-3.0-flash`, dll.).

---

## 📥 Panduan Instalasi (Untuk Pengguna Baru)

Ekstensi ini dapat dipasang dengan mudah di semua peramban berbasis Chromium (Google Chrome, Microsoft Edge, Brave, Opera, Vivaldi):

1. **Unduh / Siapkan Folder Ekstensi**:
   * Pastikan Anda telah memiliki folder `9Score` hasil ekstraksi file ZIP yang dibagikan.
2. **Buka Menu Ekstensi Browser**:
   * Ketik alamat berikut di address bar browser Anda:
     ```text
     chrome://extensions
     ```
     *(Jika menggunakan Edge: `edge://extensions`)*
3. **Aktifkan Mode Pengembang**:
   * Di pojok kanan atas layar, nyalakan tombol **Developer mode** (Mode Pengembang).
4. **Muat Ekstensi**:
   * Klik tombol **Load unpacked** (Muat yang belum dibongkar) di pojok kiri atas.
   * Pilih folder ekstensi `9Score`.
5. **Selesai!**
   * Ekstensi **9Score** berhasil terpasang dan siap digunakan. Sematkan (*pin*) ikon 9Score di toolbar browser Anda untuk kemudahan akses.

### 📦 Build & Obfuskasi Kode (Untuk Membagikan ke Teman)

Jika Anda adalah developer yang ingin mengemas ekstensi ini untuk dibagikan ke teman **tanpa menyertakan source code asli**:

```bash
npm run build
```

Perintah di atas akan secara otomatis:
1. Meng-obfuscate seluruh file JavaScript ke dalam folder `dist/` sehingga kode tidak dapat dibaca, diubah, atau di-reverse engineer.
2. Menyalin seluruh aset gambar, manifest, icon, dan stylesheet.
3. Menghasilkan arsip siap bagi `9Score-v1.3.0.zip`. Teman Anda cukup mengekstrak zip tersebut dan memuatnya via **Load unpacked** di browser mereka.

---

## 🎯 Cara Penggunaan

1. **Masuk ke LMS Mentari**:
   * Buka portal [mentari.unpam.ac.id](https://mentari.unpam.ac.id) dan login ke akun mahasiswa Anda.
2. **Widget Mengambang Otomatis**:
   * Masuk ke halaman mata kuliah Anda. Panel mengambang **9Score** akan otomatis muncul di sudut kanan bawah.
3. **Pilih Pertemuan & Jalankan**:
   * Klik checkbox pertemuan yang ingin Anda selesaikan (atau klik tombol **Belum Selesai** untuk memilih otomatis).
   * Klik tombol **Jalankan Otomatisasi**.
   * Duduk manis dan pantau perkembangan tugas Anda secara langsung melalui panel **LOG PROGRESS**!

---

## ⚙️ Ringkasan Pengaturan Ekstensi

Buka Popup 9Score di toolbar browser untuk mengakses setelan cepat:

| Pengaturan | Pilihan | Penjelasan |
| :--- | :--- | :--- |
| **Metode Provider AI** | Route Bersama / API Key Pribadi | Sumber engine AI pemroses jawaban kuis & diskusi. |
| **Model Gemini AI** | Mentari Route / Flash-Lite / Flash / Pro | Model AI yang digunakan untuk inferensi jawaban. |
| **Mode Kuis** | Humanis / Ambis / Turbo | Gaya pengerjaan kuis (akurasi & tempo waktu jeda). |
| **Error Rate (Humanis)** | 5% – 20% | Persentase simulasi salah acak agar nilai terlihat natural. |
| **Fitur Aktif LMS** | Kuis / Kuesioner / Forum | Sakelar untuk mengaktifkan atau menonaktifkan fitur tertentu. |

---

## 🛡️ Keamanan & Privasi

* **Penyimpanan Lokal**: Semua konfigurasi, pengaturan, dan riwayat sesi disimpan secara aman di penyimpanan lokal peramban Anda (`chrome.storage.local` & `sessionStorage`).
* **Tanpa Data Pribadi**: Ekstensi tidak pernah mengumpulkan data kredensial login (NIM/password) akun Mentari Anda.
* **Perlindungan Nilai Mahasiswa**: Deteksi tugas manual memastikan mahasiswa tidak mengalami kerugian nilai akibat jawaban bot pada tugas yang mewajibkan karya fisik/video.

---

## 🛠️ Arsitektur Teknologi

* **Manifest**: Google Chrome Extension Manifest V3
* **Bahasa**: Vanilla JavaScript (ES6+), HTML5, CSS3 Glassmorphism
* **DOM Sandboxing**: Web Component & Shadow DOM Architecture
* **Main World Bridge**: Isolated Page-Script Bridge untuk interaksi CKEditor & state SPA
* **AI Provider**: Google Generative Language API (Gemini Family) & OpenAI-compatible Route Relay

---

## 👥 Tim & Kredit

Ekstensi ini dikembangkan dan didedikasikan untuk kemudahan belajar mahasiswa:

* **[AnggaStwn](https://github.com/Awkwardlp)** — **Lead Feature Engineer & UI/UX Designer**  
  *Perancang & pengembang solusi fitur end-to-end, alur otomatisasi, integrasi AI, serta desain visual antarmuka pengguna.*
* **[RhaDar](https://github.com/RhaDar12)** — **Foundational System Architect**  
  *Inisiator dan perancang fondasi arsitektur basis kode awal (core codebase).*
* **Core Organization**: **`009's Core.`**
* **Inisiasi Proyek**: Asisten Belajar Mandiri LMS Mentari Universitas Pamulang (UNPAM)
* **Special Thanks**: Seluruh rekan dan kontributor pengembang komunitas mahasiswa UNPAM.

```text
   ___  ____                     
  / _ \/ ___|  ___ ___  _ __ ___ 
 | (_) \___ \ / __/ _ \| '__/ _ \
  \__, |___) | (_| (_) | | |  __/
    /_/|____/ \___\___/|_|  \___|
               Created with passion by 009's Core.
```

---

## ⚖️ Catatan Penggunaan (Disclaimer)

* Ekstensi ini dikembangkan semata-mata sebagai sarana pembantu produktivitas dan media pembelajaran mandiri.
* Pengguna disarankan tetap meninjau materi dan modul perkuliahan yang diberikan oleh dosen pengampu.
* Pengembang tidak bertanggung jawab atas penyalahgunaan ekstensi yang melanggar tata tertib akademik institusi.

---

<div align="center">
  <b>© 2026 009's Core. All rights reserved.</b>
</div>
