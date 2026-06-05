# Pergunta 2 — Documentação do Endpoint (1)

### Endpoint: GET /api/link
**Descrição:** Recupera a lista de conexões e vínculos ativos entre os cuidadores cadastrados e os idosos respondentes vinculados.

### Requisição
#### Headers
| Key | Value |
| :--- | :--- |
| Content-Type | application/json |
| Authorization | Bearer <token_jwt> |

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
