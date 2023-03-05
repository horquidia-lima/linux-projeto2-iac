# linux-projeto2-iac
Script para provisionamento de um servidor Apache


#!/bin/bash

echo " Atualizando o servidor"

apt-get update
apt-get upgrade -y
apt-get install apache2 -y
apt-get install unzip -y

echo "Baixando e copiando os arquivos da aplicacao"

cd /tmp
https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip
unzip main.zip
cd linux-sitep-dio-main
cp -R * /var/www/html/
