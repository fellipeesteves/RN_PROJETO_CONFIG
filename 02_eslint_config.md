## Eslint config - baseado nas config do airbnb

- #### Primeiro instalar o eslint global

`yarn add global eslint`

_(no seu editor de texto instalar o pacote do eslint)_

VS Code

> [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint 'marketplace visualstudio')

Atom

> [Linter-eslint](https://atom.io/packages/linter-eslint 'marketplace atom')

Sublime Text

> [SublimeLinter](https://packagecontrol.io/packages/SublimeLinter)

---

- #### Para iniciar o uso do eslint no projeto é necessário realizar a instalação das dependencias usando os comandos:

* yarn add eslint -D
* yarn eslint --init
* -> Use a popular guide
* -> airbnb
* -> json

- Instalar todas as dependencias

- #### Logo em seguida instalar outras dependencias

* yarn add babel-eslint eslint-plugin-react-native -D

```json
{
  "parser": "babel-eslint",
  "extends": ["airbnb", "plugin:react-native/all"],
  "plugins": ["react-native", "jsx-a11y", "import"],
  "env": {
    "browser": true,
    "jest": true
  },
  "rules": {
    "react/jsx-filename-extension": [
      "error",
      {
        "extensions": [".js", ".jsx"]
      }
    ],
    "react-native/sort-styles": "off",
    "semi": "off",
    "global-require": "off",
    "no-console": "off",
    "import/prefer-default-export": "off",
    "no-unused-vars": [
      "error",
      {
        "argsIgnorePattern": "^_"
      }
    ]
  },
  "globals": {
    "__DEV__": true
  }
}
```
