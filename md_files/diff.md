# diff
The `diff` command in Linux is used to compare and find the differences between two files or directories. It provides a comprehensive way to analyze changes in text files.

## Syntax

```bash
$ diff file1.txt file2.txt
```

## Usage
```bash
cat f1.txt
Gujarat
Uttar Pradesh
Kolkata
Bihar
Jammu and Kashmir

cat f2.txt
Tamil Nadu
Gujarat
Andhra Pradesh
Bihar
uttar pradesh
```

### 1. Basic Use
```bash
diff f1.txt f2.txt
0a1
> Tamil Nadu
2,3c3
< Uttar Pradesh
< Kolkata
---
> Andhra Pradesh
5c5
< Jammu and Kashmir
---
> uttar pradesh
```

#### Okay so this makes no sense but hopefully in a minute it will,
#### In the above case, `0a1` which means after lines 0(at the very beginning of file) you have to `add Tamil Nadu` to match the second file line number 1.
- #### Lines preceded by `<` are lines from the `first file`.
- #### Lines preceded by `>` are lines from the `second file`.
- #### Line containing `2,3c3` which means from line 2 to line 3 in the first file needs to be changed to match line number 3 in the second file. It then tells us those lines with the above symbols.
- #### The dashes `---` merely separate the lines of file 1 and file 2.

### 2. Message shown if files are different
```bash
diff f1.txt f2.txt -q
Files f1.txt and f2.txt differ
```
#### There is no Custom Message just a default one `Files file1 and file2 differ`.

### 3. Compare the files side by side
```bash
diff f1.txt f2.txt -y
                                                              > Tamil Nadu
Gujarat                                                         Gujarat
Uttar Pradesh                                                 | Andhra Pradesh
Kolkata                                                       <
Bihar                                                           Bihar
Jammu and Kashmir                                             | uttar pradesh
```
#### Lines with `>` mean line is from `file2`.
#### Lines with `<` mean line is from `file1`.
#### Lines with `|` mean content on the line is different in both files.