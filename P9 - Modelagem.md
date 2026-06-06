# Pergunta 9 — Modelagem do Teste de Interface (1)

### Tela: Página de Login (Daily Check-in Sênior)
**Técnica Utilizada:** Tabela de Decisão  
**Cenário:** Login válido com redirecionamento para Home

### Tabela de Decisão

| Condição / Regra | CT01 |
| :--- | :---: |
| **R1 — Email preenchido e válido** | S |
| **R2 — Senha preenchida** | S |
| **R3 — Credenciais existentes no sistema** | S |
| **Resultado Esperado** | Redirecionamento para a Home Page com título visível |

### Caso de Teste Derivado (CT01)

* **E-mail:** idoso@teste.com
* **Senha:** 123456
* **Resultado Esperado:** O sistema deve autenticar o usuário e redirecionar para `http://localhost:5173/` exibindo o título "Daily Check-in Sênior".
