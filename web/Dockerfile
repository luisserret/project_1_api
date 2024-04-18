# Utiliza una imagen base de Node.js 18
FROM node:current-alpine3.14

# Establece el directorio de trabajo en /app
WORKDIR /usr/src/app

# Copia el archivo package.json y package-lock.json a /app
COPY package.json /app

COPY . .

# Instala las dependencias utilizando npm
RUN npm set progress=false && npm install

# Expone el puerto 5173 para que sea accesible desde fuera del contenedor
EXPOSE 5173

# Establece las variables de entorno VITE_HOST y VITE_PORT
ENV VITE_HOST=0.0.0.0
ENV VITE_PORT=5173

# Inicia la aplicación con el comando predeterminado de npm start
CMD ["npm", "run","dev"]