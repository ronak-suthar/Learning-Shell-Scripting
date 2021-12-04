## File Attributes and Permissions

1. File types
    - '-' -> Regular File
    - 's' -> symbolic Link
    - 'c' -> character special
    - 'b' -> Block Special
    - 'p' -> Named Pipe
    - 'd' -> Directory
2. Get more Details of Regular files (file command)
    - ```bash
        file <filename>
      ```
3. Links
    - Points to another file
    - No extra storage
    - Changes made in link file alters original file and vice-a-versa
    - Types
        - Hard Links
            - ```bash
                ln src target
                ```
            - Point to a file not a directory
            - indistinguishable from original file
            - Can be re-located
            - Origianl file os not affected if hard link is deleted
            - If original file is deleted, then conent still remains until hard link is deleted
    
        - Soft Links
            - ```bash
                ln -s src target
                ```
            - stores the pathname to another file as target

            - path can be absolute or relative
            - Relative path link may not work when relocated
            - Original file is not affected if soft link is deleted
            - If Original file is deleted then soft link will not work
4. Device Files
    - Each device is linux is a file
    - /dev directory has all device files
    - Types of device files
        - Character special -> 
            Communicate with device with one charcter at a time
        - Block special -> 
            Communicate with device with blocks of data
        
5. Named Pipe
    - Pipe operator redirects output of one command to other ,these lasts only as long as the process and are anonymous
    - Named pipes are files exists even after process is executed and are named
    - Are created using mkfifio command
    ```bash
        mkfifo namedPipeName
    ```
    - Can be deleted using rm
    ```bash
        rm namedPipeName
    ```

6. File Permissions

    - when we do a ls -l we get output as
        ```bash
            -rw-rw-r--  1 ronak ronak 3286 Dec  2 00:03 readme.md
            permissions   owner group size (date-time)  filename  
        ```
    - Type of OwnerShip : Owner(u),Group(g),Others(o) and All(a)
    - Types of Permissions: read(r),write(w) and execute(x)
        ```bash
            rwx rwx rwx
            -u-|-g-|-o-
        ```
    - Command to Change permissions is chmod

        - Symbolic Method
            - Syntax of chmod
            ```bash
                chmod <ownership> <action> <permission> file
            ```
            - Action is denoted by add(+),remove(-)

            Example : 
            - Add execute permission to others
                ```bash
                    chmod o+x fileName
                ```
            - Remove execute permission from group and others
                ```bash
                    chmod go-x filename
                ```
        - Octal method
            - Syntax of chmod
                ```bash
                    chmod <permissions> file
                ```
            - Permissions is denoted by three digit number
            - Each number in digit represents permissions of different types of ownership
            - Number store permission from 0 to 8 as below

              |read(r)|write(w)|execute(x)|
              | :---:  |:----: |   :---:  |
              |0       |0      |0         | 
              |0       |0      |1         | 
              |0       |1      |0         | 
              |0       |1      |1         | 
              |1       |0      |0         | 
              |1       |0      |1         |
              |1       |1      |0         | 
              |1       |1      |1         |           
            - Example chmod 400 file means 
                - Owner : 4 means (100) so only read permission
                - Group : 0 means (000) so no r,w,andx permission
                - Others : 0 means (000) so no r,w,andx permission
            - Example chmod 764
                - Owner : 7 means (111) so r,w and x permission
                - Group : 6 means (110) so only r and w permission
                - Others : 4 means (100) so only r permission

7. Handling OwnerShip   
    - Super User or Root User
        - Used for System Administration
        - It is the first user and has ability to anything in system
        - Executing commands as root then we use sudo
    - User 
        - Individuals which are part of a group
        - create user
            ```bash
                sudo useradd -m <username> -p <password>
            ```
        - remove user
            ```bash
                sudo userdel -m <username> -p <password>
            ```
    - Groups
        - Is a set of users
        - create group 
            ```bash
                sudo groupadd <group name>
            ```
        - remove group
            ```bash
                sudo groupdel <group name>
            ```
    - Managing Users In Group
        - Add user to a group
            ```bash
                sudo gpasswd -a <username> <groupname>
            ```
        - Remove user from a group
            ```bash
                sudo gpasswd -d <username> <groupname>
            ```
        - View all groups
            ```bash
                cat /etc/group
            ```
    - Changing the Ownership

        - Change owner and group 
         ```bash
            chown <ownerUsername>:<groupName> <file>
         ```
        - Change only group
         ```bash
            chown :<groupName> <file>
         ```
        - Use -R option for recursive implmentation
        - Normal Users can only change ownership and group of files which