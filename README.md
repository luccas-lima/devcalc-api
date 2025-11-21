DevCalc API
Descrição

A DevCalc API é uma aplicação Java criada para fornecer operações básicas de cálculo através de endpoints HTTP.
O projeto utiliza Java + Javalin e foi desenvolvido e executado diretamente pelo IntelliJ IDEA, sem uso de comandos Maven no terminal.

Tecnologias Utilizadas

Java 17+

Javalin

JUnit 5 (testes)

Docker

IntelliJ IDEA

Estrutura do Projeto

O projeto segue a estrutura padrão:

src/
 ├─ main/
 │   └─ java/com/devcalc/
 │        ├─ App.java
 │        └─ CalculatorService.java
 └─ test/
     └─ java/com/devcalc/
          └─ CalculatorServiceTest.java

Como Executar o Projeto (IntelliJ)

Abra o IntelliJ IDEA.

Importe o projeto como Projeto Maven (automaticamente pelo pom.xml).

Vá até a classe:

com.devcalc.App


Clique em Run 'App.main()'.

A API estará disponível em:

http://localhost:7000

Endpoints da API
GET /

Retorna status simples da API:

DevCalc API is running

GET /add?a=10&b=5

Retorna a soma.

GET /subtract?a=10&b=5

Retorna a subtração.

GET /multiply?a=10&b=5

Retorna a multiplicação.

GET /divide?a=10&b=5

Retorna a divisão.

Testes Automatizados

Os testes rodam diretamente pela IDE:

Abra CalculatorServiceTest.java

Clique em Run Tests

Todos os métodos (add, subtract, multiply, divide) possuem testes dedicados.

Docker
Build da imagem

A imagem é construída a partir do Dockerfile:

docker build -t devcalc-api:1.0.0 .

Executar o container
docker run -p 7000:7000 devcalc-api:1.0.0

Docker Hub

Envio da imagem:

docker tag devcalc-api:1.0.0 SEU_USUARIO/devcalc-api:1.0.0
docker push SEU_USUARIO/devcalc-api:1.0.0

docker tag devcalc-api:1.0.0 SEU_USUARIO/devcalc-api:latest
docker push SEU_USUARIO/devcalc-api:latest
