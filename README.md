# Sistem Deteksi dan Pengenalan Nomor Bib Pelari Menggunakan YOLOv8 dan EasyOCR

Sistem deteksi dan pengenalan nomor bib (bib number) pelari secara otomatis dari data video menggunakan model deteksi objek YOLOv8 dan pengenalan teks EasyOCR, dikembangkan untuk membantu proses pencatatan hasil lomba lari secara digital.

**Program Studi Sarjana Terapan Teknik Rekayasa Perangkat Lunak**
**Politeknik Negeri Banyuwangi**

Dikembangkan bekerja sama dengan **CV Alzen Metro Data, Banyuwangi**

---

![Framework](https://img.shields.io/badge/FRAMEWORK-YOLOv8-purple) ![Language](https://img.shields.io/badge/LANGUAGE-Python-blue) ![OCR](https://img.shields.io/badge/OCR-EasyOCR-orange) ![Deployment](https://img.shields.io/badge/DEPLOYMENT-Docker-informational)

---

## 📖 Tentang Proyek

Proyek ini merupakan sistem **computer vision** untuk mendeteksi dan mengenali nomor bib pelari secara otomatis dari rekaman video event lari.

Sistem membantu proses **deteksi posisi bib**, **pengenalan angka pada bib**, dan **pencatatan hasil** secara otomatis tanpa perlu pencatatan manual satu per satu.

Sistem menggunakan **YOLOv8** untuk mendeteksi lokasi bib pada frame video, dan **EasyOCR** untuk membaca angka nomor bib dari hasil deteksi tersebut.

## ✨ Fitur Utama

- 🎯 Deteksi otomatis lokasi nomor bib pada video menggunakan YOLOv8
- 🔤 Pengenalan angka nomor bib menggunakan EasyOCR
- 🖼️ Preprocessing citra (rotasi, sharpening, koreksi kualitas gambar) untuk meningkatkan akurasi OCR
- 📊 Evaluasi performa model dengan metrik mAP, Precision, Recall, F1-Score, CER (Character Error Rate), dan FPS
- 🎥 Pemrosesan video secara langsung untuk mendeteksi bib pada momen finish
- 💾 Pencatatan hasil deteksi ke dalam basis data/spreadsheet
- 🌐 Antarmuka berbasis web untuk unggah video dan melihat hasil deteksi

## 🛠️ Teknologi yang Digunakan

| Kategori | Teknologi |
|---|---|
| Deteksi Objek | YOLOv8 (Ultralytics) |
| Pengenalan Teks (OCR) | EasyOCR |
| Bahasa Pemrograman | Python |
| Manajemen Dataset | Roboflow |
| Web Server / API | FastAPI |
| Antarmuka Pengguna | Streamlit |
| Deployment | Docker |

## 📂 Struktur Proyek

```
├── models/           # Model YOLOv8 hasil training
├── modules/          # Modul utama (deteksi, OCR, preprocessing, database)
├── scripts/          # Script evaluasi, analisis, dan pengujian
├── runs/detect/      # Hasil output deteksi
├── .streamlit/       # Konfigurasi antarmuka Streamlit
├── Dockerfile         # Konfigurasi containerization
├── requirements.txt   # Daftar dependensi Python
└── upload_server.py   # Server untuk unggah dan pemrosesan video
```

## 🚀 Cara Menjalankan

1. Clone repository ini
   ```bash
   git clone https://github.com/TRPL-JBI/TA2026-362258302147-AdamBagusSetiyawan.git
   cd TA2026-362258302147-AdamBagusSetiyawan
   ```

2. Buat virtual environment dan install dependensi
   ```bash
   python -m venv venv
   venv\Scripts\activate      # Windows
   pip install -r requirements.txt
   ```

3. Jalankan aplikasi
   ```bash
   streamlit run scripts/app.py
   ```

## 📈 Evaluasi Model

Model dievaluasi menggunakan data uji (test set) terpisah dengan metrik berikut:
- **mAP (mean Average Precision)** — akurasi deteksi objek
- **Precision & Recall** — ketepatan dan kelengkapan deteksi
- **CER (Character Error Rate)** — akurasi hasil pengenalan teks OCR
- **FPS (Frame per Second)** — kecepatan pemrosesan video

## 👤 Penulis

**Adam Bagus Setiyawan**
NIM: 362258302147
D4 Teknik Rekayasa Perangkat Lunak — Politeknik Negeri Banyuwangi

---

*Tugas Akhir ini disusun sebagai syarat kelulusan Program Studi Sarjana Terapan Teknik Rekayasa Perangkat Lunak, Politeknik Negeri Banyuwangi.*
