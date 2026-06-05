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
