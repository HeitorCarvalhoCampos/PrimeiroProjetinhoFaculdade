# Projeto Spring Boot CRUD de Produtos

## Descrição

Projeto desenvolvido com Spring Boot para demonstrar um CRUD básico de produtos utilizando API REST.

A aplicação possui três endpoints:

- **GET /products** — Lista todos os produtos.
- **POST /products** — Cadastra um novo produto.
- **DELETE /products/{id}** — Remove um produto pelo ID.

O banco de dados utilizado é o **H2 Database em memória**.

---

## Tecnologias Utilizadas

- Java 21
- Spring Boot 4
- Spring Web
- Spring Data JPA
- H2 Database
- Maven
- VS Code (IDE)
- REST Client

---

## Pré-requisitos

Antes de executar o projeto, é necessário ter instalado:

- Java 21
- Git

---

## Como Executar

Clone o repositório:

```bash
git clone https://github.com/HeitorCarvalhoCampos/PrimeiroProjetoFaculdade2.git
```

Acesse a pasta do projeto:

```bash
cd PrimeiroProjetoFaculdade2
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

Quando a aplicação estiver pronta para uso, será exibida uma mensagem semelhante a:

```text
Started DemoApplication
```

---

## Testando a API

Os testes podem ser realizados utilizando o arquivo `requests.http` disponível na raiz do projeto.

Para executar as requisições pelo VS Code:

1. Instale a extensão **REST Client**.
2. Abra o arquivo `requests.http`.
3. Clique em **Send Request** acima da requisição desejada.

### Fluxo recomendado de testes

#### 1. Listar produtos

```http
GET http://localhost:8080/products
```

Resposta esperada:

```json
[]
```

---

#### 2. Criar produto

```http
POST http://localhost:8080/products
Content-Type: application/json

{
    "name": "Notebook"
}
```

Resposta esperada:

```json
{
  "id": 1,
  "name": "Notebook"
}
```

---

#### 3. Listar produtos novamente

```http
GET http://localhost:8080/products
```

Resposta esperada:

```json
[
  {
    "id": 1,
    "name": "Notebook"
  }
]
```

---

#### 4. Remover produto

```http
DELETE http://localhost:8080/products/1
```

---

#### 5. Confirmar remoção

```http
GET http://localhost:8080/products
```

Resposta esperada:

```json
[]
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
