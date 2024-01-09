# Redirection Operators
| Operator | Description | Example |
|----------|-------------|---------|
| `>`      | Redirects standard output to a file, overwriting its contents | `ls > file.txt` |
| `>>`     | Redirects standard output to a file, appending to its contents | `echo "Hello" >> file.txt` |
| `<`      | Redirects standard input from a file | `./a.out < file.txt` |
| `2>`     | Redirects standard error to a file | `rm * 2> error.txt` |
| `2>>`    | Redirects standard error to a file, appending to its contents | `cp lines /bin 2>> error.txt` |
| `&>`     | Redirects both standard output and standard error to a file | `mkdir newdir &> output.txt` |
| `\|`      | Pipes the output of one command as input to another command | `cat new.txt \| head -n30` |
## Explanation:
- `>`: Redirects the standard output of a command to a file, overwriting its contents. For example, `ls > file.txt` will execute the `ls` command and write its output to `file.txt`, overwriting any existing content in the file.
- `>>`: Redirects the standard output of a command to a file, appending to its contents. For example, `echo "Hello" >> file.txt` will append the string "Hello" to the end of `file.txt`.
- `<`: Redirects the standard input of a command from a file. For example, `./a.out < file.txt` will execute the `a.out` program and use `file.txt` as the input for the program.
- `2>`: Redirects the standard error of a command to a file. For example, `rm * 2> error.txt` will delete all files in the current directory and redirect any error messages to `error.txt`.
- `2>>`: Redirects the standard error of a command to a file, appending to its contents. For example, `cp lines /bin 2>> error.txt` will copy the file `lines` to the `/bin` directory and append any error messages to `error.txt`.
- `&>`: Redirects both the standard output and standard error of a command to a file. For example, `mkdir newdir &> output.txt` will create a new directory named `newdir` and redirect both the standard output and standard error to `output.txt`.
- `|`: Pipes the output of one command as input to another command. For example, `cat new.txt | head -n30` will display the first 30 lines of the file `new.txt`.
