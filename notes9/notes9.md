# GREP
* **Definition**
  * `grep` is a command-line tool used to search for specific text or patterns within files or command output.
* **Usage / Formula**
  * `grep [options] "pattern" file`
* **Examples**
  * Search for a word inside a file
    * `grep "error" logfile.txt`
  * Search ignoring case sensitivity
    * `grep -i "linux" notes.txt`
  * Search recursively in a directory
    * `grep -r "main" /home/user/projects`

# AWK
* **Definition**
  * `awk` is a text-processing command used to analyze and manipulate structured text, especially files with columns.
* **Usage / Formula**
  * `awk 'pattern { action }' file`
* **Examples**
  * Print the first column of a file
    * `awk '{print $1}' data.txt`
  * Print lines where the third column is greater than 50
    * `awk '$3 > 50 {print $0}' scores.txt`
  * Use a colon as a field separator
    * `awk -F: '{print $1}' /etc/passwd`

# SED
* **Definition**
  * `sed` (stream editor) is a command used to perform basic text transformations on text streams or files.
* **Usage / Formula**
  * `sed 'command' file`
* **Examples**
  * Replace the first occurrence of a word
    * `sed 's/apple/orange/' fruits.txt`
  * Replace all occurrences of a word
    * `sed 's/cat/dog/g' pets.txt`
  * Delete lines containing a word
    * `sed '/error/d' logfile.txt`

# Using the Pipe (|)
* **Definition**
  * The pipe (`|`) redirects the output of one command and passes it as input to another command.
* **Usage**
  * Used to chain multiple commands together so the output of one becomes the input of the next.
* **Examples**
  * Filter directory listing results
    * `ls | grep ".txt"`
  * Find a running process
    * `ps aux | grep nginx`
  * Count the number of lines in a file
    * `cat file.txt | wc -l`

# Saving Output to a File (>)
* **Definition**
  * The `>` operator saves the output of a command to a file and overwrites the file if it already exists.
* **Usage**
  * Used to redirect command output into a file.
* **Examples**
  * Save a directory listing
    * `ls > files.txt`
  * Save the current date
    * `date > date.txt`
  * Save search results to a file
    * `grep "error" logfile.txt > errors.txt`

# Appending Output to a File (>>)
* **Definition**
  * The `>>` operator appends the output of a command to the end of a file without deleting existing data.
* **Usage**
  * Used when you want to add new output to a file.
* **Examples**
  * Append a directory listing
    * `ls >> files.txt`
  * Append the current date to a log
    * `date >> log.txt`
  * Append search results to an existing file
    * `grep "warning" logfile.txt >> warnings.txt`
