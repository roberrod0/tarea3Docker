# Despliegue de Aplicaciones Web - Práctica entregable 3 - Ejercicio 3. Imagen con Dockerfile - Roberto Rodríguez González

## Tabla de contenidos

1. [Previa](#1-previa)
2. [Crear archivos css, html y php](#2-crear-css-html-php)
3. [Crear Dockerfile](#3-crear-dockerfile)
4. [Crear la imagen automatizada](#4-crear-imagen-automatizada)
5. [Subir la imagen a Docker Hub](#5-subir-image-docker-hub)
6. [Borrar la imagen local](#6-borrar-imagen-local)
7. [Bajar (pull) la imagen](#8-bajar-imagen)
8. [Crear un nuevo contenedor y ejecutar desde otro puerto](#9-crear-nuevo-contenedor)



## 1. Previa

Antes de pasar al ejercicio 3 tenemos que cerrar el ejercicio 2:

![301 status ejercicio2](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\301 status ejercicio2.png)

![302 añadimos cambios](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\302 añadimos cambios.png)

Ahora subimos al remoto los cambios:

![303 subir al remoto](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\303 subir al remoto.png)

Y creamos la rama ejercicio3:

![304 crear rama ejercicio3](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\304 crear rama ejercicio3.png)

## 2. Crear archivos css, html y php

Creamos un html y un css sencillos. El contenido del php nos viene dado:

![305 html](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\305 html.png)

![307 php](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\307 php.png)

![306 css](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\306 css.png)

![308 los tres dentro del directorio](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\308 los tres dentro del directorio.png)

## 3. Crear Dockerfile

Creamos el Dockerfile de la forma más sencilla:

![309 el dockerfile](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\309 el dockerfile.png)

## 4. Crear la imagen automatizada

Ahora, creamos la imagen automatizada a partir de nuestro Dockerfile:

![310 crear la imagen automatizada](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\310 crear la imagen automatizada.png)

Comprobamos que aparece entre las imágenes en local:

![311 la imagen creada](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\311 la imagen creada.png)

Creamos un contenedor para probar que corre correctamente:

![312 crear contenedor](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\312 crear contenedor.png)

![313 contenedor corriendo](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\313 contenedor corriendo.png)

## 5. Subir la imagen a Docker Hub

Hacemos login en Docker Hub:

![314 login en docker hub](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\314 login en docker hub.png)

Subimos la imagen creada:

![315 subir la imagen creada](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\315 subir la imagen creada.png)

Comprobamos desde Docker Hub:

![316 vista desde docker hub](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\316 vista desde docker hub.png)

## 6. Borrar la imagen local

Borramos la imagen local y el contenedor creado previamente:

![317 borrar la imagen del local](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\317 borrar la imagen del local.png)

Comprobamos que ya no aparezca:

![318 listar imagenes](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\318 listar imagenes.png)

## 7. Bajar (pull) la imagen

Hacemos pull para tener la imagen en local y listamos las imágenes:

![319 pull y listado](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\319 pull y listado.png)

## 8. Crear un nuevo contenedor y ejecutar desde otro puerto

Creamos un nuevo contenedor que se ejecutará desde el puerto 1234:80:

![320 ejecutar en 1234](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\320 ejecutar en 1234.png)

Comprobamos que funcione:

![321 html](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\321 html.png)

![322 php](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio3\capturas\322 php.png)

