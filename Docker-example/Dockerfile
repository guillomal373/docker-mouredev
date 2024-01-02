# Slim es pq es ligero
FROM tiangolo/uvicorn-gunicorn-fastapi:python3.11-slim

# Working principal directory dentro de mi contenedor, acá se le pone app pq solo se corre una aplicación dentro de este contenedor
WORKDIR /app

# Copiar "." es llevarse absolutamente todo lo de mi equipo hacia dónde? --> /app
COPY . /app

# Instalar dependencias, etc
# Si este proyecto es de python hay un comando para generar los REQUERIMIENTOS que se usa acá "pip freeze > requirements.txt" 
RUN pip install -r requirements.txt

# Colocar variables de entorno, la variable debe quedar en el servicio donde se DESPLIEGUE
ENV MONGO_URI=$MONGO_URI

# Abrir puertos de comunicación, depende del puerto que tenga MI aplicación (Node 3000, ...)
EXPOSE 8000

# Comando para ejecutar una vez se haya levantado el contenedor 
CMD ["uvicorn", "main.app", "--reload", "--host", "0.0.0.0"]