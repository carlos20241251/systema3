
comandos 
ip a 
sudo su
nano /etc/network/interfaces

auto ens33
iface ens33 inet static
address 192.168.##.#
netmask 255.255.255.0
dns-nameservers 8.8.8.8 8.8.4.4
sudo reboot

manera grafica
sudo
nmtui
nmcli device show 

cat /etc/resolv.conf
# systema3
