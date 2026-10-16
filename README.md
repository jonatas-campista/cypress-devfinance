# Testes E2E — Dev Finance

![Cypress](https://img.shields.io/badge/Cypress-17202C?logo=cypress&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

Testes end-to-end com Cypress para o [Dev Finance](https://dev-finance.netlify.app/), uma aplicação
web de controle de entradas e saídas financeiras.

## Cenários

| Cenário | O que valida |
|---|---|
| Cadastrar uma entrada | uma transação positiva aparece na tabela |
| Cadastrar uma saída | uma transação negativa aparece na tabela |
| Excluir transação | ao excluir uma de duas transações, sobra só uma na tabela |

A criação de transação foi extraída para uma função reutilizável (`criarTransacao`), usada por todos
os cenários.

## Como rodar

```bash
npm install
npx cypress run    # headless
npx cypress open   # interativo
```

## Próximos passos

- Validar os totais de entradas, saídas e saldo.
- Mover `criarTransacao` para um comando customizado (`cy.criarTransacao`).
- Adicionar o script `test` no `package.json` e rodar em CI.
