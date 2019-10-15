# Lapres_Modul2_JA04

### Kelompok A04:
- Iman Afandy (05111740000129)
- Mochamad Thiesa Nabil (05111740000194)
- Rizky Andre Wibisono (05111740000183)

Palletkanto adalah sebuah Laboratorium milik Professor Oak yang meneliti pokemon. Laboratorium
tersebut memiliki 3 buah server bernama ARTICUNO, MEWTWO, dan MOLTRES. Server
ARTICUNO akan digunakan sebagai DNS Server Master, MOLTRES akan digunakan sebagai DNS
Server Slave, dan MEWTWO akan digunakan sebagai Web Server. Selain 3 server tersebut pada
infrastruktur laboratoriumnya terdapat pula sebuah router bernama PIKACHU dan klien bernama
SNORLAX dan PSYDUCK.
Kamu diminta untuk membuat sebuah website utama dengan (1) alamat http://kanto.yy.com yang
memiliki (2) alias http://www.kanto.yy.com, dan (3) subdomain http://www.pallet.kanto.yy.com
yang diatur DNS-nya pada ARTICUNO dan mengarah ke IP Server MEWTWO serta dibuatkan (4)
reverse domain. Untuk mengantisipasi server rusak, mereka meminta dibuatkan (5) DNS Server Slave
pada MOLTRES agar layanan tidak terganggu. selain website utama mereka juga meminta dibuatkan
(6) subdomain dengan alamat http://pewter.kanto.yy.com yang didelegasikan pada server
MOLTRES dan mengarah ke IP Server MEWTWO. Karena laboratorium memiliki cabang di
Vermilion City maka dibuatkan pula (7) domain dengan nama
http://vermilion.pewter.kanto.yy.com, domain ini diarahkan ke server MEWTWO.
Setelah selesai membuat keseluruhan domain, kamu diminta untuk segera mengatur web server. (8)
Domain http://kanto.yy.com memiliki DocumentRoot pada /var/www/kanto.yy.com.
Awalnya web dapat diakses menggunakan alamat http://kanto.yy.com/index.php/home. Karena
dirasa alamat urlnya kurang bagus, maka (9) diaktifkan mod rewrite agar urlnya menjadi
http://kanto.yy.com/home.

(10) Web http://pallet.kanto.yy.com akan digunakan untuk menyimpan aset file yang memiliki
DocumentRoot pada /var/www/pallet.kanto.yy.com dan memiliki struktur folder sebagai berikut:
/var/www/pallet.kanto.yy.com

/public/javascripts
/public/css
/public/images
/errors

(11) Pada folder /public dibolehkan directory listing namun untuk folder yang berada di dalamnya
tidak dibolehkan. (12) Untuk mengatasi HTTP Error code 404, disediakan file 404.html pada folder
/errors untuk mengganti error default 404 dari Apache. (13) Untuk mengakses file assets javascript
awalnya harus menggunakan url http://pallet.kanto.yy.com/public/javascripts. Karena terlalu
panjang maka dibuatkan konfigurasi virtual host agar ketika mengakses file assets menjadi
http://pallet.kanto.yy.com/js.
Untuk web http://pewter.kanto.yy.com belum dapat dikonfigurasi pada web server karena
menunggu pengerjaan website selesai. (14) sedangkan web http://vermilion.pewter.kanto.yy.com
sudah bisa diakses hanya dengan menggunakan port 8888 karena web masih dalam tahap
perkembangan dan belum selesai. DocumentRoot web berada pada /var/www/vermilion. (15) Untuk
mengakses halaman web http://vermilion.pewter.kanto.yy.com, peneliti harus menggunakan VPN
(Virtual Private Network) yang memiliki IP 10.151.252.0/22 (Informatics Wifi, Netmask
255.255.252.0 agar web tidak mudah diserang team rocket). (16) Pada Server MOLTRES
ditambahkan konfigurasi agar bisa terhubung ke jaringan luar.
Saat trainer mengunjungi IP MEWTWO, yang muncul bukan web utama http://kanto.yy.com
melainkan laman default Apache yang bertuliskan “It works!”. (17) Karena dirasa kurang profesional,
maka setiap trainer yang mengunjungi IP MEWTWO akan dialihkan secara otomatis ke
http://kanto.yy.com.
Sekian dan Selamat mengerjakan
