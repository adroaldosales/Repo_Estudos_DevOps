## 🎯 Desafios de Containers de Banco de Dados

### Desafio 01: PostgreSQL
**Comando:**
docker run -d --name meu-postgres -e POSTGRES_DB=curso_docker -e POSTGRES_USER=docker_usr -e POSTGRES_PASSWORD=docker_pwd -p 5432:5432 postgres

### Desafio 02: MySQL
**Comando:**
docker run -d --name meu-mysql -e MYSQL_ROOT_PASSWORD=docker_pwd -e MYSQL_DATABASE=curso_docker -e MYSQL_USER=docker_usr -e MYSQL_PASSWORD=docker_pwd -p 3306:3306 mysql
