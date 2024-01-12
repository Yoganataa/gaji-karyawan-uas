## Dosen Pengampu
- SAIFUL NUR BUDIMAN, S.Kom., M.Kom
## MATA KULIAH
- Pemrograman Web Lanjut
## KELOMPOK 3
- Muhammad Arbi Yoganata	21104410073
- Muhammad Rizal Razaan	21104410061
- Arni Nazira				21104410077
## Laravel Employee Payroll (UAS) 
- Ini adalah aplikasi manajemen penggajian karyawan yang dikodekan dalam laravel.misalkan jika Anda membutuhkan solusi untuk mengelola jumlah karyawan yang tinggi di industri berlian Anda, maka ini akan menjadi penghemat waktu bagi Anda.

## Installation (Local)

*Anda dapat menginstalnya di komputer lokal Anda dengan mengikuti langkah-langkah di bawah ini:*

*Unduh atau kloning repositori di sistem Anda.*

```
git clone https://github.com/Yoganataa/gaji-karyawan-uas.git
```

*Buka folder payroll-employe-uas dan buka terminal, lalu ikuti langkah-langkah di bawah ini.*

*Install Composer:*
```
composer install
```

*Buat salinan file .env.example menjadi .env:*
```
cp .env.example .env
```

*Mengatur kredensial basis data:*
```
DB_CONNECTION = mysql
DB_HOST = 127.0.0.1
DB_PORT = 3306
DB_DATABASE = payroll
DB_USERNAME = root
DB_PASSWORD=
```

* Kemudian Hasilkan Kunci Aplikasi:*
```
php artisan key:generate
```

* Kemudian Migrasi basis data:*
```
php artisan migrate
```

*Sekarang Kita Perlu membuat Izin yang ditetapkan ke Peran (pastikan untuk menjalankan perintah ini terlebih dahulu sebelum penyemaian superadmin):*
```
php artisan db:seed --class = PermissionTableSeeder
``` 

*Membuat SuperAdmin:*
```
php artisan db:seed --class=CreateSuperAdminUserSeeder
```

*Jalankan php artisan serve. Buka http://localhost:8000, Anda akan melihat halaman login.*

* Login SuperAdmin *
```
email = superadmin@mailinator.com 
password = 12345678
```

**Catatan** :
Setelah Login sebagai Superadmin, masuk ke Pangkat dari sidebar dan buat dua Pangkat lagi bernama *Employee* & *Manager* & tetapkan izin kepada mereka yang Anda inginkan. sebagai contoh tambahkan 2 pengguna dengan peran manajer dari superadmin dan login dengan dua manajer tersebut dan buat karyawan dari mereka.
