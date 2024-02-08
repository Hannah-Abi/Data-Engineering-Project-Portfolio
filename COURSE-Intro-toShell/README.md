## Chapter 1 - Manipulating files and directories

| Command Line  | Description                                       | Example                                             |
|---------------|---------------------------------------------------|-----------------------------------------------------|
| `pwd`         | Displays the absolute path of the current directory. | `pwd`                                               |
| `ls`          | Lists the contents of the current directory.       | `ls`                                                |
| `ls <directory>` | Lists the contents of the specified directory.   | `ls /home/repl`                                     |
| `cd <directory>` | Changes the current directory to the specified directory. | `cd seasonal`                                   |
| `cd ..`       | Moves up one directory level from the current directory. | `cd ..`                                             |
| `cd ../..`    | Moves up two directory levels from the current directory. | `cd ../..`                                          |
| `cd .`        | Has no effect; remains in the current directory.   | `cd .`                                              |
| `ls ~`        | Lists the contents of the home directory.          | `ls ~`                                              |
| `cd ~`        | Changes the current directory to the home directory. | `cd ~`                                              |
| `cp <source> <destination>` | Copies files from the source to the destination. | `cp original.txt duplicate.txt`                   |
| `mv <source> <destination>` | Moves files from the source to the destination.   | `mv autumn.csv winter.csv ..`                      |
| `mv <old_name> <new_name>` | Renames files from old_name to new_name.           | `mv course.txt old-course.txt`                     |
| `rm <file>`   | Deletes the specified file.                       | `rm thesis.txt backup/thesis-2017-08.txt`          |
| `rmdir <directory>` | Deletes the specified empty directory.          | `rmdir empty_directory`                             |
| `rm -r <directory>` | Deletes the specified directory and its contents. | `rm -r directory_with_contents`                     |

## Chapter 2 . Data Manipulation with Unix Shell
Here's the table with examples included:

| Command Line                      | Description                                                                                                  | Example                                             |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| `cat FILE`                        | Displays the entire contents of the specified file on the screen.                                            | `cat agarwal.txt`                                  |
| `less FILE1 FILE2 ...`            | Displays file contents one page at a time, enabling easy scrolling through multiple files.                  | `less seasonal/spring.csv seasonal/summer.csv`     |
| `head FILE`                       | Displays the first few lines of the specified file, typically the first 10 lines by default.                | `head seasonal/summer.csv`                        |
| `ls -R`                           | Lists all files and directories recursively in the current directory and its subdirectories.                | `ls -R`                                             |
| `man COMMAND`                     | Retrieves detailed information about the specified command, including its purpose, usage, and options.      | `man head`                                          |
| `cut OPTIONS FILE`                | Extracts specific columns from a text file based on the provided options and delimiter.                      | `cut -f 2-5,8 -d , values.csv`                     |
| Use the command history          | Allows recalling and repeating previously executed commands efficiently.                                       | Use up-arrow key or `!55` to repeat commands.      |
| `grep PATTERN FILE`               | Searches for lines containing the specified pattern in the specified file and prints matching lines.         | `grep molar seasonal/autumn.csv`                   |
| `grep OPTIONS PATTERN FILE`       | Searches for lines containing the specified pattern in the specified file and prints matching lines based on the provided options. In the example, `-v -n` inverts the match and displays line numbers. | `grep -v -n molar seasonal/spring.csv`           |
