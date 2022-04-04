
# Desarrollo de actividad 4
###### 1. Practica de gestion de usuarios
###### Para la parctica, se usaran los comandos:
```linux
sudo groupadd nombreGrupo
``` 

```linux
sudo adduser nombreUsuario
``` 

```linux
sudo passwd nombreUsuario
``` 
```linux
sudo usermod -g nombreGrupo nombreUsuario
```
```linux
mkdir nombreDirectorio
``` 
######  donde :
nombreGrupo: es el nombre del grupo, que para el taller debe ser estudiante/profesor
nombreUsuario: Representa al usuario diana,laura,claudia

###### 2. Se inicia con la creación de los grupos
```linux
sudo groupadd profesor
sudo groupadd estudiante
``` 
![Imagen creacion de grupos](https://github.com/HectorBlandon/linux1/blob/c37d3cc2cf6cce3525cfc6c442ea8811d0c5b80f/Seguimiento/4/taller4Linux/captura2.png)

###### Para verificar que se hayan creado los grupos correctamente, se ejecuta el comando ``` cat /etc/group ``` 
![Imagen creacion de grupos](https://github.com/HectorBlandon/linux1/blob/c37d3cc2cf6cce3525cfc6c442ea8811d0c5b80f/Seguimiento/4/taller4Linux/captura2.png)
###### 3. Ahora, se crean los usuarios:
```linux
sudo adduser diana
sudo adduser laura
sudo adduser claudia
``` 
###### 4. se cambian o asignan las contraseñas para los usuarios creados con el comando:
```linux
sudo passwd claudia
sudo passwd laura
sudo passwd diana

``` 
![Imagen creacion de usuarios](https://github.com/HectorBlandon/linux1/blob/c37d3cc2cf6cce3525cfc6c442ea8811d0c5b80f/Seguimiento/4/taller4Linux/captura4.png)
![Imagen creacion de usuarios](https://github.com/HectorBlandon/linux1/blob/c37d3cc2cf6cce3525cfc6c442ea8811d0c5b80f/Seguimiento/4/taller4Linux/captura5.png)
###### 5. Se asignan los usuarios creados a los grupos pertenecientes como indica la guia del taller:
"Conociendo que: diana es un profesor; laura es una estudiante y
claudia es un profesor y un estudiante.
Adicione todos los usuarios a los grupos correspondientes."

###### 6. Se agregan los usuarios a los grupos profesor o estudiante
```linux
sudo usermod -G profesor claudia
sudo usermod  -g estudiante laura
sudo usermod  -gprofesor  diana
sudo usermod  -g estudiante claudia
``` 
###### Para validar que hayan sido asignados correctamente, se pueden evidenciar los grupos a los que pertenece un usuario con el comando ``` groups laura ``` , ``` groups diana ``` , ``` groups claudia ```
![Imagen agregar usuarios a grupos](https://github.com/HectorBlandon/linux1/blob/c37d3cc2cf6cce3525cfc6c442ea8811d0c5b80f/Seguimiento/4/taller4Linux/captura6.png)
