# What is the Command Line?
The command line is a text interface for the computer’s operating system. 
You can use it to traverse and edit your computer’s filesystem. Through the command line, you can create new files, edit the contents of those files, delete files, and more!

## Navigating the file system

* pwd - Print Working Directory, gives us an idea where are we right now.
* ls - lists all all files and directories inside the current directory.
  * ls -a - Lists all hidden files
  * ls -l - Lists all files with long format
  * ls -alt - List all contents, including hidden files and directories, in long format, ordered by the date and time they were last modified.
* cd - change diretory
* cd .. - Go one level up
* cd../.. - Go two levels up
* mkdir - makes a new directory
* touch - creates a new file in the directory

## Manupulating files
* cat - used to display the contents of a file without opening it.
* cp - copies the file. Use cp with the first argument being the file name, and the second argument being the destination directory’s path. With cp command, we can copy multiple files.
* Wild cards - we can use special characters like * to select groups of files. 
    * cp * my_directory/.   => Copies all files from current directory to destination directory
    * cp w*.txt my_directory/ => Copies all files starting with w and with an txt to destination directory.
* mv - moves files from one directory to another directory without making a copy. For eg. mv my_file.txt my_directory/ 
* rm - rm commands removes files and directories. When rm -r unwanted_directory is passes it deletes the file permanatly. r stands for recursive. 
