# Special Directory and files

- when multiple users need to work routinely on the same directories and files, these permissions may not be enough. The special permissions setuid, setgid and the sticky bit are designed to address these concerns.
- __setuid__ : 
    - To add the setuid permission symbolically, run
        - chmod u+s filename
        - To add the setuid permisssion numerically add 4000 to the file permission of the original file i.e. if file permisssion is 775 then to add setuid run :
            - chmod 4775 filename
        - to remove setuid subtract 4000 from current value.

- __setgid__ : setgid permission is similar to setuid, but it makes use of the group owner permissions. There are two forms of setgid permissions: setgid on a file and setgid on a directory
    - Use the following syntax to add the setgid permission symbolically:
        - chmod g+s <file|directory>
    - To add the setgid permission numerically, add 2000 to the file's existing permissions (assume in the following example that the directory originally had 775 for its permissions):
        - chmod 2775 <file|directory>
    - To remove the setgid permission symbolically, run:
        - chmod g-s <file|directory>
    - To remove the setgid permission numerically, subtract 2000 from the file's existing permissions:
        - chmod 0775 <file|directory>
    
- __Sticky Bit__ : 
    - sticky bit permission is used to prevent other users from deleting files that they do not own in a shared directory.Recall that any user with write permission on a directory can create files in that directory, as well as delete any file in the directory, even if they do not own the file!.
    - To set the sticky bit permission symbolically, execute a command like the following:
        - chmod o+t <directory>
    - To set the sticky bit permission numerically, add 1000 to the directory's existing permissions (assume the directory in the following example originally had 775 for its permissions):
        - chmod 1775 <file|directory>
    - To remove the sticky permission symbolically, run:
        - chmod o-t <directory>
    - ‌⁠​​⁠​To remove the sticky bit permission numerically, subtract 1000 from the directory's existing permissions:
        - chmod 0775 <directory>

- __Links__ : 
    - every file created, there is a block of data on the file system that stores the metadata of the file.
    - This metadata is called the file's inode table. The inode table also includes pointers to the other blocks on the file system called data blocks where the data is stored.
    - Every file on a partition has a unique identification number called an inode number. The ls -i command displays the inode number of a file.
    - when to files are assigned same inode number then they create a hard link.
    - To create hard links, the ln command is used with two arguments. The first argument is an existing file name to link to, called a target, and the second argument is the new file name to link to the target.
        - ln target link_name
        - example : _ln file.original file.hard.1_
    - __soft links__ : 
        - A symbolic link, also called a soft link, is simply a file that points to another file.
        - To create a symbolic link, use the -s option with the ln command:
            - _ln -s target link_name_
- Advantages and disadvantages of the links : 
    - Hard links don’t have a single point of failure.
    -  Soft links are easier to see.
    -  Soft links can link to any file.
    - Soft links can link to a directory.

    