#linux2

	// contando a quantidade de linhas
	cat file | wc -l  
	grep -c '.*' file  
#
	//reverse string
	echo linux and life | rev 
#
	// swap colunas
	awk -F, '{print $2,$1,$3}' OFS=, file
	Output:
	teste1,teste2,teste3 > teste2,teste1,teste3
#
	//display line number
	nl file 
	cat -n file
#
	//read 2 files alternatively line by line
	paste -d"\n" file1 file2
	Output:
	file1_1
	file2_1
	file1_2
	file2_2
	file1_3
	file2_3
#
	//last command of app. ex.: vim
	!vim
#
	// history commands
	history | grep "mv" 
#
	// Ctrl + R
	search commands