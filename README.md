# Jarkom-Modul-1-ITB05-2022
Kelompok ITB05

1. M.Fernando N.Sibarani (5027201015)
2. Richard Nicolas (5027201021)
3. Muhammad Ihsanul Afkar (5027201024)

# Daftar Isi
* [Soal 1](#soal-1) 
* [Soal 2](#soal-2) 
* [Soal 3](#soal-3) 
* [Soal 4](#soal-4) 
* [Soal 5](#soal-5) 
* [Soal 6](#soal-6) 
* [Soal 7](#soal-7) 
* [Soal 8](#soal-8) 
* [Soal 9](#soal-9) 
* [Soal 10](#soal-10) 

# Soal-1
Sebutkan web server yang digunakan pada "monta.if.its.ac.id"!
## Penyelesaian Soal 1
Untuk melihat web server yag digunakan "monta.if.its.ac.id", pertama harus dilihat traffic pada "monta.if.its.ac.id" dengan menggunakan filter **http.host == monta.if.its.ac.id**
![1_1](img/soal1_1.png)
Setelah itu, dipilih salah satu untuk dilihat tcp streamnya. Caranya dengan **klik kanan > Follow > TCP Stream**
![1_2](img/soal1_2.png)
Hasilnya akan telihat seperti dibawah ini 
![1_3](img/soal1_3.png)
Terlihat pada bagian bawah server yang digunakan adalah **nginx/1.10.3**
# Soal-2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan **detail topik** pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?
## Penyelesaian Soal 2
Untuk melihat web server yag digunakan "monta.if.its.ac.id", pertama harus dilihat traffic pada "monta.if.its.ac.id" dengan menggunakan filter **http.host == monta.if.its.ac.id**
![2_1](img/soal2_1.png)
Terlihat semua traffic yang melalui "monta.if.its.ac.id" dan terlihat pada paket 576, terjadi pemanggilan detail topik (judul topik) oleh ishaq.
![2_2](img/soal2_2.png)
Setelah dilihat lebih detail akan didapatkan link http://monta.if.its.ac.id/index.php/topik/detailTopik/194 pada Hypertext Trandfer Protocol > Full Request URI
![2_3](img/soal2_3.png)
Setelah dibuka link tersebut akan telihat detail topik yang dibuka ishaq, yaitu **Evaluasi unjuk kerja User Space Filesystem (FUSE)** oleh WAHYU SUADI, pada Rabu 17 Maret 2021 pukul 05:13:50 WIB
# Soal-3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!
## Penyelesaian Soal 3
Filter display yang digunakan adalah **tcp.dstport == 80**
![3](img/soal3.png)
# Soal-4
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!
## Penyelesaian Soal 4
Filter display yang digunakan adalah **tcp.srcport == 21**
![4](img/soal4.png)
# Soal-5
# Soal-6
# Soal-7
# Soal-8
# Soal-9
# Soal-10
