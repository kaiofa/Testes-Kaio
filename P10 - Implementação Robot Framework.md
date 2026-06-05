# Pergunta 10 — Script de Teste de Interface

```robot
*** Settings ***
Library    SeleniumLibrary
Suite Setup       Dado que o usuário acessa o sistema local
Suite Teardown    E fecha o navegador

*** Variables ***
${URL_CADASTRO}        http://localhost:3000/cadastro
${BROWSER}             chrome
${INPUT_NOME}          id=nome
${INPUT_EMAIL}         id=email
${INPUT_SENHA}         id=password
${INPUT_CONFIRMAR}     id=confirmPassword
${BOTAO_CADASTRAR}     id=btn-register
${MENSAGEM_ALERTA}     id=alert-message

*** Test Cases ***
CT02 - Deve validar erro ao tentar cadastrar email já existente
    [Setup]    Go To    ${URL_CADASTRO}
    Dado que o usuário informa o nome    Kaio Farias
    E informa o e-mail    kaio.duplicado@teste.com
    E informa a senha    senhaSegura123
    E confirma a senha    senhaSegura123
    Quando solicitar o cadastro
    Então o sistema deve apresentar a mensagem de erro    Este e-mail já está sendo utilizado por outro usuário

*** Keywords ***
Dado que o usuário acessa o sistema local
    Open Browser    about:blank    ${BROWSER}
    Maximize Browser Window
Dado que o usuário informa o nome
    [Arguments]    ${nome}
    Input Text    ${INPUT_NOME}    ${nome}
E informa o e-mail
    [Arguments]    ${email}
    Input Text    ${INPUT_EMAIL}    ${email}
E informa a senha
    [Arguments]    ${senha}
    Input Password    ${INPUT_SENHA}    ${senha}
E confirma a senha
    [Arguments]    ${confirmar}
    Input Password    ${INPUT_CONFIRMAR}    ${confirmar}
Quando solicitar o cadastro
    Click Button    ${BOTAO_CADASTRAR}
Então o sistema deve apresentar a mensagem de erro
    [Arguments]    ${mensagem}
    Element Text Should Be    ${MENSAGEM_ALERTA}    ${mensagem}
E fecha o navegador
    Close Browser
```

**Link de referência no GitHub:**  
https://github.com/kaiofa/Testes-Kaio/blob/main/P10-Interface-Script.robot
