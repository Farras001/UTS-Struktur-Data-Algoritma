<div align="center">

# 📅 ABSENCEPAT
### Sistem Absensi Mahasiswa Berbasis CLI dengan Fitur Riwayat Undo

<br>

![C](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Status](https://img.shields.io/badge/Status-Project_Praktikum-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-Academic-orange?style=for-the-badge)
![Universitas](https://img.shields.io/badge/Universitas-Syiah%20Kuala-blueviolet?style=for-the-badge)

<br>

> **ABSENCEPAT** adalah program berbasis CLI yang mendigitalisasi proses pencatatan kehadiran mahasiswa menggunakan bahasa pemrograman C. Program ini dirancang untuk menyelesaikan masalah pencatatan absensi manual yang kaku, lambat direkapitulasi, dan rentan terhadap *human error* (seperti salah input status kehadiran). Pendekatan sistem ini cukup menarik secara teknis karena memadukan `Singly Linked List` untuk penyimpanan riwayat secara dinamis, `Stack` untuk mengeksekusi fitur *Undo* secara instan, serta meminjam struktur `Array` temporer untuk melakukan *sorting* tanpa merusak urutan asli pointer pada memori.
<br>

</div>

---

## ✨ Fitur Utama

| # | Fitur | Deskripsi |
|:---:|---|---|
| 1 | ➕ **Tambah Data Dinamis** | Mencatat kehadiran mahasiswa tanpa batasan kapasitas kaku berbasis Linked List |
| 2 | ⏪ **Undo Pembatalan Instan** | Mencegah kesalahan input (*human error*) dengan membatalkan aksi terakhir |
| 3 | 📅 **Smart Sorting Tanggal** | Urutkan riwayat absensi dari tanggal terlama ke terbaru |
| 4 | 🔤 **Smart Sorting Nama** | Urutkan rekapitulasi daftar mahasiswa secara alfabetis (A-Z) |
| 5 | 💾 **Persistensi Data** | Simpan dan baca riwayat secara otomatis ke *file* `absensi.txt` |

---

## 🛠 Arsitektur Sistem

### 🌳 Struktur Data

| Struktur Data | Digunakan Untuk |
|---|---|
| **Singly Linked List** | Menyimpan riwayat absensi mahasiswa secara dinamis tanpa batasan kapasitas memori kaku. |
| **Stack** | Mengelola riwayat *input* terakhir untuk fitur *Undo* (LIFO) pembatalan data. |
| **Array** | Wadah sementara (*buffer*) untuk menyalin dan mengeksekusi algoritma *sorting*. |

### ⚙️ Algoritma

| Algoritma | Kompleksitas | Digunakan Untuk |
|---|---|---|
| **Insertion Sort** | O(n^2) | Mengurutkan data absensi secara *real-time* berdasarkan tanggal/waktu masuk. |
| **Bubble Sort** | O(n^2) | Mengurutkan laporan akhir absensi secara alfabetis (A-Z) berdasarkan nama. |
| **Traversal** | O(n) | Menelusuri *linked list* untuk menampilkan tabel data dan proses simpan/baca *file* teks. |

---

## 💻 Cara Menjalankan

### Prasyarat

Pastikan *compiler* GCC telah terinstal: Windows (MinGW-w64), Linux (`build-essential`), atau macOS (`xcode-select --install`).

### Langkah Instalasi & Kompilasi

```bash
# 1. Clone repositori (opsional jika menggunakan git)
git clone [https://github.com/username/absencepat.git](https://github.com/username/absencepat.git)
cd absencepat

# 2. Kompilasi program
gcc a.c -o absensi

# 3. Jalankan program
./absensi      # Untuk Linux / macOS
.\absensi.exe  # Untuk Windows
