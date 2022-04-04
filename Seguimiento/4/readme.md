
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
###### 5. Se asignan los usuarios creados a los grupos pertenecientes como indica la guia del taller:
"Conociendo que: diana es un profesor; laura es una estudiante y
claudia es un profesor y un estudiante.
Adicione todos los usuarios a los grupos correspondientes."
