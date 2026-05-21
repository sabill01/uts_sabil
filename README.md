Deskripsi Project

Project ini merupakan implementasi basis data untuk sistem monitoring jaringan pada perusahaan penyedia layanan internet. Sistem ini digunakan untuk memantau kondisi perangkat jaringan seperti:

Router
Switch
Access Point
Server

Sistem monitoring bertujuan untuk:

Mencatat status perangkat
Memantau penggunaan bandwidth
Mencatat downtime jaringan
Mendokumentasikan aktivitas teknisi jaringan

Database dibuat menggunakan DBMS:

MySQL
MariaDB
Tujuan Sistem

Sistem monitoring jaringan dibuat untuk membantu perusahaan dalam:

Memantau perangkat jaringan secara real-time
Mengontrol penggunaan bandwidth
Mengetahui downtime perangkat
Menyimpan histori maintenance jaringan
Mengelola aktivitas teknisi jaringan
Entity yang Digunakan
1. Tabel perangkat

Menyimpan data perangkat jaringan.

Field:
id_perangkat
nama_perangkat
jenis_perangkat
ip_address
lokasi
status_perangkat
tanggal_instalasi
2. Tabel monitoring_bandwidth

Menyimpan data penggunaan bandwidth.

Field:
id_monitoring
id_perangkat
waktu_monitoring
bandwidth_upload
bandwidth_download
latency
3. Tabel downtime

Menyimpan data gangguan jaringan.

Field:
id_downtime
id_perangkat
waktu_mulai
waktu_selesai
durasi_menit
penyebab
4. Tabel teknisi

Menyimpan data teknisi jaringan.

Field:
id_teknisi
nama_teknisi
telepon
email
shift_kerja
5. Tabel aktivitas_teknisi

Menyimpan aktivitas maintenance teknisi.

Field:
id_aktivitas
id_teknisi
id_perangkat
jenis_aktivitas
tanggal_aktivitas
keterangan
Relasi Antar Tabel
Relasi:
Satu perangkat memiliki banyak monitoring bandwidth
Satu perangkat memiliki banyak downtime
Satu teknisi dapat melakukan banyak aktivitas
Satu perangkat dapat ditangani banyak aktivitas teknisi
