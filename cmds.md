# Commands List


| Command | Description | File |
|---------|-------------|------|
| `pwd`   | Print the current working directory | [pwd.md](pwd.md) |
| `ls`    | List files and directories | [ls.md](ls.md) |
| `cd`    | Change directory | [cd.md](cd.md) |
| `cat`   | Concatenate and display file content | [cat.md](cat.md) |
| `cp`    | Copy files and directories | [cp.md](cp.md) |
| `mv`    | Move or rename files and directories | [mv.md](mv.md) |
| `mkdir` | Create directories | [mkdir.md](mkdir.md) |
| `rm`    | Remove files and directories | [rm.md](rm.md) |
| `rmdir` | Remove empty directories | [rmdir.md](rmdir.md) |
| `grep`  | Search for patterns in files | [grep.md](grep.md) |
| `head`  | Display the beginning of a file | [head.md](head.md) |
| `tail`  | Display the end of a file | [tail.md](tail.md) |
| `diff`  | Compare files line by line | [diff.md](diff.md) |
| `wc`    | Count lines, words, and characters in a file | [wc.md](wc.md) |
| `tar`   | Archive files | [tar.md](tar.md) |
| `chmod` | Change file permissions | [chmod.md](chmod.md) |

### Most Important: `scp`

The `scp` command is used to securely copy files between a local and remote host over a network. It stands for "secure copy" and is based on the SSH (Secure Shell) protocol. `scp` provides encryption and authentication, making it a secure way to transfer files.

To use `scp`, you need to specify the source file or directory and the destination where you want to copy the file or directory. The source and destination can be on the local machine or on a remote machine.

For detailed usage see: [scp.md](scp.md)

# Redirection Operators

| Operator | Description |
|----------|-------------|
| `>`      | Redirects the output of a command to a file, overwriting the file if it already exists |
| `>>`     | Redirects the output of a command to a file, appending the output to the file if it already exists |
| `<`      | Redirects the input of a command from a file |
| `2>`     | Redirects the error output of a command to a file, overwriting the file if it already exists |
| `2>>`    | Redirects the error output of a command to a file, appending the output to the file if it already exists |
| `&>`     | Redirects both the standard output and error output of a command to a file, overwriting the file if it already exists |
| `&>>`    | Redirects both the standard output and error output of a command to a file, appending the output to the file if it already exists |
