# Pergunta 9 — Modelagem do Teste de Interface (1)

### Tela: Cadastro de Usuário (Daily Check-in Sênior)
**Técnica Utilizada:** Tabela de Decisão  
**Cenário:** Cadastro com falha — E-mail já cadastrado

### Tabela de Decisão

| Condição / Regra | CT02 |
| :--- | :---: |
| **R1 — Nome preenchido** | S |
| **R2 — E-mail preenchido e válido** | S |
| **R3 — Senha >= 8 caracteres** | S |
| **R4 — Confirmar Senha igual à Senha** | S |
| **R5 — Email informado já está cadastrado** | S |
| **Resultado Esperado** | Mensagem de erro na tela: "Este e-mail já está sendo utilizado por outro usuário" |

### Caso de Teste Derivado (CT02)

* **Nome:** Kaio Farias
* **E-mail:** kaio.duplicado@teste.com
* **Senha:** senhaSegura123
* **Confirmar Senha:** senhaSegura123
* **Resultado Esperado:** O sistema deve bloquear o envio e exibir o alerta de e-mail duplicado na interface do usuário.

**Link de referência no GitHub:**  
https://github.com/kaiofa/Testes-Kaio/blob/main/P9-Interface-Docs.md
