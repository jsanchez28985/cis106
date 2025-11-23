# Wildcards and how to use them.
* **The * Wildcard**
  * The asterisk matches zero or more characters in a filname.
* **Examples** 
  * ls Downloads/*
  * ls Downloads/*.txt
  * ls Downloads/f*.txt
  * ls *file*

* **The ? Wildcard**
  * The ? wildcard metacharacter matches precisely one character. The ? wildcard proves very useful when working with hidden files (hidden files are also called dot files). 
* **Examples** 
  * ls ./.??*
  * ls ../.??*
  * ls b??k*
  * ls f?l*
  * ls *.??

* **The [] wildcard**
  * The brackets wildcard matches a single character in a range. The brackets wildcard use the exclamation mark to reverse the match.
* **Examples**
  * ls f[aeiou]*
  * ls f[!aeiou]*
  * ls f[a-z]*

# Brace Expansion and how to use it. 
* **Brace expansion**
  * Brace expansion is a feature of the bash shell that generates argument strings. These strings can be used by commands to operate on files. Brace expansion does not make calls to the operating system like wildcards do.
* **Examples and how to use it.**
  * Start with an open brace with no spaces, type your string seperating entries by a command, close the brace.
  * mkdir -pv example_site/{assets/large,docs/share,scripts/js}