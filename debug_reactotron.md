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
import Reactotron from 'reactotron-react-native';

const tron = Reactotron.configure()
  .useReactNative()
  .connect();

tron.clear();

console.tron = tron;
```

- fazer o import ReactotronConfig dentro do arquivo no qual vc quer debugar

`import ReactotronConfig from './config/ReactotronConfig';`

------------

Para mostrar os console.log no Reactotron:

`console.tron.log('Teste');`

------------

### Caso queira rodar ele em um dispositivo fisico ( decubra o seu ip e coloque o connect da seguinte forma)

```js
import Reactotron from 'reactotron-react-native'

const tron = Reactotron.configure()
  .useReactNative()
  .connect()
  .configure({ host: '192.168.0.0' })

tron.clear()

console.tron = tron
```