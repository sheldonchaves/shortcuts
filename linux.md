#linux

	ls -la
	//Lista com detalhes
#
	rm -r XXX
	//remove diretorio XXX recursivo
#
	cp -r XX YY
	//copia dir XX para YY recursivo
#
	mv teste1.txt XXX
	//mover teste1.txt para XXX
#	
	mv teste1.txt teste2.txt
	//renomear teste1 > teste2
#
	Echo "teste" > teste.txt
	//altera o conteudo/cria arquivo
#
	Echo "teste2" >> teste.txt
	//incrementa conteudo
#
	tar -cz work > work.tar.gz
	//compactar tar gz
#
	tar -xz < work.tar.gz
	//descompactar tar gz
#
	ps -ef | grep firefox
	//Processos com o texto firefox
#
	Kill 17322
	//matar Processo 17322 (-9 = force)
#
	killall -9 firefox
	//matar processos firefox
#
	chmod +x teste.sh
	//mudar pemissao + ou - (x r w)
#
	locate firefox
	//localizar arquivo
#
	which firefox
	//localizar app
#
	env | grep PATH
	//variaveis de ambiente
#
	PATH=$PATH:/home/sheldon/workspace  
	//PATH temporario (: > adiciona)
#
	sudo apt-get update
	apt-cache search XXX  
	sudo apt-get XXX  
	sudo apt-get remove XXX  
#
	dpkg -i setup.deb
	//instalar o pacote
#
	dpkg -r nome_pacote
	//remover o pacote
#
	service nome_servico start
	//Serviços start ou stop
#
	ls /etc/init.d/
	//path services startup
#
	ssh usuario@192.168.0.8
	//conectar SSH
#
	ssh -X usuario@192.168.0.8
	//conectar modo grafico
#
	scp t.zip user@192.168.0.8:/home
	//ssh copiar arquivo local destino