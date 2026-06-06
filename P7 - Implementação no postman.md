# Pergunta 7 — Implementação no Postman (2)

### Endpoint: `POST http://localhost:3333/api/auth/register`

**Configuração padrão da requisição:**
* **Headers:** `Content-Type: application/json`

### Caso de Teste CT02 — Cadastro com Sucesso

#### Body (Request)

```json
{
  "name": "Kaio Farias",
  "email": "kaio.sucesso1@teste.com",
  "password": "senhaSegura123",
  "role": "RESPONDENTE"
}
```

#### Testes (Postman — aba Tests)

```javascript
pm.test("Status code deve ser 201", function () {
    pm.response.to.have.status(201);
});

pm.test("Resposta deve conter token JWT", function () {
    var json = pm.response.json();
    pm.expect(json).to.have.property("token");
});
```
