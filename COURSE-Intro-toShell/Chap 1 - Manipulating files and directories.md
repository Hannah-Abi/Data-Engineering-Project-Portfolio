### **Understanding Your Location in the Filesystem:**
- The filesystem organizes files and directories, each identified by **an absolute path**.
- **Absolute paths** start from the root directory (`/`) and specify the full path to a file or directory.
- The `pwd` command displays the absolute path of your current working directory.

### **Identifying Files and Directories:**
- Use the `ls` command to list the contents of your **current** directory.
- Typing `ls` on its own lists the contents of the current directory.
- Adding file or directory names as arguments to `ls` lists their contents.
- For example, `ls /home/repl` shows the contents of the `/home/repl` directory.

### **Understanding Absolute and Relative Paths:**
- Absolute paths are fixed locations in the filesystem, starting from the root directory.
  - **Example**: `/home/repl/course.txt` is an absolute path to the file `course.txt` located in the `/home/repl` directory.
- Relative paths specify locations relative to the current working directory.
  - **Example**: If the current directory is `/home/repl`, the relative path `seasonal` refers to the `/home/repl/seasonal` directory.

### **Navigating Between Directories:**
- Use the `cd` command to change directories.
- For example, `cd seasonal` moves to the `/home/repl/seasonal` directory.
- After changing directories, confirm the current location with `pwd`.
- To return to the home directory (`/home/repl`), use `cd /home/repl`.

### **Moving Up a Directory:**
- The parent directory of a directory is the directory above it in the filesystem hierarchy.
- For example, `/home` is the parent of `/home/repl`, and `/home/repl` is the parent of `/home/repl/seasonal`.
- To move up a directory, use the special path `..`, which represents "the directory above the one I'm currently in".
- For instance, if you are in `/home/repl/seasonal`, `cd ..` moves you up to `/home/repl`, and `cd ../..` puts you in `/home`.
- The command `cd .` has no effect because it moves you into the directory you're currently in.
- Another special path is `~`, which represents "your home directory", such as `/home/repl`.
- `ls ~` lists the contents of your home directory, and `cd ~` takes you to your home directory.

### **Copying Files:**
- Use the `cp` command to copy files, move them to other directories, or rename them.
    - For example, `cp original.txt duplicate.txt` creates a copy of `original.txt` called `duplicate.txt`.
- If the last parameter to `cp` is an existing directory, all files are copied into that directory.
    - For instance, `cp seasonal/summer.csv backup/summer.bck` copies the `summer.csv` file from the `seasonal` folder to the `backup` folder and renames it `summer.bck`.

### Moving Files
To move files, you use the `mv` command. For instance:
```bash
mv autumn.csv winter.csv ..
```
This moves `autumn.csv` and `winter.csv` up one directory.

### Renaming Files
The `mv` command can also rename files. For example:
```bash
mv course.txt old-course.txt
```
This renames `course.txt` to `old-course.txt`.

### Deleting Files
To delete files, use the `rm` command:
```bash
rm thesis.txt backup/thesis-2017-08.txt
```
This removes both `thesis.txt` and `backup/thesis-2017-08.txt`.

### Managing Directories
Directories can be renamed using `mv`. To delete them, you can use `rmdir`, which only works on empty directories. Experienced users can use the `-r` option with `rm` to delete directories and their contents.
