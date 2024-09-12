## Viewing File Permissions

To view the permissions of a file or directory, you can use the `ls` command with the `-l` option:
`ls -lh <filename>`

For example:
`ls -l test.txt`

The output will look something like this:
`-rw-r--r-- 1 brian squad 2.9K Jun 14 10:23 test.txt`

Here is a breakdown of the components:

1. **First Character: File Type**
    - **`-`**: Indicates a regular file.
    - **`d`**: Indicates a directory.
    
2. **File Permissions**
    - The next nine characters represent the file permissions, divided into three groups:
	    - **`rw-`**: Owner has read and write permissions.
        - **`rw-`**: Group members have read and write permissions.
        - **`r--`**: Others have read permissions only.
        
3. **Number of Hard Links** 
    - **`1`**: Number of hard links to the file.
4. **File Owner**
    - **`brian`**: Username of the file owner.
5. **Group Name**
    - **`squad`**: Name of the group that owns the file.
6. **File Size**
    - **`2.9K`**: File size of 2.9 kilobytes.
7. **Last Modified Date and Time**
	- **`Jun 14 10:23`**: Last modified date and time (June 14 at 10:23 AM).
8. **File Name**
    - **`test.txt`**: Name of the file.

## Permission Types

There are three basic permission types in Linux:
1. **Read (r)**
    - Allows users to view the contents of a file or list the contents of a directory.
    
2. **Write (w)**
    - Allows users to modify a file's contents or add, remove, or rename files within a directory.
    
3. **Execute (x)**
    - Allows users to execute a file as a program or traverse (enter) a directory.
    

## Permission Classes

Permissions are defined for three types of users:
1. **Owner (u)**
    - The user who created the file.
    
2. **Group (g)**
    - Users who are members of the file's group.
    
3. **Others (o)**    
    - Users who are not the owners of the file and do not belong to the group.
    
4. **All (a)**   
    - Represents all three types of access classes.
    

## Changing File Permissions

## Symbolic Method

The `chmod` command is used to change file permissions. Here are examples using the symbolic method:

- **Set Permissions:** shell
    `chmod u=rwx <filename>`
    
    - **`u`**: User
    - **`g`**: Group
    - **`o`**: Other
    - **`a`**: All (user, group, other)
    
- **Add Permissions:** shell
    `chmod go=rwx <filename> # or chmod go+rwx <filename>`
    
- **Remove Permissions:** shell
    `chmod go-wx <filename>`
    
    - Removes write and executable permissions from group and others.

Examples:
 	
 	`chmod 755 foo.txt` 
 	`chmod +x eshan.me` 
 	`chmod u-x water.mp3`
 	`chmod u=rwx,g=rx,o= merry.txt`
 	
    

## Binary/Octal Method

Permissions can also be changed using octal notation:

- **Read:** 4
- **Write:** 2
- **Execute:** 1

For example:

`chmod 742 <filename>`

- **`7`**: `rwx` (user)
- **`4`**: `r` (group)
- **`2`**: `w` (others).

## Special Permissions

1. **Set User ID (setuid)**
    
    - Allows a user to execute a file with the permissions of the file's owner.
    - Commonly used for executable files that need to be run with elevated privileges.
    
2. **Set Group ID (setgid)**
    
    - Allows a user to execute a file with the permissions of the file's group.
    - Often used for directories to ensure that files created within the directory inherit the group ownership of the directory.
    
3. **Sticky Bit**
    
    - Ensures that only the owner of a file within a directory or the root user can delete or rename the file, even if other users have write permissions on the directory.
    

## Changing File and Directory Ownership

1. **Change Owner:** shell
    `chown <owner> <filename>`
    
    - **`<owner>`** : New owner's username.
    - **`<filename>`** : File or directory name.
    
2. **Change Group:** shell
    `chgrp <group> <filename>`
    
    - **`<group>`**: New group's name.
    - **`<filename>`**: File or directory name.
    

## Best Practices

- **Grant Permissions Only When Necessary:**
    
    - Avoid giving unnecessary permissions to users or groups to maintain security.
    
- **Use Correct User and Group Associations:**
    
    - Ensure that users are associated with the correct groups and have the appropriate permissions.
    
- **Be Cautious with Recursive Permissions Changes:**
    
    - Be careful when using `chmod -R` to change permissions recursively, as it can affect all subdirectories and files.
