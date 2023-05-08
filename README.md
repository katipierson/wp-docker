# Docker-Entwicklungsumgebung für Wordpress mit NGINX und APACHE

* Nicht gleichzeitig starten!

## Versionsstand am 13.01.2023

* Nginx 1.23.x
* Apache 2.4.x
* PHP-FPM 7.4.x
* PHP 8.2.x
* MariaDB 11.1.x

## Apache
### LAMP
#### 7.4
* Apache
* PHP 7.4.x - Dockerfile
* MariaDB
#### 8.0 - 8.2
* Apache
* PHP 8.x - latest
* MariaDB

## Nginx
### LEMP
#### 7.4
* Nginx
* PHP 7.4.x - Dockerfile
* MariaDB
#### 8.2
* Nginx
* PHP 8.x - latest
* MariaDB

## Struktur
* in LEMP & LAMP sind die Konfigurationen
* Apache-Verzeichnis ist für alle Apache-Stacks gleich
* Nginx-Verzeichnis ist für alle Nginx-Stacks gleich
* MySQL-Verzeichnis ist für alle Stacks gleich
* PHP-Verzeichnis enthält für PHP 7.4 latest
* PHP8-Verzeichnis enthält PHP 8.x latest
* Jeder Ordner enthält eine Environment-Datei (.env) mit der mySQL-Plattform

## Apache-Hosts
* apache/conf/sites-available
* pro Host eine Datei

## Nginx-Hosts
* nginx/conf/sites-available
* pro Host eine Datei