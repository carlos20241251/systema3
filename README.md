
comandos 
ip a 
sudo su
nano /etc/network/interfaces

auto ens33
iface ens33 inet static
address 192.168.##.#
netmask 255.255.255.0
dns-nameserver 8.8.8.8 8.8.4.4
sudo reboot

manera grafica
sudo
nmtui
nmcli device show 

cat /etc/resolv.conf

# Gestion de Usuario y grupos
sudo su
adduser nombre_usuario

cat /etc/passwd | grep -i nombre_usuario
usermod -aG sudo nombre_usuario

#crear grupo
addgroup nombre_groupo

#crear otro usuario para añadirlo al grupo 

#agregar usuario al grupo 
gpasswd -a nombre_usuario nombre_grupo

id


#eliminar usuario y grupo 
userdel -f nimbre_usuarioda
groupdel -f nombre_group

#verificar que estan eliminados
cat /etc/group | grep -I nombre_groupp
cat /etc/passwd | grep -I nombre_usuario
