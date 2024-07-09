## 🔨 Objetivos do projeto

A ideia central do projeto é que o mesmo era um monolito e estamos iniciando a decomposição em microsserviços. Começamos implementando a API e projeto do microsserviço de pagamento, tendo um banco de dados próprio [MySQL](https://www.mysql.com).

Além disso, fazemos a implementação do Service Discovery utilizando o [Eureka](https://spring.io/projects/spring-cloud-netflix), solução desenvolvida pela Netflix e que faz parte do [Spring Cloud](https://spring.io/projects/spring-cloud). Incluímos também à arquitetura um [API Gateway](https://spring.io/projects/spring-cloud-gateway), que vai atuar como ponto central para as nossas requisições. É feita a inclusão de um novo microsserviço, que é o de pedidos, onde praticamos a comunicação síncrona e o balanceamento de carga, quando há mais de uma instância do projeto em execução.

Para fechar, tratamos os conceitos de circuit breaker e fallback, utilizando o [Resilience4J](https://resilience4j.readme.io/docs/getting-started-3) e promovendo uma alternativa quando um dos serviços está inoperante.
