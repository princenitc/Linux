# Linux

*  Image magic is a tool which could be used to manupulate the images through programs.
*  KeypassX can be used to generate and manage the passwords.
*  Gufw is the graphical firewall manager for ubuntu.
*  Docker and Cubernates are the containers for virtual machines.


# Linux Commands

### Options
- -l -> shows the result in the listing format
- -r -> reverses the result
- -h -> show the result along with the size of the files  

All the options can be combined with any of the other irrespective of the order of the combination.

### Variables 
These are the features which allows the shell to store some values which in turn can be used to modify the behaviour of the command.

## Commands
- __history__ -> this will provide with the history of the desired commands.  
    - If you find any command to be used from the hostory then you can call that by _!<command_number>_ this will run the particular command from the history table.  
    - Also to execute the nth command from the bottom you can type as _!<commmad_position>_.  
    - To execute most recent command type !!
    - To execute the most recent iteration of a particular commmand type _!<command>_.

- __echo__ -> It is used to display output in the terminal. To acces a varibale in echo you can include $ sign before the variable name. e.g.
    - variable = prince
    - echo "Hello $variable" will show the result as "Hello prince".