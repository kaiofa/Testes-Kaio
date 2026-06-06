# Pergunta 13 — Implementação — Script Robot Framework — Teste 2

```robot
*** Settings ***
Library    SeleniumLibrary
Suite Setup       Open Browser    http://localhost:5173/login    chrome
Suite Teardown    Close Browser

*** Variables ***
${URL_HOME}        http://localhost:5173/
${INPUT_EMAIL}     css=input[type='email']
${INPUT_SENHA}     css=input[type='password']
${BTN_ENTRAR}      css=button[type='submit']
${TITULO_HOME}     xpath=//h1[contains(text(),'Daily Check-in')]

*** Test Cases ***
CT02 - Pagina home deve carregar corretamente apos login
    Maximize Browser Window
    Input Text        ${INPUT_EMAIL}    idoso@teste.com
    Input Password    ${INPUT_SENHA}    123456
    Click Button      ${BTN_ENTRAR}
    Wait Until Location Is         ${URL_HOME}    timeout=5s
    Wait Until Element Is Visible  ${TITULO_HOME}    timeout=5s
    Page Should Contain            Daily Check-in Sênior

*** Keywords ***
E fecha o navegador
    Close Browser
```
