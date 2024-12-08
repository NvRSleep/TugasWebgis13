
# WebGIS: Pemetaan Kabupaten Provinsi Lampung dengan CodeIgniter

## Deskripsi Proyek

Proyek ini bertujuan untuk membangun aplikasi **WebGIS** yang menampilkan data administrasi wilayah **Provinsi Lampung**, termasuk **13 kabupaten** dan **2 kotamadya**. Aplikasi ini dibangun menggunakan framework **CodeIgniter** dan menggunakan **MariaDB** untuk penyimpanan data. Data yang ditampilkan meliputi informasi penting seperti **koordinat geografis**, **luas wilayah**, **jumlah penduduk**, dan **ibu kota** masing-masing kabupaten/kotamadya.

Aplikasi ini memungkinkan pengguna untuk:
1. Melihat data wilayah administrasi Provinsi Lampung secara terstruktur.
2. Menggunakan peta interaktif untuk melihat lokasi masing-masing kabupaten/kotamadya.
3. Mengelola data wilayah melalui database lokal.

Proyek ini mencakup proses berikut:
- Membuat **database** untuk menyimpan data kabupaten.
- Menghubungkan **CodeIgniter** dengan **MariaDB** untuk menampilkan data melalui aplikasi web.

## Fitur Utama

- **Database Lokal**: Membuat dan mengelola database lokal menggunakan **MariaDB** untuk menyimpan data kabupaten/kotamadya.
- **Peta Interaktif**: Menampilkan lokasi kabupaten di peta menggunakan **WebGIS**.
- **CRUD Data**: Memasukkan, mengedit, dan menampilkan data menggunakan **CodeIgniter** dan **MariaDB**.
- **Tampilan Data Tabel**: Menampilkan data kabupaten dalam format tabel yang dapat diakses melalui browser.

## Teknologi yang Digunakan

- **CodeIgniter**: Framework PHP untuk pengembangan aplikasi web.
- **MariaDB**: Sistem manajemen database untuk menyimpan data wilayah.
- **HTML5**: Untuk struktur halaman web.
- **CSS3**: Untuk styling halaman web.
- **PHP**: Untuk server-side scripting.
- **JavaScript**: Untuk interaktivitas peta dan tampilan dinamis.
- **Leaflet.js**: Pustaka JavaScript untuk pembuatan peta interaktif.

## Instalasi dan Pengaturan

Ikuti langkah-langkah di bawah ini untuk menginstal dan menjalankan aplikasi **WebGIS** di komputer lokal Anda.

### 1. Clone Repositori

Clone repositori ini ke komputer lokal Anda menggunakan perintah Git:

```bash
git clone https://github.com/username/webgis-pemetaankabupaten-lampung.git
```

### 2. Menyiapkan Database

1. Buka **phpMyAdmin** atau **MariaDB** melalui **XAMPP**.
2. Buat database baru dengan nama **`db_webgis`**.
3. Buat tabel **`tb_provinsi_lampung`** sesuai dengan struktur yang dijelaskan di bagian **Struktur Tabel**.
4. Tambahkan data untuk **13 kabupaten** dan **2 kotamadya**.

### 3. Konfigurasi Koneksi Database

Buka file **`application/config/database.php`** dan pastikan pengaturan berikut sudah benar:

```php
$db['default'] = array(
    'dsn'   => '',
    'hostname' => 'localhost',
    'username' => 'root',
    'password' => '',
    'database' => 'db_webgis',
    'dbdriver' => 'mysqli',
    'dbprefix' => '',
    'pconnect' => FALSE,
    'db_debug' => (ENVIRONMENT === 'development'),
    'cache_on' => FALSE,
    'cachedir' => '',
    'char_set' => 'utf8',
    'dbcollat' => 'utf8_general_ci',
    'swap_pre' => '',
    'encrypt' => FALSE,
    'compress' => FALSE,
    'stricton' => FALSE,
    'failover' => array(),
    'save_queries' => TRUE
);
```

### 4. Menjalankan Aplikasi

Setelah database disiapkan dan file konfigurasi telah diperbarui, buka **`http://localhost/[folder_proyek]`** di browser Anda untuk melihat aplikasi berjalan.

### 5. Mengedit Model, Controller, dan View

- **Model**: Buat file **`application/models/Provinsi_model.php`** untuk mengambil data dari database.
- **Controller**: Edit file **`application/controllers/Welcome.php`** untuk mengambil data dari model dan menampilkan ke view.
- **View**: Edit atau buat file **`application/views/welcome_message.php`** untuk menampilkan data di halaman web.

## Struktur Proyek

```
/application
    /config
        - database.php
    /controllers
        - Welcome.php
    /models
        - Provinsi_model.php
    /views
        - welcome_message.php
/database
    - db_webgis.sql
/public
    - index.html
    - styles.css
```

## Penggunaan

Setelah aplikasi diinstal dan dijalankan, pengguna dapat:

1. **Menambahkan Data**: Masukkan data wilayah kabupaten/kotamadya ke dalam tabel melalui **phpMyAdmin** atau langsung menggunakan aplikasi.
2. **Melihat Data**: Akses halaman **`welcome_message.php`** untuk melihat data yang ditampilkan dalam format tabel.
3. **Interaksi Peta**: Data kabupaten akan ditampilkan pada **peta interaktif** yang memungkinkan navigasi ke lokasi masing-masing kabupaten/kotamadya.

## Demo

Lihat demo aplikasi WebGIS ini yang di-host di **GitHub Pages** (jika di-deploy):

[Demo WebGIS Kabupaten Lampung](https://username.github.io/webgis-pemetaankabupaten-lampung)

## Kontribusi

Kami menyambut kontribusi dari siapa saja! Jika Anda ingin berkontribusi pada proyek ini, ikuti langkah-langkah berikut:

1. **Fork repositori** ini ke akun GitHub Anda.
2. **Clone repositori** fork ke komputer lokal Anda:
   ```bash
   git clone https://github.com/username/webgis-pemetaankabupaten-lampung.git
   ```
3. **Buat branch baru**:
   ```bash
   git checkout -b fitur-baru
   ```
4. **Lakukan perubahan** dan **commit** perubahan:
   ```bash
   git add .
   git commit -m "Menambahkan fitur baru"
   ```
5. **Push perubahan** ke repositori fork:
   ```bash
   git push origin fitur-baru
   ```
6. **Buat Pull Request** ke repositori utama untuk penggabungan perubahan.

## Lisensi

Repositori ini dilisensikan di bawah **MIT License**. Silakan lihat file [LICENSE](LICENSE) untuk informasi lebih lanjut.

---

## Referensi

1. **CodeIgniter Documentation**: [https://codeigniter.com/](https://codeigniter.com/)
2. **MariaDB Documentation**: [https://mariadb.org/](https://mariadb.org/)
3. **Leaflet.js Documentation**: [https://leafletjs.com/](https://leafletjs.com/)
4. **phpMyAdmin**: [https://www.phpmyadmin.net/](https://www.phpmyadmin.net/)

## Contact

- **Nama**: M. Gilang Martiansyah M
- **Email**: mgilang.121450056@student.itera.ac.id
- **GitHub**: [github.com/username](https://github.com/username)

---

Terima kasih telah mengunjungi repositori ini! Jika Anda memiliki pertanyaan atau saran, silakan buka **issue** atau buat **pull request**.
