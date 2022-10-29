# Jarkom-Modul-2-B08-2022

## Anggota Kelompok
<table>
 	<tr>
 		<td> Nama </td>
 		<td> NRP</td>
 	</tr>
 	<tr>
 		<td> Aaliyah Farah Adibah </td>
 		<td> 5025201070 </td>
 	</tr>
  <tr>
 		<td> Rafael Asi Kristanto Tambunan </td>
 		<td> 5025201168 </td>
 	</tr>
  <tr>
 		<td> Sejati Bakti Raga </td>
 		<td> 5025201007 </td>
 	</tr>
 </table>
 
 ## Daftar Isi
  + [Intro Soal](#intro-soal)
  + [Soal 1](#soal-1)
  + [Soal 2](#soal-2)
  + [Soal 3](#soal-3)
  + [Soal 4](#soal-4)
  + [Soal 5](#soal-5)
  + [Soal 6](#soal-6)
  + [Soal 7](#soal-7)
  + [Soal 8](#soal-8)
  + [Soal 9](#soal-9)
  + [Soal 10](#soal-10)
  + [Soal 11](#soal-11)
  + [Soal 12](#soal-12)
  + [Soal 13](#soal-13)
  + [Soal 14](#soal-14)
  + [Soal 15](#soal-15)
  + [Soal 16](#soal-16)
  + [Soal 17](#soal-17)
  + [Kendala](#kendala)

## Intro Soal
***Twilight (〈黄昏 (たそがれ) 〉, <Tasogare>) adalah seorang mata-mata yang berasal dari negara Westalis. Demi menjaga perdamaian antara Westalis dengan Ostania, Twilight dengan nama samaran Loid Forger (ロイド・フォージャー, Roido Fōjā) di bawah organisasi WISE menjalankan operasinya di negara Ostania dengan cara melakukan spionase, sabotase, penyadapan dan kemungkinan pembunuhan. Berikut adalah peta dari negara Ostania:***
<img alt="peta soal" src="pic/petasoal.png">

Dikarenakan gambaran peta tersebut, dibuat peta yang sama di GNS
<img alt="peta" src="pic/peta.png">

Lalu, lakukan pengaturan node. Sesuai yang telah ditetapkan, kelompok BO8 memiliki prefik 10.7 sehingga menjadi

**Foosha**                            
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.7.1.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 10.7.2.1
	netmask 255.255.255.0

auto eth3
iface eth3 inet static
	address 10.7.3.1
	netmask 255.255.255.0
 ```

## Soal 1
***WISE akan dijadikan sebagai DNS Master, Berlint akan dijadikan DNS Slave, dan Eden akan digunakan sebagai Web Server. Terdapat 2 Client yaitu SSS, dan Garden. Semua node terhubung pada router Ostania, sehingga dapat mengakses internet***<br><br>
Dilakukan pengaturan IP untuk setiap nodneya. Kelompok in memiliki prefix 10.7. sehingga pengaturan node


## Soal 2
***Untuk mempermudah mendapatkan informasi mengenai misi dari Handler, bantulah Loid membuat website utama dengan akses wise.yyy.com dengan alias www.wise.yyy.com pada folder wise***<br><br>

## Soal 3
***Setelah itu ia juga ingin membuat subdomain eden.wise.yyy.com dengan alias www.eden.wise.yyy.com yang diatur DNS-nya di WISE dan mengarah ke Eden***<br><br>

## Soal 4
***Buat juga reverse domain untuk domain utama***<br><br>

## Soal 5
***Agar dapat tetap dihubungi jika server WISE bermasalah, buatlah juga Berlint sebagai DNS Slave untuk domain utama***<br><br>

## Soal 6
***Karena banyak informasi dari Handler, buatlah subdomain yang khusus untuk operation yaitu operation.wise.yyy.com dengan alias www.operation.wise.yyy.com yang didelegasikan dari WISE ke Berlint dengan IP menuju ke Eden dalam folder operation***<br><br>

## Soal 7
***Untuk informasi yang lebih spesifik mengenai Operation Strix, buatlah subdomain melalui Berlint dengan akses strix.operation.wise.yyy.com dengan alias www.strix.operation.wise.yyy.com yang mengarah ke Eden***<br><br>

## Soal 8
***Setelah melakukan konfigurasi server, maka dilakukan konfigurasi Webserver. Pertama dengan webserver www.wise.yyy.com. Pertama, Loid membutuhkan webserver dengan DocumentRoot pada /var/www/wise.yyy.com***<br><br>

## Soal 9
***Setelah itu, Loid juga membutuhkan agar url www.wise.yyy.com/index.php/home dapat menjadi menjadi www.wise.yyy.com/home***<br><br>

## Soal 10
***Setelah itu, pada subdomain www.eden.wise.yyy.com, Loid membutuhkan penyimpanan aset yang memiliki DocumentRoot pada /var/www/eden.wise.yyy.com***<br><br>

## Soal 11
***Akan tetapi, pada folder /public, Loid ingin hanya dapat melakukan directory listing saja***<br><br>

## Soal 12
***Tidak hanya itu, Loid juga ingin menyiapkan error file 404.html pada folder /error untuk mengganti error kode pada apache***<br><br>

## Soal 13
***Loid juga meminta Franky untuk dibuatkan konfigurasi virtual host. Virtual host ini bertujuan untuk dapat mengakses file asset www.eden.wise.yyy.com/public/js menjadi www.eden.wise.yyy.com/js***<br><br>

## Soal 14
***Loid meminta agar www.strix.operation.wise.yyy.com hanya bisa diakses dengan port 15000 dan port 15500***<br><br>

## Soal 15
***dengan autentikasi username Twilight dan password opStrix dan file di /var/www/strix.operation.wise.yyy***<br><br>

## Soal 16
***dan setiap kali mengakses IP Eden akan dialihkan secara otomatis ke www.wise.yyy.com**<br><br>

## Soal 17
***Karena website www.eden.wise.yyy.com semakin banyak pengunjung dan banyak modifikasi sehingga banyak gambar-gambar yang random, maka Loid ingin mengubah request gambar yang memiliki substring “eden” akan diarahkan menuju eden.png. Bantulah Agent Twilight dan Organisasi WISE menjaga perdamaian!***<br><br>
