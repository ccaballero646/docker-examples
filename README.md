# Ejemplos de Docker y docker-compose

Estos ejemplos proporcionan un punto de inicio para integrar diferentes servicios construidos usando Docker y orquestados utilizando docker-compose.

# Introduccion
Con estas instrucciones podremos crear y desplegar ejemplos de aplicaciones en contenedores con docker-compose.

## Prerequisitos
* Asegurate de tener instalado docker y docker-compose
  * Windows y MacOS: [Instalar Docker Desktop](https://www.docker.com/get-started)
  * Linux: [Instala Docker](https://www.docker.com/get-started) y luego [Docker Compose](https://github.com/docker/compose)
* Descarga los ejemplos que te interesen de este repositorio

## Ejecutando un ejemplo
El directorio raiz de cada ejemplo contiene un archivo `docker-compose.yml` que describe los servicios y sus requerimientos. Todos estos ejemplos pueden ejecutarse de forma local entrando en el directorio raiz de cada ejemplo y ejecutando el comando:
```
docker-compose up -d
```
Dentro de cada ejemplo, el archivo `README.md` tendra mas detalles sobre su estructura.

Para eliminar todo lo creado para cada entorno, ejecutamos el comando:
```
docker-compose down
```

