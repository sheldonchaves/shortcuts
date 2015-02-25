#GIT

	git checkout -b teste
	//Cria e ja entra na branch
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