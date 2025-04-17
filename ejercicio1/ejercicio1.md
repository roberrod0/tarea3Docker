# Despliegue de Aplicaciones Web - Práctica entregable 3 - Ejercicio 1. Contenedores en red y Docker Desktop (resolución con Docker Desktop) - Roberto Rodríguez González

## Tabla de contenidos

1. [Previa](#1-previa)
2. [Crea una red bridge `redej1`](#2-crear-red-bridge-redej1)
3. [Crea un contendor con una imagen de mariaDB que estará en la red `redej1`. Este contenedor se ejecutará en segundo plano, y será accesible a través del puerto 3306 ](#3-crear-contenedor-mariadb)
4. [Crea un contenedor con Adminer o con phpMyAdmin que se pueda conectar al contenedor de la BD](#4-crear-contenedor-adminer-y-conectar-bd)
5. [Desde la interfaz gráfica elegida, conéctate a la BD con tu usuario personal, ejecuta el script con los datos de los módulos y muestra la BD y la tabla creados](#5-ejecutar-script-y-mostrar-bd)
6. [Instala la extensión Disk Usage y muestra el espacio ocupado, borra algo](#6-disk-usage)



## 1. Previa

Lo primero es crear el repositorio en GitHub:

![101 crear repositorio](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\101 crear repositorio.png)

Luego, crear el repositorio en local, crear carpetas y añadirlas:

![102 crear repositorio local y crear carpetas](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\102 crear repositorio local y crear carpetas.png)

Vinculamos repositorios:

![103 vincular repositorios](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\103 vincular repositorios.png)

![104 vista github](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\104 vista github.png)

Creamos la rama ejercicio1:

![105 crear rama ejercicio1](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\105 crear rama ejercicio1.png)



## 2. Crea una red brige `redej1`

Instalada la extensión PortNavigator, creamos la red bridge como se nos pide:

![106 crear red brige redej1](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\106 crear red brige redej1.png)

![107 redej1 ya creada](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\107 redej1 ya creada.png)



## 3. Crea un contenedor con una imagen de mariaDB que estará en la red `redej1`. Este contenedor se ejecutará en segundo plano, y será accesible a través del puerto 3306

Buscamos la imagen de mariaDB, la descargamos (Pull) y ejecutamos (Run):

![108 buscar la imagen mariadb](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\108 buscar la imagen mariadb.png)

La configuramos tal y como se nos pide. Los nombres de las variables los encontramos en la web https://mariadb.com/kb/en/mariadb-server-docker-official-image-environment-variables/:

![109 ajustes opcionales](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\109 ajustes opcionales.png)

El contenedor corriendo (creado en el puerto 3307 porque en el 3306 tenía mysql): 

![110 contenedor corriendo](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\110 contenedor corriendo.png)

Generamos un script SQL: 

![111 script tabla](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\111 script tabla.png)



## 4. Crea un contenedor con Adminer que se pueda conectar al contenedor de la BD

Buscamos la imagen de adminer y creamos un contenedor, de la misma forma que hicimos con la imagen de mariadb previamente:

![112 crear contenedor adminer](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\112 crear contenedor adminer.png)

Vamos a desconectar los contenedores de la red bridge que nos sale por defecto y conectarla a la que hemos creado (`redej1`):

![113 conexiones](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\113 conexiones.png)

![114 conectar a redej1](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\114 conectar a redej1.png)

![115 los dos conectados a redej1](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\115 los dos conectados a redej1.png)



## 5. Desde la interfaz gráfica elegida, conéctate a la BD con tu usuario personal, ejecuta el script con los datos de los módulos y muesta la BD y la tabla creados

Conectamos a la BD:

![116 localhost8081](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\116 localhost8081.png)

Antes de llevar a cabo nada:

![117 previo crear nada](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\117 previo crear nada.png)

Creamos la tabla en Comando SQL:

![118 crear tabla](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\118 crear tabla.png)

Estos son los datos que muestra la tabla:

![119 datos de la tabla](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\119 datos de la tabla.png)



## 6. Instala la extensión Disk Usage y muestra el espacio ocupado, borra algo
Nos decidimos por la extensión Disk Usage básicamente por ser la primera opción. La instalamos y mostramos el espacio ocupado:

![120 disk usage](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\120 disk usage.png)

Borramos un contenedor y mostramos Disk Usage después:

![121 borrar contenedor](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\121 borrar contenedor.png)

![122 tras borrar contenedor mariadb](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\122 tras borrar contenedor mariadb.png)

Ahora, tal y como se nos pide, procedemos a borrar todo:

![123 borrar todos los contenedores](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\123 borrar todos los contenedores.png)

![124 borrar red](C:\iCloudDrive\FP_DESARROLLO_WEB\24-25\DESPLIEGUE\WORKSPACE.DESPLIEGUE\Tarea 3 - Docker\repositorioTarea3Docker\ejercicio1\capturas\124 borrar red.png)

