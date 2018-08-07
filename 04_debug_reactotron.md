# Reactotron

Baixar o reactotron e olhar a documentação
>https://github.com/infinitered/reactotron

Quick Start for React Native
> https://github.com/infinitered/reactotron/blob/master/docs/quick-start-react-native.md

------------

- Instalar dependencias no projeto

`npm i --save-dev reactotron-react-native`

- Criar pasta config dentro do src e criar o arquivo

*ReactotronConfig.js*

com o seguinte conteúdo
```js
import Reactotron from 'reactotron-react-native'

if (__DEV__) {
  const tron = Reactotron
    .configure()
    .useReactNative()
    .connect()

  tron.clear()

  console.tron = tron
}
```

- fazer o import ReactotronConfig dentro do arquivo no qual você quer debugar

*_Caso esteja usando o babel module resolver_

```js
import ReactotronConfig from 'config/ReactotronConfig';
```

*_Caso não esteja usando o babel module resolver, mapear de acordo com caminho criado por você_

```js
import ReactotronConfig from './config/ReactotronConfig';
```

------------

Para mostrar os console.log no Reactotron:

`console.tron.log('Teste');`

------------

### Caso queira rodar ele em um dispositivo fisico ( decubra o seu ip e coloque o connect da seguinte forma)

#### * _Para descobrir o seu ip:_

```js
  add shell ip route
```

#### * _Não esqueceur de linkar os seu dispositivo com o seguinte comando:_

```js
  adb reverse tcp:9090 tcp: 9090
```

```js
import Reactotron from 'reactotron-react-native'

const tron = Reactotron
  .configure()
  .useReactNative()
  .connect()
  .configure({ host: '192.168.0.0' }) // no meu caso esse foi o meu ip

tron.clear()

console.tron = tron
```