# Cat
* **Definition**
  * The cat command is used for displaying the content of a file. Cat is short for concatenate which is the command's intended use.
* **Usage**
  * cat + option + file(s) to display. Used to display the content of a file.
* **Formula** 
  * cat + option + file to display
* **Examples**
  * cat ~/Documents/sample_files/Code/helloWorld.py
  * cat -n ~/Documents/sample_files/Code/helloworld.py
  * cat -A ~/Documents/sample_files/Code/helloworld.py

# TAC
* **Definition**
  * The TAC command is used for displaying the content of a file in reverse order. Just like cat, tac concatenates files and displays the output of the concatenation.
* **Usage**
  * tac + option + file(s) to display. The tac command is used for displaying the content of a file in reverse order.
* **Formula**
  * tac + option + file(s) to display
* **Examples**
  * tac ~/Documents/sample_files/Code/helloworld.py
  * tac ~ /Documents/sample_files/Code/helloworld.py 
    ~/Documents/sample_files/code/helloworld.sh

# Head
* **Definition**
  * The head command displays the top N number of lines of a given file. BY default, it prints the first 10 lines. If more than one file name is provided then data from each file is preceded by its file name.
* **Usage**
  * Used to display the first 10 lines. head + option + file(s)
* **Formula** 
  * head + option + file(S)
* **Examples**
  * head ~/Documents/Book/dracula.txt
  * head -5 ~/Documents/Book/dracula.txt
  * head -n 1 Csv/*.csv Code/*.py
  
  # Tail
* **Definition**
  * The tail command displays the last N number of lines fo a given file. By default, it prints the last 10 liens. If more than one file name is provided then data from each file is preceded by its file name.
* **Usage**
  * tail + option + file(s)
* **Formula** 
  * tail + option + file(s)
* **Examples**
  * tail ~/Documents/sample_files/
  * tail -5 ~/Documents/sample_files/

# Cut
* **Definition**
  * The cut command is used to extract a specific section of each line of a file and display it to the screen.
* **Usage**
  * cut + option + file(s) used to extract a specific section of each line of a file and display it to the screen.
* **Formula**
  * cut + option + file(s)
* **Examples**
  * cut -d ':' -f1 /etc/passwd
  * cut -d ':' -f1,7 /etc/passwd

# Sort
* **Definition**
  * The sort command is sued for sorting files. The sort command supports sorting: alphabetically, in reverse order, by number, and by month. The sort command follows this order unless specified otherwise. Lines starting with a number will appear before lines starting with a letter. Lines starting with a letter that appears earlier in the alpabet will appear before lines starting with a letter that appears later in the alphabet. Lines starting with a lowercase letter will appear before lines starting with the same letter in uppercase.
* **Usage**
  * sort + option + file
* **Formula** 
  * sort + option + file
* **Examples**
  * sort users.lst
  * sort -o sorted.lst users.lst
  * sort -r users.txt

# wc
* **Definition**
  * the wc command is used for printing the number of lines, characters and bytes in a file
* **Usage**
  * wc + option + file(s)
* **Formula** 
  * wc + option + file(s)
* **Examples**
  * wc -m users.txt
  * wc -l users.txt
  * wc -w users.txt