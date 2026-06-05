# Pergunta 6 — Documentação do Endpoint (2)

### Endpoint: `POST /api/auth/register`

**Descrição:** Cria credenciais de acesso no sistema e define se o perfil inserido atuará como `RESPONDENTE` ou `CUIDADOR` na aplicação.

---

### Requisição

#### Headers

| Key          | Value            |
| :----------- | :--------------- |
| Content-Type | application/json |

#### Body

```json
{
  "name": "string",
  "email": "string",
  "password": "string",
  "role": "RESPONDENTE"
}
```

---

### Respostas

#### 201 — Cadastrado com sucesso

```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "user": {
    "id": "cmpx7kaio12345",
    "name": "Kaio Farias",
    "email": "kaio.sucesso1@teste.com",
    "role": "RESPONDENTE"
  }
}
```
