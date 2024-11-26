# Github-Examples
A repo containing GitHub for programmatic examples

## Git Hidden Folder

The hidden folder ```.git``` (you can view with ```ls -la```) indicates that the project is a git repo. The ```.git``` folder is automatically added to the folder you cloned. 

If you are working from scratch, and want your project to be a git repo. Use `git init`.
```sh
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch readme.md #create the file
code readme.md
# make changes to readme.md file 
git status
git add . 
git commit -m "add readme file" 
```


## Cloning 
 3 ways to clone : HTTPS, SSH, Github CLI.

 Since we are using Github codespaces, it creates automatically a **workspace*s*** folder. In it, we'll create a a folder called temp. (We probably should have created a *workspace* folder).
 ```sh
mkdir tmp
cd tmp
 ```


 ### HTTPS

 ```sh
git clone https://github.com/ExamProCo/Github-Examples.git
ls -la
cd Github-Examples
ls -la
 ```

 ### Git add

 When we want to Stage all the changes we made `git add .`


 ### Reset 

Allows you to move move Staged changes to be Unstaged. Useful when you want to revert the files to be commited. 
```sh
git add .
git reset
```
> git reset will revert a git add . 

### Status

Will show you what files will or will not be commited.

```
git status 
```

### Commit 

Commit, commit your code. It opens the commit message editor (editor that needs to be config prior). 
```sh
git commit
```
Set the gloabl editor 
```sh
git config --global core.editor emacs 
```


### Gitconfig file 

The `gifconfig` file is what stores your global configurations for git. Such as email, name, editor and more. 

Showing the content of our .gitconfig file
```sh
git config --list
```
