# Gerando splash e icon

- _Usar imagens indicadas pelo site_

> [apetools](https://apetools.webprofusion.com/app/#/tools/imagegorilla)

_Projeto Android_

- Remover icones e splash padrão
- Inserir dentro da pasta os arquivos gerado pelo site acima "src/res""
- AndroidManifest.xml -> alterar android:icon="@drawable/nomeDoIcone"
- AndroidManifest.xml -> alterar android:icon="@drawable/nomeDoIcone"
- Na pasta values no arquivo styles.xml inserir o seguinte codigo

```xml
  <resources>

    <!-- Base application theme. -->
    <style name="AppTheme" parent="Theme.AppCompat.Light.NoActionBar">
        <item name="android:windowBackground">@drawable/nome_do_seu_arquivo</item>
    </style>

  </resources>
```

- No arquivo strings.xml -> alterar o nome que voce quer que aparecer como nome do aplicativo

```xml
  <resources>
    <string name="app_name">Nome_Do_App</string>
  </resources>
```

_Projeto iOS_

- Abrir o projeto pelo Xcode, (navegue dentro da pasta do seu projeto, encotrara a pasta "iOS", dentro dela, vera um arquivo para executar no xcode o projeto)
- Display Name -> Colocar nome do aplicativo que vai aparecer em Tela
- Bundle identifier -> Colocar o seu dominio
- Associe a seu time ou licença de desenvolvimento apple
- remover a LauchScreen Padrao
- Marcar "User asstes catalog"
- Inserir pastas dentro do projeto nas pasta "Images.Assets" _appIcon_ e _LauchScreen_
