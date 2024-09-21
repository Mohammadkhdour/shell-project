#Name: Mohammad Khdour
#ID:1212517
command=("cat" "cut" "ls" "mv" "grep" "date" "clear" "expr" "tr" "pwd" "wc" "paste" "rm" "head")
while true
do
echo -e "\n1)Generate the manual for commands"
echo -e "2)Print list of commands"
echo "3)write example for command"
echo "4)verify for command"
echo "5)Search for command or word"
echo "6)Recommend command"
echo "7)EXIT"
echo -e "\nEnter Number"
read number
case "$number"
in

1 ) for i in "${command[@]}"; do
if [ ! -e $i.txt ]; then
touch $i.txt
fi
  echo "$(man $i |awk '/^DESCRIPTION$/,/^$/' |grep -v '^$')" > $i.txt
  echo -e "\n__________________________________________________________________\n" >> $i.txt
  echo "$(man $i |awk '/^SYNOPSIS$/,/^DESCRIPTION$/' |grep -v '^DESCRIPTION$')" >> $i.txt
  echo -e "\n__________________________________________________________________\n" >> $i.txt
if [[ "$i" = "cat" ]]; then

	echo -e "EXAMPLES\n	 should we have a file to print contants" >> $i.txt
	filename=file.txt
	echo -e "	 we assume we have file called $filename\n" >> $i.txt
	echo -e "	 we use echo " hello world"  > $filename" >>$i.txt
	echo " hello world" > $filename
	echo -e "	 cat $filename\n" >> $i.txt
	EXAMPLE_cat=$(cat $filename)
	echo -e "	 $EXAMPLE_cat" >> $i.txt
	rm -r $filename

elif [[ "$i" = "cut" ]]; then

	echo -e " EXAMPLES\n	cut should be related with string" >> $i.txt
	echo -e " 	echo " cut my name mohammad " | cut -c12- " >> $i.txt
	EXAMPLE_cut=$(echo " cut my name mohammad" | cut -c13-)
	echo -e " 	Output will be:$EXAMPLE_cut" >> $i.txt

elif [[ "$i" = "ls" ]]; then
	echo -e "EXAMPLES\n	ls\n	$(ls)" >> $i.txt
	EXAMPLE_ls=$(ls)
elif [[ "$i" = "mv" ]]; then
	echo -e "EXAMPLES\n	rename the file marks.txt to grade.txt" >> $i.txt
	
	touch marks.txt
	echo -e "	$(ls | grep marks)" >> $i.txt
	echo -e "	mv marks.txt grade.txt" >> $i.txt
	mv marks.txt grade.txt
	EXAMPLE_mv=$(ls | grep grade)
	echo -e "	$EXAMPLE_mv" >> $i.txt
	rm grade.txt

elif [[ "$i" = "grep" ]]; then
	echo -e "EXAMPLES\n	find specific pattern from file called file.txt\n" >> $i.txt
	echo -e "	we put in file called file.txt: echo -e 'my name mohammad\n	my id 1212517' > file.txt" >> $i.txt
	echo -e "my name is mohammad\n my id is 1212517" >> file.txt
	echo "	grep '[0-9]' file.txt" >> $i.txt
	EXAMPLE_grep=$(grep '[0-9]' file.txt)
	echo "	$EXAMPLE_grep" >> $i.txt
	rm -r file.txt

elif [[ "$i" = "date" ]]; then
	EXAMPLE_date=$(date)
	echo -e "EXAMPLES\n	date\n	$EXAMPLE_date" >> $i.txt
elif [[ "$i" = "clear" ]]; then
	echo -e "EXAMPLES\n	clear" >> $i.txt
	echo -e "\n__________________________________________________________________\n" >> $i.txt
	echo -e "Version History\n	$(uname -r)" >> $i.txt
	echo -e "\n__________________________________________________________________\n" >> $i.txt

elif [[ "$i" = "expr" ]]; then
        echo "$(man $i |awk '/^DESCRIPTION$/,/^AUTHOR$/' |grep -v '^AUTHOR$')" > $i.txt
	echo -e "\n__________________________________________________________________\n" >> $i.txt
	echo -e "EXAMPLES\n	Suppose NUM1=5 and NUM2=4" >> $i.txt
	NUM1=5
	NUM2=4
	EXAMPLE_expr=$(expr $NUM1 + $NUM2)
	echo -e "	expr NUM1 + NUM2 \n	=$(expr $NUM1 + $NUM2)\n	expr NUM1 - NUM2\n     =$(expr $NUM1 - $NUM2)\n	expr NUM1 \* NUM2\n     =$(expr $NUM1 \* $NUM2)\n	expr NUM1 / NUM2\n     =$(expr $NUM1 / $NUM2) " >> $i.txt

