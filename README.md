# Accessing-Firebird-DB-of-Accurate-Desktop_5
Memanfaatkan Lingkungan Colab dan Python untuk membuka akses database Firebird (.gdb) milik Accurate Desktop v5.

Tujuan dari proyek ini adalah untuk mengekstraksi database Firebird berekstensi.gdb dari Accurate Desktop v5.
Hasil ujicoba menunjukkan bahwa Accurate Desktop v5 yang digunakan masih menggunakan versi 2.1 dengan ODS 11.1, dan versi ini sudah tidak didukung oleh versi Firebird terbaru.
Karena itu, untuk mendapatkan akses ke databasenya diperlukan jenis server harus diekstraksi serta menggunakan user yang tepat.

Menggunakan lingkungan Colab, saya menginstall libncurses5/libtinfo5 secara langsung menggunakan dpkg.
Disertai dengan penggunaan Python, Pandas, Firebird SQL, dan scripting Linux Shell untuk fungsi yang lebih kompleks.

Tujuan dari proyek ini ialah untuk mempersiapkan diri dalam migrasi database Accurate Desktop v5 ke sistem ERP (Odoo).
Karena tidak menggunakan data lama seutuhnya, proses ekstraksi ini sangat membantu dalam memaksimalkan proses migrasi data antar sistem karena memiliki ekosistem yang berbeda.

# Informasi Lain:
- SYSDBA tidak menggunakan password default 'masterkey' >> Password dalam mengakses Database terbuat secara dinamis saat proses instalasi server Firebird.
- Uses SYSDBA tidak bisa digunakan untuk mengakses databases >> SYSDBA memiliki role yang sama dengan Administrator, sehingga harus menggunakan user lain yang memiliki hak akses setara.
- Firebird masih bisa menambahkan user baru selain SYSDBA agar bisa menemukan user yang memiliki role setara SYSDBA.
- Ubah nama file (.gdb) sesuai database yang dimiliki serta user yang memiliki role setara agar bisa membuka aksesnya.
