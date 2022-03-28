
# Desarrollo de actividad 3
###### 1. Practica de comprimir y descomprimir  archivos o directorios
###### Para la parctica, se usaran los comandos:
## ``` tar -cvf nombreDirectorio.tar /ruta ``` para comprimir un directorio 
###### Donde:
###### -c  se usa para indicar que se debe crear un nuevo archivo
###### v  PAra observar el comportamiento mediante verbose,logs
###### f indica que el siguiente dato es el nombre del comprimido
###### x Se usa para descomprimir un archivo
###### -C Se usa para especificar la ruta donde se desea agregar el comprimido  (Recordar que la C es mayuscula)

## ``` tar -xvf nombreDirectorio.tar /ruta ``` para descomprimir un directorio

## ``` tar -cvf nombreDirectorio1 nombreDirectorio2 nombreDirectorio3 /ruta ``` para comprimir mulriples  directorios en un solo comprimido
1. Comprimir directorios bisabuela y bisabuelo del taller anterior con tar; para ello se debe dirigir al directorio en el que se encuentran los directorios bisabuelo y bisabuela que para el ejemplo es el directorio taller1. ``` cd /home/hector/Documentos/taller1 ```

###### Para comprimir los directorios con tar ejecutamos el comando ``` tar -cvf bisabuela.tar . ```  y ``` tar -cvf bisabuelo.tar . ``` como se observa en la siguiente figura

![Imagen comando bisabuela.tar](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura1.png)

Se observa que para la imagen anterior, se indico despues del tar un **.** y esto indica la ruta actual (la ruta es la misma donde se esta ejecutando el comando)

![Imagen comando bisabuelo.tar](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura2.png)

2. Comprimir directorios bisabuela y bisabuelo del taller anterior con tar.gz ; para ello se debe dirigir al directorio en el que se encuentran los directorios bisabuelo y bisabuela que para el ejemplo es el directorio taller1. ``` cd /home/hector/Documentos/taller1 ```

###### Para comprimir los directorios con tar ejecutamos el comando ``` tar -cvf bisabuela.tar.gz . ```  y ``` tar -cvf bisabuelo.tar.gz . ``` como se observa en la siguiente figura

![Imagen comando tar.gz](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura3.png)

una vez comprimidos los directorios, se ejecuta el comando ``` tree ``` para visualizar la creación de los nuevos comprimidos

![Imagen arbol con nuevos comprimidos](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura4.png)

3. Descomprimir los archivos creados, pero en rutas especificas como: /tmp y /root

Para ello se debe ejecutar el comando   ``` sudo tar -xvf bisabuela.tar -C /tmp ``` y  ``` sudo tar -xvf bisabuelo.tar -C /tmp ```. Se debe ejecutar el comando con sudo para dar permisos ya que no es una carpeta de usuario, sino de root. Se realiza el comando acompañado de -C para indicar o especificar la ruta donde se descomprimirá el comprmido

![Imagen descomprimir bisabuela.tar en /tmp](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura5.png)

Ahora se debe ejecutar el comando   ``` sudo tar -xvf bisabuela.tar -C /root ``` y  ``` sudo tar -xvf bisabuelo.tar -C /root ```. Se debe ejecutar el comando con sudo para dar permisos ya que no es una carpeta de usuario, sino de root. Se realiza el comando acompañado de -C para indicar o especificar la ruta donde se descomprimirá el comprmido

![Imagen descomprimir bisabuela.tar en /root](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura6.png)

4. Descomprmir el archivo bisabuelo.tar.gz y bisabuela.tar.gz en los directorios /tmp y /root 
 Para ello se debe ejecutar el comando   ``` sudo tar -xvf bisabuela.tar.gz -C /tmp ``` y  ``` sudo tar -xvf bisabuela.tar.gz -C /root ```. Se debe ejecutar el comando con sudo para dar permisos ya que no es una carpeta de usuario, sino de root. Se realiza el comando acompañado de -C para indicar o especificar la ruta donde se descomprimirá el comprmido. Lo mismo se hace para descomprimir bisabuelo.tar.gz en los mismos directorios

![Imagen descomprimir bisabuela.tar en /root](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura7.png)

para confirmar que se hallan creado los archivos descomprimidos, se ejecuta el comando ``` ls ``` como se observa en la siguiente figura.

![Imagen descomprimidos bisabuela.tar en /root](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura7.png)

5. Comprimir los directorios bisabuelo y bisabuela con .zip 

Se comprime en formato .zip con el comando ``` zip bisabuelo .``` y ``` zip bisabuela .```

6. Se procede a ejecutar el comando ``` ls ``` para validar la creación de los comprmidos con .zip
7. Para visualizar que se descompriman los archivos .zip recien creados, se crea un directorio vacio llamado descomprimidos_zip con el comando ``` mkdir descomprimidos_zip ```
8. Se descomprmimen los nuevos archivos bisabuela.zip y bisabuelo.zip  en el directorio descomprimidos_zip con ayuda del comando ``` zip bisabuelo /descomprimidos_zip``` para indicar la ruta donde se desea descomprmir

![Imagen descomprimidos bisabuela.zip en /descomprmidos_zip](https://github.com/HectorBlandon/linux1/blob/b0cafcb614c05bf2ff65bc80ff019347d810d315/Seguimiento/3/taller3/captura9.png)
