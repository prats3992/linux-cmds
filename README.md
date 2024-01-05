# Linux Commands for Beginners

## Introduction

Welcome to the world of Linux commands! This guide is designed for beginners to help you get started with some essential commands for navigating and interacting with the Linux terminal.

# Commands List


| Command | Description | More Details |
|---------|-------------|------|
| `pwd`   | Print the current working directory | [pwd.md](md_files/pwd.md) |
| `ls`    | List files and directories | [ls.md](md_files/ls.md) |
| `cd`    | Change directory | [cd.md](md_files/cd.md) |
| `cat`   | Concatenate and display file content | [cat.md](md_files/cat.md) |
| `cp`    | Copy files and directories | [cp.md](md_files/cp.md) |
| `mv`    | Move or rename files and directories | [mv.md](md_files/mv.md) |
| `mkdir` | Create directories | [mkdir.md](md_files/mkdir.md) |
| `rm`    | Remove files and directories | [rm.md](md_files/rm.md) |
| `rmdir` | Remove empty directories | [rmdir.md](md_files/rmdir.md) |
| `grep`  | Search for patterns in files | [grep.md](md_files/grep.md) |
| `head`  | Display the beginning of a file | [head.md](md_files/head.md) |
| `tail`  | Display the end of a file | [tail.md](md_files/tail.md) |
| `diff`  | Compare files line by line | [diff.md](md_files/diff.md) |
| `wc`    | Count lines, words, and characters in a file | [wc.md](md_files/wc.md) |
| `tar`   | Archive files | [tar.md](md_files/tar.md) |
| `chmod` | Change file permissions | [chmod.md](md_files/chmod.md) |

### Most Important: `scp`

The `scp` command is used to securely copy files between a local and remote host over a network. It stands for "secure copy" and is based on the SSH (Secure Shell) protocol. `scp` provides encryption and authentication, making it a secure way to transfer files.

To use `scp`, you need to specify the source file or directory and the destination where you want to copy the file or directory. The source and destination can be on the local machine or on a remote machine.

For detailed usage see: [scp.md](md_files/scp.md)

# [Redirection Operators](md_files/operator.md)

| Operator | Description |
|----------|-------------|
| `>`      | Redirects the output of a command to a file, overwriting the file if it already exists |
| `>>`     | Redirects the output of a command to a file, appending the output to the file if it already exists |
| `<`      | Redirects the input of a command from a file |
| `2>`     | Redirects the error output of a command to a file, overwriting the file if it already exists |
| `2>>`    | Redirects the error output of a command to a file, appending the output to the file if it already exists |
| `&>`     | Redirects both the standard output and error output of a command to a file, overwriting the file if it already exists |
| `&>>`    | Redirects both the standard output and error output of a command to a file, appending the output to the file if it already exists |
