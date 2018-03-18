| Comando | Descrição |
| ------------- | ------------------------------ |
| `git config --global user.name` | Define um nome padrão para o usuário |
| `git config --global user.email` | Define um email padrão para o usuário  |
| `git config --global -l`               | Verifica todas as configurações padrão   |
| `git init`                                     | Inicia o git no projeto                               |
| `git status`                                 | Verifica arquivos que que sofreram alteração |
| `git add` | Informar para o git os arquivos que serao adicinados na historia |
|`git commit` | Criar o ponto na historia -m "mensagem do commit" (indicar alteração no codigo) |
|`git log`| Ver todos os pontos de commit que ja foram feitos ("q", para fechar) |
|`git diff`| Mostrar alteraçoes antes do git add (\*.html, add tudo com essa extensao) |
| *.gitignore* |  Serve para remover pastas o arquivos no quais você não quer que suba para o git exemplo { node_modules/ } |
|`git log + commit && git checkout + cod` | Voltar versao |
|`git checkout "nome"`|  Para mudar de branch no projeto |
|`git branch "nome"` | Cria um novo ramo (novo espaço de trabalho)|
|`git branch` | Mostra todos os ramos disponiveis|
| `git merge "nome da branch" `| Voltar para branchq vc quer rodar |
| `git branc -D "nome brench" `| Deleta o caule e manter so o master (o git q vc ira usar)|
|`git remote add origin "add url"`| vincular repositorio online no local |
|`git remote -v `| Mostra os repositorios remotos|
|`git push origin master`| Subir as alteraçoes |
|`git clone "url do projeto"`| baixar projeto |