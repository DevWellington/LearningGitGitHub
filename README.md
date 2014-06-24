# Commands of git

- iniciar um repositorio git
`git init`

 verificar status 
`git status`

 prepapar arquivo para commit
`git add arquivo.ext`

 preparar todos os arquivos para commit
`git add .`

 commitar arquivos
`git commit -m "Mensagem"`

 commitar sem preparar - direto
`git commit -a -m "Mensagem"`

 retirar arquivo do preparo para commitar (unstage)
`git reset HEAD arquivo.ext`

 voltar versao de um commit
 obs.: cria um branch separado.
`git checkout 01f3` //..... <- hash completo

 Voltar para branch principal
`git checkout master`

 Voltar commit 
 ~1 quantos commits quer voltar
 --soft - volta com arquivo preparado para commitar
 
`git reset HEAD~1 --soft `

 Voltar commit 
 ~1 quantos commits quer voltar
 --hard - remove os arquivos do commit 
  CUIDADO 
`git reset HEAD~1 --hard`

 retirar alterações de um arquivo commitado
`git checkout -- arquivo.ext`


## Examples - LOG

 Log completo com alterações
`git log -p`

 Log completo com alterações - 2 = ultimos 2 commits
`git log -p -2`

 Estatisticas dos últimos commits
`git log --stat`

 Todos os commits em linha
`git log --pretty=oneline`

 formatando os commits:

 -%h = inicio do hash (md5)
 -$an = quem commitou - usuario
 -%ar = commitou ha quanto tempo - 6 minutes ago
 -%s = descrição do commit - "initial commit"

 Example: 92883a0 -Wellington Ribeiro, 6 minutes ago : Commit all files changes
`git log --prety=format:"%h - %an, %ar : %s";`

 Ultimo commit realizado a = 2.minutes / 2.days / 2.hours ....
`git log --since=2.minutes`


###Trabalhando com branchs (galhos)

 criando um branch
 '-b branch'
`git checkout -b nomeDoBranch`

 saber qual branch estou
`git branch`

 trocar de branch
`git checkout nomeDoBranch`

 merge branchs (grudar os branchs)
`git merge nomeDoBranch`

 rebase commit - organiza os commits
  retira a necessidade do commit 
  do commit do merge
   - A diferença do merge é que ele não reordena os commits
		
`git rebase nomeDoBranch`

 remover um branch
`git branch -D nomeDoBranch`

### Modulo GitHub

# Gerar chave ssh
`ssh-keygen`


