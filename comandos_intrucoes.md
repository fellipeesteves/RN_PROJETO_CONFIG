#### Rodar comando apenas quando for instalar ele pela primeira vez
` react-native run-ios || react-native run-android `

------------

#### Rodar comando quando so alterou código JS
` react-native start `

------------

#### Rodar comando quando for uma instalação de pacotes que precisam ser linkados ao projeto iOS ou android
` react-native link `

------------

#### Rodar comando quando obtiver erro de tela vermelha
` react-native start --reset-cache `

------------

#### Component Stateless
```js
About = ({ props }) => (
	<View>
		<Text>{props.about}</Text>
    	<Text>{props.back}</Text>
		<Text>Go to Contact</Text>
	</View>
);
```

------------

#### Component Class
```js
export default class About extends Component {
	render() {
		const { about, back } = this.props;
		return (
			<View>
				<Text>{about}</Text>
					<Text>{back}</Text>
					<Text>Go to Contact</Text>
		  </View>
		);
	}
}
```