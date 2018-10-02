# Babel Resolver

#### Definir a pasta src como padrao do projeto, caminho relativo, remover o './'

##### \* Abra o terminal na pasta do projeto e insira os seguintes comandos, para que possamos fazer a instalação:

`npm install -D babel-plugin-module-resolver eslint-import-resolver-babel-module`
`yarn add babel-plugin-module-resolver eslint-import-resolver-babel-module --dev`

- _Dentro do arquivo .babelrc, que se encontra na raiz do seu projeto colocar as seguinte código._

```json
{
  "presets": ["react-native"],
  "plugins": [
    [
      "module-resolver",
      {
        "cwd": "babelrc",
        "root": ["./src"],
        "extensions": [".js", "ios.js", "android.js"]
      }
    ]
  ]
}
```

- Logo apos salvar e fechar o _.babelrc_, abra o arquivo _.eslintrc_ e logo acima da opção "dev", inserir o seguinte codigo, ou acima do globals

```json
"settings": {
  "import/resolver": {
    "babel-module": {}
  }
},
```
