---
Name: Angela Vazquez
Course: CIS-106
Semester: Spring 23
Instructor: R. Alberto
---
# Final Linux Assignment 
## awk
### Description: 
awk is a scripting language that is used for processing and displaying text as well 
#### Formula:
awk + options + {awk command} + file
#### Examples:
* How to print the first field of a file:

awk -F : {print $1} /etc/passwrd
* How to start printing from a different line

awk NR > 3 {print} /etc/passwrd
* How to change a filed to upper case

awk -F : {print topper($1)}

## cat command

### Description: 
Cat command is used for displaying the content of a file
### Formula:
* cat + option + file(s) to display
### Examples:
* Display the content of a file located in the pwd

cat todo.lst
* Display content of a file using absolute path

cat ~/Documents/todo.lst
* Display content of a file with line numbers

cat -n ~/Documents/todo.md

## Cp Command

### Description: 
copies files/directories from a source to a destination
### Formula
cp + files to copy + destination
### Examples
* To copy directories using r function

tp -r + directory to copy +destination
* To copy a file
  
cp Downloads/pizza.png Pictures/
* To copy a directory using absolute path
  
cp -r ~/Downloads/wallpapers ~/Pictures/
## cut command 
### Description:
cut command is used to extract a specific section of each line of a file and display it to the screen.
### Formula
cut + option + file(s)
### Examples:
* Display the list of all the users in your system
 
 cut -d ':' -f1 /etc/passwd
* Display a list of all the users in your system with their login shell

cut -d ':' -f1,7 /etc/passwd\
* cut a file excluding a given field

cut -d ',' --complement -s -f3 users.txt

## Grep Command

### Description
Grep is used to search text in given file. Grep works line by line
### Formula:
grep + option + search criteria + file(s)
### Examples
* search any line given that contains the word dracula in the file

grep 'peperoni' ~/Documents/pizza.txt
* enables case sensitivity

grep -i
* Matches only the given word (pattern) by itself.
  
grep -w

## Head Command 
### Description
Displays top number of lines given file
### Formula
head + option + file(s)
### Examples
Display the first ten lines of a file
* head ~/Documents/movies/IT.txt

Display the first 5 lines of a file
* head -5 ~/Documents/movies/IT.txt
Display the first 20 lines of a file
* head -20 ~/Documents/Book/dracula.txt

## ls command
### Description:
ls is used for listing the content of a given directory or the file/directory itself
### Formula:
ls + option + directory to list
### Example:
List all files inside current working directory including hidden files
* ls -a
List all files inside given directory
* ls -a ~/Pictures
List all the options of the ls command
* ls --help

## man command

### Description:
Describes/shows the Linux shell commands
### Formula
man + command
### Examples:
* Show all available pages of a command
  
man -a passwd

* open man page of passwd command

man passwd
* Shows the man page section of the passwd command

man -f passwd

## mkdir

### Description:
is used for creating single directories or multiple
### Formula
mkdir + name of directory
### Examples
* Creating a directory

mkdir wallpapers
* Creating a directory using absoloute path

mkdir ~/wallpapers/nightsky
* Creating a directory with a parent directory

mkdir -p wallpapers_1/final


## mv

### Description:
Moves and renames directories
### Formula
mv + source + destination
### Examples:
* Renaming files or directories

mv + file/directory to rename + new name
* To move a file from a directory to another using relative path

mv Downloads/map.pdf Documents/
* To move a file from one directory to another combining absolute path and relative path

mv Downloads /music1.docx /media/music/songs/

## tac

### Description:
Used for displaying the content of a file in reverse order
### Formula:
tac + option + file(s) to display
### Examples:
* Displaying the content of a file located in pwd

tac final.md
* Displaying the content of a file using absolute path

tac ~/Documents/movies.md
* Displaying the content using relative path

tac /home/downloads/movies.md

## tail command 
### Description
tail commands displays last number of lines give by a file
### Formula
tail + option + file
### Examples
* Displays the last 10 lines of a file

tail ~/Documents/book/dracula.txt
* Display the last 5 lines of a file

tail -5 ~/Documents/Book/dracula.txt
* Display the last 30 lines of a file

tail -30 ~/Documents/Book/Dracula.txt

## touch

## Description
Used for creating files
## Formula:
touch +file name
## Examples
* Create a file

touch list
* Create a file using absolute path

touch ~/Downloads/games.txt
* Create several files

touch list_of_cars.txt document.txt

## tr

### Description
tr command is used for translating or deleting characters from standard output
### Formula
standard output | tr + option + set + set
### Examples
* Translate one character to another

cat file.txt | tr '.' ','
* Translate white space into tabs

cat program.py | tr "[:space:"] '\t'
* Translate tabs into space

cat file.py | tr -s "[:space:]" ' '

## tree

### Description
A recursive directory listing program that produces a depth-indented
### Formula
tree + directory
### Examples
* Tree list current directory

tree
* Tree list a directory

tree Downloads/
* Tree list using absolute path

tree ~/Downloads/

## vim/nano

### Description: 
a text editor
### Formula:
nano + file name
vim + file name
### Examples:
* Enter nano UI

nano
* Enter Vim UI

vim

# Question 2

### How to work with multiple terminals open?
Short cut is CTRL + Shift + N
### How to work with manual pages?
To open the man page you type man and the linux command that you would like to read the manual pages for
### How to parse (search) for specific words in the manual page
man -K keyword
### How to redirect output (> and |)
'>' command saves the output to a file name on the other hand, the | applies the output to the next command

### How to append the output of a command to a file

'>' use command with file name
### How to use wildcards
Wildcards use letters and characters to specify a file name for searches
ls -A *.txt *.py

### For copying and moving multiple files at the same time
cp dir2/*.png dir2/*.png dir 3

How to use brace expansion (For creating entire directory structures in a single command)
mkdir -p {audio/{aac,mp3},docs/{docx,pdf,xls}}













