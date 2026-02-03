# API de Clientes - Spring boot + Gradle
Este projeto é uma API básica de clientes, desenvolvida em Java com Spring boot, utilizando o Gradle como sistema de build.

O objetivo Este projeto foi desenvolvido com o objetivo de aprender, na prática, como criar uma API REST utilizando Spring Boot. Ele faz parte dos meus estudos iniciais com o framework e foi pensado para consolidar conceitos fundamentais, como CRUD, arquitetura em camadas e boas práticas, mantendo a simplicidade e a didática.

## Objetivos do projeto:

- Criar uma API RESTful utilizando Spring Boot
- Implementar um CRUD completo de Clientes
- Utilizar Gradle como ferramenta de build
- Aplicar arquitetura em camadas
- Servir como base para evoluções futuras

## Tecnologias utilizadas:

- Java 17 (LTS)
- Spring Boot
- Spring Web
- Spring Data JPA
- H2 Database
- Gradle
- IntelliJ IDEA

## Arquitetura do projeto
O projeto segue uma arquitetura em camadas, e foi organizada da seguinte maneira:

Controller -> Service -> Repository -> Database

A arquitetura foi definida dessa maneira para separar as responsabilidades de maneira clara, deixando o código mais organizado e legível para que a manutenção e os testes sejam facilitados e de maneira que o torne escalável para um projeto maior.

## Estrutura de pastas

<img width="368" height="364" alt="image" src="https://github.com/user-attachments/assets/57154c2f-ee81-4420-9271-e43887079f33" />

## Camadas do projeto
### > Model
Representa a entidade Cliente, ou seja, como os dados são estruturados no sistema e no banco de dados.

<img width="579" height="714" alt="image" src="https://github.com/user-attachments/assets/0ebc1f4b-e7bd-4a06-b678-4cc965ec2008" />

Responsabilidades:

- Mapear a tabela do banco (JPA)
- Representar o domínio da aplicação

### > Repository
Camada responsável pelo acesso ao banco de dados.

<img width="768" height="194" alt="image" src="https://github.com/user-attachments/assets/9d6573ea-f3d9-4190-9dc8-0572c54cdc04" />

Responsabilidades:
- Persistir dados
- Buscar dados
- Excluir dados

Utiliza Spring Data JPA, o que elimina a necessidade de escrever SQL manualmente.

### > Service
Camada onde ficam as regras de negócio.

<img width="763" height="749" alt="image" src="https://github.com/user-attachments/assets/a0f07e3d-edc8-455f-b714-c342dc5e597d" />

Responsabilidades:
- Validar dados
- Centralizar a lógica da aplicação
- Evitar regras dentro do Controller

### > Controller
Camada responsável por expor a API REST.

<img width="772" height="743" alt="image" src="https://github.com/user-attachments/assets/3eb2f58a-21ab-4009-a8c5-686ae46465a4" />

Responsabilidades:
- Receber requisições HTTP
- Chamar o Service
- Retornar respostas HTTP

Aqui são definidos os endpoints da aplicação.

## Configuração da aplicação
O arquivo application.yml contém as configurações principais:

- Banco de dados H2 em memória
- JPA com ddl-auto: update
- Console do H2 habilitado

Isso permite rodar o projeto sem instalar banco externo.

## Como executar o projeto
### 1. Pré requisitos

- Java 17 instalado
- Gradle Wrapper

### 2. Passos

- Clone o repositório:

(adicionar print do comando)

- Acesse a pasta do projeto:

(adicionar print do comando)

- Execute a aplicação:

(adicionar print do comando)

- A API estára disponível em:

(Adicionar print do url)

## Possíveis evoluções futuras
Este projeto foi pensado para crescer. Algumas evoluções naturais:

- Dockerização
- Deploy em Kubernetes
- Banco PostgreSQL
- Autenticação com JWT

## Conclusão
Este projeto representa uma base sólida para o meu aprendizado na utilização do Spring boot para a criação de APIs

Ele demonstra:

- Fundamentos de APIs REST
- Organização de código
- Boas práticas iniciais
- Preparação para ambientes profissionais
