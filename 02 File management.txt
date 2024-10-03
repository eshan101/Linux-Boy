## Navigation and Information

- **pwd**: Print the current working directory.
    
    - **Example:** `pwd` to display the full path of the current directory.
    
- **ls**: List files and directories in the current directory.
    
    - **Options:**
        
        - **ls**: List files and directories.
        - **ls -l**: List files and directories in a detailed list view, including date modified and other details.
        - **ls -a**: Show all files, including hidden files.
        - **ls -al**: Show all files in a detailed list view.
        - **ls -lh**: List files in a detailed view with sizes in human-readable format.
        - **ls -lR Desktop/**: List everything recursively, starting with the items on the desktop and then showing files in every folder and subfolder.
        
    
- **cd**: Change the current directory.
    
    - **Examples:**
        
        - **cd /**: Change to the root directory.
        - **cd ~**: Change to the home directory.
        - **cd ..**: Move up one directory level.
        
    
- **whatis <command>**: Display a brief description of what a command does.
    
    - **Example:** `whatis ls` to know what the `ls` command does.
    

## File Creation and Editing

- **touch <filename>**: Create a new, empty file.
    
    - **Example:** `touch example.txt` to create a new file named `example.txt`.
    
- **echo "line of text"**: Display a line of text or create and write to files.
    
    - **Examples:**
        
        - **echo "Hello World"**: Display the text "Hello World".
        - **echo "Hello World" > example.txt**: Save the text "Hello World" to a file named `example.txt`.
        - **echo "Hello World" >> example.txt**: Append the text "Hello World" to the end of the file `example.txt`.
        
    
- **cat <filename>**: Concatenate files and print on the standard output.
    
    - **Examples:**
        
        - **cat example.txt**: Display the contents of `example.txt`.
        - **cat example1.txt > example2.txt**: Copy the contents of `example1.txt` to `example2.txt`.
        
    

## File and Directory Management

- **mkdir <Directory_name>**: Create a new directory.
    
    - **Example:** `mkdir mydirectory` to create a new directory named `mydirectory`.
    
- **cp <file_name> <location>**: Copy a file to a specified location.
    
    - **Example:** `cp example.txt /home/user/documents` to copy `example.txt` to the `/home/user/documents` directory.
    
- **mv <file_name> <location>**: Move a file to a specified location or rename a file.
    
    - **Examples:**
        
        - **mv example.txt /home/user/documents**: Move `example.txt` to the `/home/user/documents` directory.
        - **mv example1.txt example2.txt**: Rename `example1.txt` to `example2.txt`.
        
    
- **rm <filename>**: Remove files or directories.
    
    - **Examples:**
        
        - **rm example.txt**: Remove the file `example.txt`.
        - **rm -R mydirectory**: Recursively remove everything from the directory and remove the directory itself.
        
    

## Additional File Management Commands

- **ln <file_name> <link_name>**: Create a symbolic link to a file.
    
    - **Example:** `ln --symbolic example.txt example_link.txt` to create a symbolic link named `example_link.txt` to `example.txt`.
    
- **chown <user> <file_name>**: Change the ownership of a file or directory.
    
    - **Example:** `chown user example.txt` to change the ownership of `example.txt` to the user `user`.
    
- **chmod <permissions> <file_name>**: Change the permissions of a file or directory.
    
    - **Example:** `chmod 755 example.txt` to change the permissions of `example.txt` to read, write, and execute for the owner, read and execute for the group, and read and execute for others.
    
- **find <path> -name <filename>**: Search for files by name.
    
    - **Example:** `find /home/user -name example.txt` to search for files named `example.txt` in the `/home/user` directory.
    
- **grep <pattern> <file_name>**: Search for patterns within a file.
    
    - **Example:** `grep "Hello World" example.txt` to search for the pattern "Hello World" in the file `example.txt`.
    

## Other Useful Commands

- **whoami**: Display the current user.
    
    - **Example:** `whoami` to show the current user.
    
- **date**: Display the current date and time.
    
    - **Example:** `date` to show the current date and time.
    
- **man <command>**: Display the manual for a command.
    
    - **Example:** `man ls` to display the manual for the `ls` command.
    
- **clear**: Clear the terminal screen.
    
    - **Example:** `clear` to clear the terminal screen.
    
- **less <filename>**: View the contents of a file with scrolling capabilities.
    
    - **Example:** `less example.txt` to view the contents of `example.txt`.
    
- **nano <filename>**: Open a file in the nano text editor.
    
    - **Example:** `nano example.txt` to open `example.txt` in nano.
    
- **head <filename>**: Display the first few lines of a file.
    
    - **Example:** `head example.txt` to display the first 10 lines of `example.txt`.
    
- **tail <filename>**: Display the last few lines of a file.
    
    - **Example:** `tail example.txt` to display the last 10 lines of `example.txt`.
    
- **diff <file1> <file2>**: Compare two files.
    
    - **Example:** `diff file1.txt file2.txt` to compare `file1.txt` and `file2.txt`.
    
