#GIT

### alterando origin
	git remote rm origin
	git remote add origin https://sheldonchaves@bitbucket.org/rlenzi365/abril-commerce.git
	git branch --set-upstream-to=origin/master

### alterando de SSH pra HTTPs
	git remote set-url origin https://github.com/USERNAME/OTHERREPOSITORY.git
	//or
	git remote set-url origin git@github.com:USERNAME/OTHERREPOSITORY.git

###Ferramentas de configuração (define quem fez as atualizações)
	$ git config –global user.name "[nome/nick do desenvolvedor]"
Define o nome ou o apelido de quem realiza as alterações, o nome é enviado ao GIT e descreve quem realizou a alteração de maneira simples.

	$ git config –global user.email "[e-mail do desenvolvedor]"
Define o e-mail de quem realiza as alterações, o e-mail é enviado ao GIT e descreve quem realizou a alteração de maneira simples.

	$ git config –global color.ui auto
As interações por linha de comando ficam coloridas com esse comando.

###Criar Repositórios (inicia um novo repositório ou obtém de um já existente)
	$ git init [nome do projeto]
Cria um novo repositório local com um nome já definido

	$ git clone [url]
Baixa um projeto e os históricos de versões

###Fazendo atualização pontual (revisão de alterações commit manual de alterações)
	$ git status
Lista todas as alterações que precisam ser comitadas
	
    $ git diff
Apresenta as diferenças entre arquivos que não estão staged
	
    $ git add [files]
Adiciona o arquivo para o grupo (staged) que será comitado
	
    $ git diff –staged
Apresenta as diferenças entre os arquivos staging e a ultima versão.
	
    $ git reset [file]
Remove o arquivo do grupo (staged) que será comitado mas preserva seu conteúdo.
	
    $ git commit -m "[descrição da alteração]"
Gera um snapshot que pode ser utilizado futuramente para roolback por exemplo. Isso não gera uma versão apenas um snapshot, isso é importante para que as alterações sejam documentadas. Essa operação é realizada apenas localmente.

###Fazendo atualizações para entregar uma funcionalidade
	$ git branch
Lista todos os branches (termo que podemos utilizar para definir versões funcionais)
	
    $ git branch [nome de uma nova branch]
Cria uma nova branch com o nome informado
	
    $ git checkout [nome de uma branch existente]
Altera o conteúdo do local de trabalho para o snapshot da branch informada
	
    $ git merge [nome de uma branch existente]
Combinará o código da branch informada com o conteúdo da branch atual que o git esta configurado no instante.
	
    $ git branch -d [nome de uma branch existente]
Remove a branch informada

###Remover arquivos
	
    $ git rm [file]
Remove o arquivo do local de trabalho e do stage
	
    $ git rm –cached [file]
Remove o arquivo do stage mas não remove do local de trabalho
	
    $ git mv [nome do arquivo original] [novo nome do arquivo]
Altera o nome do arquivo local e na area do stage, pronto para comitar.

###Removendo arquivos e diretórios de commit acidental/indevido
	*.log
	build/
	temp-*
Esse é deve ser o conteúdo do .gitignore nesse arquivo ficam todos os diretórios arquivos ou padrões de arquivos que não devem ser comitados.

	$ git  ls-files –other –ignored –exclude-standard
Lista todos os arquivos ignorados nesse projeto

###Como salvar alterações incompletas sem comitar
	
    $ git stash
Seria como um commit temporário não oficial.
	
    $ git stash pop
Recupera os arquivos que foram salvo pelo stash
	
    $ git stash list
Lista todos os stash realizados e não recuperados
	
    $ git stash drop
Descarta os stash mais recente realizado.

###Histórico
	
    $ git log
Lista o histórico das versões da branch atual
	
    $ git log –follow [file]
Lista o histórico de versão de um arquivo, incluindo se também foi renomeado
	
    $ git diff [nome da primeira branch] [nome da segunda branch]
Apresenta a diferença entre as duas branch
	
    $ git show [nome ou código de um commit]
Apresenta todos os detalhes  as mudanças de um commit especifico

###Rollback dos commits realizados
	
    $ git reset [nome do commit_1]
Desfaz todos os commits após o commit_1, mantendo as alterações locais
	
    $ git reset –hard [nome do commit_1]
Descarta todos os histórico de mudanças após o commit_1 e atualizada a área de trabalho com a versão do commit_1

###Atualizando o servidor com os commits locais
	
    $ git fetch [geralmente utilizam o nome "origin”]
Faz download de todo o histórico do repositório, nesse exemplo seria do "origin”
	
    $ git merge [geralmente utiliza o nome "origin”]/[nome de uma branch]
Combina o branch do origin com a branch local
	
    $ git push [geralmente utilizam o nome "origin”] [o nome da branch remota]
Faz upload de todo o conteúdo local  para o servidor do Git
	
    $ git pull
Faz o download de todo histórico do repositório incluindo as mudanças

### Merge branch to master

    git checkout newMaster
    git merge --strategy=ours master    # mantem o conteudo da branch e grava um merge
    git checkout master
    git merge newMaster             	# faz o merge da master com a newMaster



#GIT

	git remote -v
	//ver origin do repositorio
#

	git checkout -b teste
	//Cria e ja entra na branch
#

	git checkout --orphan teste
	//Cria uma branch "sem pai"chamada teste
#

	git branchs
	//Mostrar as branchs remotas e locais	
#

	git push -u origin design
	//Para enviar nova branch	
#

	git checkout -t origin/XXX
	//checkout na branch remota, ja copiando o conteudo remoto para local	
#

	git push origin :XXX
	//Deletar branch remota XXX	
#

	git users
	//Lista usuarios projeto	
#

	git last
	//Show commits since last pull	
#

	git reset HEAD~1 --soft
	//remove ultimo commit e mantem arquivos	
#

	git reset HEAD~1 --hard
	//remove ultimo commit e arquivos	
#

	git rm --cached XXX
	//Retirar o arquivo XXX do commit	
#

	git clean -f
	//remove arquivos untrackeds	
#

	git clean -fd
	//remove arquivos e diretorios untrackeds	
#

	gedit ~/.gitconfig
	//editar atalhos
