<div align="center">
  
  # Documento Técnico
</div>

<details>
<summary>Atividade Avaliativa</summary>
  
## Atividade Avaliativa

Criar um documento técnico contendo:
- Diferença entre PUT, PATCH e DELETE
- Principais status codes e seus significados
- Exemplo de payload JSON bem estruturado
- Criação de testes de Integração

</details>

## 1. Métodos HTTP
### 1.1 Diferença entre  PUT, PATCH e DELETE
São os métodos HTTP mais comuns para modificar uma API.

| Método | Uso | Característica |
| --- | --- | --- |
| **PUT** | Usado para atualizar um recurso existente | Substituição total
| **PATCH** | Atualiza parcialmente um recurso | Altera apenas os campos informados |
| **DELETE** | Exclui um recurso | Remove um recurso específico |

#### 1.1.1 PUT
- Se o recurso não existe ainda, o servido cria esse recurso com os dados enviados e retorna `201 Created`.
- Se o recurso já existe, ele é totalmente substituído e a resposta é `200 OK` se houver corpo ou `204 No Content` se não houver.
- PUT é *idempotente* (fazer a mesma requisição várias vezes terá sempre o mesmo efeito).

#### 1.1.2 PATCH

#### 1.1.3 DELETE

---

## 2. Status Codes

- Respostas Informativas (100 – 199)
- Respostas bem-sucedidas (200 – 299)
- Mensagens de redirecionamento (300 – 399)
- Respostas de erro do cliente (400 – 499)
- Respostas de erro do servidor (500 – 599)

### 2.1 Principais códigos

| Código | Significado |
| --- | --- |
| **200 OK** | Indica que a requisição foi processada com sucesso. |
| **201 Created** | Indica que um novo recurso foi criado com sucesso. |
| **204 No Content** | Indica que a requisição foi processada com sucesso, mas não há conteúdo para retornar. |
| **400 Bad Request** | Indica que a requisição possui algum problema, como dados inválidos ou formato incorreto. |
| **401 Unauthorized** | O cliente deve se autenticar para obter a resposta solicitada. |
| **403 Forbidden** | Indica que o cliente foi identificado, mas não possui permissão para executar a operação. |
| **404 Not Found** | Indica que o recurso solicitado não foi encontrado. |
| **422 Unprocessable Content** | A solicitação foi bem formada, mas não pôde ser atendida devido a erros semânticos. |
| **500 Internal Server Error** | Indica um erro interno inesperado no servidor. |

---

## 3. Exemplo de Payload JSON

### Exemplo de cadastro de usuário

```json
{
  "id": 123,
  "nome": "Natan",
  "email": "natan@example.com",
  "ativo": true,
  "perfil": {
    "cargo": "Desenvolvedor",
    "nivel": "Pleno"
  },
  "tags": ["API", "HTTP", "Integração"]
}
```

---

## Fontes
- [Métodos de requisição HTTP](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Reference/Methods)
- [Métodos HTTP REQUEST - GET, POST, PUT, PATCH, DELETE. (Um passo a passo com JavaScript's Fetch API)
](https://ichi.nghiatu.com/pt/metodos-http-request-get-post-put-patch-delete-um-passo-a-passo-com-javascript-s-fetch-api-250115341607584)
- [Códigos de status de resposta HTTP
](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status)

---

<div align="center">
  
25/09/2026
</div>
