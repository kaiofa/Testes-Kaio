# Pergunta 12 — Modelagem do Teste de Interface (2)

### Tela: Home Page (Pós-Autenticação)
**Técnica Utilizada:** Tabela de Decisão  
**Cenário:** Verificar carregamento e validação estrutural da página principal

### Tabela de Decisão

| Condição / Regra | CT03 |
| :--- | :---: |
| **R1 — Chamar URL válida da Home Page** | S |
| **Resultado Esperado** | Página renderizada inteiramente com título correto na aba do navegador |

### Caso de Teste Derivado (CT03)

* **Ação:** Abrir a rota `/home`.
* **Resultado Esperado:** O navegador deve validar se o elemento `Title` da aba corresponde exatamente a "Daily Check-in Sênior - Home".

**Link de referência no GitHub:**  
https://github.com/kaiofa/Testes-Kaio/blob/main/P9-Interface-Docs.md
