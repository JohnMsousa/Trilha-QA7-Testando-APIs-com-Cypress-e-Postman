# Criando uma API Restful com IA

Este projeto foi desenvolvido durante a **Cypress Masterclass** do canal **[Fernando Papito](https://www.youtube.com/@fernandopapito)**, onde o desafio foi criar uma API Restful com ajuda do **ChatGPT**. O curso foi dividido em duas partes, abordando desde a criação da API até a implementação de testes automatizados, proporcionando uma visão completa do processo.

## Resumo do Projeto

O objetivo foi desenvolver uma API para gerenciar livros, permitindo operações como cadastro, consulta e exclusão. Para agilizar os testes iniciais, utilizei o **Postman** com a extensão no **VSCode**, o que me permitiu testar as funcionalidades diretamente no editor. As principais funcionalidades implementadas foram:

-   Cadastro de livros
-   Listagem de todos os livros
-   Busca de um livro por ID
-   Exclusão de livros

Para otimizar os testes, criei variáveis como `baseUrl` (para manter a URL fixa) e `livroId` (para armazenar o ID do livro criado). Essa abordagem ajudou a evitar retrabalho e manter a organização.

Em seguida, parti para a automação dos testes usando **Cypress**. Nessa etapa, foquei em validar campos essenciais, como título, autor, editora, ano de publicação e número de páginas, garantindo que todas as informações fossem corretamente cadastradas.

Um dos pontos altos do projeto foi a implementação de uma verificação para evitar a criação de livros com títulos duplicados. Essa funcionalidade trouxe um aprendizado valioso sobre validações e boas práticas em APIs.

## O que Aprendi

Ao longo do curso, explorei diversas ferramentas e conceitos, consolidando conhecimentos importantes:

-   **Conexão com MongoDB**: Aprendi a integrar a API ao MongoDB utilizando o **Mongoose**, além de modelar e manipular dados por meio de schemas.
-   **Semi CRUD**: Como a API não incluiu a funcionalidade de atualização, implementamos um semi CRUD, com operações de criação, leitura e exclusão de livros.
-   **Automação com Cypress**: Utilizei o Cypress para automatizar os testes da API, descobrindo que ele pode ser integrado diretamente ao repositório da API, embora também seja comum separar os testes em repositórios distintos.
-   **Gerenciamento de Dependências**: A instalação do Cypress foi feita com o comando `npm i cypress -D`, garantindo que ele fosse adicionado apenas como dependência de desenvolvimento (`devDependencies`). Isso mantém o ambiente de produção mais leve e eficiente.
-   **Organização de Ambientes**: Durante o desenvolvimento, utilizei o **nodemon** com o comando `npm run dev`, que reinicia o servidor automaticamente após alterações. Já o `npm start` é usado para iniciar o servidor em produção, sem incluir dependências de desenvolvimento. Essa separação contribui para um ambiente de produção mais limpo e organizado.

## Tecnologias Usadas

-   **Node.js**
-   **Express**
-   **MongoDB** (com Mongoose)
-   **Postman** (com extensão no VSCode)
-   **Cypress** (para testes automatizados)
-   **Nodemon** (para reiniciar o servidor durante o desenvolvimento)
