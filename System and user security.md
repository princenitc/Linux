# System and User security 

- su [options] [username] : It is used to perform actions as different user. i.e. root or someone else.
    - Different ways to access the login shell are : 
        - su -
        - su -l
        - su --login
        - These commands are used to login into the shell as root/different user.

- sudo [options] command : Gives the access to the file at the user level. Password asked in this case is not the root password but the user password.

- id command is used to print user and group information for a specified user
    - id [options] username
    - To print only the user's primary group, use the -g option.
    - id command can also be used to verify the user's secondary group memberships using the -G option. This will print all the groups that a user belongs to, both primary and secondary.
    -  who:  command displays a list of users who are currently logged into the system, where they are logged in from, and when they logged in.
    -  w command provides a more detailed list about the users currently on the system than the who command.    
    - last command reads the entire login history from the /var/log/wtmp file and displays all logins and reboot records by default.
    -  who command reads from the /var/log/utmp file which logs current users.
    - last command reads from the /var/log/wtmp file, which keeps a history of all user logins.
    