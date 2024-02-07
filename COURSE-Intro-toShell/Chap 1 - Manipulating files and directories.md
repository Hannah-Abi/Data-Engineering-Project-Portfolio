### **Understanding Your Location in the Filesystem:**
- The filesystem organizes files and directories, each identified by an absolute path.
- Absolute paths start from the root directory (`/`) and specify the full path to a file or directory.
- The `pwd` command displays the absolute path of your current working directory.

### **Identifying Files and Directories:**
- Use the `ls` command to list the contents of your current directory.
- Typing `ls` on its own lists the contents of the current directory.
- Adding file or directory names as arguments to `ls` lists their contents.
- For example, `ls /home/repl` shows the contents of the `/home/repl` directory.

### **Understanding Absolute and Relative Paths:**
- Absolute paths are fixed locations in the filesystem, starting from the root directory.
  - Example: `/home/repl/course.txt` is an absolute path to the file `course.txt` located in the `/home/repl` directory.
- Relative paths specify locations relative to the current working directory.
  - Example: If the current directory is `/home/repl`, the relative path `seasonal` refers to the `/home/repl/seasonal` directory.

### **Navigating Between Directories:**
- Use the `cd` command to change directories.
- For example, `cd seasonal` moves to the `/home/repl/seasonal` directory.
- After changing directories, confirm the current location with `pwd`.
- To return to the home directory (`/home/repl`), use `cd /home/repl`.
