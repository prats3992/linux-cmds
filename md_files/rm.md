# rm
### `rm` stands for remove. 
### By default, it does not remove directories. 
> [!IMPORTANT]
> ### This command works silently by default and you should be very careful while running rm command because once you delete the files then you are not able to recover the contents of files and directories.

## Syntax
```bash
rm [OPTION] file(s)
```
### 1. Default Usage
```bash
rm lines.txt
```
### 2. Removing more than one file at a time
```bash
rm lines.txt new.txt
```
#### This can also be done using wildcard or Regex
#### Like if I want to remove all `.txt files`
```bash
rm *.txt
```

### 3. To get confirmation before removal of file
```bash
rm -i md_files/new.txt 
rm: remove regular file 'md_files/new.txt'? n
```
#### This is useful when removing multiple files or when you want to remove only some files that match the regex pattern provided.

### 4. Remove all files from the directory and its subdirectories
```bash
ls
assets  images  md_files
```
```bash
rm *
rm: cannot remove 'assets': Is a directory
rm: cannot remove 'images': Is a directory
rm: cannot remove 'md_files': Is a directory
```
```bash
rm -r *
```
```bash
ls
```