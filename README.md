# Commands of git

iniciar um repositorio git
```
git init
```

- verificar status 
```
git status
```

- prepapar arquivo para commit
```
git add arquivo.ext
```

- preparar todos os arquivos para commit
```
git add .
```

- commitar arquivos
```
git commit -m "Mensagem"
```

- commitar sem preparar - direto
```
git commit -a -m "Mensagem"
```

- retirar arquivo do preparo para commitar (unstage)
```
git reset HEAD arquivo.ext
```

- voltar versao de um commit
- obs.: cria um branch separado.
```
git checkout 01f3//..... <- hash completo
``` 

- Voltar para branch principal
``` 
git checkout master
```

- Voltar commit 
1. ~1 quantos commits quer voltar
2. --soft - volta com arquivo preparado para commitar
 
```
git reset HEAD~1 --soft 
```

- Voltar commit 
1. ~1 quantos commits quer voltar
2. --hard - remove os arquivos do commit 
####  CUIDADO ##
```
git reset HEAD~1 --hard
```

- retirar alterações de um arquivo commitado
```
git checkout -- arquivo.ext
```


## Examples - LOG #

- Log completo com alterações
```
git log -p
```

- Log completo com alterações - 2 = ultimos 2 commits
```
git log -p -2
```

- Estatisticas dos últimos commits
```
git log --stat
```

- Todos os commits em linha
```
git log --pretty=oneline
```

- formatando os commits:

1. -%h = inicio do hash (md5)
2. -$an = quem commitou - usuario
3. -%ar = commitou ha quanto tempo - 6 minutes ago
4. -%s = descrição do commit - "initial commit"

. Example: 92883a0 -Wellington Ribeiro, 6 minutes ago : Commit all files changes
```
git log --prety=format:"%h - %an, %ar : %s";
```

- Ultimo commit realizado a = 2.minutes / 2.days / 2.hours ....
```
git log --since=2.minutes
```


### Trabalhando com branchs (galhos) ##

- criando um branch
1. '-b branch'
```
git checkout -b nomeDoBranch
```

- Saber qual branch estou
```
git branch
```

- trocar de branch
```
git checkout nomeDoBranch
```

- merge branchs (grudar os branchs)
```
git merge nomeDoBranch
```

- rebase commit - organiza os commits
1.  retira a necessidade do commit do commit do merge
- A diferença do merge é que ele não reordena os commits
```
git rebase nomeDoBranch
```

- remover um branch
```
git branch -D nomeDoBranch
```

### Modulo GitHub ##

- Gerar chave ssh
```
ssh-keygen
```

- Adiciona ao repositorio remoto
```
git remote add origin git@github.com:User/Repository.git
```

- Sobe os arquivos para o repositorio remoto
```
git push -u origin master
```

- Subir arquivos depois do commit
```
git push orgin master
```

- Clonar repositorio do GitHub
```
git clone https://url.gitHub
```

- Visualizar todos os branchs (Locais e remotos)
```
git branch -a
```

- enviar branch para servidor remoto
```
git push origin nomeDoBranch
```

- Pegar os branchs remotos
1. branchLocal -> nome do branch local
2. origin/branchRemoto -> localizacao do branch Remoto
```
git checkout -b branchLocal origin/branchRemoto
```

- verificar se arquivos estao sincronizados
```
git pull
```

- Puxar as alterações do repositorio remoto
```
git pull orign master
```

- Removendo branch remoto
```
git push origin :nome-do-branch
```

### TAGs ##
##### Releases - Versões

- Criar uma tag
1. 1.0.0 -> valor da tag, ou versão do sistema
```
git tag 1.0.0
```

- Listar todas as tags
```
git tag -l
```

- Enviar tag para repositorio remoto
```
git push origin master --tags
```

- remover tag local
```
git tag -d 1.0.0
```

- remover tag remota
```
git push origin :refs/tags/1.0.0
```

```
 Verionamento Semantico
 1.0.0 
 1.    -> versao principal do sistema - MAJOR 
 		   quebra compatibilidade
 1.0   -> versao dentro de uma versao - MINOR 
 		   pode quebrar compatibilidade
 1.0.0 -> melhorias e correcoes de erros - PATCH
		   não quebra compatibilidade
		   
	http://semver.org/
```

















