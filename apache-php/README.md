## Aplicacion de ejemplo Compose
### Aplicacion PHP con Apache2

Estructura:
```
.
├── docker-compose.yml
├── app
    ├── Dockerfile
    └── index.php

```
[_docker-compose.yaml_](docker-compose.yaml)
```
services:
  web:
    build: app
    ports: 
      - '80:80'
    volumes:
      - ./app:/var/www/html/
```

## Desplegar con docker-compose

```
$ docker-compose up -d
Creating network "php-docker_web" with the default driver
Building web
Step 1/6 : FROM php:7.2-apache
...
...
Creating php-docker_web_1 ... done

```

## Resultados esperados

Listar los contenedores debe mostrar una salida similar a: 
```
$ docker ps
CONTAINER ID        IMAGE                        COMMAND                  CREATED             STATUS              PORTS                  NAMES
2bc8271fee81        php-docker_web               "docker-php-entrypoi…"   About a minute ago  Up About a minute   0.0.0.0:80->80/tc    php-docker_web_1
```

Luego que la aplicacion inicie, abre en un navegador la URL: `http://localhost:80` o ejecuta en un terminal:
```
$ curl localhost:80
Hello World!
```

Detener y eliminar los contenedores
```
$ docker-compose down
```