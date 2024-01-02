# Dockerfile

1. Primero se crea el dockerFile
2. requirements.txt
3. Comandos de consola

    - Crear imagen: "docker build -t nombre-imagen ."
    - Listar imágenes: "docker images"
    - Eliminar imagen: "docker rmi nombre-imagen"
    - Una vez creada la imagen ya se tiene que crear y ejecutar un contenedor,
    correr y ejecutar "docker run ..."
    detach "... -d ..." es ejecutar sin bloquear la línea de comandos
    nombrar "... --name ..."
    variables de entorno source:destiny "... -v Absolute-path.env:/app/.env ..."
    puerto de comunicación source:destiny "... -p port-number-origen:port-number-destiny ..."
    con base en qué imagen se construye este contenedor "... nombre-imagen"
    --> "docker run -d --name contenedor-ejemplo-fastapi -v E:\desarrollo_2024\docker\docker-mouredev\Docker-example\.env:/app/.env -p 8000:8000 imagen-ejemplo-fastapi"
    - Listado de contenedores: "docker ps"
    - Detener contenedor "docker stop contenedor-ejemplo-fastapi"
    - Listado contenedores que existen así no se estén ejecutando "docker ps -a"
    - Eliminar contenedor "docker rm contenedor-ejemplo-fastapi"

4. Ahora vamos a cargar a DOCKERHUB "...guillomal373/..."

    - Crear imagen: "docker build -t guillomal373/ejemplo-despliegue-fast-api:v0.1 ."
    - Subir la imagen al repositorio: "docker push guillomal373/ejemplo-despliegue-fast-api:v0.1"
    