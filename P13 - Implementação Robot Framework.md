# Pergunta 13 — Script de Teste de Interface (2)

```robot
*** Settings ***
Library    SeleniumLibrary
Suite Setup       Dado que o usuário acessa o sistema local
Suite Teardown    E fecha o navegador

*** Variables ***
${URL_HOME}            http://localhost:3000/home
${BROWSER}             chrome
${TITULO_ESPERADO}     Daily Check-in Sênior - Home

*** Test Cases ***
CT03 - Deve verificar se a página home carrega corretamente
    [Setup]    Go To    ${URL_HOME}
    Então a página deve carregar com o título correto

*** Keywords ***
Dado que o usuário acessa o sistema local
    Open Browser    about:blank    ${BROWSER}
    Maximize Browser Window
Então a página deve carregar com o título correto
    Title Should Be    ${TITULO_ESPERADO}
E fecha o navegador
    Close Browser
```

**Link de referência no GitHub:**  
https://github.com/kaiofa/Testes-Kaio/blob/main/P10-Interface-Script.robot
