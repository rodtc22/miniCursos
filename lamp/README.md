# Instalacion LAMP (Linux Apache Mysql Php)

```bash
sudo apt-get install aptitude
```

> Nota: ubuntu tambien tiene el servidor lighttpd, revisar


# 1. VERIFICAR LOS PAQUETES QUE TENGO INSTALADOS

```bash
dpkg --get-selections | grep "apache2"
dpkg --get-selections | grep "mysql"
dpkg --get-selections | grep "php"
```

# 2. INSTALAR APACHE2

```bash
sudo aptitude install apache2
systemctl status apache2
```
> Tambien se puede usar `service apache2 status`


# 3. INSTALAR MYSQL
Se recomienda instalarlo antes que phpmyadmin

```bash
sudo aptitude install mysql-server mysql-client
```

> El password puede ser: 123456

# 4. INSTALAR PHP

```bash
sudo aptitude install phpmyadmin
```

> Nota: Si pide seleccionar el servidor, elegir apache en lugar de Lightpd

# 5. INCLUIR PHPMYADMIN A APACHE2

```bash
cd /etc/apache2
gedit apache2.conf
```

> Al final del archiv incluir la linea
`Include /etc/phpmyadmin/apache.conf`

# 6. RESETEAMOS EL SERVIDOR

```bash
service apache2 restart
```

# 7. CREAMOS UN VIRTUAHOST

Creamos la carpeta para nuestro sitio y sus respectivos archivos en la carpeta `var/www` y le damos privilegios para ejecutar y editarlo posteriormente

```bash
cd /var/www
mkdir rodrixpage
touch rodrixpage/index.html
chmod 777 -R rodrixpage
chown -R rodrix:rodrix rodrixpage
```

Ahora si creamos los virtual host, en la carpeta de sitios disponibles del servidor de apache

```apacheconf
cd /etc/apache2/sites-available
cp 000-default.conf rodrixpage.conf
gedit rodrixpage.conf
```

Modificamos el contenido para dejarlo asi, donde nuestro virtual host escuchara en el puerto 80:

```apacheconf
<VirtualHost *:80>
	ServerAdmin webmaster@localhost
	DocumentRoot /var/www/rodrixpage
	ServerName www.rodrixpage.com
	ServerAlias rodrixpage.com
	ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

Desactivamos el sitio por defecto `000-default.conf` y activamos el nuestro `rodrixpage.conf`
```apacheconf
cd /etc/apache2/sites-enabled
a2dissite 000-default.conf
a2ensite rodrixpage.conf
service apache2 reload
```

> Podemos entrar al la pagina con la direccion **127.0.0.1** o teclando **localhost** en la URL. 

Si queremos entrar a la pagina con el nombre **rodrixpage.com**, hacemos lo siguiente:

```bash
gedit /etc/hosts
```

y modificamos el archivo, para tener

```cpp
127.0.0.1	localhost
127.0.0.1	rodrixpage
127.0.1.1	rodrix-VirtualBox

# The following lines are desirable for IPv6 capable hosts
::1     ip6-localhost ip6-loopback
fe00::0 ip6-localnet
ff00::0 ip6-mcastprefix
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
```

> Ahora podemos entrar con el nombre ***rodrixpage/***
Nota: Podemos ver que localhost tiene la misma direccion que rodrixpage, pero como lo deshabilitamos en el paso anterior, entonces nuestra pagina se encuentra disponible en esa direccion


# 8. PARA USAR VARIOS VIRTUALHOST
1. Cambiaremos la direccion IP de nuestro sitio con la **nueva direccion 127.0.0.10**

```
nano /etc/apache2/sites-available/rodrixpage.conf
```

Adentro del archivo hacemos las modificaciones para obtener:

```apacheconf
<VirtualHost 127.0.0.10>
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/rodrixpage
        ServerName www.rodrixpage.com
        ServerAlias rodrixpage.com
        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

2. Tambien modificamos en el directorio de los hosts

```
nano /etc/hosts
```

Adentro de la pagina:

```cpp
127.0.0.1       localhost
127.0.0.10      rodrixpage
127.0.0.20      siatpage        # esta es otra pagina que podria tener
127.0.1.1       rodrix-VirtualBox

# The following lines are desirable for IPv6 capable hosts
::1     ip6-localhost ip6-loopback
fe00::0 ip6-localnet
ff00::0 ip6-mcastprefix
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
```

3. Para entrar a los navegadores, siempre podemos poner las IP, pero tambien podemos poner los nombres de nuestros VirtualHosts, en nuestro caso rodrixpage, siatpage

