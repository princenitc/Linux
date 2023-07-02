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
- __Local Variables__ : Variable which are created and stored locally upto the runtime of command line are called local variables.e.g. - name = "prince"
    - These variables are available only to the user through which it is created.

- __Global Variables/Environment Variables__ : These vaiables are available in system wide to all over the system. Some of global variables are 
    - _HISTSIZE_ -> shows how many previous commands to be stored in the history size.
    - _HOME_ -> show the home directory of the user.
    - _PATH_ -> It defines the list of directory for shell to look for commands.
        - You can always add the custom directory to PATH variable to access the custom commands.
_env_ shows the list of all available global variables in the system.
- _export <variable name>_ : can be used to set a local variable as a global variable.
- _unset <variable name>_ : can be used to remove a exported global variable from the global variable list.

## Commands


- __type__ -> To know the type of any command : _type <command_name>_ gives the type of command_name.
    - __Internal Commands__ : Built in command or internal commands are built in to the shell. examples - cd.
    - __External Commands__ : These are executable binaries which are runned by the shell stored in path directories.  

_which <command_name>_ : gives the location of command in PATH variable.

-a option with type command gives all the location of that command.


- __history__ -> this will provide with the history of the desired commands.  
    - If you find any command to be used from the hostory then you can call that by _!<command_number>_ this will run the particular command from the history table.  
    - Also to execute the nth command from the bottom you can type as _!<commmad_position>_.  
    - To execute most recent command type !!
    - To execute the most recent iteration of a particular commmand type _!<command>_.

- __echo__ -> It is used to display output in the terminal. To acces a varibale in echo you can include $ sign before the variable name. e.g.
    - variable = prince
    - echo "Hello $variable" will show the result as "Hello prince".

- __Aliases__ : Aliases are used to map the longer commands to shorter commands. To know which commmand is aliased to which can be known by command _alias_  
    - aliases can be setted by providing commands as _alias mycal = "cal 2019".
    - Now mycal will work same as that of _cal 2019_ command.

Newly created and assigned aliases are only valid until shell is opened in which they are opened. If shell is closed then all the aliases temporarily created will be lost.

- __functions__ : Functions can also be built using existing commands to either create new commands, or to override commands built-in to the shell or commands stored in files. Functions are useful in running multiple commmands at a single run.
    - my_function(){
        \t_cd Documents_
        \t_date_
        \t_echo "This is test for functions"_
    }
    after this we can always call my_function to run all the mentioned command consecutively.\\