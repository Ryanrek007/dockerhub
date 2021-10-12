# Dockerhub
----
Kumpulan Dockerfile dari Ryan. Merupakan simple/basic package yang terdapat dalam repository / image dockerfile yang ada.


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
  
 Cek /  search di repo dockerhub: ryanrek007

----
## UPDATE
Mulai nginx-debian-webserver:1.3 telah terinstall php7.4-fpm

----

## TERIMA KASIH !!!
