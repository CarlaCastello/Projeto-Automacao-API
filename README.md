# Projeto de Testes de API – ServeRest
📖 Descrição

Este projeto contém a automação de testes da API ServeRest
, utilizando Cypress e o padrão Page Object Model (POM) para organizar melhor o código.

O objetivo principal é validar os fluxos de CRUD de Usuários e Login com captura de Token, garantindo que a API funcione corretamente e de forma estável em execuções repetidas (como em pipelines de CI/CD).

🛠️ Tecnologias Utilizadas

Cypress
 – Framework de testes E2E

Node.js (>= 18) – Runtime necessário

NPM – Gerenciador de dependências


📂 Estrutura do Projeto
cypress/

  e2e/
  
      crud_usuarios.cy.js      # Testes de CRUD de Usuários
      
      login_token.cy.js        # Testes de Login e captura de Token
 
   support/
   
      usuarios_api.js          # Page Object de Usuários
      
      login_api.js             # Page Object de Login
            
      cypress.config.js         # Configuração base do Cypress
 
       package.json             # Dependências e scripts

▶️ Como Executar os Testes

Rodar no modo interativo

npx cypress open

📌 Cenários de Teste Implementados

🔹 CRUD de Usuários

Criar usuário

Consultar usuário pelo ID

Editar usuário

Deletar usuário e validar exclusão

🔹 Login e Captura de Token

Criar usuário válido

Realizar login

Validar retorno de token JWT

🔑 Boas Práticas Adotadas

✔ Page Object Model (POM): requests organizados em classes, facilitando reuso e manutenção.

✔ Emails dinâmicos: uso de Date.now() para evitar duplicidade em pipelines.

✔ Validações explícitas: verificação de status code e mensagens de retorno.

✔ failOnStatusCode: false: utilizado em cenários onde o erro é esperado (ex: usuário não encontrado).

✔ Reutilização de token: token de login pode ser armazenado via cy.wrap(token).as('authToken') para outros testes.

👩‍💻 Autor

Projeto desenvolvido como desafio técnico de QA – Carla Castello de Sousa
