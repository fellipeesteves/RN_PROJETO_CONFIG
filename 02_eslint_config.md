## Eslint config - baseado nas config do airbnb

* #### Primeiro instalar o eslint global

`yarn global add eslint`

_(no seu editor de texto instalar o pacote do eslint)_

VS Code

> [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint 'marketplace visualstudio')

Atom

> [Linter-eslint](https://atom.io/packages/linter-eslint 'marketplace atom')

Sublime Text

> [SublimeLinter](https://packagecontrol.io/packages/SublimeLinter)

---

* #### Verificar a última versão do eslint-airbnb
* #### Rode o comanado abaixo para no cmd ou terminal para verificar a ultima versão

`npm info "eslint-config-airbnb@latest" peerDependencies`

* #### Comando irá imprimir as seguintes informações (não copiar daqui pois, pode estar defasado)

```json
{
  "eslint": "^4.9.0",
  "eslint-plugin-import": "^2.7.0",
  "eslint-plugin-jsx-a11y": "^6.0.2",
  "eslint-plugin-react": "^7.4.0"
}
```

* _OBS o código acima virar com aspas simples ao invés de dupla ao passar para o json, não esquecer de mudar._

_Pegar a dependência de retorno e inserir no package.json no laço devDependences._

---

* #### Rodar comandos para instalar dependências

`yarn || npm install`

Logo após instalar as dependências acima, instalar os seguintes pacotes

`yarn add babel-eslint eslint-config-airbnb eslint-plugin-react-native --dev`

depois de instalar todas as dependencias criar o arquivo _.eslintrc_, na pasta raiz com seguinte codigo

> [.eslintrc - base curso goNative autor Diego Fernandes](https://gist.github.com/diego3g/fdc8dc51fd60b88e2e3611fb1b59d380 '.eslintrc')

ou

```json
{
  "parser": "babel-eslint",
  "env": {
    "browser": true,
    "jest": true
  },
  "plugins": ["react-native", "jsx-a11y", "import"],
  "extends": ["airbnb", "plugin:react-native/all"],
  "rules": {
    "react/jsx-filename-extension": [
      "error",
      {
        "extensions": [".js", ".jsx"]
      }
    ],
    "global-require": "off",
    "no-console": "off",
    "import/prefer-default-export": "off",
    "no-unused-vars": [
      "error",
      {
        "argsIgnorePattern": "^_"
      }
    ],
    "arrow-body-style": 0,
    "no-underscore-dangle": "off",
    "arrow-parens": [2, "as-needed"],
    "semi": "off",
    "function-paren-newline": ["error", "consistent"]
  },
  "settings": {
    "import/resolver": {
      "babel-module": {}
    }
  },
  "globals": {
    "__DEV__": true
  }
}
```

_No modelo do eslint acima, tem algumas regras adicionais que foram inseridas, por gosto pessoal._

* _Outra OBS: Lembrando que esse arquvivo ja tem um código para usar o babel resolver, caso você nao use, por favor remover_

```json
settings": {
  "import/resolver": {
    "babel-module": {}
  }
},
```
