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
  - Use the `cp` command to copy files.
  - Example: `cp original.txt duplicate.txt`

### **Moving Files:**
  - The `mv` command moves files from one directory to another.
  - Example: `mv autumn.csv winter.csv ..`

### **Renaming Files:**
  - `mv` can rename files.
  - Example: `mv course.txt old-course.txt`

### **Deleting Files:**
  - Use `rm` to delete files.
  - Example: `rm thesis.txt backup/thesis-2017-08.txt`

### **Creating and Deleting Directories:**
  - Use `rmdir` to delete empty directories.
  - Use `rm -r` for directories with contents.
