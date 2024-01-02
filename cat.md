# cat
### Allows users to view the contents of the files primarily.
### The basic syntax is as follows
```bash
cat file_name
```
### For Example
#### On running the following command
```bash
cat temp.txt
```
#### I get the following output
```bash
Bunch of random Text
You can find temp.txt on my github
it wont be available here srry my bad
```

### Now this command also allows for a bunch of interesting stuff like
### 1. View Contents of a File along with Line Numbers
#### Syntax:
```bash
cat file_name -n
```
#### Usage:
```bash
cat temp.txt -n
    1  Bunch of random Text
    2  You can find temp.txt on my github
    3  it wont be available here srry my bad
```
### 2. Create a file and add content
#### Syntax:
```bash
cat > file_name
```
#### Usage
```bash
cat > temp_new.txt
Now you can type your text on the terminal itself 
then press Ctrl + D once done
you can even press Enter and write multiple lines before Ctrl + D for 
multi-line text to be saved onto the file
```
### 3. Append the Contents of One File to the End of Another File
#### Syntax:
```bash
cat file_name1 >> file_name2
```
#### Appending here means that if the destination or target file i.e. `file_name2` already has some content then it won't be overwritten.

#### Usage:
```bash
cat temp.txt
Bunch of random Text
You can find temp.txt on my github
it wont be available here srry my bad
```
```bash
cat new.txt
/home/pratham/linux-cmds
```
```bash
cat temp.txt >> new.txt
```
#### This will append the content of `temp.txt` to `new.txt` i.e. the appended content starts from the next line
```bash
cat new.txt
/home/pratham/linux-cmds
Bunch of random Text
You can find temp.txt on my github
it wont be available here srry my bad
```

### 4. Merge Contents of Multiple Files
#### Syntax:
```bash
cat file1.txt file2.txt > merged_file.txt
```
#### It can take even more files if there are more to be merged.
#### Also note that the content is merged in the order the files are plced in the syntax.

#### Usage:
```bash
cat temp.txt temp_new.txt > merged.txt
```
```bash
cat merged.txt
Bunch of random Text
You can find temp.txt on my github
it wont be available here srry my badNow you can type your text on the terminal itself 
then press Ctrl + D once done
you can even press Enter and write multiple lines before Ctrl + D for 
multi-line text to be saved onto the file
```
#### Note that the 3<sup>rd</sup> line of `merged.txt` the words [ <i><u>badNow</u></i> ] combined because the first file had no trailing whitespaces so the second continued from exactly where the first file ended.