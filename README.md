# Dockerhub
----
Kumpulan Dockerfile. Yang berisi simple/basic package yang terinstall di dalam repository / image dockerfile yang ada. <br />
visit or pull my docker repository images "**ryanrek007**" in dockerhub.


## Cara Pakai
1. `git clone https://github.com/Ryanrek007/dockerhub.git` ataupun download direktori yang dikehendaki
2.  Masuk ke dalam direktori yang dikendaki e.g: `cd build-ubuntu-apache` 
3.  jalankan syntax build image from repository, `docker build -t <tagname-repo>:<tag-version-repo>  .`
4.  images repository telah siap digunakan

### atau
1. tinggal pull dari docker hub `docker pull ryanrek007/apache-ubuntu-webserver:<tagname>`


#### NB
 - `<tagname-repo>:<tag-version-repo>` = nama dan tag-version dapat dicustomize sesuai yang diinginkan
 - `<tagname>` = harus menyesuaikan dengan docker hub yang telah diterbitkan oleh author
  
 Cek /  search di repo dockerhub: `ryanrek007`

----
## UPDATE
 - untuk `nginx-debian-webserver:1.3` telah terinstall php7.4-fpm
 - untuk `nginx-debian-webserver:1.4` ubah root directory nginx ke /var/www/html
 - jangan lupa untuk hapus `nginx.conf ` _< default > dari nginx_ pada path `/etc/nginx`, dan rename `nginx1-bak.conf` jadi `nginx.conf` pada path `/etc/nginx` agar menjadi default config untuk nginx yang terbaru pada container yang aktif
 - setelah itu jalankan syntax `service nginx restart` lalu `service php7.4-fpm start` pada container yang aktif guna untuk menjalankan service php
 - untuk `nginx-debian-webserver:1.5` tambah mounting volume log-nginx untuk dapat di monitor
 - untuk `nginx-debian-webserver:1.6` tambah PHP-Composer built on docker images.
----

## TERIMA KASIH !!!
