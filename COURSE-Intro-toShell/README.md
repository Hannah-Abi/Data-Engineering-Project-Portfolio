## Introduction to Shell 

### Chapter 1 - Manipulating files and directories

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

### Chapter 2 . Data Manipulation with Unix Shell
