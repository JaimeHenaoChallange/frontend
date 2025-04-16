# Usa una imagen base de Node.js para el frontend
FROM node:18

# Establece el directorio de trabajo
WORKDIR /app

# Copia los archivos del frontend
COPY package*.json ./
COPY . .

# Instala las dependencias
RUN npm install

# Construye la aplicación para producción
RUN npm run build

# Usa una imagen base de Nginx para servir el frontend
FROM nginx:alpine
COPY --from=0 /app/build /usr/share/nginx/html

# Expone el puerto del frontend
EXPOSE 80

# Comando para iniciar Nginx
CMD ["nginx", "-g", "daemon off;"]
