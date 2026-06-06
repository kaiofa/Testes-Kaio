# Pergunta 3 — Implementação no Postman (1)

### Endpoint: `GET http://localhost:3333/api/link`

**Configuração padrão da requisição:**
* **Headers:** `Content-Type: application/json`
* **Autenticação:** Bearer Token → `TOKEN_ALUNO_7`

### Caso de Teste CT01 — Token Ativo

#### Testes (Postman — aba Tests)

```javascript
pm.test("Status code deve ser 200", function () {
    pm.response.to.have.status(200);
});
```
