# Lapres Jarkom-Modul-2-TI4-2021

**Oleh:**
  * Muhammad Nur Fauzan (05311940000035)
  * Ghimnastiar Al Abiyyuna (05311940000042)
  * Christopher Bennedict (05311840000024)

---

## **Soal**

**1.** EniesLobby akan dijadikan sebagai DNS Master, Water7 akan dijadikan DNS Slave, dan Skypie akan digunakan sebagai Web Server. Terdapat 2 Client yaitu Loguetown, dan       Alabasta. Semua node terhubung pada router Foosha, sehingga dapat mengakses internet

**Solusi**
```
tes
```


**2.** Luffy ingin menghubungi Franky yang berada di EniesLobby dengan denden mushi. Kalian diminta Luffy untuk membuat website utama dengan mengakses franky.yyy.com dengan alias www.franky.yyy.com pada folder kaizoku

**Solusi**
```
tes
```


**3.** Setelah itu buat subdomain super.franky.yyy.com dengan alias www.super.franky.yyy.com yang diatur DNS nya di EniesLobby dan mengarah ke Skypie

**Solusi**
```
tes
```


**4.** Buat juga reverse domain untuk domain utama

**Solusi**
```
tes
```

**5.** Supaya tetap bisa menghubungi Franky jika server EniesLobby rusak, maka buat Water7 sebagai DNS Slave untuk domain utama

**Solusi**
```
tes
```

**6.** Setelah itu terdapat subdomain mecha.franky.yyy.com dengan alias www.mecha.franky.yyy.com yang didelegasikan dari EniesLobby ke Water7 dengan IP menuju ke Skypie dalam folder sunnygo

**Solusi**
```
tes
```

**7.** Untuk memperlancar komunikasi Luffy dan rekannya, dibuatkan subdomain melalui Water7 dengan nama general.mecha.franky.yyy.com dengan alias www.general.mecha.franky.yyy.com yang mengarah ke Skypie

**Solusi**
```
tes
```

**8.** Setelah melakukan konfigurasi server, maka dilakukan konfigurasi Webserver. Pertama dengan webserver www.franky.yyy.com. Pertama, luffy membutuhkan webserver dengan DocumentRoot pada /var/www/franky.yyy.com

**Solusi**
```
tes
```


**9.** Setelah itu, Luffy juga membutuhkan agar url www.franky.yyy.com/index.php/home dapat menjadi menjadi www.franky.yyy.com/home

**Solusi**
```
tes
```

**10.** Setelah itu, pada subdomain www.super.franky.yyy.com, Luffy membutuhkan penyimpanan aset yang memiliki DocumentRoot pada /var/www/super.franky.yyy.com

**Solusi**
```
tes
```

**11.** Akan tetapi, pada folder /public, Luffy ingin hanya dapat melakukan directory listing saja

**Solusi**
```
tes
```

**12.** Tidak hanya itu, Luffy juga menyiapkan error file 404.html pada folder /error untuk mengganti error kode pada apache

**Solusi**
```
tes
```

**13.** Luffy juga meminta Nami untuk dibuatkan konfigurasi virtual host. Virtual host ini bertujuan untuk dapat mengakses file asset www.super.franky.yyy.com/public/js menjadi www.super.franky.yyy.com/js. 

**Solusi**
```
tes
```

**14.** Dan Luffy meminta untuk web www.general.mecha.franky.yyy.com hanya bisa diakses dengan port 15000 dan port 15500

**Solusi**
```
tes
```

**15.** Dengan autentikasi username luffy dan password onepiece dan file di /var/www/general.mecha.franky.yyy

**Solusi**
```
tes
```


**16.** Dan setiap kali mengakses IP Skypie akan dialihkan secara otomatis ke www.franky.yyy.com

**Solusi**
```
tes
```

**17.** Dikarenakan Franky juga ingin mengajak temannya untuk dapat menghubunginya melalui website www.super.franky.yyy.com, dan dikarenakan pengunjung web server pasti akan bingung dengan randomnya images yang ada, maka Franky juga meminta untuk mengganti request gambar yang memiliki substring “franky” akan diarahkan menuju franky.png. Maka bantulah Luffy untuk membuat konfigurasi dns dan web server ini!


**Solusi**
```
tes
```
