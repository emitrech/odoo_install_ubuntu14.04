# odoo_install_ubuntu14.04
# Instalación de Odoo 9.0 en servidor Ubuntu 14.04

# Lo primero que hago es actualizar los repositorios (servidores desde donde se descargan las aplicaciones que instalo)
# El usuario root no necesita escribir el comando "sudo".
apt-get update

# Instalo el comando "yum"
apt-get install yum
apt-get install yum-utils
yum-config-manager --enable



# Empiezo la instalación de Odoo 9.0




















wget -O - https://nightly.odoo.com/odoo.key | apt-key add -
echo "deb http://nightly.odoo.com/9.0/nightly/deb/" >> /etc/apt/sources.list

# Acá pongo otro link donde están los python para Odoo 9.0
echo "deb http://ca.archive.ubuntu.com/ubuntu/vividmain/universe" >> /etc/apt/sources.list
# Instalar el python que falla
apt-get install python-ofxparse

apt-get update && apt-get install odoo




# Primero instalo Apache2
sudo apt-get install apache2

# Instalar el comando gedit
sudo apt-get install gedit

# Para ver las líneas con error en el sources.list 
sudo -H gedit /etc/apt/sources.list

