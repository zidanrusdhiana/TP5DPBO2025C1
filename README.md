# TP5DPBO2025C1
 
## Janji
Saya Mochamad Zidan Rusdhiana dengan NIM 2305464 mengerjakan Tugas Praktikum 5 dalam mata kuliah Desain dan Pemrograman Berorientasi Objek untuk keberkahanNya maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

## Desain
![tp5 drawio](https://github.com/user-attachments/assets/3a5b4ba4-4fa4-4037-8143-2df169f475d6)

## Penjelasan Kelas

### 1. Database
Kelas ini menangani koneksi dan interaksi dengan database MySQL:
- Membuat koneksi ke database `db_mahasiswa` pada server lokal
- Menyediakan metode untuk mengeksekusi query SELECT, INSERT, UPDATE, dan DELETE
- Menangani error database dengan exception handling

### 2. Mahasiswa
Kelas model yang merepresentasikan entitas mahasiswa:
- Menyimpan atribut mahasiswa: NIM, nama, jenis kelamin, dan kelas
- Menyediakan konstruktor untuk inisialisasi objek
- Menyediakan metode getter dan setter untuk mengakses dan memodifikasi atribut

### 3. Menu
Kelas utama yang mengimplementasikan interface pengguna:
- Menampilkan GUI dengan Swing
- Mengelola interaksi pengguna melalui event listener
- Menghubungkan interface dengan database melalui kelas Database

## Alur Program  
Program ini adalah aplikasi desktop berbasis Java yang menggunakan Swing untuk interface pengguna dan MySQL untuk penyimpanan data. Aplikasi ini dirancang untuk mengelola data mahasiswa, termasuk NIM, nama, jenis kelamin, dan kelas.

### 1. Tampilan Utama  
Saat program dijalankan, pengguna akan melihat interface yang terdiri dari:  
- **Formulir input data**, mencakup NIM, nama, jenis kelamin, dan kelas.  
- **Tabel data mahasiswa**, yang menampilkan daftar mahasiswa dari database.  
- **Tombol aksi**, yaitu:  
  - **"Add/Update"** – Menambah atau memperbarui data mahasiswa.  
  - **"Delete"** – Menghapus data mahasiswa yang dipilih. Terdapat Alert sebelum menghapus, untuk meminta konfirmasi ulang hapus data.
  - **"Cancel"** – Mengosongkan formulir input.  

### 2. Pengelolaan Data Mahasiswa  
- **Menambahkan Data**  
  Pengguna mengisi formulir, memilih jenis kelamin dari ComboBox, dan menentukan kelas menggunakan RadioButton (C1 atau C2). Program akan melakukan validasi data, termasuk pengecekan NIM unik, sebelum menyimpan ke database dengan query INSERT.
  
- **Mengubah Data**  
  Pengguna dapat mengklik salah satu baris di tabel untuk memuat data ke dalam formulir. Setelah perubahan dilakukan, program melakukan validasi dan memperbarui database dengan query UPDATE.
  
- **Menghapus Data**  
  Pilih data yang ingin dihapus dari tabel, lalu tekan **"Delete"**. Setelah konfirmasi, data akan dihapus dari database dengan query DELETE.
  
- **Membatalkan Input**  
  Klik **"Cancel"** untuk mengosongkan formulir tanpa menyimpan perubahan.  

### 3. Informasi Tabel  
- Tabel menampilkan semua data mahasiswa yang diambil dari database melalui query SELECT.
- Data ditampilkan dalam format tabel dengan kolom: NO, NIM, NAMA, JENIS KELAMIN, dan KELAS.
- Klik salah satu baris di tabel untuk memuat data ke dalam formulir agar bisa diperbarui atau dihapus.  

### 4. Validasi Data
- Program memastikan semua field terisi sebelum melakukan operasi database.
- Validasi NIM unik untuk mencegah duplikasi.
- Konfirmasi sebelum menghapus data untuk mencegah penghapusan yang tidak diinginkan.
- Penanganan error database dengan try-catch untuk menjaga stabilitas aplikasi.

### 5. Struktur Penyimpanan Data  
- Data mahasiswa disimpan secara permanen dalam database MySQL `db_mahasiswa` dalam tabel `mahasiswa`.
- Operasi database (SELECT, INSERT, UPDATE, DELETE) ditangani oleh kelas Database.
- Tabel pada interface diperbarui secara dinamis berdasarkan query ke database setelah setiap operasi.

### 6. Alur Koneksi Database
- Program membuat koneksi ke database saat aplikasi dimulai.
- Query database dieksekusi sesuai dengan interaksi pengguna.
- Data hasil query diproses dan ditampilkan dalam interface pengguna.
- Koneksi database dikelola untuk mencegah kebocoran sumber daya.

## Dokumentasi
### Dialog/prompt error jika masih ada input yang kosong saat insert/update.
![1 2](https://github.com/user-attachments/assets/52ea8ee2-0467-4fde-b271-e7399ee74d4c)
![1](https://github.com/user-attachments/assets/93ec1a4b-8863-495b-90db-6061edafe85c)

### Dialog/prompt error jika sudah ada NIM yang sama saat insert.
![2](https://github.com/user-attachments/assets/c609b18d-e028-4739-968a-bc736c5edb35)

### Insert data dan perubahannya di database.
![3](https://github.com/user-attachments/assets/3bf7ce85-8064-4179-8a73-63caf653504c)
![4](https://github.com/user-attachments/assets/0f259fef-16c2-4370-87fa-76a4b5fd12ea)

### Update data dan perubahannya di database.
![5](https://github.com/user-attachments/assets/dc37ea1b-045f-46df-923f-b8ded7b508ed)
![6](https://github.com/user-attachments/assets/1978a33b-1b13-4b63-b0fc-58f46ea8ffc6)

### Delete data dan perubahannya di database.
![7](https://github.com/user-attachments/assets/df1ae5cf-2f66-4a4a-b711-7dae66683ec1)
![8](https://github.com/user-attachments/assets/376f8bdd-56e0-40da-a791-83f9f17be8e5)
