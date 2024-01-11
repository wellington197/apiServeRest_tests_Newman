# Automação de testes de API com Postman e criação de Pipeline
Esta é a collection de testes da API de ServeRest do site https://serverest.dev/ utilizando o postman e Newman e subindo CI

## O que é?

## Tecnologias
- Postman versão web
- node version v16.13.2
- Newman 5.3.2
- Newman-reporter-htmlextra
- Git actions

## Documentações
- Análise Técnica: Analise/
- Doc da API: [Consultar Swagger da API serverRest](https://serverest.dev/)


## Como instalar o ambiente
- Primeiro: Instalar o node em seu computador [Baixe o Node](https://nodejs.org/en/download/current)
- Segundo: Instalar o Newman de forma global [Baixe as dependências do newman](https://www.npmjs.com/package/newman)

```
npm install -g newman
```

- Terceiro: Instalar as depedênbcias de relatórios (Opcional) [newman-reporter-html](https://www.npmjs.com/package/newman-reporter-html)
```
npm -g newman-reporter-html
```
ou também pode usar o npm i newman-reporter-htmlextra. Com opções mais estilizadas [newman-repórter-htmlextra](https://www.npmjs.com/package/newman-reporter-htmlextra)
```
npm install -g newman-reporter-htmlextra
```
## Como rodar os testes
### Pelo Postman ou desktop
- Import a collection e o environment
<img src="https://github.com/wellington197/apiServeRest_tests_Newman/assets/98292924/c9b322e6-b426-4a77-8b07-ae1bb9efe062" width="500" height="250">

- Execute os testes de forma manual ou automatizado

### Pelo Newman (Via console)
- Abra o console de sua preferência
- Execute a seguinte linha de comando para rodar os testes, e visualizar a ação no console
```
newman run servRest.postman_collection.json -e servRest_test.postman_environment.json -r cli
```
<img src="https://github.com/wellington197/apiServeRest_tests_Newman/assets/98292924/98df5b66-1c47-49f3-9b33-60c1e682e15d" width="500" height="500">

- Execute os testes com relatório
```
newman run servRest.postman_collection.json -e servRest_test.postman_environment.json -r htmlextra
```
<img src="https://github.com/wellington197/apiServeRest_tests_Newman/assets/98292924/5184af62-7a3b-445d-9c24-954732283af5" width="500" height="500">


### Report

Ao rodar os testes com htmlextra, será gerado arquivo em html com o resultado dos testes. O arquivo encontra-se na pasta de **newman** que foi criado no local em que os arquivos de collection e environment se encontram.

![image](https://github.com/wellington197/apiServeRest_tests_Newman/assets/98292924/4a0c793f-45c9-4f76-bd8b-eab53f126366)



## Entre em contato

email: fco.learning@gmail.com
