# Pergunta 1 — Modelagem do Teste de API (1)

### Endpoint: GET /api/link — Listar Vínculos Autenticado
**Técnica:** Particionamento de Equivalência  
**Campo analisado:** `Authorization` (Header)

### Partições de Equivalência

| Índice | Partição | Descrição | Resultado Esperado |
| :--- | :--- | :--- | :--- |
| **P1** | Token Ativo | Envio de token JWT válido no Header | HTTP 200 com array de vínculos ativos |
| **P2** | Token Ausente | Requisição enviada sem o campo de autenticação | HTTP 401 — Unauthorized |

### Casos de Teste

#### CT01 — Partição P1: Token Ativo

* **Headers:** `Authorization: Bearer TOKEN_ALUNO_7`
* **Resultado esperado:** 200 OK com a lista de conexões.
