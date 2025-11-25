

### Instalación Wordpress.org en un servidor Ubuntu 24.04

```bash
cd /tmp
wget https://wordpress.org/latest.tar.gz
tar -xzvf latest.tar.gz
sudo mv wordpress /var/www/html/
```

Creacion de la base de datos
CREATE DATABASE wordpress_db;
CREATE USER 'wpuser'@'192.168.0.22' IDENTIFIED BY 'paso'
GRANT ALL PRIVILEGES ON wordpress_db.* TO 'wpuser'@'192.168.0.22';
FLUSH PRIVILEGES;
EXIT;

Configurar permisos 
```bash
sudo chown -R www-data:www-data /var/www/html/wordpress
sudo chmod -R 755 /var/www/html/wordpress
```

Configurar apache para wordpress
```bash
sudo nano /etc/apache2/sites-available/wordpress.conf
```

Se configura Apache
```bash
<VirtualHost *:80>
    ServerName localhost
    DocumentRoot /var/www/html/wordpress
    <Directory /var/www/html/wordpress>
        AllowOverride All
    </Directory>
</VirtualHost>
```

SE activa el sitio y modulo
```bash
sudo a2ensite wordpress.conf
sudo a2enmod rewrite
sudo systemctl restart apache2
```

Y se instala Wordpress
Abrir en el navegador : http://192.168.0.22/wordpress/
y seguir los pasos...

Elegir el idioma y dar a continuar

![alt text](images/idioma.png)

Aparece un mensaje con la información a tener a mano antes de seguir.  
![alt text](images/mensajeInfo.png)

Se indica la informacion sobre la base de datos  
![alt text](images/infoBD.png) 

Sale un mensaje para informar que la conexion con la base de datos es correcta. Hacer clic en Realizar la instalación.
![alt text](images/mensajeBDOK.png)  

Rellenar el formulario de instalación con los datos de usuario.  
![alt text](images/formInstalacion.png)

y sale un mensaje de confimración y se hace clic en acceder.
![alt text](images/mensajeConfirmacion.png)

aparece un formulario para pedir las credenciales  
![alt text](images/formCredenciales.png)