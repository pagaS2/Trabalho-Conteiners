# 🐳 Inicialização de Banco de Dados PostgreSQL com Docker no Windows

Este projeto demonstra o processo de criação e execução de um contêiner Docker com PostgreSQL em um ambiente Windows, utilizando o terminal (CMD). Ideal para quem deseja configurar um banco de dados local de forma rápida e prática usando Docker.

---

## 📄 Descrição

O objetivo deste projeto é apresentar um ambiente de banco de dados PostgreSQL configurado via Docker no Windows. A configuração é feita diretamente pelo terminal (CMD), desde o download da imagem até a criação do contêiner com persistência de dados e exposição da porta padrão do PostgreSQL.

---

## 🚀 Tecnologias Utilizadas

- **MySQL** – Sistema gerenciador de banco de dados relacional.
- **Docker** – Plataforma para criação e gerenciamento de contêineres.
- **CMD (Prompt de Comando)** – Interface de linha de comando do Windows utilizada para executar os comandos.

---

## ⚙️ Funcionalidades

- Baixar a imagem oficial do PostgreSQL via Docker Hub.
- Criar e executar um contêiner com PostgreSQL.
- Configurar senha de acesso ao banco de dados.
- Persistência de dados com volume nomeado.
- Exposição da porta 5432 para acesso externo.

---

## 🧰 Comandos Utilizados

```bash
# 1. Baixar a imagem do PostgreSQL
docker pull postgres

# 2. Verificar se a imagem foi baixada com sucesso
docker images

# 3. Criar e executar o contêiner
docker run --name trabalho ^
  -e POSTGRES_PASSWORD=1302 ^
  -v trabalho:/var/lib/postgresql/data ^
  -p 5432:5432 ^
  -d postgres
