# Despliegue de Aplicaciones Web - Práctica entregable 3 - Ejercicio 2. Docker Compose - Roberto Rodríguez González

## Tabla de contenidos

1. [Previa](#1-previa)
2. [Escribir un fichero `compose.yaml`](#2-escribir-fichero-compose)
3. [Desplegar FileBrowser](#3-desplegar-filebrowser)
4. [Carpetas y volúmenes creados](#4-carpetas-y-volúmenes-creados)
5. [Subida de un fichero y cambio de lenguaje de la aplicación](#5-subida-de-ficher-y-cambio-de-lenguaje)
6. [FileBrowser](#6-qué-hace-filebrowser)



## 1. Previa

Antes de pasar al ejercicio 2 tenemos que cerrar el ejercicio 1:

![201 guardado ejercicio1](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\201 guardado ejercicio1.png)

Ahora subimos al remoto los cambios:

![202 subimos los cambios al remoto](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\202 subimos los cambios al remoto.png)

Y creamos la rama ejercicio2:

![203 comenzar ejercicio2](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\203 comenzar ejercicio2.png)

## 2. Escribir un fichero `compose.yaml`

A partir del `yaml` que aparece en https://hub.docker.com/r/hurlenko/filebrowser creamos nuestro `compose.yaml`: 

![204 compose](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\204 compose.png)

## 3. Desplegar FileBrowser

Para desplegar la aplicación:

![205 docker compose up](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\205 docker compose up.png)

![206 filebrowser tirando](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\206 filebrowser tirando.png)

Y desde Docker Desktop podemos ver el contenedor corriendo:

![207 contenedor filebrowser](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\207 contenedor filebrowser.png)

Como no añadimos la opción `container_name` dentro del `yaml`, el contenedor coge el nombre de la carpeta donde está el `yaml` como nombre del proyecto. Pero podemos ver que sí que filebrowser es el nombre del servicio, que sí definí dentro del `yaml`.

Abrimos desde el navegador:

![208 filebrowser corriendo](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\208 filebrowser corriendo.png)

Antes de añadir nada:

![209 filebrowser vacio](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\209 filebrowser vacio.png)



## 4. Carpetas volúmenes creados

Vemos los volúmenes creados desde cmd:

<img src="C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\210 volumenes creados.png" alt="210 volumenes creados" style="zoom:75%;" />

Y desde Docker Desktop:

![211 volumenes creados desde docker](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\211 volumenes creados desde docker.png)



## 5. Subida de un fichero y cambio de lenguaje de la aplicación

Añadimos una carpeta, subimos el enunciado de la tarea y cambiamos el idioma de la aplicación:

![212 subido archivo, creada carpeta y cambiado idioma](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio2\capturas\212 subido archivo, creada carpeta y cambiado idioma.png)

## 6. FileBrowser

- FileBrowser es una aplicación de gestión de archivos y directorios desde un navegador web. 

- Permite gestionar, visualizar y compartir archivos desde cualquier navegador. 

- Es ligera y muy rápida. 

- Es totalmente gratis y de código abierto. 
- Permite el acceso a varios usuarios a los archivos, pudiendo diferenciar entre usuarios y administradores.