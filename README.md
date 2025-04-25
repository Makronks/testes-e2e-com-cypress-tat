# Testes End-to-End com Cypress

Projeto de exemplo para demonstrar testes end-to-end (e2e) escritos com [Cypress](https://cypress.io), rodando no GitHub Actions.

## Pré-requisitos

Para clonar e rodar este projeto, você vai precisar de:

- [git](https://git-scm.com/downloads) (usei a versão `2.34.1` ao escrever este documento)
- [Node.js](https://nodejs.org/en/) (usei a versão `v18.15.0`)
- npm (usei a versão `9.5.0`)

**Observação:** Ao instalar o Node.js, o npm é instalado automaticamente. 🚀

## Instalação

Para instalar as dependências de desenvolvimento, execute:

```bash
npm install
Configurando variáveis de ambiente
Antes de rodar os testes, é necessário configurar algumas variáveis de ambiente.

Faça uma cópia do arquivo cypress.env.example.json com o nome cypress.env.json e preencha os valores apropriados para todas as variáveis.

Nota: O arquivo cypress.env.json não é rastreado pelo git, pois está listado no .gitignore.

Executando os testes
Neste projeto, você pode rodar os testes nos modos interativo e headless, tanto em visualização de desktop quanto de tablet.

Modo headless (sem interface)
Execute
npm test
(ou npm t) para rodar todos os testes no modo headless com viewport de desktop.

Execute:
npm run test:tablet
para rodar os testes no modo headless com viewport de tablet.

Modo interativo
Execute:
npm run cy:open
para abrir o Cypress App e rodar os testes no modo interativo com viewport de desktop.

Execute:
npm run cy:open:tablet
para abrir o Cypress App no modo interativo com viewport de tablet.

Opcional: Gravando os testes no Cypress Dashboard
Se quiser gravar a execução dos testes no Cypress Dashboard, você precisa passar a flag --record junto com a sua Record Key:

npx cypress run --record --key <sua_record_key>
Caso não queira gravar os testes, simplesmente execute:

npx cypress run
Sobre o uso de TypeScript
Se você estiver escrevendo testes com TypeScript, é importante ter um arquivo tsconfig.json na raiz do projeto. 

Exemplo básico:
{
  "compilerOptions": {
    "target": "ES6",
    "module": "commonjs",
    "strict": true
  },
  "include": ["cypress/**/*.ts"]
}
Nota: Este projeto utiliza JavaScript puro. Se aparecer um aviso sobre tsconfig.json, você pode ignorar com segurança.


