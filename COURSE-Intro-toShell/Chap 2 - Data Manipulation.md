## Viewing File Contents
- **Using `cat`**: Displays the entire contents of a file on the screen.
- Example: `cat agarwal.txt`

- **Paging Output with `less`**: Displays file contents one page at a time, allowing easy scrolling.
- Example: `less seasonal/spring.csv seasonal/summer.csv`

- **Using `head` to Preview Files**: Displays the first few lines of a file, typically 10 by default.
- Example: `head seasonal/summer.csv`

## Navigating and Listing Directory Contents
- **Recursive Listing with `ls`**: Lists all files and directories recursively.
- Example*: `ls -R`

## Getting Command Help
- **Using `man` Command**: Retrieves detailed information about a command, including its purpose, usage, and available options.
- Example*: `man head`

## Selecting Specific Columns from a File
- **Using `cut` Command**: Extracts specific columns from a text file based on the specified delimiter.
- Example*: `cut -f 2-5,8 -d , values.csv`

## Repeating and Recalling Commands
- **Command History**: Allows recalling and repeating previously executed commands efficiently.
- Example*: Use the up-arrow key to cycle through recent commands, or use `!55` to rerun the 55th command.

## Selecting Lines with Specific Values
- **Using `grep`**: Searches for specific patterns or values within files and prints matching lines.
- Example*:
  - `grep molar seasonal/autumn.csv`
  - `grep -v -n molar seasonal/spring.csv` (Inverts match to show lines not containing the word "molar")

These commands provide essential functionalities for efficiently viewing, navigating, and manipulating files and directories in Unix shell environments.
