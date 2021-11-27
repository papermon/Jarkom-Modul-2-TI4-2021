# Lapres Jarkom-Modul-2-TI4-2021

**Oleh:**
  * Muhammad Nur Fauzan (05311940000035)
  * Ghimnastiar Al Abiyyuna (05311940000042)
  * Christopher Benedict (05311840000024)

---

## **Soal1**

**1. EniesLobby akan dijadikan sebagai DNS Master, Water7 akan dijadikan DNS Slave, dan Skypie akan digunakan sebagai Web Server. Terdapat 2 Client yaitu Loguetown, dan       Alabasta. Semua node terhubung pada router Foosha, sehingga dapat mengakses internet**

**Solusi**
![messageImage_1635585422759](https://user-images.githubusercontent.com/73151866/139528104-cdabea1a-f176-4771-bd2d-09545fd9fc64.jpg)
Gambar diatas adalah topologi jaringan yang sudah disesuaikan sesuai dengan ketentuan soal EniesLobby sebagai DNS Master, Water7 sebagai DNS Slave, Skypie sebagai Web Server, Loguetown dan Alabasta sebagai Client, dan Foosha sebagai router


## **Soal2**

**2. Luffy ingin menghubungi Franky yang berada di EniesLobby dengan denden mushi. Kalian diminta Luffy untuk membuat website utama dengan mengakses franky.yyy.com dengan alias www.franky.yyy.com pada folder kaizoku**

**Solusi**

Melakukan konfigurasi terhadap file  `/etc/bind/named.conf.local` dengan menambahkan  
```
zone "franky.TI4.com" {  
        type master;  
        file "/etc/bind/kaizoku/franky.TI4.com";
};
```  
Membuat direktori baru yaitu `/etc/bind/kaizoku`  
Menambahkan konfigurasi pada `/etc/bind/kaizoku/franky.TI4.com`  

Melakukan restart service bind9 dengan `service bind9 restart`  

![messageImage_1635585526011](https://user-images.githubusercontent.com/73151866/139528149-f10cac05-ec9f-4775-9a26-a606e66e84b0.jpg)
![messageImage_1635585475317](https://user-images.githubusercontent.com/73151866/139528154-a9bb466e-08e4-4d8c-9264-30b37177a934.jpg)


## **Soal3**

**3. Setelah itu buat subdomain super.franky.yyy.com dengan alias www.super.franky.yyy.com yang diatur DNS nya di EniesLobby dan mengarah ke Skypie**

**Solusi**

Server EniesLobby
Melakukan Edit pada file /etc/bind/kaizoku/franky.TI$.com menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/73151866/139528187-2957b4f8-b8a8-4020-b4d9-b8c8b831ef49.png)
![messageImage_1635585574467](https://user-images.githubusercontent.com/73151866/139528221-1f4a8f74-8df0-47c5-a617-df6298e09a1e.jpg)


## **Soal4**

**4. Buat juga reverse domain untuk domain utama**

**Solusi**

Server EsniesLobby
Edit file `/etc/bind/named.conf.local` menjadi sebagai berikut:

![messageImage_1635585701971](https://user-images.githubusercontent.com/73151866/139528246-66d492ce-5362-4219-a4ef-995364c9ed28.jpg)
![messageImage_1635585666279](https://user-images.githubusercontent.com/73151866/139528248-3b2e7d07-044d-4d26-a161-b257705e5b77.jpg)
![messageImage_1635585640005](https://user-images.githubusercontent.com/73151866/139528254-c040cbd7-b2b8-44fa-b3e4-e5df333c6151.jpg)


## **Soal5**

**5. Supaya tetap bisa menghubungi Franky jika server EniesLobby rusak, maka buat Water7 sebagai DNS Slave untuk domain utama**

**Solusi**

Service Water7
lakukan konfigurasi pada file /etc/bind/named.conf.local sebagai berikut untuk melakukan konfigurasi DNS Slave yang mengarah ke water7:

Jangan lupa melakukan restart sevice bind9 dengan `service bind9 restart`

![messageImage_1635585727883](https://user-images.githubusercontent.com/73151866/139528281-ea1c21da-40d3-4238-a3d1-ebad692ffe17.jpg)


## **Soal6**

**6.Setelah itu terdapat subdomain mecha.franky.yyy.com dengan alias www.mecha.franky.yyy.com yang didelegasikan dari EniesLobby ke Water7 dengan IP menuju ke Skypie dalam folder sunnygo**

**Solusi**

**Server Enieslobby**  
Melakukan konfigurasi `/etc/bind/kaizoku/franky.TI4.com`  

![image](https://user-images.githubusercontent.com/73151866/139528303-d0afce0d-b6d8-40cb-a66b-c09a51d0e53e.png)
![messageImage_1635585932994](https://user-images.githubusercontent.com/73151866/139528310-25e025ee-f7df-4ab7-9175-43bb43a0e31a.jpg)
![messageImage_1635585984646](https://user-images.githubusercontent.com/73151866/139528313-ff41693b-bfe3-4e06-b491-a0ed3eded638.jpg)


## **Soal7**

**7.Untuk memperlancar komunikasi Luffy dan rekannya, dibuatkan subdomain melalui Water7 dengan nama general.mecha.franky.yyy.com dengan alias www.general.mecha.franky.yyy.com yang mengarah ke Skypie**

**Solusi**

konfigurasi file `/etc/bind/sunnygo/mecha.franky.TI4.com` dengan
![messageImage_1635586059272](https://user-images.githubusercontent.com/73151866/139528321-ea700d3f-350d-4bff-9a44-2078f896c245.jpg)

![messageImage_1635586045481](https://user-images.githubusercontent.com/73151866/139528323-420cccfc-6d32-42e1-bbea-73225a476db7.jpg)


## **Soal8**

**8. Setelah melakukan konfigurasi server, maka dilakukan konfigurasi Webserver. Pertama dengan webserver www.franky.yyy.com. Pertama, luffy membutuhkan webserver dengan DocumentRoot pada /var/www/franky.yyy.com**

**Solusi**
konfigurasi file `/etc/apache2/sites-available/franky.TI4.com.conf`. DcumentRoot diletakkan  di `/var/www/franky.TI4.com.` Jangan lupa untuk menambah servername dan serveralias

![messageImage_1635586100675](https://user-images.githubusercontent.com/73151866/139528328-700f1515-2861-4034-b7a6-b461be362b46.jpg)
![messageImage_1635586126084](https://user-images.githubusercontent.com/73151866/139528331-81e207ed-9fa1-4d1a-9e33-a8a6ad1425f6.jpg)


## **Soal9**

**9. Setelah itu, Luffy juga membutuhkan agar url www.franky.yyy.com/index.php/home dapat menjadi menjadi www.franky.yyy.com/home**

**Solusi**

Memberikan Alias dengan konfigurasi file pada `/etc/apache2/sites-available/franky.TI4.com.conf` 
![image](https://user-images.githubusercontent.com/73151866/139528480-dc08e0e1-5d78-4bb3-8b92-776d91676fb1.png)


## **Soal10**

**10. Setelah itu, pada subdomain www.super.franky.yyy.com, Luffy membutuhkan penyimpanan aset yang memiliki DocumentRoot pada /var/www/super.franky.yyy.com**

**Solusi**
konfigurasi file `/etc/apache2/sites-available/super.franky.TI4.com.conf` dan mengubah DocumentRoot sesuai kebutuhan
![messageImage_1635586259374](https://user-images.githubusercontent.com/73151866/139528355-547e2769-6cda-4341-a882-a4d83e486857.jpg)


## **Soal11**

**11. Akan tetapi, pada folder /public, Luffy ingin hanya dapat melakukan directory listing saja**

**Solusi**
konfigurasi file `/etc/apache2/sites-available/super.franky.TI4.com.conf` menamahkan Options +Indexes ke direktori yang ingin di directory list

![messageImage_1635586307275](https://user-images.githubusercontent.com/73151866/139528368-046c1a07-a3e5-454d-8764-4a3db94bf715.jpg)
![image](https://user-images.githubusercontent.com/73151866/139528387-b011ddeb-ee49-4063-967f-262ce65d57f0.png)



## **Soal12**

**12.Tidak hanya itu, Luffy juga menyiapkan error file 404.html pada folder /error untuk mengganti error kode pada apache**

**Solusi**

konfigurasi file `/etc/apache2/sites-available/super.franky.TI4.com.conf` menambahkan konfigurasi ErrorDocumentuntuk setiap error yang ada yang diarahkan ke file /error/404.html

![messageImage_1635586326804](https://user-images.githubusercontent.com/73151866/139528393-67890bd2-e645-46aa-a945-884f487175d0.jpg)
![messageImage_1635586353393](https://user-images.githubusercontent.com/73151866/139528397-72a82607-959d-4c2b-9b24-d06b5d3f43e1.jpg)



## **Soal13**

**13.Luffy juga meminta Nami untuk dibuatkan konfigurasi virtual host. Virtual host ini bertujuan untuk dapat mengakses file asset www.super.franky.yyy.com/public/js menjadi www.super.franky.yyy.com/js. **

**Solusi**

konfigurasi file `/etc/apache2/sites-available/super.franky.TI4.com.conf` menambahkan konfigurasi Alias untuk alamat js

![messageImage_1635586379756](https://user-images.githubusercontent.com/73151866/139528402-fc265dde-4e92-4f5e-9ad5-353d3d6c2e71.jpg)
![messageImage_1635586398846](https://user-images.githubusercontent.com/73151866/139528403-b4ecceac-c404-4594-b769-e420912ea6cd.jpg)


## **Soal14**

**14.Dan Luffy meminta untuk web www.general.mecha.franky.yyy.com hanya bisa diakses dengan port 15000 dan port 15500**

**Solusi**
konfigurasi file `/etc/apache2/sites-available/general.mecha.franky.TI4.com.conf` disini menambahkan VirtualHost baru yang berada pada port 15000 dan 15500 dan kemudia
konfigurasi file `/etc/apache2/ports.conf` menambahkan Listen 15000 dan 15500 dengan

![messageImage_1635586831721](https://user-images.githubusercontent.com/73151866/139528435-d842fa7d-1d2b-4d56-9df1-9dbb3cbbadcc.jpg)
![messageImage_1635586859652](https://user-images.githubusercontent.com/73151866/139528439-c132a507-7cfa-4574-b0e5-620d2eb0524b.jpg)

## **Soal15**

**15. Dengan autentikasi username luffy dan password onepiece dan file di /var/www/general.mecha.franky.yyy**

**Solusi**
Jalankan Command `htpasswd -c -b /var/www/general.mecha.franky.TI4.com/.htpasswd luffy onepiece`
konfigurasi file `/etc/apache2/sites-available/general.mecha.franky.TI4.com.conf` 
Lalu edit file `/var/www/general.mecha.franky.TI4.com/.htaccess`

![messageImage_1635586920457](https://user-images.githubusercontent.com/73151866/139528442-42c64530-150a-42dd-b086-80e0e089d8b4.jpg)


## **Soal16**

**16. Dan setiap kali mengakses IP Skypie akan dialihkan secara otomatis ke www.franky.yyy.com**

**Solusi**
**Server Skypie**   
konfigurasi file `/etc/apache2/sites-available/000-default.conf` dengan     
```
<VirtualHost *:80>

        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html

        RewriteEngine On
        RewriteCond %{HTTP_HOST} !^franky.TI4.com$
        RewriteRule /.* http://franky.TI4.com/ [R]

        ErrorLog \${APACHE_LOG_DIR}/error.log
        CustomLog \${APACHE_LOG_DIR}/access.log combined

</VirtualHost>
```    
Melakukan restart service apache2 dengan `service apache2 restart`  


## **Soal17**

**17.Dikarenakan Franky juga ingin mengajak temannya untuk dapat menghubunginya melalui website www.super.franky.yyy.com, dan dikarenakan pengunjung web server pasti akan bingung dengan randomnya images yang ada, maka Franky juga meminta untuk mengganti request gambar yang memiliki substring “franky” akan diarahkan menuju franky.png. Maka bantulah Luffy untuk membuat konfigurasi dns dan web server ini!**


**Solusi**

Pertama, aktifkan bagian `AllowOverride All` pada konfigurasi virtual host `/etc/apache2/sites-available/penanjakan.semerut03.pw.`

![messageImage_1635586741582](https://user-images.githubusercontent.com/73151866/139528412-b0b76041-c02d-4394-bb42-47f54c8c987c.jpg)

Lalu edit `/var/www/super.franky.TI4.com` agar memiliki RewriteRule untuk mengarahkan semua akses yang memiliki substring "super.franky" menjadi menuju `/public/images/franky.png`

![image](https://user-images.githubusercontent.com/73151866/139528519-55726084-8b29-4f1c-a1ea-88fcaddae271.png)
![messageImage_1635586767611](https://user-images.githubusercontent.com/73151866/139528416-b4757454-fb4c-4f6b-9d5b-b8a0d1debb5f.jpg)

