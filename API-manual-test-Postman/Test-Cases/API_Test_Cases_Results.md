# Documentação dos Casos de Teste de API Manual - JSONPlaceholder

**Objetivo:** Realizar testes manuais em uma API RESTful utilizando o Postman, focando na validação de diferentes tipos de requisições (GET, POST, PUT, DELETE) e suas respostas, explorando diversos recursos (IDs) da API.

**Ferramenta Utilizada:** Postman

**API Alvo:** [JSONPlaceholder](https://jsonplaceholder.typicode.com)

---

## Cenário de Teste 1: Listar Todos os Posts (GET)

* **ID do Teste:** `API_GET_001`
* **Funcionalidade:** Listagem de Posts
* **Descrição:** Verificar se a API retorna a lista completa de posts existentes com status de sucesso.
* **Requisição:**
    * **Método:** `GET`
    * **URL:** `https://jsonplaceholder.typicode.com/posts`
* **Resultado Esperado:**
    * Status code `200 OK`.
    * O corpo da resposta deve conter um array de objetos JSON, representando os posts, com estrutura de dados consistente (ex: `userId`, `id`, `title`, `body`).
* **Resultado Real:**
    * Status code `200 OK`.
    * Corpo da resposta: Array de objetos JSON contendo múltiplos posts, conforme esperado.
* **Status:** Passou
* **Evidência:** `GET-test.png`

---

## Cenário de Teste 2: Obter um Post Específico por ID (GET - ID 5)

* **ID do Teste:** `API_GET_002`
* **Funcionalidade:** Consulta de Post por ID
* **Descrição:** Verificar se a API retorna corretamente um post específico quando um ID válido (5) é fornecido.
* **Requisição:**
    * **Método:** `GET`
    * **URL:** `https://jsonplaceholder.typicode.com/posts/5`
* **Resultado Esperado:**
    * Status code `200 OK`.
    * O corpo da resposta deve conter um objeto JSON com os detalhes do post correspondente ao ID 5.
* **Resultado Real:**
    * Status code `200 OK`.
    * Corpo da resposta: Objeto JSON com `userId: 1`, `id: 5`, `title`, e `body` correspondentes ao post 5.
* **Status:** Passou
* **Evidência:** `GET-test-id-5.png`

---

## Cenário de Teste 3: Criar um Novo Post (POST - Com dados específicos)

* **ID do Teste:** `API_POST_001`
* **Funcionalidade:** Criação de Posts
* **Descrição:** Verificar se a API responde corretamente ao tentar criar um novo post com dados customizados.
* **Requisição:**
    * **Método:** `POST`
    * **URL:** `https://jsonplaceholder.typicode.com/posts`
    * **Body (raw JSON):**
        ```json
        {
          "Name": "Arthux",
          "City": "Vienna",
          "Age": 27,
          "userId": 13
        }
        ```
* **Resultado Esperado:**
    * Status code `201 Created`.
    * O corpo da resposta deve conter os dados enviados (`Name`, `City`, `Age`, `userId`), além de um `id` gerado pela API (neste caso, `101`).
* **Resultado Real:**
    * Status code `201 Created`.
    * Corpo da resposta:
        ```json
        {
          "Name": "Arthux",
          "City": "Vienna",
          "Age": 27,
          "userId": 13,
          "id": 101
        }
        ```
* **Status:** Passou
* **Evidência:** `POST-id101-created.png`

---

## Cenário de Teste 4: Atualizar um Post Existente (PUT - ID 13)

* **ID do Teste:** `API_PUT_001`
* **Funcionalidade:** Atualização de Post
* **Descrição:** Verificar se a API responde corretamente ao tentar atualizar um post específico (ID 13) com novos dados.
* **Requisição:**
    * **Método:** `PUT`
    * **URL:** `https://jsonplaceholder.typicode.com/posts/13`
    * **Body (raw JSON):**
        ```json
        {
          "Name": "Arthux",
          "City": "Vienna",
          "Age": 27,
          "userId": 13,
          "id": 13
        }
        ```
* **Resultado Esperado:**
    * Status code `200 OK`.
    * O corpo da resposta deve conter os dados enviados para atualização, incluindo o `id` do post que foi atualizado (13).
* **Resultado Real:**
    * Status code `200 OK`.
    * Corpo da resposta:
        ```json
        {
          "Name": "Arthux",
          "City": "Vienna",
          "Age": 27,
          "userId": 13,
          "id": 13
        }
        ```
* **Status:** Passou
* **Evidência:** `PUT-id13-JSON.png` (ou `PUT-id13-preview.png` se preferir o formato de visualização)

---

## Cenário de Teste 5: Deletar um Post (DELETE - ID 75)

* **ID do Teste:** `API_DELETE_001`
* **Funcionalidade:** Exclusão de Post
* **Descrição:** Verificar se a API responde corretamente ao tentar deletar um post específico (ID 75).
* **Requisição:**
    * **Método:** `DELETE`
    * **URL:** `https://jsonplaceholder.typicode.com/posts/75`
* **Resultado Esperado:**
    * Status code `200 OK`.
    * O corpo da resposta deve ser vazio (`{}`) ou conter uma confirmação de exclusão, indicando sucesso na operação.
* **Resultado Real:**
    * Status code `200 OK`.
    * Corpo da resposta: `{}` (vazio), conforme esperado para uma exclusão bem-sucedida.
* **Status:** Passou
* **Evidência:** `DEL-id-75.png`