# Configração REDUX

* Instalar pacote no projeto

`yarn add redux react-redux`

* Dentro da pasta src criar uma pasta _store_ e dentro dela o arquivo _index.js_

```js
import { createStore } from 'redux'
const store = createStore(() => {})

export default store
```

* Dentro da raiz _src_ no arquivo* index.js* inserir os seguintes imports

```js
import { Provider } from 'react-redux'
import store from 'store'

<Provider store={store}>
  <View />
</Provider>
```

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
