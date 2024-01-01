# Linux Commands for Beginners

## Introduction

Welcome to the world of Linux commands! This guide is designed for beginners to help you get started with some essential commands for navigating and interacting with the Linux terminal.

# Commands List


| Command | Description | More Details |
|---------|-------------|------|
| `pwd`   | Print the current working directory | [pwd.md](pwd) |
| `ls`    | List files and directories | [ls.md](ls) |
| `cd`    | Change directory | [cd.md](cd) |
| `cat`   | Concatenate and display file content | [cat.md](cat) |
| `cp`    | Copy files and directories | [cp.md](cp) |
| `mv`    | Move or rename files and directories | [mv.md](mv) |
| `mkdir` | Create directories | [mkdir.md](mkdir) |
| `rm`    | Remove files and directories | [rm.md](rm) |
| `rmdir` | Remove empty directories | [rmdir.md](rmdir) |
| `grep`  | Search for patterns in files | [grep.md](grep) |
| `head`  | Display the beginning of a file | [head.md](head) |
| `tail`  | Display the end of a file | [tail.md](tail) |
| `diff`  | Compare files line by line | [diff.md](diff) |
| `wc`    | Count lines, words, and characters in a file | [wc.md](wc) |
| `tar`   | Archive files | [tar.md](tar) |
| `chmod` | Change file permissions | [chmod.md](chmod) |

### Most Important: `scp`

The `scp` command is used to securely copy files between a local and remote host over a network. It stands for "secure copy" and is based on the SSH (Secure Shell) protocol. `scp` provides encryption and authentication, making it a secure way to transfer files.

To use `scp`, you need to specify the source file or directory and the destination where you want to copy the file or directory. The source and destination can be on the local machine or on a remote machine.

For detailed usage see: [scp.md](scp)

# [Redirection Operators](operator)

| Operator | Description |
|----------|-------------|
| `>`      | Redirects the output of a command to a file, overwriting the file if it already exists |
| `>>`     | Redirects the output of a command to a file, appending the output to the file if it already exists |
| `<`      | Redirects the input of a command from a file |
| `2>`     | Redirects the error output of a command to a file, overwriting the file if it already exists |
| `2>>`    | Redirects the error output of a command to a file, appending the output to the file if it already exists |
| `&>`     | Redirects both the standard output and error output of a command to a file, overwriting the file if it already exists |
| `&>>`    | Redirects both the standard output and error output of a command to a file, appending the output to the file if it already exists |
