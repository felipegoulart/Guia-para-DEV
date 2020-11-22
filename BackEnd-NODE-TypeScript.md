# Anotações sobre Back-End com NODE

## Instalando NODE.
1. Acesse <https://nodejs.org> e escolha a versão desejada.
2. Dê preferência para a versão LTS.<br>
 _A versão LTS foi mais testada e contém menos BUGS Por isso de a preferência a ela._
3. Baixe a versão escolhida e instale.

## Iniciando Back-End com NODE e TypeScript
> * Os comandos a seguir são inseridos no terminal. 
> * Yarn é um gerenciador de pacotes do node. Com eles você pode instalar bibliotecas necessárias no projeto.
> * Você pode instalar yarn digitando o comando `npm install -g yarn`, para fazer uma instalação global.
* yarn/npm init -y
* yarn add typescript -D

## Configurações em arquivos
1. yarn tsc --init
2. Vá ao arquivo **tsconfig.json** e mude:

  > `strictPropertyInitialization = true` para `false`<br> _Isso vai fazer com que não acuse alguns erros em classes do ORM_ 

  > `"target": "es5"` para `es2017`

3. No arquivo **package.json** crie as linhas:
  ~~~json
  "script": {
    "dev": "ts-node-dev --transpile-only --ignore-watch node_modules ./src/server.ts",

    // Se for usar typeorm vc deve usar a cli dele com typescript

    "typeorm": "ts-node-dev ./node_modules/typeorm/cli.js"
  }
  ~~~ 
~~~javascript
import express from 'express'
~~~