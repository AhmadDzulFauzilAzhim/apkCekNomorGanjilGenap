# Aplikasi Cek Nomor Ganjil Genap
 
Aplikasi berbasis Java Swing ini dirancang untuk memeriksa apakah sebuah angka merupakan bilangan **ganjil** atau **genap**, sekaligus mengecek apakah angka tersebut merupakan **bilangan prima**. Program ini menggunakan antarmuka grafis (GUI) sederhana untuk memberikan pengalaman pengguna yang mudah dan intuitif.

---

## Fitur Utama
1. **Cek Ganjil atau Genap**
   - Aplikasi dapat menentukan apakah angka yang dimasukkan adalah ganjil atau genap.

2. **Cek Bilangan Prima**
   - Selain ganjil/genap, aplikasi juga memeriksa apakah angka tersebut merupakan bilangan prima.

3. **Validasi Input**
   - Hanya angka yang dapat dimasukkan ke dalam kolom input. Karakter selain angka tidak akan diterima.

4. **Antarmuka Sederhana**
   - Menggunakan Java Swing untuk menyediakan GUI sederhana dengan tombol "Cek Nomor" dan "Bersihkan".

---

## Cara Menggunakan
1. **Input Angka**
   - Masukkan angka yang ingin diperiksa pada kolom teks yang tersedia.

2. **Cek Nomor**
   - Klik tombol **Cek Nomor** untuk melihat hasil apakah angka tersebut ganjil/genap dan apakah bilangan tersebut merupakan bilangan prima.

3. **Bersihkan**
   - Klik tombol **Bersihkan** untuk mengosongkan kolom input dan hasil.

---

## Penjelasan Kode

### 1. Struktur Program
- **`initComponents`**
  - Menginisialisasi komponen GUI seperti panel, tombol, teks, dan label.
- **`jButton1ActionPerformed`**
  - Fungsi yang dijalankan ketika tombol "Cek Nomor" diklik. Fungsi ini:
    - Membaca input angka dari kolom teks.
    - Mengecek apakah angka tersebut ganjil/genap.
    - Mengecek apakah angka tersebut bilangan prima.
    - Menampilkan hasil melalui `JOptionPane` dan label hasil.
- **`jButton2ActionPerformed`**
  - Fungsi untuk membersihkan kolom input dan label hasil.

### 2. Validasi Input
- Fungsi **`jTextField1KeyTyped`** memastikan hanya angka yang dapat dimasukkan ke dalam kolom input. Jika pengguna mencoba mengetik karakter selain angka, karakter tersebut akan diabaikan.

### 3. Logika Cek Ganjil/Genap dan Prima
- **Cek Ganjil/Genap**:
  ```java
  String hasil = (number % 2 == 0) ? "Genap" : "Ganjil";
  ```
- **Cek Bilangan Prima**:
  ```java
  private boolean isPrime(int number) {
      if (number <= 1) return false;
      for (int i = 2; i <= Math.sqrt(number); i++) {
          if (number % i == 0) return false;
      }
      return true;
  }
  ```

### 4. Tampilan Hasil
- Hasil pengecekan ditampilkan dengan dua cara:
  - Dialog menggunakan `JOptionPane`.
  - Label di bawah kolom input untuk menampilkan hasil secara langsung di GUI.

---

## Prasyarat
- **Java Development Kit (JDK)**
  - Minimal versi 8.

---

## Cara Menjalankan
1. Buka proyek di IDE seperti **NetBeans** atau **IntelliJ IDEA**.
2. Jalankan file utama `apkCekNomorGanjilGenap`.
3. Aplikasi akan terbuka dalam bentuk GUI.

---

## Struktur File
- **`apkCekNomorGanjilGenap.java`**
  - File utama yang berisi implementasi GUI dan logika aplikasi.

---

## Contoh Penggunaan
1. Masukkan angka **7** di kolom input.
2. Klik tombol **Cek Nomor**.
3. Hasil akan menampilkan:
   - "Angka 7 adalah Ganjil dan Prima".
4. Klik tombol **Bersihkan** untuk mengosongkan kolom input.

---

## Catatan
- Aplikasi ini hanya memproses angka positif atau nol.
- Jika input bukan angka atau kosong, aplikasi akan menampilkan pesan error.

---

## Pembuat Aplikasi
Ahmad Dzul Fauzil Azhim - 2210010389

## Demo

 ![App Screenshot](https://github.com/AhmadDzulFauzilAzhim/apkCekNomorGanjilGenap/blob/main/img/demo%20cek%20nomor%20ganjil%20genap.gif)
