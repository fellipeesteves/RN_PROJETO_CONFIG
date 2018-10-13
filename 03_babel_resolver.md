# Babel Resolver

#### Definir a pasta src como padrao do projeto, caminho relativo, remover o './'

##### \* Abra o terminal na pasta do projeto e insira os seguintes comandos, para que possamos fazer a instalação:

- `yarn add babel-plugin-module-resolver --dev`

```json
{
  "presets": ["react-native"],
  "plugins": [
    [
      "module-resolver",
      {
        "cwd": "babelrc",
        "root": ["./src"],
        "extensions": [".js", "ios.js", "android.js"],
        "alias": {
          "test": "./test",
          "underscore": "lodash"
        }
      }
    ]
  ]
}
```

Para funcionar corretamente, vamos instalar dois módulos do ESLint, o eslint-plugin-import e o eslint-import-resolver-babel-module:

- `yarn add eslint-plugin-import eslint-import-resolver-babel-module --dev`

* _Dentro do arquivo .babelrc, que se encontra na raiz do seu projeto colocar as seguinte código._

- Logo apos salvar e fechar o _.babelrc_, abra o arquivo _.eslintrc_ e logo acima da opção "dev", inserir o seguinte codigo, ou acima do globals

```json
"settings": {
    "import/resolver": {
      "node": {
        "paths": ["src"]
      },
      "babel-module": {}
    }
  },
```
