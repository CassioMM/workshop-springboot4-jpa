# Workshop Spring Boot 4 - JPA
[![NPM](https://img.shields.io/npm/l/react)](https://github.com/CassioMM/workshop-springboot4-jpa/blob/main/LICENSE) 

# Sobre o projeto

Uma API REST básica em Java usando **Spring Boot + JPA (Hibernate)** para persistência de dados e acesso ao banco.

Esse projeto faz parte do workshop de Spring Boot & JPA, implementando operações CRUD e relacionamentos entre entidades.

## Tecnologias Utilizadas
- Java 25
- Spring Boot
- Spring Data JPA
- Hibernate
- Banco de dados H2 (em memória) / MySQL opcional
- Maven

### Implantação em produção

- Banco de dados: H2 (Em memoria)

## Modelo conceitual
<img width="1139" height="444" alt="Screenshot 2026-01-21 at 15-47-11 Microsoft Word - web-services-Spring-Boot-JPA-Hibernate docx - web-services-Spring-Boot-JPA-Hibernate pdf" src="https://github.com/user-attachments/assets/dd4ff86f-bf92-42aa-94d9-060330c5871d" />

## Layout H2 Console
<img width="820" height="420" alt="H2Console" src="https://github.com/user-attachments/assets/2e4509db-e31c-4656-865d-9f654139722f" />


## Layout Postman
<img width="847" height="620" alt="Postman" src="https://github.com/user-attachments/assets/ce1ff365-6a69-4d72-b98e-9ed83f728fc9" />


## Organização em Camadas
O projeto segue a arquitetura em camadas:

- Resource (Controller): Responsável por expor os endpoints REST.

- Service: Contém as regras de negócio da aplicação.

- Repository: Responsável pela comunicação com o banco de dados via JPA.

- Entity: Representa as tabelas do banco de dados.


## Controllers (Endpoints da API)

Os controllers estão localizados no pacote:

```com.educandoweb.course.resources```

### UserResource

Responsável pelas operações relacionadas aos usuários.

| Método | Endpoint      | Descrição               |
| ------ | ------------- | ----------------------- |
| GET    | `/users`      | Lista todos os usuários |
| GET    | `/users/{id}` | Busca usuário por ID    |
| POST   | `/users`      | Insere um novo usuário  |
| PUT    | `/users/{id}` | Atualiza um usuário     |
| DELETE | `/users/{id}` | Remove um usuário       |

### OrderResource

Gerencia os pedidos realizados pelos usuários.

| Método | Endpoint       | Descrição              |
| ------ | -------------- | ---------------------- |
| GET    | `/orders`      | Lista todos os pedidos |
| GET    | `/orders/{id}` | Busca pedido por ID    |
| POST   | `/orders`      | Cria um novo pedido    |

### ProductResource

Controla os produtos disponíveis.

| Método | Endpoint         | Descrição               |
| ------ | ---------------- | ----------------------- |
| GET    | `/products`      | Lista todos os produtos |
| GET    | `/products/{id}` | Busca produto por ID    |

### CategoryResource

Responsável pelas categorias de produtos.

| Método | Endpoint      | Descrição                 |
| ------ | ------------- | ------------------------- |
| GET    | `/categories` | Lista todas as categorias |


## Banco de Dados

- Banco utilizado: H2 (em memória)
- Console H2 disponível em:
```bash
  http://localhost:8080/h2-console
```

### Configurações padrão:

- JDBC URL: ```jdbc:h2:mem:testdb```

- Usuário: sa

- Senha: (em branco)

## Como Executar o Projeto
Pré-requisitos:

- Java 17+ (preferencia o Java 25)
- Maven

### Passos:
```bash
  git clone https://github.com/CassioMM/workshop-springboot4-jpa.git
  cd workshop-springboot4-jpa
  mvn spring-boot:run
```
A aplicação ficará disponível em:
```arduino
http://localhost:8080
```


# Autor

Cássio Montenegro

www.linkedin.com/in/cássio-montenegro-marques

# Dedicatoria

[DevSuperior](https://devsuperior.com "Site da DevSuperior")

