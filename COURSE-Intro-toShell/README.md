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
| Command Line                       | Description                                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `cat agarwal.txt`                  | Displays the entire contents of the file `agarwal.txt` on the screen.                                        |
| `less seasonal/spring.csv seasonal/summer.csv` | Displays file contents one page at a time, allowing easy scrolling.                                           |
| `head seasonal/summer.csv`        | Displays the first few lines of the file `seasonal/summer.csv`, typically 10 by default.                     |
| `ls -R`                            | Lists all files and directories recursively in the current directory and its subdirectories.                |
| `man head`                         | Retrieves detailed information about the `head` command, including its purpose, usage, and available options.|
| `cut -f 2-5,8 -d , values.csv`     | Extracts specific columns from the file `values.csv` based on the specified delimiter.                        |
| Use the up-arrow key to cycle through recent commands, or use `!55` to rerun the 55th command. | Allows recalling and repeating previously executed commands efficiently.                                      |
| `grep molar seasonal/autumn.csv`  | Searches for lines containing the word "molar" in the file `seasonal/autumn.csv` and prints matching lines.    |
| `grep -v -n molar seasonal/spring.csv` | Inverts match to show lines not containing the word "molar" in the file `seasonal/spring.csv`, along with line numbers. |
