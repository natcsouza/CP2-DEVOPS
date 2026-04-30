# CP2 - Docker DimDim

## Descrição
Projeto desenvolvido para demonstrar a utilização de containers Docker com comunicação entre aplicação e banco de dados.

## Tecnologias
- Docker
- MySQL
- Adminer

## Como executar

### 1. Criar rede
docker network create dimdim-network

### 2. Subir banco MySQL
docker run -d --name mysql-dimdim --network dimdim-network -e MYSQL_ROOT_PASSWORD=1234 -e MYSQL_DATABASE=dimdim -v mysql-data:/var/lib/mysql -p 3306:3306 mysql:5.7

### 3. Subir Adminer
docker run -d --name adminer-dimdim --network dimdim-network -p 8081:8080 adminer

### 4. Acessar
http://localhost:8081

## Acesso
- Servidor: mysql-dimdim
- Usuário: root
- Senha: 1234
- Banco: dimdim