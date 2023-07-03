# Managing files and directories 

- __Glob Characters__ : These are the characters which has a special meaning to the shell. Glob characters are also called as wild cards.  
    - '*' - consider the zero or more occurances of the characters.
    - '?' - Marks a single charcter
    - [] - may be used to show the set of charcters or range of characters.
    - ["!characters "] - This is used to take theconjuction of  negation of the range. 
    - To view the directory names only always use the _ls -d <path>_ or else in normal cases it shows the filename in the matched directory.

- __cp source destination__ : where source is the source path and destionation is the path of the destination directory.
    - _cp -i source destination_ : To avoid the unintentional copying and replacing of file.
    - _cp -n source destination_ : To automatically mark the replacing file as no.
    - _cp -r source_directory destination_directory_ : can be used to copy a directory from one place to other.

- _mv source destination_ : Command can be used to move files from source to destination.
    - mv command can be also used to rename a filename. as _mv oldname newname_

- _touch <filename>_ : command can be used to create a filename file.
- _rm <filename>_ : Can be used to remove a file. (It can also be combined with the -i option to avoid accidental removals.)
- __Deleting Directories__ : 
    - _rm -r <directory>_ : This will delete the specified directory.
    - _rmdir <directory>_ : This can also be used to delete the directories.(Only empty directories)

- __Creating Directories__ :
    - _mkdir <dirname>_ : Creates a new empty directory.
    