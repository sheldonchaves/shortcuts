#CSS

##position:
	static
	// padrão

	absolute
	// posicao relativo ao primeiro pai com algum position
	// sai do fluxo

	relative
	// a posicao continua normal (como se layer)

	fixed
	// posicao em relacao a janela 
	// sai do fluxo

##display
	inline
	// perde width e height

##clear
	// principalmente controle do float
	// referente apenas ao elemento
	// ex.: clear:left >> mantem a esquerda limpa, se tiver elemento, desce

##float
	// sai do fluxo

##seletores
	div[class|="menu"] {
	// seleciona todas as <div> que o atributo class comece com menu
	// ex.: menu-teste, menu-exemplo

	div[class*="footer"] {
	// seleciona todas as <div> que o atributo class contenha a palavra footer
	// ex.: menu-footer, footer-exemplo