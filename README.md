# postman-api-serverest
# Testes de API - ServeRest (Módulo 13 - EBAC)

Este repositório contém os testes automatizados da API **ServeRest**, desenvolvidos como parte da atividade prática do curso de Qualidade de Software da EBAC. O foco principal foi a funcionalidade de **Usuários**.

## Objetivo do Projeto
Validar os endpoints da funcionalidade de usuários, garantindo que as regras de negócio (cenários positivos e negativos) estejam sendo cumpridas através de asserções automatizadas no **Postman**.

## Tecnologias Utilizadas
* [Postman](https://www.postman.com/) - Ferramenta de teste de API.
* [Node.js](https://nodejs.org/) - Ambiente de execução para rodar o ServeRest localmente.
* [ServeRest](https://serverest.dev/) - API simulada para testes de e-commerce.
* [JavaScript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript) - Linguagem utilizada para os scripts de teste.

## Cenários de Teste Mapeados

### **Endpoint: /usuarios**
* **GET - Listar Usuários:** - [x] Listagem completa de usuários.
    - [x] Filtros por Query Params (Nome, Admin).
* **POST - Cadastrar Usuário:**
    - [x] Sucesso no cadastro.
    - [x] Erro ao cadastrar e-mail já existente (Cenário Negativo).
* **GET - Buscar por ID:**
    - [x] Sucesso ao buscar ID válido.
    - [x] Erro ao buscar ID inexistente (Cenário Negativo).
* **PUT - Editar Usuário:**
    - [x] Alteração de dados com sucesso.
    - [x] Criação de novo usuário caso o ID não seja encontrado (Upsert).
* **DELETE - Excluir Usuário:**
    - [x] Sucesso na exclusão.
    - [x] Validação quando nenhum registro é excluído.

## Como rodar os testes

1. **Instale o ServeRest localmente:**
   ```bash
   npx serverest@latest

2. **Importe a Collection:**

Baixe o arquivo Testes de API-ServRest.postman_collection.json deste repositório.

No Postman, clique em Import e selecione o arquivo.

3. **Configure as Variáveis:**

Certifique-se de configurar uma variável de ambiente no Postman para a URL base (ex: http://localhost:3000).

4. **Execute os Testes:**

Você pode rodar cada request individualmente ou usar o Collection Runner do Postman para rodar tudo de uma vez.

Autor
[JONATHAN CAVALCANTI]
