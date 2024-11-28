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
# We did not create a GitHub repo to push our code to. To do so, We need to create a repo on Github, by going to the website. Name the repo, the same way as our local repo and don't initialize it with a readme.md file as our local repo already exists.
cd /workspaces/tmp/new-project
git remote add origin https://github.com/<your-username>/<repository-name>.git
git push -u origin main 
```


## Cloning 
 3 ways to clone : HTTPS, SSH, Github CLI.

 Since we are using Github codespaces, it creates automatically a **workspace*s*** folder. In it, we'll create a a folder called temp. (We probably should have created a *workspace* folder).
 ```sh
mkdir tmp
cd tmp
# modify the files 
git add .
git commmit -m 'files updated'
git push 
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
git commit #in this case a windows in the editor should open to write a message 
# an alternative is 
git commit -m "WRITE INFO CONCERNING THE COMMIT"
```
Set the gloabl editor 
```sh
git config --global core.editor emacs 
```

### log 

`git log` will show recent git commit to teh git tree. 


### Gitconfig file 

The `gifconfig` file is what stores your global configurations for git. Such as email, name, editor and more. 

Showing the content of our .gitconfig file
```sh
git config --list
```
