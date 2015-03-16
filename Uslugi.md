# Wprowadzenie #
Lista portów na jakich działają usługi
  * 10000 - webmin / https
  * 8200 - MiniDLNA
  * 8080 - qbittorrent-nox
  * 3000 - ntop
  * 8082 motion configuracja
  * 8083 motion webcam
  * 8050 OpenHab



## Samba ##
Kazdy domy serwer nie obejdzie sie bez serwera plików. A najlepiej udostepniać je za pomocą samby

instalacja jest oczywista
```
sudo apt-get install samba
```


Aby nie grzebać w plikach konfiguracje poszczególnych zasobów najlepiej zrobić za pomoca Webmin


## Webmin ##

Najszybszym sposobem zarządzania serwerem z poziomu web jest webmin

```
sudo apt-get install perl libnet-ssleay-perl openssl libauthen-pam-perl libpam-runtime libio-pty-perl apt-show-versions python

Dodajemy do  /etc/apt/sources.list  

deb http://download.webmin.com/download/repository sarge contrib
deb http://webmin.mirror.somersettechsolutions.co.uk/repository sarge contrib

dodajemy klucz
 sudo wget -O - http://www.webmin.com/jcameron-key.asc | apt-key add -

lub 

wget http://www.webmin.com/jcameron-key.asc
sudo apt-key add jcameron-key.asc

sudo apt-get update
sudo apt-get install webmin
```


## MiniDLNA ##
port
Konfiguracja tak samo prosta

```
 sudo apt-get install minidlna

plik konfiguracyjny 

sudo vim /etc/minidlna.conf

ilość plików sprawdzamy na adresie
 http://192.168.1.11:8200/

```

## Client Torrent ##
Najfajniejszym klientem jaki znalazłem z poziomu WWW jest qbittorrent-nox. Instaluje się go z repozytorium

```
sudo apt-get install qbittorrent-nox

nohup qbittorrent-nox &

```

## Motion ##
http://www.lavrsen.dk/foswiki/bin/view/Motion/WebHome

> Oprogramowanie do wykrywania ruchu i określenia akcji  na tej podstawie.


## Monitoring - ntop ##
ntop port 3000

> Monitorowanie ruchu w sieci

## OpenHAB ##
port 8050

