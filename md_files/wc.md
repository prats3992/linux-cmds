# wc
### It is mainly used for counting purpose. `wc` stands for word count.
### It is used to find out number of `lines`, `word count`, `byte and characters count` in the files passed to wc in the same order.

## Syntax
```bash
wc [option] file_name(s)
```

## Usage
#### Now let's say I have the following

```bash
cat friends.txt
Patil
Sharma
Sogani
Paliwal
```
```bash
cat juniors.txt
Daga
Atharv
Yuvi
Swarup

PS: Swarup is a junior even though he is from '26.
```

#### So I have the above two files with the shown content now let's use wc on these files.

### 1. BASIC USAGE
```bash
wc juniors.txt
5 15 75 juniors.txt
```
#### So as we can compare with the file content we have `5 LINES` (counting starts from 0), `15 WORDS`, and `75 CHARACTERS`.

### 2. USING ON MULTIPLE FILES IN ONE GO
```bash
wc juniors.txt friends.txt 
5  15  75 juniors.txt
3   4  27 friends.txt
8  19 102 total
```
#### Here it also shows the total number of lines, words, characters in all files passed to `wc`.

### 3. Get number of Lines
#### Use `-l` flag for getting only the number of `lines`.
```bash
wc juniors.txt -l
5 juniors.txt
```
```bash
wc juniors.txt friends.txt -l
5 juniors.txt
3 friends.txt
8 total
```

### 4. Get number of Words
#### Use `-w` flag for getting only the number of `words`.
```bash
wc juniors.txt -w
15 juniors.txt
```
```bash
wc juniors.txt friends.txt -w
15 juniors.txt
 4 friends.txt
19 total
```
### 5. Get number of Characters or Bytes
#### Use `-c` flag for getting only the number of `bytes`.
#### Use `-m` flag for getting only the number of `characters`.
#### Note: An ASCII character is `8-bit` or `1 byte`
```bash
wc juniors.txt -c
27 friends.txt
```
```bash
wc juniors.txt -m
27 friends.txt
```

### Application of `wc`
- #### Getting how many files and directories are in the current working directory

```bash
ls
README.md  assets  images  index.html  md_files
```
```bash
ls | wc -l
5
```
#### But notice the following
```bash
ls -l
total 36
-rw-r--r-- 1 pratham pratham  2942 Jan  5 23:28 README.md
drwxr-xr-x 6 pratham pratham  4096 Jan  5 23:25 assets
drwxr-xr-x 2 pratham pratham  4096 Jan  5 23:25 images
-rw-r--r-- 1 pratham pratham 17893 Jan  6 19:07 index.html
drwxr-xr-x 2 pratham pratham  4096 Jan  6 21:32 md_files
```
```bash
ls -l| wc -l
6
```

#### See that the second output came out wrong as compared to expected, it is because `ls -l` gave an extra line at the starting of its output that reads `total 36`.