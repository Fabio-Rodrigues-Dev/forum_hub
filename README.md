# Fórum API (FórumHub)

Este projeto é um desafio proposto no programa ONE - Oracle Next Education, uma parceria entre a Alura e a Oracle.

## Descrição do Desafio

O objetivo é implementar uma API REST de um fórum.

- Implementar rotas seguindo as práticas do modelo REST.
- Realizar validações das regras de negócio.
- Implementar uma base de dados relacional para a persistência da informação.
- Utilizar um serviço de autenticação/autorização para restringir o acesso à informação.

## Funcionalidades

- **Autenticação:** Gerar e validar um token JWT.
- **Criar um novo tópico:** Permite a criação de novos tópicos no fórum.
- **Mostrar todos os tópicos criados:** Exibe uma lista de todos os tópicos.
- **Mostrar um tópico específico:** Exibe detalhes de um tópico específico.
- **Atualizar um tópico:** Permite a atualização de um tópico existente.
- **Excluir um tópico:** Permite a exclusão de um tópico.

## Tecnologias Utilizadas

- **Java 17**
- **Maven**
- **Spring Boot**
- **Spring Data JPA**
- **Spring Security** (Autenticação)
- **SpringDoc** (Documentação com Swagger)
- **MySQL** (Banco de dados)
- **Flyway Migration**
- **Auth0**
- **Lombok**

## Instalação

Para executar a aplicação localmente:

1. **Clone este repositório:**
    ```bash
    git clone https://github.com/seu-usuario/forumhub.git
    ```

2. **Certifique-se de ter a JDK do Java 17 ou superior instalado.**

3. **Certifique-se de ter o MySQL 8 ou superior instalado.**

4. **Importe o projeto utilizando o Maven em uma IDE de sua preferência.**

5. **Configure o MySQL atualizando as configurações no arquivo `application.properties`:**
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/forumhub
    spring.datasource.username=seu-usuario
    spring.datasource.password=sua-senha
    spring.jpa.hibernate.ddl-auto=update
    ```

6. **Execute a classe `ForumApiApplication.java` para iniciar a aplicação.**

7. **Acesse a documentação da API no navegador:**
    ```url
    http://localhost:8080/swagger-ui/index.html
    ```

8. **Gere um token de autenticação:**
    - Use o endpoint `/login` no controlador de autenticação (`autenticacao-controller`).
    - Passe no corpo da requisição o seguinte JSON:
      ```json
      {
        "email": "teste@email.com",
        "senha": "123456"
      }
      ```

**Atenção:** O projeto inclui migrations do Flyway que, além de criar as tabelas, cadastra alguns dados no banco para facilitar o início dos testes.

---

Desenvolvido como parte do programa ONE - Oracle Next Education.
