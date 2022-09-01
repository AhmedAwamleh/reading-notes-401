## Linux is Case Sensitive
Linux is not like this. As such it is possible to have two or more files and directories with the same name but letters of different case.
Also be aware of case sensitivity when dealing with command line options. For instance with the command ls there are two options s and S both of which do different things. A common mistake is to see an option which is upper case but enter it as lower case and wonder why the output doesn't match your expectation.
## Spaces in names
Spaces in file and directory names are perfectly valid but we need to be a little careful with them. As you would remember, a space on the command line is how we seperate items. They are how we know what is the program name and can identify each command line argument

-The first approach involves using quotes around the entire item. You may use either single or double quotes ''
-Another method is to use what is called an escape character, which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.

## Hidden Files and Directories
Linux actually has a very simple and elegant mechanism for specifying that a file or directory is hidden. If the file or directory's name begins with a . (full stop) then it is considered to be hidden. You don't even need a special command or action to make a file hidden. Files and directories may be hidden for a variety of reasons. Configuration files for a particular user (which are normally stored in their home directory) are hidden for instance so that they don't get in the way of the user doing their everyday tasks.
he command ls which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option -a so that it does show hidden files and directories.


ls Documents
FILE1.txt File1.txt file1.TXT
...
ls -a Documents
. .. FILE1.txt File1.txt file1.TXT .hidden .file.txt
...

## summary
file
obtain information about what type of file a file or directory is.
ls -a
List the contents of a directory, including hidden files.
