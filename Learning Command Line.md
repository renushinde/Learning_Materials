# What is the Command Line?
The command line is a text interface for the computer’s operating system. 
You can use it to traverse and edit your computer’s filesystem. Through the command line, you can create new files, edit the contents of those files, delete files, and more!

## Navigating the file system

* pwd => Print Working Directory, gives us an idea where are we right now.
* ls => lists all all files and directories inside the current directory.
  * ls -a => Lists all hidden files
  * ls -l => Lists all files with long format
  * la -t => orders files and directories by the time they were last modified
  * ls -alt => List all contents, including hidden files and directories, in long format, ordered by the date and time they were last modified.
* cd => change diretory
* cd .. => Go one level up
* cd../.. => Go two levels up
* mkdir => makes a new directory
* touch => creates a new file in the directory

## Manupulating files
* cat => used to display the contents of a file without opening it.
* cp => copies the file. Use cp with the first argument being the file name, and the second argument being the destination directory’s path. With cp command, we can copy multiple files.
* Wild cards => we can use special characters like * to select groups of files. 
    * cp * my_directory/.   => Copies all files from current directory to destination directory
    * cp w*.txt my_directory/ => Copies all files starting with w and with an txt to destination directory.
* mv => moves files from one directory to another directory without making a copy. For eg. mv my_file.txt my_directory/ 
* rm => rm commands removes files and directories. When rm -r unwanted_directory is passes it deletes the file permanatly. r stands for recursive. 
* rm -rf => We could combine the option -r with the option -f, which will delete forcibly without individually confirming each piece of content inside the directory.

## Redirection
* echo "Hello"=> The echo command accepts the string "Hello"as standard input, and echoes the string “Hello” back to the terminal as standard output.
* echo "Hello" > hello.txt => The > command redirects the standard output to a file. Here, "Hello" is entered as the standard input, and is then redirected to the file hello.txt by >
* cat deserts.txt > forests.txt. => Here the output of deserts.txt(left side) is passed to forests.txt and the contents in forests.txt are overwritten.
* cat deserts.txt >> forests.txt => Here the contents of deserts.txt (left side) is appended to forests.txt. With >> operator we can append the contents without overwriting it.
* | (pipe character) => The | takes the standard output of the command on the left, and pipes it as standard input to the command on the right. You can think of this as “command to command” redirection.
* sort => sorts the files alphabetically without changing them.
* uniq deserts.txt => uniq stands for “unique.” It filters out adjacent, duplicate lines in a file.
* grep => kind of like regEX. grep stands for “global regular expression print.” It searches files for lines that match a pattern and then returns the results. It is also case sensitive.  
* grep -i => This will search for all patterns with case insensitive in mind. 
* grep -R  => searches all files in a directory and outputs filenames and lines containing matched results. -R stands for “recursive”. 
* greap -Rl => grep -Rl searches all files in a directory and outputs only filenames with matched results (so no lines).
* sed 's/snow/rain/' forests.txt  => sed stands for “stream editor.” It accepts standard input and modifies it based on an expression, before displaying it as output data. It is similar to “find and replace.”
* sed -i 's/snow/rain/g' forests.txt => Here search(s) for any word 'snow' and replace it with 'rain' globally and rewrite the file using -i
