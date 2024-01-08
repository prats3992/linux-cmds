# cp
## A common and important job is copying files and on linux it can be done using `cp`.
## Syntax
```bash
cp Source-File Destination
```
- #### If `Destination` does not exist, it is created.
- #### If `Destination` already exists, it is overwritten without any warning.

## Usage
### 1. Basic Usage
```bash
cat copied.txt
cat: copied.txt: No such file or directory
```
```bash
cp lines.txt copied.txt
```
#### And this created a new file `copied.txt` with data from `lines.txt`.

#### Now that `copied.txt` exists if we use it as a destination now, the previous content will be overwritten without <u><b>ALERT</b></u> so be careful.
```bash
cp new.txt copied.txt
```

### 2. Copy Multiple Files
```bash
cp Src_1 Src_2 Src_3 Destination_Directory
```
```bash
cp lines.txt friends.txt new.txt /home/pratham/
```
#### When `cp` has one or more source files and is followed by a destination directory, it copies each source file to the destination directory with the same name. 
- #### If the destination directory does not exist, it is created. 
- #### If it already exists, the files are overwritten without warning.

### 3. Copy all files of Src Directory into Destination Directory
#### There are 2 ways to copy all files of a source directory
1. Use the wildcard symbol `*`
```bash
cp /home/pratham/linux-cmds/* /home
```

2. Use `-R` option for recursive copying.

```bash
cp -R /home/pratham/linux-cmds /home
```
#### Note: If `Destination Directory` exists, the copy of `Source Directory` becomes a sub-directory under `Destination Directory`
