# cd
### Since Linux is supposed to be a CLI, this command helps in moving around the computer’s folders and files, which we call the file system.
### The `cd` stands for "change directory".


### For the examples we are going to be using the following file tree
> [!NOTE]
> #### The files are shown with extensions while the directories don't have extensions.
```bash
.
├── __init__.py
├── __pycache__
│   ├── __init__.cpython-310.pyc
│   ├── urls.cpython-310.pyc
│   └── views.cpython-310.pyc
├── admin.py
├── apps.py
├── migrations
│   └── __init__.py
├── models.py
├── templates
│   └── blog
│       ├── about.html
│       └── home.html
├── tests.py
├── urls.py
└── views.py

4 directories, 13 files
```
```bash
pwd
/home/pratham/blog/blog/django_project/blog
```

## Syntax
```bash
cd directory
```

## Usage
### 1. Move out of a directory and into the parent directory
```bash
cd ..
```
```bash
pwd
/home/pratham/blog/blog/django_project
```
### 2. Move into a child directory
```bash
cd migrations
```
```bash
pwd
/home/pratham/blog/blog/django_project/blog/migrations
```
### 3. Go directly to home directory
```bash
cd ~
```
```bash
pwd
/home/pratham
```

### 4. Go to a specific directory using absolute/relative path
```bash
cd ../django_project
```
#### So the above path moves up the tree to the parent directory then go to another child directory called `django_project`.

```bash
pwd
/home/pratham/blog/blog/django_project/django_project
```

> [!TIP]
> #### If the file name or directory or the path you are passing to `cd` has a space then put the whole thing in quotes(`""`)
> #### Like `cd "Useless New Folder"` or `cd "/home/pratham/dumb blog/blog/django_project/blog/migrations"`

### 5. Go to previously accessed directory
```bash
pwd
/home/pratham/blog/blog/django_project/blog
```
```
cd ~/linux-cmds/md_files/
```
```bash
pwd
/home/pratham/linux-cmds/md_files
```
```bash
cd -
```
```bash
pwd
/home/pratham/blog/blog/django_project/blog
```

#### So, `cd -` directly sent me back to the last directory I was in i.e. `/home/pratham/blog/blog/django_project/blog`. It is kinda like switching between the last app you have open on your phone and the current one.