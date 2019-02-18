# Syntax Notes
## Directory paths
Unix/Linux conventions differ from Windows conventions, when it comes to file system navigation:

Windows Directory Path | *nix Directory Path
-|-
C:\Users\MyUserFolder | c/Users/MyUserFolder

## Strings with spaces
Input strings that we provide need to be enclosed in quotes if they contain spaces. 
> Best practice: Enclose all input strings in quotes.

## The "Home" directory
In *nix systems there is a "Home" directory, that maps to "C\Users\MyUserFolder" in Windows.\
This Home folder is where the terminal opens. It is represented by the ~ symbol.\
Typing only _**cd**_ after the command prompt will return you to the root level of the home folder.\


# Navigate the File System
### Navigate to the Home Directory
```bash
$ cd
```
### Navigate to a specific folder
```bash
$ cd /c/SomeFolder/
```
### Navigate to a specific folder (with spaces)
```bash
$ cd "/c/Some Folder/"
```
### Go back to the previous location
```bash
$ cd -
```
### Go up one directory level
```bash
$ cd ..
```

# Show directory contents
### List contents of the current directory
```bash
$ ls
```
### List all contents of the current directory (including hidden)
```bash
$ ls -a
```
### List contents of the current directory in long form
```bash
$ ls -l
```
### List all contents of the current directory in long form
```bash
$ ls -al
```
### List contents of the current directory one item per row (as a column)
```bash
$ ls -1
```
### List contents of the current directory, including subdirectory contents
```bash
$ ls *
```
### List contents of the current directory, including subdirectory contents, one item per row
```bash
$ ls -1 *
```
### List only subdirectories (not files) within current directory 
```bash
$ ls -d */
```

# Create files
### Create a new empty file in the current directory
```bash
$ touch newFile.txt
```
### Create a new empty file in the specific existing directory
```bash
$ touch ~/SomeFolder/newFile.txt
```
### Create multiple new files in the current directory
```bash
$ touch newFile1.txt newFile2.txt
```
### Append text to a file, in the current directory. If the file doesn't exist, create file
```bash
$ echo "This text is appended to the file contents" >> newFile.txt
```
### Overwrite text in a file, in the current directory. If the file doesn't exist, create file
```bash
$ echo "This text is appended to the file contents" > newFile.txt
```
### Append text to a file, at the specified path. If the file doesn't exist, create file
```bash
$ echo "This text is appended to the file contents" >> ~/ExistingParentDirectory/newFile.txt
```
### Overwrite text in a file, at the specified path. If the file doesn't exist, create file
```bash
$ echo "This text is appended to the file contents" > ~/ExistingParentDirectory/newFile.txt
```

# Create new directory
### Create a new directory in the current directory
```bash
$ mkdir NewFolderName
```
### Create a new directory (string with spaces) in the current directory 
```bash
$ mkdir "New Folder Name"
```
### Create a new directory at the specific path in the home directory
```bash
$ mkdir ~/ExistingParentFolder/NewFolderName
```
### Create a new directory at the specific path in the home directory, create parent directories as needed
```bash
$ mkdir -p ~/NewParentFolder/NewFolderName
```
### Create a new directory at the specific path in the home directory, create parent directories as needed, print details of what was done
```bash
$ mkdir -p --verbose /c/NewParentFolder/NewFolderName
```

# Remove files
### Remove specified file from the current directory
```bash
$ rm fileName.txt
```
### Prompt for confirmation before removal of the specified file from the current directory
```bash
$ rm -i fileName.txt
```
### Remove specified file from the current directory, report what was done
```bash
$ rm -v fileName.txt
```

# Remove directories
### Remove empty folder
```bash
$ rmdir FolderName
```
### Remove folder and all contents
```bash
$ rm -rf FolderName
```
