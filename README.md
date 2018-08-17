# Docker Compose para desarrollo con PHP
Este ejemplo, permite levantar una bateria se servidores Docker's para el desarrollo de APP'S en PHP.

Instancias Docker:
+ Nginx
+ PHP
+ MYSQL
+ PHP MyAdmin

#### Detalle de Contenido:
> + **Mysql** \
> Dockerfile con version 5.7 de mysql, que soporta las configuraciones de coenxión de las aplicaciones de este ejemplo.
> + **Nginx** \
> Sites Available | Ejemplos de configuraciones *.conf de App PHP y Framework Codeigniter PHP, para que Nginx publique en algún puerto la App.
> + **PhP** \
> Dockerfile con actualización de sistema y complementos para conexión con Mysql.
> + **Project** \
> Este direcotorio, contienen 2 proyectos pre-configurados con mi servidor Nginx(*.conf), para su ejecución directa al levantar con `up`.
>   - _php-app_ Aplicación pura PhP, en este caso es un único archivo, con la ipresión de los modulos y la info de mi instalación PHP.
>   - _codeigniter-php-app_ App para descarga de Framework Codeigniter y ejecución

#### Clonación de proyecto Codeigniter
El proyecto debe ser clonado en la carpeta _codeigniter-php-app_
```sh
git clone https://github.com/bcit-ci/CodeIgniter.git projects/codeigniter-php-app
```

### Ejecución del Compose
Construcción de las imágenes Docker
```sh
docker-compose build
docker-compose up -d
#Si no funciona Correctamente PHP MyAdmin, debemos reiniciar El Docker
docker-compose restart phpmyadmin
```

Referencias:
- [Example Docker Compose](https://gist.github.com/michaelneu/2ca7987ef00fa3fbe4fd7b9c07834cc7)
- [Example Docker Compose](https://gist.github.com/jcavat/2ed51c6371b9b488d6a940ba1049189b)
