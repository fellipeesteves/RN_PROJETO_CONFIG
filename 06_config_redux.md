# Configração REDUX

* Instalar pacotes no projeto

`yarn add redux react-redux`

* Dentro da pasta src criar uma pasta _store_ e dentro dela o arquivo _index.js_

```js
import { createStore } from 'redux'
const store = createStore(() => {})

export default store
```

* Dentro da raiz _src_ no arquivo* index.js* inserir os seguintes imports

_Lembrando que estou utilizando o babel module resolve para usar os caminhos relativos dos arquvios_

```js
import { Provider } from 'react-redux'
import store from 'store'

<Provider store={store}>
  <View />
</Provider>
```

* Criar pasta reducers dentro da Store

* Pacote para o Reactotron pegar as features do redux

`yarn add reactotron-redux`

* No arquivo onde está importando o redux colocar o código

* _Lembrando que essas configuraçoes estão associadas ao uso do reactotron_

```js
import { createStore, applyMiddleware } from 'redux'
import reducers from './reducers'

const middleware = []

const createApppropriateStore = __DEV__ ? console.tron.createStore : createStore
const store = createApppropriateStore(reducers, applyMiddleware(...middleware))

export default store
```
