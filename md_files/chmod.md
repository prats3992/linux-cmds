# chmod

### The `chmod` command is used to modify permissions so that it can grant or restrict access to directories and files, the permissions like who can read(`r`), write(`w`) or execute(`x`) the file.

## Syntax

```bash
chmod [OPTIONS] [MODE] file_name
```

#### MODE: The permissions to be set, represented by a three-digit octal number or alphabetic form.

## Some Important Information

| Operators | Definition                                  |
| --------- | ------------------------------------------- |
| `+`       | Add permissions                             |
| `-`       | Remove permissions                          |
| `=`       | Set the permissions to the specified values |

| Letters | Definition         | Octal Values |
| ------- | ------------------ | ------------ |
| `r`     | Read permission    | 4            |
| `w`     | Write permission   | 2            |
| `x`     | Execute permission | 1            |

> [!IMPORTANT]
>
> ### First digit specify the permission for Owner.
>
> ### Second digit specify the permission for Group.
>
> ### Third digit specify the permission for Others.
>
> ### The digits are calculated by adding the values of the individual permissions.

| Reference | Class  |
| --------- | ------ |
| `u`       | Owner  |
| `g`       | Group  |
| `o`       | Others |
| `a`       | All    |

#### To check current file permissions

```bash
ls -l filename
```

## How to use it ?

### Making a file executable

```bash
chmod a+x filename
```

#### By default it applies provided permissions to all so, we could also do

```bash
chmod +x filename
```

#### This means all (owner,groups,others) got the permission to execute the file. It's octal equivalent is:

```bash
chmod 111 filename
```

### Using Octal more proficiently

```bash
chmod 764 filename
```

- #### `7` represent permission of <b><u> Owner</u></b> which are (`rwx`). {4+2+1}
- #### `6` represent permission of <b><u>Group</u></b> which are (`rw`). {4+2}
- #### `4` represent permission of <b><u>Other</u></b> which is (`r`). {4}
