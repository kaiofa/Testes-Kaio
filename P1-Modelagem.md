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
**Headers:** `Authorization: Bearer TOKEN_ALUNO_7`  
**Resultado esperado:** 200 OK com a lista de conexões.

---

# Pergunta 5 — Modelagem do Teste de API (2)

### Endpoint: POST /api/auth/register — Cadastro com Sucesso
**Técnica:** Particionamento de Equivalência  
**Campos analisados:** `name`, `email`, `password`, `role` (Body)

### Partições de Equivalência

| Índice | Partição | Descrição | Resultado Esperado |
| :--- | :--- | :--- | :--- |
| **P3** | Dados Válidos | Envio de payload completo e correto | HTTP 201 com token e dados do usuário |

### Casos de Teste

#### CT02 — Partição P3: Dados Válidos
```json
{
  "name": "Kaio Farias",
  "email": "kaio.sucesso1@teste.com",
  "password": "senhaSegura123",
  "role": "RESPONDENTE"
}
```
**Resultado esperado:** 201 Created com as credenciais geradas.
