FROM node:18.11.0
#MKDIR e CD
WORKDIR /app
#Copiar as dependenciar pro diretório corrente e instalar
COPY package*.json ./
RUN npm install
#Copiar o projeto pro diretório corrente
COPY . .
#Expor a porta do container
EXPOSE 8080
#Iniciar o node
CMD ["node", "server.js"]
