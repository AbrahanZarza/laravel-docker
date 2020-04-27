# Laravel Docker

Docker para empezar a trabajar en un proyecto basado en Laravel de forma rápida, limpia y sencilla.

## Para empezar

Por favor, sigue las instrucciones que se detallan a continuación para que todo funcione correctamente y no te saltes 
ningún paso.

Si tienes sugerencias de mejora y crees que se puede optimizar algo en el proceso y/o código o simplemente tienes dudas, 
ponte en contacto conmigo.

### Requisitos

Para poder ejecutar el proyecto, necesitamos tener en nuestra máquina los siguientes requerimientos:

* Instalación de [Docker](https://www.docker.com/).
* Instalación de [Docker Compose](https://docs.docker.com/compose/).

### Proceso de instalación

Descargamos el proyecto en zip o por haciendo uso de git.

```
git clone https://github.com/AbrahanZarza/laravel-docker.git
```

Nos movemos hasta el directorio raíz del proyecto y una vez allí, arrancamos los servicios de docker.

```
cd your_path/laravel-docker
docker-compose up -d --build
```

Ahora, una vez montados los servicios docker, hay que generar el proyecto de laravel para poder trabajar. Para
ello vamos a ejecutar el siguiente comando.

```
docker-compose exec php-fpm composer create-project laravel/laravel .
```

Este comando ejecutará la creación de todos los ficheros necesarios para un proyecto de Laravel básico y limpio.
El código de nuestro proyecto de Laravel se generará dentro del directorio `/src`.

Una vez generado nuestro proyecto base de Laravel, ya podemos acceder a él desde el navegador web.

```
http://localhost
```

## Base de datos

Este proyecto ya crea una base de datos en el proceso de creación de los servicios de Docker.

### Conexión con laravel

Para conectar esta base de datos al nuestro proyecto de Laravel, abrimos el fichero `/src/.env` y tenemos que 
introducir los siguientes valores para configurar la conexión a la base de datos.

```
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root
```

## Construido con

* [Docker](https://www.docker.com/) - Software de contenerización.
* [Docker Compose](https://docs.docker.com/compose/) - Wrapper para Docker.
* [Composer](https://getcomposer.org/) - Sistema de gestión de paquetes
* [Laravel](https://laravel.com/) - Framework de PHP 

## Autores

* [Abrahan Zarza](https://abrahanzarza.com) - *Proyecto inicial*

## Licencia

Este proyecto está abierto al uso de cualquier desarrollador que quiera para adentrarse en el mundo de Laravel

## Conocimientos recomendados

* PHP
* Composer
* Laravel

