# Despliegue de Aplicaciones Web - Práctica entregable 3 - Ejercicio 1. Contenedores en red y Docker Desktop (resolución con Docker Desktop) - Roberto Rodríguez González

## Tabla de contenidos

- [Despliegue de Aplicaciones Web - Práctica entregable 3 - Ejercicio 1. Contenedores en red y Docker Desktop (resolución con Docker Desktop) - Roberto Rodríguez González](#despliegue-de-aplicaciones-web---práctica-entregable-3---ejercicio-1-contenedores-en-red-y-docker-desktop-resolución-con-docker-desktop---roberto-rodríguez-gonzález)
  - [Tabla de contenidos](#tabla-de-contenidos)
  - [1. Previa](#1-previa)
  - [2. Crea una red brige `redej1`](#2-crea-una-red-brige-redej1)
  - [3. Crea un contenedor con una imagen de mariaDB que estará en la red `redej1`. Este contenedor se ejecutará en segundo plano, y será accesible a través del puerto 3306](#3-crea-un-contenedor-con-una-imagen-de-mariadb-que-estará-en-la-red-redej1-este-contenedor-se-ejecutará-en-segundo-plano-y-será-accesible-a-través-del-puerto-3306)
  - [4. Crea un contenedor con Adminer que se pueda conectar al contenedor de la BD](#4-crea-un-contenedor-con-adminer-que-se-pueda-conectar-al-contenedor-de-la-bd)
  - [5. Desde la interfaz gráfica elegida, conéctate a la BD con tu usuario personal, ejecuta el script con los datos de los módulos y muesta la BD y la tabla creados](#5-desde-la-interfaz-gráfica-elegida-conéctate-a-la-bd-con-tu-usuario-personal-ejecuta-el-script-con-los-datos-de-los-módulos-y-muesta-la-bd-y-la-tabla-creados)
  - [6. Instala la extensión Disk Usage y muestra el espacio ocupado, borra algo](#6-instala-la-extensión-disk-usage-y-muestra-el-espacio-ocupado-borra-algo)



## 1. Previa

Lo primero es crear el repositorio en GitHub:

![101 crear repositorio](.\capturas\101 crear repositorio.png)

Luego, crear el repositorio en local, crear carpetas y añadirlas:

![102 crear repositorio local y crear carpetas](.\capturas\102 crear repositorio local y crear carpetas.png)

Vinculamos repositorios:

![103 vincular repositorios](.\capturas\103 vincular repositorios.png)

![104 vista github](.\capturas\104 vista github.png)

Creamos la rama ejercicio1:

![105 crear rama ejercicio1](.\capturas\105 crear rama ejercicio1.png)



## 2. Crea una red brige `redej1`

Instalada la extensión PortNavigator, creamos la red bridge como se nos pide:

![106 crear red brige redej1](.\capturas\106 crear red brige redej1.png)

![107 redej1 ya creada](.\capturas\107 redej1 ya creada.png)



## 3. Crea un contenedor con una imagen de mariaDB que estará en la red `redej1`. Este contenedor se ejecutará en segundo plano, y será accesible a través del puerto 3306

Buscamos la imagen de mariaDB, la descargamos (Pull) y ejecutamos (Run):

![108 buscar la imagen mariadb](.\capturas\108 buscar la imagen mariadb.png)

La configuramos tal y como se nos pide. Los nombres de las variables los encontramos en la web https://mariadb.com/kb/en/mariadb-server-docker-official-image-environment-variables/:

![109 ajustes opcionales](.\capturas\109 ajustes opcionales.png)

El contenedor corriendo (creado en el puerto 3307 porque en el 3306 tenía mysql): 

![110 contenedor corriendo](.\capturas\110 contenedor corriendo.png)

Generamos un script SQL: 

![111 script tabla](.\capturas\111 script tabla.png)



## 4. Crea un contenedor con Adminer que se pueda conectar al contenedor de la BD

Buscamos la imagen de adminer y creamos un contenedor, de la misma forma que hicimos con la imagen de mariadb previamente:

![112 crear contenedor adminer](.\capturas\112 crear contenedor adminer.png)

Vamos a desconectar los contenedores de la red bridge que nos sale por defecto y conectarla a la que hemos creado (`redej1`):

![113 conexiones](.\capturas\113 conexiones.png)

![114 conectar a redej1](.\capturas\114 conectar a redej1.png)

![115 los dos conectados a redej1](.\capturas\115 los dos conectados a redej1.png)



## 5. Desde la interfaz gráfica elegida, conéctate a la BD con tu usuario personal, ejecuta el script con los datos de los módulos y muesta la BD y la tabla creados

Conectamos a la BD:

![116 localhost8081](.\capturas\116 localhost8081.png)

Antes de llevar a cabo nada:

![117 previo crear nada](.\capturas\117 previo crear nada.png)

Creamos la tabla en Comando SQL:

![118 crear tabla](.\capturas\118 crear tabla.png)

Estos son los datos que muestra la tabla:

![119 datos de la tabla](.\capturas\119 datos de la tabla.png)



## 6. Instala la extensión Disk Usage y muestra el espacio ocupado, borra algo
Nos decidimos por la extensión Disk Usage básicamente por ser la primera opción. La instalamos y mostramos el espacio ocupado:

![120 disk usage](.\capturas\120 disk usage.png)

Borramos un contenedor y mostramos Disk Usage después:

![121 borrar contenedor](.\capturas\121 borrar contenedor.png)

![122 tras borrar contenedor mariadb](.\capturas\122 tras borrar contenedor mariadb.png)

Ahora, tal y como se nos pide, procedemos a borrar todo:

![123 borrar todos los contenedores](.\capturas\123 borrar todos los contenedores.png)

![124 borrar red](.\capturas\124 borrar red.png)

