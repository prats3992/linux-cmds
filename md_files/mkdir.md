# mkdir
### `mkdir` stands for "make directory."
### Syntax
```bash
mkdir [OPTION] dir_name(s)
```

### Usage
### 1. Basic Usage
```bash
mkdir dir1
```
#### Makes a directory named `dir1` in the current working directory

### 2. Multiple Directories in one go
```bash
mkdir dir1 dir2 dir3
```

### 3. Displays a message for every directory created
```bash
mkdir dir1 dir2 dir3 -v
mkdir: created directory 'dir1'
mkdir: created directory 'dir2'
mkdir: created directory 'dir3'
```

### 4. Create all required parent directories
```bash
mkdir ./parent/child/any_name_works
mkdir: cannot create directory ‘/parent/child/any_name_works’: No such file or directory
```
#### This happened because `./parent` and `./parent/child` don't exist so `./parent/child/any_name_works` could not be made but we can do the following and to see how it works we use the `-v` option.

```bash
mkdir ./parent/child/any_name_works -p -v
mkdir: created directory './parent'
mkdir: created directory './parent/child'
mkdir: created directory './parent/child/any_name_works'
```