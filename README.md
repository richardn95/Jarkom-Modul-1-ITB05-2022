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
![1_1](img/soal1_1.png) <br>
Setelah itu, dipilih salah satu untuk dilihat tcp streamnya. Caranya dengan **klik kanan > Follow > TCP Stream**
![1_2](img/soal1_2.png) <br>
Hasilnya akan telihat seperti dibawah ini 
![1_3](img/soal1_3.png) <br>
Terlihat pada bagian bawah server yang digunakan adalah **nginx/1.10.3**

# Soal-2
Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan **detail topik** pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?

## Penyelesaian Soal 2
Untuk melihat web server yag digunakan "monta.if.its.ac.id", pertama harus dilihat traffic pada "monta.if.its.ac.id" dengan menggunakan filter **http.host == monta.if.its.ac.id**
![2_1](img/soal2_1.png) <br>
Terlihat semua traffic yang melalui "monta.if.its.ac.id" dan terlihat pada paket 576, terjadi pemanggilan detail topik (judul topik) oleh ishaq.
![2_2](img/soal2_2.png) <br>
Setelah dilihat lebih detail akan didapatkan link http://monta.if.its.ac.id/index.php/topik/detailTopik/194 pada Hypertext Trandfer Protocol > Full Request URI
![2_3](img/soal2_3.png) <br>
Setelah dibuka link tersebut akan telihat detail topik yang dibuka ishaq, yaitu **Evaluasi unjuk kerja User Space Filesystem (FUSE)** oleh WAHYU SUADI, pada Rabu 17 Maret 2021 pukul 05:13:50 WIB

# Soal-3
Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!

## Penyelesaian Soal 3
Filter display yang digunakan adalah **tcp.dstport == 80**
![3](img/soal3.png) <br>

# Soal-4
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!

## Penyelesaian Soal 4
Filter display yang digunakan adalah **tcp.srcport == 21**
![4](img/soal4.png) <br>

# Soal-5

Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

## Penyelesaian Soal 5

Filter display yang digunakan adalah **tcp.srcport == 443**

![5](img/soal5.png)

# Soal-6

Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !

## Penyelesaian Soal 6

Pertama-tama, lakukan ping pada **lipi.go.id** untuk mendapatkan ip.

![6](img/soal6_1.png)

Setelah berhasil mendapatkan ip, lakukan display filter **ip.dst_host == 203.160.128.158**

![](img/soal6_2.png)

# Soal-7

Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

## Penyelesaian Soal 7

Ketahui ip komputer masing-masing dengan cmd, lalu gunakan capture filter **src host 192.168.100.13**

![](img/soal7.png)

# Soal-8

Untuk soal ini, kami melakukan follow TCP stream. Sehingga ditemukan beberapa paket yang berisi percakapan mencurigakan antara 2 mahasiswa yang melakukan tindak kecurangan dalam kegiatan praktikum. Berikut adalah hasil paket-paket data yang ditemukan.

**tcp.stream eq 12**
![8](/img/soal8_1.png) <br>

**tcp.stream eq 41**
![8_1](img/soal8_2.png) <br>

**tcp.stream eq 90**
![8_2](img/soal8_3.png) <br>

# Soal-9

Dari percakapan yang diperoleh, didapatkan informasi bahwa mereka bertukar file dengan menggunakan port 9002. Sehingga kami melakukan filter terhadap port 9002. 

**tcp.port == 9002**
![9](img/soal9.png) <br>


Setelah itu kami melakukan follow TCP Stream. Didapatkan file salted yang sudah didekripsi.

**tcp.stream eq 29**
![9_2](img/soal9_2.png) <br>

# Soal-10

Setelah mendapat file hasil enkripsi kami menyimpannya, kemudian kami melihat percakapan tersebut dan ditemukan clue untuk password file adalah nama karakter anime yang kembar 5 dan adanya kesamaan. Kemudian didapatkan juga informasi bahwa file tersebut dapat didekripsi dengan menggunakan openssl dengan metode des3.

Karena itu, kami melakukan pencarian terhadap nama karakter anime kembar 5. Kami menemukan bahwa nama anime yang dimaksud adalah Go-Toubun no Hanayome. Dengan kesamaan nama karakternya adalah Nakano. Kemudian kami melakukan dekripsi des3 dengan menggunakan openssl dengan perintah
**openssl des3 -d -in [Input File] -out [Output File]**

Setelah itu, dihasilkan file baru yang berisi flag yang merupakan jawaban untuk soal ini

![10](img/soal10.png) <br>

