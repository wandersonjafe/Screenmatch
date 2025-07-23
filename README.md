# 🎬 ScreenMatch

O **ScreenMatch** é um sistema em Java desenvolvido com **Spring Boot** que permite o cadastro, consulta e listagem de filmes e séries, com integração opcional à **OMDb API** (The Open Movie Database).  
Ideal para explorar, organizar e consultar informações do mundo do entretenimento via console.

---

## ✨ Funcionalidades

- ✅ Cadastro de títulos (filmes/séries) manualmente
- ✅ Consulta de dados detalhados de filmes por nome usando API externa
- ✅ Listagem geral de títulos cadastrados
- ✅ Filtragem por avaliação
- ✅ Menu interativo via terminal/console

---

## 🛠 Tecnologias utilizadas

- **Java 17+**
- **Spring Boot**
- **Spring Data JPA**
- **PostgreSQL** ou **H2 Database** (para testes)
- **OMDb API**
- **Gson / OkHttp / RestTemplate**
- **Maven**

---


## 🚀 Como executar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/screenmatch.git
cd screenmatch

# Configuração do banco de dados
spring.datasource.url=jdbc:postgresql://localhost:5432/screenmatch
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

# Chave da OMDb API
omdb.api.key=SUA_CHAVE_AQUI

💡 Você também pode usar H2 para testes locais:

spring.datasource.url=jdbc:h2:mem:screenmatchdb
spring.datasource.driver-class-name=org.h2.Driver
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect

3. Crie o banco no PostgreSQL

sql

CREATE DATABASE screenmatch;

4. Execute a aplicação
No terminal ou IntelliJ:

bash

./mvnw spring-boot:run

💡 Exemplo do Menu via Console

***** ScreenMatch - Catálogo de Filmes *****

1 - Cadastrar título manualmente
2 - Buscar título por nome (OMDb)
3 - Listar todos os títulos
4 - Filtrar por avaliação
0 - Sair

🔌 Integração com OMDb API
A OMDb API permite a busca de informações reais de filmes/séries diretamente de uma fonte pública confiável.

Como obter uma chave da OMDb:
Acesse: https://www.omdbapi.com/apikey.aspx

Cadastre-se com seu e-mail

Receba sua chave por e-mail

Adicione no application.properties:

omdb.api.key=SUA_CHAVE_AQUI

---
