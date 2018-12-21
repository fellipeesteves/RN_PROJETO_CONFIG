# Babel Root import

#### Definir a pasta src como padrao do projeto, caminho relativo, remover o './'

##### \* Abra o terminal na pasta do projeto e insira os seguintes comandos, para que possamos fazer a instalação:

- `yarn add babel-plugin-root-import -D`

##### \* Logo em seguida edite o arquibo _.babelrc_


```json
{
  "presets": ["module:metro-react-native-babel-preset"],
  "plugins": [
    [
      "babel-plugin-root-import",
      {
        "rootPathSuffix": "src"
      }
    ]
  ],
  "env": {
    "production": {
      "plugins": [
        [
          "babel-plugin-root-import",
          {
            "rootPathSuffix": "src"
          }
        ]
      ]
    }
  }
}
```

##### \* Depois adicionar o seguinte pacote:

* yarn add eslint-import-resolver-babel-plugin-root-import -D

##### \* Depois adicionar o codigo no arquivo _.eslintrc.json_

```
"settings": {
    "import/resolver": {
      "babel-plugin-root-import": {}
    }
  }
```

##### \* criar o arquivo _jsonconfig.json_ e adicionar os seguintes comandos para que o vsCode possa completar os caminhos das pastas!

```
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "~/*": ["src/*"]
    }
  }
}
```
