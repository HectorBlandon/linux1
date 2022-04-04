

# Desarrollo de actividad 5
###### 1. Practica de scripts y procesos persistentes
###### Para la parctica, se realizará un script con una serie de comandos para la instalación de epel (paquetes par alinux empresarial), instalar e inicializar nginx; tambien se busca modificar el archivo index.html de la pagina inicial de nginx con el fin de que aparezca un mensaje y que este sea persistente (que al reiniciar el equipo, se mantenga la modificación del index.html y el servicio este arriba). 

## Comandos a ejecutar:
Para iniciar el script con nombre deploy, se ejecuta el siguiente comando, posterior a ello, se debe presionar ´´´ insert ´´´ para que permita la edición del archivo
´´´linux
vi deploy.sh
´´´

El archivo se realiza con una ´´´ function main ´´´  para indicar que funciones deben realizarse y ne que orden. Una ´´´ function deploy_nginx ´´´ que contiene los comandos de instalación e inicialización de nginx y    ´´´ function reemplazarIndex ´´´ que reemplazará el index.html del nginx por el mensaje o nombre que se indique. El codigo completo del script es el siguiente:


´´´linux
#!/bin/bash

function main {
install_epel_release -y
echo "Instalando epel .........."
}

function deploy_nginx {
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
}

function reemplazarIndex {
sudo echo "Hector Luis Blandon" > /usr/share/nginx/html/index.html
}

main
´´´
![Imagen arbol con nuevos comprimidos](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura4.png)
El comando   ´´´ sudo systemctl start nginx ´´´  permite inicializar nginx. Para comprobar que el servicio este en ejecución, se puede dirigir al navegador y escribir en la barra de busqueda, la ip del equipo o escribir ´´´  http://localhost/ ´´´ y debe mostrar la pagina index de nginx. Como en el ejercicio actual, lo que se desea es reemplazar esa pagina por un mensaje, lo que debe aparecer es el mensaje ´´´ echo "Hector Luis Blandon" ´´´ . Para asegurar que al reiniciar el equipo, se levante automaticamente el servidor y el mensaje persista, dentro del script se indico el comando  ´´´ sudo systemctl enable nginx ´´´ y con la redireccion ´´´ > ´´´ se indico que se debia reemplazar el index.html por el mensaje. EL resultado final, se puede evidenciar en la siguiente imagen.

![Imagen arbol con nuevos comprimidos](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura4.png)
