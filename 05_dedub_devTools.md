# Instalar reactdevTools

- Olhe a documentação caso tenha duvidas:

> [Documentação]('https://github.com/facebook/react-devtools/blob/master/packages/react-devtools/README.md')

- Executar para instalar globalmente
  `yarn global add react-devtools`

- Executar o seguinte comando dentro do seu projeto

`yarn add react-devtools --dev`

- Criar pasta Config dentro do src (ignoarar caso tenha seguido os tutorias anteriores)
- Dentro da pasta Config criar o arquivo DevToolsConfig.js

- Dentro do arquivo DevToolsConfig.js, colocar o seguinte codigo

- Esse comando é para que seja apenas executado no ambiente de desenvolvimento)

```js
if (__DEV__) {
  require('react-devtools')
}
```

- Fazer o import DevToolsConfig dentro do arquivo no qual vc quer debugar(inspencionar elementos)

```js
import DevToolsConfig from 'config/DevToolsConfig'
```

- Dentro do package.json, inserir o seguinte comando "react-devtool":"react-devtools"

```json
"scripts": {
  "start": "node node_modules/react-native/local-cli/cli.js start",
  "test": "jest",
  "react-devtool":"react-devtools",
},
```

- Dentro do terminal rodar o seguinte comoando

`yarn run react-devtool`
