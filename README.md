# ABSENCEPAT: Sistem Absensi Mahasiswa Berbasis CLI

[cite_start]ABSENCEPAT adalah sebuah purwarupa sistem pencatatan kehadiran mahasiswa berbasis *Command Line Interface* (CLI) yang ditulis dalam bahasa C[cite: 37, 39]. [cite_start]Sistem ini dirancang untuk mendigitalisasi proses absensi secara efisien, aman, dan meminimalisir risiko kelalaian manusia (*human error*)[cite: 21, 82]. 

[cite_start]Proyek ini dibangun sebagai bagian dari Praktikum Struktur Data dan Algoritma, Program Studi Informatika, Fakultas Matematika dan Ilmu Pengetahuan Alam, Universitas Syiah Kuala[cite: 10, 11, 12, 13].

## ✨ Fitur Utama

Sistem ini menawarkan serangkaian fitur untuk mempermudah administrasi kelas:
* [cite_start]**Tambah Data Absensi:** Mencatat kehadiran mahasiswa (NPM, Nama, Jurusan, Semester, Tanggal) secara dinamis tanpa batasan kapasitas kaku[cite: 26, 98].
* [cite_start]**Tampilkan Semua Data:** Menyajikan riwayat kehadiran dalam format tabel yang terstruktur dan rapi[cite: 98].
* [cite_start]**Fitur Undo (Pembatalan Instan):** Mencegah kesalahan input dengan membatalkan data absen yang paling terakhir dimasukkan hanya dalam hitungan detik[cite: 27, 82, 98].
* [cite_start]**Pengurutan Berdasarkan Tanggal:** Mengurutkan riwayat absensi dari tanggal terlama ke terbaru[cite: 98].
* [cite_start]**Pengurutan Berdasarkan Nama:** Mengurutkan daftar mahasiswa secara alfabetis (A-Z) untuk mempermudah rekapitulasi[cite: 70, 98].
* [cite_start]**Persistensi Data (File I/O):** Seluruh data otomatis disimpan dan dibaca kembali dari file `absensi.txt`, sehingga riwayat tidak hilang setelah program ditutup[cite: 42, 98].

## 🛠️ Arsitektur Struktur Data & Algoritma

Sistem ini dioptimalkan dengan mengintegrasikan beberapa struktur data dan algoritma pokok:

* [cite_start]**Singly Linked List:** Berfungsi sebagai penyimpanan utama yang dinamis untuk riwayat absensi harian yang terus bertambah[cite: 26, 55].
* [cite_start]**Stack:** Menjadi mesin penggerak fitur *Undo* dengan prinsip LIFO (*Last In, First Out*)[cite: 57, 59].
* [cite_start]**Array (Temporary Buffer):** Digunakan sebagai wadah sementara untuk memproses algoritma pengurutan data agar lebih efisien dengan akses indeks `O(1)`, tanpa merombak *pointer* asli pada Linked List[cite: 28, 50, 258].
* [cite_start]**Insertion Sort:** Diterapkan untuk menyisipkan dan mengurutkan data berdasarkan parameter waktu/tanggal[cite: 67, 74].
* [cite_start]**Bubble Sort:** Diterapkan untuk mengurutkan laporan rekapitulasi berdasarkan nama mahasiswa secara alfabetis[cite: 70, 74].
* [cite_start]**Traversal:** Menelusuri seluruh simpul (*node*) untuk menampilkan tabel absen dan menyimpannya ke *file* teks[cite: 73].

## 🚀 Cara Instalasi & Menjalankan Program

Pastikan kamu memiliki *compiler* C seperti `gcc` terinstal di komputermu.

1. **Clone repositori ini:**
   ```bash
   git clone [https://github.com/username/absencepat.git](https://github.com/username/absencepat.git)
   cd absencepat
