# Projeto Spring Boot CRUD de Produtos

## Descrição

Projeto desenvolvido com Spring Boot para demonstrar um CRUD básico de produtos utilizando API REST.

A aplicação possui três endpoints:

* GET /products — Lista todos os produtos.
* POST /products — Cadastra um novo produto.
* DELETE /products/{id} — Remove um produto pelo ID.

O banco de dados utilizado é o H2 Database em memória.

---

## Tecnologias Utilizadas

* Java 21
* Spring Boot 4
* Spring Web
* Spring Data JPA
* H2 Database
* Maven
* VS Code (IDE)
* REST Client

---

## Pré-requisitos

Antes de executar o projeto, é necessário ter instalado:

* Java 21 ou superior
* Git

---

## Como Executar

Clone o repositório:

```bash
git clone https://github.com/HeitorCarvalhoCampos/PrimeiroProjetoFaculdade2.git
```

Acesse a pasta do projeto:

```bash
cd primeiroProjeto
```

Execute a aplicação:

### Linux/Mac

```bash
./mvnw spring-boot:run
```

### Windows

```cmd
mvnw.cmd spring-boot:run
```

A aplicação iniciará na porta:

```text
http://localhost:8080
```

---

## Testando a API

Os testes podem ser realizados utilizando o arquivo `requests.http` disponível na raiz do projeto.

### Listar Produtos

```http
GET http://localhost:8080/products
```

### Criar Produto

```http
POST http://localhost:8080/products
Content-Type: application/json

{
    "name": "Notebook"
}
```

### Remover Produto

```http
DELETE http://localhost:8080/products/1
```

---

## Estrutura do Projeto

```text
src/
├── main/
│   ├── java/com/example/demo/
│   │   ├── controller/
│   │   ├── model/
│   │   ├── repository/
│   │   ├── service/
│   │   └── DemoApplication.java
│   │
│   └── resources/
│       └── application.properties
│
└── test/
```

---

## Autor

Heitor Carvalho Campos
