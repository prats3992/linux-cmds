# mv

### In Linux, `mv` has 2 distinct uses

### 1. Renaming a file or directory.

### 2. Moving a file or directory to another location.(Move here means Cut and Paste)

## Syntax

```bash
mv [OPTION(s)] Source_file_name(s) Destination_file_name
```

### Here,

- ### Source_file_name(s): The name of the files that we want to rename or move.
- ### Destination_file_name: The name of the new location or the name of the file.

## Uses

### 1. Rename a file

```bash
mv old_name new_name
```
#### NOTE: This command renames `old_name` to `new_name`. If `new_name` already exists, in that case, it will be overwritten without prompting for confirmation.

### 2. Move a File

```bash
mv file destination_path
```

### 3. Move Multiple files
```bash
mv file_1 file_2 file_3 destination_path
```

