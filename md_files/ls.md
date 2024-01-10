# ls

### It returns the contents of the directory.

On running this command

```bash
pratham@Pratham-Inspiron:~/linux-cmds$ ls
```

I get the following output

```bash
README.md  assets  images  index.html  md_files
```

Here the command `ls` takes the current working directory as the default argument.

The `ls` command is used to list the files and directories in a directory. It can be customized with various options to display different information. Here are some commonly used options:

- `-R`: Recursively lists all files and directories in the specified directory and its subdirectories.

```bash
ls -R
.:
README.md  assets  images  index.html  md_files

./assets:
css  js  sass  webfonts
AND IT GOES ON
```

- `-a`: Shows all files and directories, including hidden ones that start with a dot (`.`).

```bash
ls -a
.  ..  .git  README.md  assets  images  index.html  md_files
```
> [!NOTE]
> Here `.` and `..` are special references to the directory itself and the parent directory respectively.

- `-l`: Displays detailed information about each file and directory, including permissions, owner, size, and modification date.

```bash
ls -l
total 36
-rw-r--r-- 1 pratham pratham  2885 Jan  7 02:05 README.md
drwxr-xr-x 6 pratham pratham  4096 Jan  9 19:36 assets
drwxr-xr-x 2 pratham pratham  4096 Jan  7 08:24 images
-rw-r--r-- 1 pratham pratham 18217 Jan  7 08:27 index.html
drwxr-xr-x 2 pratham pratham  4096 Jan  8 14:01 md_files
```

- `-t`: Sorts the files and directories by modification time, with the most recently modified ones appearing first.

```bash
ls -t
assets  md_files  index.html  images  README.md
```
