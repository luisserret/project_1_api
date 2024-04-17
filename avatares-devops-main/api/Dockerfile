# Utilizamos la imagen oficial de Python 3.10
FROM python:3.10

# Establecemos el directorio de trabajo en /app
WORKDIR /app

# Copiamos los archivos necesarios al contenedor
COPY . /app

# Instalamos las dependencias de la aplicación
RUN pip install -r /app/requirements.txt

# Definimos las variables de entorno necesarias para Flask
ENV FLASK_APP=api/app.py
ENV FLASK_ENV=development

# Exponemos el puerto 5000 para que Flask pueda ser accedido desde fuera del contenedor
EXPOSE 5000

# Comando para ejecutar la aplicación Flask
CMD ["flask", "run", "--host=0.0.0.0"]
