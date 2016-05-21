# odoo_install_ubuntu14.04
# Instalación de Odoo 9.0 en servidor Ubuntu 14.04

# Lo primero que hago es actualizar los repositorios (servidores desde donde se descargan las aplicaciones que instalo)
## El usuario root no necesita escribir el comando "sudo".
apt-get update

# Después actualizo el Ubuntu
apt-get upgrade

# Empiezo la instalación de Odoo 9.0
wget -O - https://nightly.odoo.com/odoo.key | apt-key add -

echo "deb http://nightly.odoo.com/9.0/nightly/deb/" >> /etc/apt/sources.list

# Acá https://github.com/odoo/odoo/issues/798 dicen que la url correcta ahora cambió a esta: 
# deb http://nightly.openerp.com/9.0/nightly/deb/ ./ (entonces el comando correcto quedaría así):
echo "deb http://nightly.openerp.com/9.0/nightly/deb/ ./" >> /etc/apt/sources.list

# Acá pongo otro link que saqué de acá (https://www.youtube.com/watch?v=P1EpmtuIroQ&index=2&list=PLJakXodQ0d5JtGDp6qoLAe5GXSUwvbR--)
echo "deb http://ca.archive.ubuntu.com/ubuntu vividmain universe" >> /etc/apt/sources.list

apt-get update

# Instalar el paquete que falla
apt-get install python-ofxparse

https://raw.githubusercontent.com/jseutter/ofxparse/master/ofxparse/ofxparse.py






# Instalo el comando "yum"
apt-get install yum
apt-get install yum-utils
yum-config-manager --enable

# Primero instalo Apache2
sudo apt-get install apache2

# Instalar el comando gedit
sudo apt-get install gedit

# Para ver las líneas con error en el sources.list 
sudo -H gedit /etc/apt/sources.list