elif [[ "$i" = "tr" ]]; then
	echo -e "EXAMPLES\n	you should have file to change on it\n" >> $i.txt
	echo -e "	echo "my name is mohammad" | tr m H" >> $i.txt
	EXAMPLE_tr=$(echo "my name is mohammad" | tr m H)
	echo -e "	$EXAMPLE_tr" >>$i.txt

elif [[ "$i" = "pwd" ]]; then
	EXAMPLE_pwd=$(pwd)
	echo -e "EXAMPLES\n	 pwd\n	$EXAMPLE_pwd " >> $i.txt
        echo -e "\n__________________________________________________________________\n" >> $i.txt
	echo -e "\nVersion History\n	$(uname -r)" >> $i.txt
	echo -e "\n__________________________________________________________________\n" >> $i.txt

elif [[ "$i" = "wc" ]]; then
	echo -e "EXAMPLES\n	you should have file to count lines, word, character\n	wc file.txt\n	COUNT LINES	wc -l file.txt\n	COUNT WORD	wc-w file.txt\n	COUNT CHARACTER	wc -c file.txt" >> $i.txt
	echo -e "	suppose we have file.txt and we put in it:\n	echo hello world > file.txt" >> $i.txt
	echo "hello world" >> file.txt
	EXAMPLE_wc=$(wc file.txt)
	echo -e "	$EXAMPLE_wc" >> $i.txt
	rm -r file.txt	

elif [[ "$i" = "paste" ]]; then
	echo -e "EXAMPLES\n	paste file1.txt file2.txt" >> $i.txt
	echo -e "	echo -e 'mohand\n	ahmad\n	salh' > names.txt" >> $i.txt
	echo -e "       echo -e '100\n	200\n	300' > ids.txt" >> $i.txt
	echo -e "mohand\nahmad\nsalh" > names.txt
	echo -e "100\n200\n300" > ids.txt
	EXAMPLE_paste=$(paste names.txt ids.txt)
	echo -e "$EXAMPLE_paste" >> $i.txt
	rm ids.txt names.txt

elif [[ "$i" = "rm" ]]; then
	echo -e "EXAMPLES\n	rm file1\n" >> $i.txt
	touch file1
	touch file2 
	echo -e "	$(ls)" >> $i.txt
	echo -e "	rm file1" >>$i.txt
	rm file1
	EXAMPLE_rm=$(ls)
	echo -e "	$EXAMPLE_rm" >> $i.txt
	rm file2
elif [[ "$i" = "head" ]]; then
        echo -e "EXAMPLES\n     head -n 2 file.txt " >> $i.txt
	echo -e "	echo -e '10\n	20\n	30\n	40\n	50' >> file.txt" >> $i.txt
	echo -e "	10\n	20\n	30\n	40\n	50" >> file.txt
	EXAMPLE_head=$(head -n 2 file.txt)
	echo -e "$EXAMPLE_head" >> $i.txt
	rm -r file.txt

fi

if [ "$i" != "clear" -a "$i" != "pwd" ]; then
	echo -e "\n__________________________________________________________________\n" >> $i.txt
	echo -e "\nVersion History \n" >> $i.txt
	echo "	$($i --version |head -n 1)" >> $i.txt
	echo -e "\n__________________________________________________________________\n" >> $i.txt
fi
echo -e "\n Related command\n   $(compgen -c | grep $i )" >> $i.txt


sed  's/DESCRIPTION/\x1b[1m&\x1b[0m/g' $i.txt > temp.txt && mv  temp.txt $i.txt 
sed 's/SYNOPSIS/\x1b[1m&\x1b[0m/g' $i.txt > temp.txt && mv temp.txt $i.txt
sed 's/EXAMPLE/\x1b[1m&\x1b[0m/g' $i.txt > temp.txt && mv temp.txt $i.txt
sed 's/Version History/\x1b[1m&\x1b[0m/g' $i.txt > temp.txt && mv temp.txt $i.txt
sed 's/Related command/\x1b[1m&\x1b[0m/g' $i.txt > temp.txt && mv temp.txt $i.txt

