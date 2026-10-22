# Imagen base liviana de Node.js
FROM node:18-alpine

# Directorio de trabajo en el contenedor
WORKDIR /usr/src/app

# Copiar archivos de gestión de dependencias
COPY package*.json ./

# Instalación limpia de dependencias
RUN npm ci --only=production

# Copiar el resto del código del microservicio
COPY . .

# Exponer el puerto de ms.menu
EXPOSE 3002

# Comando para iniciar la aplicación
CMD ["node", "src/app.js"]