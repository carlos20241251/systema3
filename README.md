## Configuración de parametros de red.
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

## Gestion de Usuario y grupos
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

## Gestion de Permisos de archivos
Crear carpeta y archivo
mkdir materia
cd materia
touch estudiantes.txt

Editar archivo con vi
vi estudiantes.txt


i = modo inserción

Escribir: nombre y matrícula

Esc = salir de inserción

:wq = guardar y salir

Ver contenido del archivo
cat estudiantes.txt

Volver al directorio anterior
cd ..

Permisos: solo el propietario con control total
chmod 700 materia/estudiantes.txt

Verificar permisos
cd materia
ls -l
cd ..

Permisos: solo el grupo con control total
chmod 070 materia/estudiantes.txt

Crear segunda carpeta y copiar archivo
mkdir materia2
cp materia/estudiantes.txt materia2/

Verificar copia
cd materia2
ls
cat estudiantes.txt
cd ..

Eliminar carpeta materia con su contenido
rm -rf materia
ls

Eliminar carpeta materia2
rm -rf materia2
ls


#eliminar usuario y grupo 
userdel -f nimbre_usuarioda
groupdel -f nombre_group

#verificar que estan eliminados
cat /etc/group | grep -I nombre_groupp
cat /etc/passwd | grep -I nombre_usuario
