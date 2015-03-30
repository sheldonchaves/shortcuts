#linux install

	sudo apt-get update
#
	Apps: ========================

	sudo apt-get install virtualbox gcolor2 audacity remarkable
#
	browsers: ====================

	sudo apt-get install firefox chromium-browser google-chrome-stable
#
	dev: ====================
	
	sudo apt-get install git maven3 mysql-server adminer openvpn
#
	dev_extras: =====================

	sudo apt-get install brackets atom arduino
#
	extras: =====================

	sudo apt-get install filezilla libreoffice rar skype 
#
	codecs: =====================

	sudo apt-get install ubuntu-restricted-extras ubuntu-restricted-addons mplayer mpg123
#
	Java: =====================

	sudo apt-get install openjdk-7-jdk openjdk-8-jdk 

	sudo apt-get install oracle-java7-installer oracle-java7-set-default
#
	Prompt: =====================

	sudo gedit ~/.bashrc	

	function git_branch_name() {
		git branch 2>/dev/null | grep -e '^*' | sed -E 's/^\* (.+)$/(\1) /'
	}
	function show_colored_git_branch_in_prompt() {
		PS1="\[\033[01;32m\]\u@\h:\[\033[01;34m\]\w\[\033[31m\]\$(git_branch_name)\[\033[m\]$ "
	}
	show_colored_git_branch_in_prompt
http://hltbra.blogspot.com.br/2010/05/prompt-colorido-e-com-git-branch.html

eclipse

chrome ext : ======================

Chrome Poster
JSONView
