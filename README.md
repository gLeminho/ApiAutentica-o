# 🔐 Projeto AuthServer - API de Autenticação com JWT (Spring Boot)

Este projeto é uma API RESTful desenvolvida com Spring Boot que implementa autenticação e autorização via JWT. Ele conta com documentação interativa via Swagger, testes automatizados com JUnit e testes de carga com JMeter.

---

## 📁 Estrutura do Projeto

src/
├── main/
│ ├── java/com/example/authserver/
│ │ ├── controller/
│ │ ├── service/
│ │ ├── repository/
│ │ ├── model/
│ │ └── config/
│ └── resources/
│ └── application.yml
├── test/
│ └── java/com/example/authserver/
│ └── AuthIntegrationTests.java
jmeter-tests/
└── login_stress_test.jmx
pom.xml
README.md

yaml
Copiar
Editar

---

## 🚀 Como Executar o Projeto

### 1. Clonar o Repositório

```bash
git clone https://github.com/SEU_USUARIO/seu-repositorio.git
cd seu-repositorio
2. Requisitos
Java 21

Maven

Git

(Opcional) Apache JMeter 5.6.3

3. Rodar a Aplicação
bash
Copiar
Editar
./mvnw spring-boot:run
A aplicação será iniciada em:
📍 http://localhost:8080

🔑 Acesso e Teste de Endpoints
Login
pgsql
Copiar
Editar
POST /auth/login
Content-Type: application/x-www-form-urlencoded

username=admin
password=123456
Resposta:

php-template
Copiar
Editar
<token JWT>
Endpoints Protegidos
GET /api/hello → qualquer usuário autenticado

GET /api/admin → apenas usuários com ROLE_ADMIN

📚 Documentação Swagger
Acesse a documentação interativa em:

bash
Copiar
Editar
http://localhost:8080/swagger-ui/index.html
💾 Console do Banco de Dados H2
Acesse:

bash
Copiar
Editar
http://localhost:8080/h2-console
JDBC URL: jdbc:h2:mem:testdb

User: sa

Password: (em branco)

🧪 Testes Automatizados
Execute os testes com:

bash
Copiar
Editar
./mvnw test
Arquivo principal de testes:

swift
Copiar
Editar
src/test/java/com/example/authserver/AuthIntegrationTests.java
📈 Testes de Carga com JMeter
Requisitos
Apache JMeter 5.6.3: Download aqui

Rodar o Plano de Teste
Abrir o JMeter (bin/jmeter.bat no Windows)

Abrir o arquivo: jmeter-tests/login_stress_test.jmx

Clicar no botão ▶️ para iniciar o teste

📦 Dependências Principais
spring-boot-starter-web

spring-boot-starter-security

spring-boot-starter-oauth2-resource-server

spring-boot-starter-data-jpa

com.auth0:java-jwt

org.springdoc:springdoc-openapi-starter-webmvc-ui

org.springframework.boot:spring-boot-starter-test

org.projectlombok:lombok

com.h2database:h2



