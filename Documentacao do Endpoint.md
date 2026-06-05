# Pergunta 2 — Documentação do Endpoint (1)

### Endpoint: `GET /api/link`

**Descrição:** Recupera a lista de conexões e vínculos ativos entre os cuidadores cadastrados e os idosos respondentes vinculados.

---

### Requisição

#### Headers

| Key           | Value              |
| :------------ | :----------------- |
| Content-Type  | application/json   |
| Authorization | Bearer <token_jwt> |

---

### Respostas

#### 200 — Lista de vínculos retornada com sucesso

```json
[
  {
    "id": "clxb1234567890",
    "caregiverId": "id-cuidador",
    "respondentId": "id-idoso",
    "status": "ACTIVE"
  }
]
```

#### 401 — Usuário não autorizado

```json
{
  "message": "Unauthorized"
}
```

---

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
