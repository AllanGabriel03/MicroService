# MicroService

 O projeto foi desenvolvido com o objetivo de demonstrar uma estrutura de microsserviços desacoplada, em que cada serviço é responsável por uma funcionalidade específica e se comunica com os demais por meio de APIs REST.
 Cada microsserviço tem sua própria base de dados (MongoDB) e é executado de forma independente no Apache Tomcat, possibilitando escalabilidade e manutenção isolada de componentes.

## Estrutura do Projeto

O sistema é composto pelos seguintes microsserviços:

cliente:	Gerencia os dados dos clientes (nome, CPF, endereço, etc).
produto:	Responsável pelos dados dos produtos (nome, preço, estoque, etc).
venda:	Processa as vendas, relacionando clientes e produtos.
config:	Centraliza as configurações externas dos demais microsserviços usando Spring Cloud Config.

## Tecnologias Utilizadas

Java 21
Spring Boot
Maven
MongoDB
Apache Tomcat
REST APIs
Spring Cloud Config

## Como Usar

1. Clone o repositório:
   
git clone https://github.com/AllanGabriel03/MicroService.git
cd MicroService

2. Inicie o MongoDB localmente:

3. Execute o microsserviço de configuração:

cd config
mvn spring-boot:run

4. Em seguida, execute os demais microsserviços:

cd cliente
mvn spring-boot:run

cd produto
mvn spring-boot:run

cd venda
mvn spring-boot:run