echo "Generat $i"
done;;

2 ) for c in "${command[@]}"; do
echo -e "$c\n"
done ;;

3 ) echo -e "\nwrite command for example\n"
read comnd
case "$comnd"
in 
"cat" ) echo " My name is Mohammad " > file.txt && echo "BY using: cat file.txt" && cat file.txt && rm -r file.txt ;;
"cut" ) echo " time now is 11:20" && echo ' By using: echo "time now is 11:20" |cut -c13-' && echo "time now is 11:20" | cut -c13-;;
"ls" ) echo "print all file and Directory in the current Directory" && ls;;
"mv" ) mkdir MOVE && cd MOVE && echo " my name is mohammad" > file.txt && echo " mv file.txt newfile.txt"  && echo " Before Change"  &&ls && mv file.txt newfile.txt && echo " After change"  && ls && cd .. && rm -r MOVE;;
"grep" ) echo -e "my name is mohammad\n my id is 1212517\n" > file.txt && cat file.txt && echo "With using grep '[0-9]' filename" && grep '[0-9]' file.txt && rm file.txt ;; 
"date" ) date;;
"clear" ) clear;;
"expr" ) echo " expr 5 + 5" && expr 5 + 5 ;; 
"tr" ) echo -e "my name is mohammad\n my id is 1212517\n" > file.txt && cat file.txt && echo -e "tr m H < file.txt" && tr m H < file.txt && rm file.txt;;
"pwd" ) pwd;;
"wc" ) echo -e "my name is mohammad\n my id is 1212517" > file.txt&& echo -e "use wc, wc -l, wc -w, wc -c\n" && wc file.txt && wc -l file.txt && wc -w file.txt && wc -c file.txt && rm file.txt ;;
"paste" ) echo -e " mohand\n ahmad\n salh\n qassam" > file1.txt && echo -e " 1000\n2000\n 3000\n 4000" > file2.txt && echo -e " jersulam\n ramllah\n jenin\n jerico" > file3.txt && paste file1.txt file2.txt file3.txt && rm file1.txt file2.txt file3.txt;; 
"rm" ) mkdir DIRECTORY && cd DIRECTORY  && touch file1.txt && touch file2.txt && ls  &&echo -e "\n rm file1.txt" && rm file1.txt && ls && cd .. && rm -r DIRECTORY;;
"head" ) echo -e " mohand\n ahmad\n salh\n qassam" > file1.txt && cat file1.txt && echo -e "\nBY using : head -n 2 file1.txt\n" && head -n 2 file1.txt && rm file1.txt;;
* ) echo -e "\nSOORY COMMAND NOT FOUND"
esac ;;

4 ) ./verification_1212517;;
5 ) echo -e "\nSearch for command select (c) Search for word select (w)"
read comand
if [[ "$comand" = "c" ]]; then
echo "Enter command name"
read comand
	if [[ ! -e "$comand.txt" ]]; then
	echo "This command not found"
	else 
	cat $comand.txt
	fi
elif [[ "$comand" = "w" ]]; then
echo "Enter word name"
read word
grep $word *.txt
else
echo " Sorry you should select w for word or c for command"
fi;; 
6 )echo "Enter command name"
 read comand
if [[ -e "$comand.txt" ]]; then
case "$comand"
in
"head" )echo -e "\ncat\npwd\necho\nprintf\ntail\npaste" | sort;;
"paste" )echo -e "\ncat\ntail\nhead" | sort;;
"cat" ) echo -e "\npwd\necho\nhead\ntail\nprintf\nls" | sort;;
"wc" ) echo -e "\nsort";;
"rm" )echo -e "\nrmdir\nmkdir\ntouch" | sort ;;
"tr" ) echo -e "\nsed\ngrep" | sort;;
"ls" ) echo -e "\ncat\nhead\ntail\nalias" | sort;;
"mv" ) echo -e "\nrename\ntouch\nrm\nrmdir"\ sort;;
esac
compgen -c | grep $comand | sort | tail -n 5

elif [ "$(command -v $comand)" ]; then
compgen -c | grep $comand | sort | head -n 8

else
echo "command not found"
fi;;

7 ) echo -e "\nGOOD BYE" && exit 1;;
* ) echo "SORRY command not found" 
esac
done 
