# Chapter - 6 (Getting Help)

- __Man Pages__ : Documentation of help done by the creator of linux to help the users is called as man pages. Man pages provides the features of a command and also gives the short description about the command.
    - _man <command_name>_ : command opens the documentation for the command_name.
    - To quite the documentation press Q.
    - Sections of a man pages are as following :
        - __Name__ : Provides the name of a command and a very brief description.
        - __Synopsis__ : This give a very consice example of how the command can be used. [] (square brackets) in the synopsis are optional.
        - __Description__ : Provides the more detailed description of command.
        - __Options__ : Provides the list of options as well as how they can be used with the command and what is there usefulness.
        - __Files__ : Lists the files that are associated with the command as well as a description of how they are used.
        - __Author__ : Name of the author who has written the documentation.

    - __Searching in man pages__ : To search anything in man page press / and then the term which needed to be searched. To move to the next match pattern of the text press n and to move back press CTRL + N.
    - These are the different types of the man command - 
        - General Commands
        - System Calls
        - Library Calls
        - Special Files
        - File Formats and Conventions
        - Games
        - Miscellaneous
        - System Administration Commands
        - Kernel Routines
    - _whatis_ / _man -f_ : shows what section a man page is store in. Example : _whatis <command_name>
    - _whereis <comamnd_name>_ : shows the location of the man pages of the command.
    - _locate <file_name>_ : is used to locate the the file and folders with filename.

- __Info__ : Provides the book like organised documentation of the commands.  
    - _info <command_name>_ : shows the info documentation of the command name.

- Shift + H key Gives the list of movement commands while reading the documentation.
- _cat --help_ : shows the help documenation.

