# Ownership and Permissions
- __Changing Group ownership__ :
    - _id_ : shows the details of the user and groups available to use.
    - _newgrp group_name_ : following command can be used to change the primary group of a user to group_name.(this is the temporary setup which happens in the new shell generated to exit this new shell user can enter exit command to quite the shell.)
    - _usermod -g groupname username_ : this will make the groupname as the permanent primary group of the username.

    - To change the group owner of an existing file the chgrp command can be used.
        - Syntax : chgrp group_name file
        - To change the group ownership of all of the files of a directory structure, use the recursive -R option to the chgrp command
         - Syntax :  chgrp -R groupname dirname
        - stat command displays more detailed information about a file, including providing the group ownership both by group name and GID number.

- __Changing user ownership__ : 
    - chown command allows the root user to change the user ownership of files and directories. However chown also give the permission to change the group ownership either by root or by owner user.
    - There are different ways to change the owner of a file - 
        - chown username /path/to/file
        - chown username:groupname /path/to/file or chown username.groupname /path/to/file
        - chown :groupname /path/to/file or chown .groupname /path/to/file(This is only to change the ownership of groups and it doesnt requires root access.)
- __Permissions__ :
    - output of the ls -l command displays ten characters at the beginning of each line. These characters indicate the type of file and the permissions of the file :
        - first character -> this indicates about the type of file.
            - '-' -> regular file, d -> directory , l -> symbolic link, b -> block file , c -> character file, p -> pipe file and s-> socket.
        - Next nine characters -> this indicates about the set of permissions of the file.
            - __user owner__ : Characters 2-4 indicate the permissions for the user that owns the file.If you are the owner of the file, then only the user owner permissions are used to determine access to that file.
            - __group owner__ : Characters 5-7 indicate the permissions for the group that owns the file. If you are not the owner but are a member of the group that owns the file, then only group owner permissions are used to determine access to that file.
            - __others__ : Characters 8-10 indicate the permissions for others or what is sometimes referred to as the world's permissions. This group includes all users who are not the file owner or a member of the file's group.
            - Three type of permission available for all user are of type read(r), write(w) and execute(x).
        - important points -> 
            - The permissions of all parent directories must be considered before considering the permissions on a specific file.
            - The r permission allows a user to view a listing of the directory.
            - The w permission allows a user to delete files from a directory, but only if the user also has x permission on the directory.
            - The x permission is required to "get into" a directory, but the r permission on the directory is not necessary unless you want to list the directory's contents.
            -  You must look at each file and directory permissions separately and be aware of which groups the user account belongs to.
            - Don't provide permissions to the group owner and "others" without applying at least the same level of access to the owner of the file.

- __Changing permission__ : chmod (change mode) command is used to change permissions on files and directories. There are two techniques that can be used with this command: symbolic and numeric. Both techniques use the following basic syntax:
    - chmod new_permission file_name
    - To change the permissions of a file either you have to be the owner of the file or root user.
    - When specifying the new_permission of the chmod command following three types of information are required : 
        - __Permisssion Groups__ : a(user owner), g(group owner), o(others) and a(all users).
        - __How to modify__ : + (add) , - (remove)  and = (equals)
        - __permissions type__ : r (read), w (write) and x(execute)
    - Example : chmod g+w abc.txt(adds the write permission to group owner)
    - Many permission can also be combined with each other - 
        - chmod ug+x,o-r abc.txt
    - = adds specified permissions and causes unmentioned ones to be removed.
        - example : chmod u=rx abc.txt(this removes the write permission of the user while providing the read and execute privilages.)

- __Default permissions__ : 
    -  umask command is a feature that is used to determine default permissions that are set when a file or directory is created. Default permissions are determined when the umask value is subtracted from the maximum allowable default permissions. The maximum default permissions are different for files and directories.
    - File default are - 666
    - Directory default are - 777
    - Default permissions are calculated by subtracting the umask from respective file/directory defaults.

* using chmod with octal notation : 
    - read - 4 , write - 2 , execute - 1 points are considered.
    - means if value is 7 then all permissions are given if it is 3 then only w,x.
    - Value can be assigned by giving total of the permission points.
    - this pattern can be used to provid the consice values -
    - for example : rwxrw-r--
    - for user : rwx -> 4 + 2 + 1 = 7
    - for groups : rw- -> 4 + 2 = 6
    - for others : r-- -> 4
    - Hence octal value is 764.
    - It is useful to change the permission of all the users.
