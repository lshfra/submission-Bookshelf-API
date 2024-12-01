Ini adalah dokumen submission


# Project Android Title:  Checker 

## Deskripsi : Merupakan aplikasi berbasis mobile dengan framwork Flutter menerapkan arsitektur BLoC (Business Logic Component) dengan tujuan utama adalah mampu untuk scan QR code pada tiket wisata yang di hasilkan pada gerbang utama wisata. 

## Tujuan Dokumentasi : Mengarahkan pengembang dalam memahami, menggunakan code serta menjalankan aplikasi pada perangkat fisik dengan mudah

### Teknologi Library yang di gunakan 
- Flutter dan versi SDK 
- Library Utama: 
 * flutter_bloc: Management State
 * http: Untuk komunikasi API
 * mobile_scanner: Untuk Membaca QR code
- Library Pendukung: 
* fl_chart: Membuat grafik dan visualisasi data
* intl: Format dan manipulasi data waktu, angka, atau teks
* equatable: Membantu membandingkan objek
* provider: State management sederhana
* pdf: Membuat dan membaca file pdf
* path_provider: Mengakses direktori file di perangkat
* sqflite: Database lokal berbasis SQLite
* path: Manipulasi path file atau direktori
* permission_handler: Mengelola izin aplikasi (kamera, lokal, dan lain lain)
* connectivity_plus: Memeriksa koneksi internet
* fluttertoast: Menampilkan pesan singkat (toast)
* shared_preferences: Penyimpanan data kecil secara lokal
* device_info_plus: Mengambil informasi perangkat

# Instalasi Program

### 1.Persyaratan
* Instalasi Software:
- FLutter SDK (versi yang digunakan)
- Android Studio atau Visual Studio Code (dengan Flutter dan Dart plugin terinstal)
- Git untuk cloning repository

* Platform Tools:
- Android Emulator atau perangkat fisik (smartphone)

### 2.Clone Repository
- git clone [URL_REPOSITORY]
cd [NAMA_FLODER_PROJEK]

### 3.Instalasi Dependencies
- flutter pub get

### 4.Menjalankan Proyek
- pilih device tujuan (emulator atau perangkat fisik)
- flutter run (di terminal proyek) atau klik icon "Start Debugging"

### 5.Rilis Aplikasi 
- flutter build apk --release

  
# how to register? 
- registerasi akun baru hanya bisa dilakukan oleh master union
- hanya karyawan yang sudah dibuatkan akun aplikasi "checker" yang dapat login

# how to login?
- karyawan akan diberi akun berupa "username" dan "password" oleh master union
- karyawan bisa login dengan akun tersebut yang terdiri dari entitas "username" dan "password"

# contoh login di aplikasi 
- username : ***test_palawi***
- password : ***test_palawi***
- lalu klik button login 

# How to use functionalitas Scan QR Aplikasi ? 
**1. Home Page**
- jika berhasil login, maka akan ada "toast" atau seperti pop up bahwa "login berhasil"
- di halaman utama, karyawan yang telah login bisa memulai aksi scan QR Code untuk scan QR pada Tiket yang di cetak oleh gerbang utama
- klik button "Scan Tiket Here"

**2. Qr Scan Page**
- Permintaan izin akses akan di berikan oleh sistem sebagai persetujuan antara sistem dengan pengguna 
- Jika di izinkan maka, izin kamera akan aktif dan dapat memulai kerja scan QR Code
- silahkan arahkan kamera kotak scan ke QR Code 
- Jika berhasil, maka akan menampilkan alert dialog berubah "Data Terferifikasi" 
- Kamera akan menyimpan string dari QR Code dan memasukan ke dalam databae local perangkat pengguna "SQLite" 
- Jika berhasil, lalu klik "OK" pada alert dialog, dan kamera akan bekerja kembali untuk scan 
- Scan dapat dilakukan berkali-kali unutuk QR Code yang unik (tidak duplikat)
- Jika Pengguna memaksa untuk Scan QR Code dengan kode unik yang sama, maka sistem akan menampilkan alert dialog "Ticket Sudah Pernah Dipindai. Silakan Pindai QR Code Lain."

**3. Tiket Terusan Page**
- SInkronasi terverifikasi valid Ticket yang telah di scan ke database akan dilakukan sistem melalui API secara online apabila aplikasi mendapatkan konek internet
= Terdapat "count" atau jumlah dari riwayat scan tiket yang sudah masuk ke database sistem
- pengguna dapat melakukan aksi download dengan klik pada icon button "download" 
- setelah klik download, pengguna akan diminta memasukan rentang tannggal scan. contoh mulai tanggal "10.10.2024" sampai tanggal "12.11.2024". rentang tanggal untuk download riwayat scan tiket hanya dapat dialkukan sebelum tanggal "now" sampai rentang tanggal "now" 
- apabila sudah menentukan rentang tanggal, pengguna dapat klik "download" 
- Sebelum mendownload, sistem akan menampilkan izin penyimpanan internal pada pengguna sebagai syarat keamanan dalam menyimpan di perangkat tujuan
- Riwayat Scan Tiket akan terdownload berdsarkan rentang tanggal yang sudah dipilih 
- Jika berhasil, maka sistem akan menampilkan "toast" atau pop up berupa "PDF berhasil disimpan /storage/emulated/0/Download" 
- Pengguna dapat memastikan hasil download di direktory file manager "penyimpanan internal->folder download->temukan file dengan nama $scan_riwayat_tiket.pdf" 
- klik file untuk membuka dan membaca hasil riwayat dalam bentuk pdf

**4. Logout Page**
- pengguna dapat klik drawer atau menu geser samping pada icon "menu" seperti "humberger"
- klik logout 
- setelah logout, aplikasi akan berada di layar login 

