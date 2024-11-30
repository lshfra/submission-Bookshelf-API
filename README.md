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
- Android Studio atau Visual Studio Code (dengan Flutter plug in terinstal)
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

