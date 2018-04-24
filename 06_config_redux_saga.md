# Configração REDUX SAGA

### Instalar pacotes no projeto

* `yarn add redux react-redux`
* `yarn add reactotron-redux` _caso use o reactotron_
* `yarn add redux-saga`
* `yarn add reactotron-redux-saga` _caso use o reactotron_

Dentro da pasta _src_ criar uma pasta chamada _store_ e dentro dela o arquivo _index.js_ com o seguinte conteúdo:

```js
import { createStore, applyMiddleware } from 'redux'
import createSagaMiddleware from 'redux-saga'
import reducers from './ducks'
import sagas from './sagas'

const sagaMonitor = __DEV__ ? console.tron.createSagaMonitor() : null
const sagaMiddleware = createSagaMiddleware({ sagaMonitor })

const middleware = [sagaMiddleware]

const createAppropriateStore = __DEV__ ? console.tron.createStore : createStore
const store = createAppropriateStore(reducers, applyMiddleware(...middleware))

sagaMiddleware.run(sagas)

export default store

```

Dentro da pasta _store_ , criar a pasta _ducks_ e dentro dela o _index.js_ com o seguinte conteúdo:

```js
import { combineReducers } from 'redux'

export default combineReducers({
  empty: (state = {}) => state,
})

```

Dentro da pasta _store_ , criar a pasta _sagas_ e dentro dela o _index.js_ com o seguinte conteúdo:

```js
import { all } from 'redux-saga/effects'

export default function* rootSaga() {
  return yield all([])
}

```

Dentro da raiz _src_ no arquivo _index.js_ inserir os seguintes imports

_Lembrando que estou utilizando o babel module resolve para usar os caminhos relativos dos arquvios_

```js
import React from 'react'
import { Provider } from 'react-redux'
import { View } from 'react-native'

import 'config/ReactotronConfig'
import store from 'store'

const App = () => (
  <Provider store={store}>
    <View />
  </Provider>
)

export default App

```

Dentro do pasta config no arquivo _ReactotronConfig.js_

```js
import Reactotron from 'reactotron-react-native'
import { reactotronRedux } from 'reactotron-redux'
import sagaPlugin from 'reactotron-redux-saga'

const tron = Reactotron.configure()
  .useReactNative()
  .use(reactotronRedux())
  .use(sagaPlugin())
  .connect()

tron.clear()

console.tron = tron

```