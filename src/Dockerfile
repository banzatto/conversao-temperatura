# imagem de origem
FROM node
# Criar diretorio de trabalho
WORKDIR /app
# copia os arquivos package.json e package-lock.json para o diretorio de trabalho
COPY package*.json ./
# roda o npm install para baixar e instalar as dependencias
RUN npm install
# copia todos os arquivos do diretorio para dentro do workdir
# ignorando os arquivos listados no .dockerignore
COPY . .
# Expoe a porta 8080 do conteiner para acesso externo
EXPOSE 8080
# executa o node server.js para rodar a aplicação depois da criação do container
CMD ["node","server.js"]