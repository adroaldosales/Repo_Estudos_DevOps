## 🎯 Desafios de Containers de Banco de Dados

### Desafio 01: PostgreSQL
**Comando:**
docker run -d --name meu-postgres -e POSTGRES_DB=curso_docker -e POSTGRES_USER=docker_usr -e POSTGRES_PASSWORD=docker_pwd -p 5432:5432 postgres

### Desafio 02: MySQL
**Comando utilizado:**
docker run -d --name meu-mysql -e MYSQL_ROOT_PASSWORD=sua_senha_root -e MYSQL_DATABASE=docker_db -e MYSQL_USER=docker_usr -e MYSQL_PASSWORD=docker_pwd -p 3306:3306 mysql

**Status:**
Validado com sucesso via `docker ps`. O container está a aceitar conexões na porta padrão 3306

### Desafio 03: MongoDB
**Comando:**
docker run -d --name meu-mongo -e MONGO_INITDB_ROOT_USERNAME=mongo_usr -e MONGO_INITDB_ROOT_PASSWORD=mongo_pwd -p 27017:27017 mongo.
