<div align="center">
  
  # Análise da API ReqRes
</div>

## 1. Endpoint GET - Listar usuários

### 1.1 Identificação e Finalidade

**Endpoint/Rota:**

`GET /api/users?page=2`

**Objetivo de Negócio:**

Essa chamada permite consultar uma lista de usuários cadastrados no sistema. Em um sistema real, poderia ser utilizada para exibir usuários em uma tela administrativa, consultar registros ou carregar dados para outras operações.

---

### 1.2 Estrutura do Request

**Método HTTP:**

`GET`

**URL Completa:**

`https://reqres.in/api/users?page=2`

**Headers:**

```text
x-api-key: SUA_API_KEY
```

O ReqRes atualmente exige uma chave de API (`x-api-key`) para as chamadas da API. A documentação oficial também utiliza esse header nos exemplos de `GET /api/users`.

**Body:**

`N/A`

Requisições GET desse endpoint não possuem corpo JSON. O parâmetro `page=2` é enviado na própria URL para indicar a página dos resultados.

---

### 1.3 Estrutura do Response

**Status Code Esperado:**

`200 OK`

**Payload de Retorno:**

Um exemplo de resposta documentado pelo ReqRes é:

```json
{
  "page": 2,
  "per_page": 6,
  "total": 12,
  "total_pages": 2,
  "data": [
    {
      "id": 7,
      "email": "michael.lawson@reqres.in",
      "first_name": "Michael",
      "last_name": "Lawson",
      "avatar": "https://reqres.in/img/faces/7-image.jpg"
    }
  ]
}
```

A resposta contém informações de paginação, como `page`, `per_page`, `total` e `total_pages`, além da lista de usuários dentro do campo `data`. O status esperado para a consulta é `200 OK`.

# 2. Endpoint POST - Criar usuário

## 2.1 Identificação e Finalidade

**Endpoint/Rota:**

`POST /api/users`

**Objetivo de Negócio:**

Essa chamada permite enviar os dados necessários para criar um novo usuário. Em um sistema real, poderia ser utilizada durante o cadastro de um novo usuário por uma aplicação ou sistema administrativo.

---

## 2.2 Estrutura do Request

**Método HTTP:**

`POST`

**URL Completa:**

`https://reqres.in/api/users`

**Headers:**

```text
Content-Type: application/json
x-api-key: SUA_API_KEY
```

O `Content-Type` informa ao servidor que o corpo da requisição está no formato JSON. O `x-api-key` é utilizado para autenticação da chamada na versão atual da API.

**Body:**

```json
{
  "name": "Jane",
  "job": "QA Engineer"
}
```

O endpoint utiliza os campos `name` e `job` no corpo da requisição para representar o usuário que será criado.

---

## 2.3 Estrutura do Response

**Status Code Esperado:**

`201 Created`

O código `201` indica que a solicitação foi processada e um novo recurso foi criado.

**Payload de Retorno:**

Exemplo de resposta:

```json
{
  "name": "Jane",
  "job": "QA Engineer",
  "id": "123",
  "createdAt": "2026-02-06T10:30:00.000Z"
}
```

A resposta retorna novamente os dados enviados e acrescenta informações geradas pelo servidor, como o `id` e a data de criação (`createdAt`).

---

# 3. Resumo do Contrato de Integração

| Endpoint            | Método | Finalidade         | Body | Status esperado |
| ------------------- | ------ | ------------------ | ---- | --------------- |
| `/api/users?page=2` | GET    | Consultar usuários | N/A  | `200 OK`        |
| `/api/users`        | POST   | Criar usuário      | JSON | `201 Created`   |

## Conclusão

A análise dos dois endpoints permite compreender o contrato básico de comunicação entre cliente e servidor.

No `GET /api/users`, o cliente envia uma solicitação de leitura e recebe uma lista de usuários, juntamente com informações de paginação.

No `POST /api/users`, o cliente envia um objeto JSON contendo os dados do novo usuário. O servidor processa a solicitação e retorna os dados enviados junto de informações geradas no processo de criação, como o identificador e a data de criação.

Esses dois endpoints permitem compreender conceitos fundamentais que serão utilizados posteriormente na automação de testes de API, como método HTTP, URL, headers, body, status code e payload de resposta.
