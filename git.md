### [Git](https://git-scm.com/) commands

#### General
- List config
````bash
git config --list
````
- Set config
````bash
git config --global user.name "Fulano de Tal"
git config --global user.email fulanodetal@exemplo.br
````
- Commiting
````bash
git commit -a -m "Lorem Ipsum"
````
- Upload
````bash
git push origin branch-name
````
- Checking branch status
````bash
git status
````
- Download commits from remote branch
````bash
git pull origin branch-name
````
- Using tool to merge branches
````bash
git mergetool
````
- Undo commits permanently and also throw away any uncommitted changes
````bash
git reset --hard branch-name
````
````bash
git reset --hard HEAD~
````
- Undo the most recent local commits while leaving your working tree (the state of your files on disk) untouched
````bash
git reset HEAD~1
````
- Untrack a file that has been committed
````bash
git rm -r --cached file-name
````

#### Logs
- Checking commit logs
````bash
git log
````
- Checking operation logs
````bash
git reflog
````
- Checking logs of specific file
````bash
git log -p file-name
git log --graph --oneline --all
````

#### Branch
- changing branches
````bash
git checkout nome_branch
````
- show branches
````bash
git branch
````
- create a branch
````bash
git branch nome_branch
````
- create a branch off from the main branch
````bash
git checkout -b nome_branch main
````
- show all branches
````bash
git branch -a
````
- show remote branches
````bash
git branch -r
````

#### Stash
- save modified and staged changes
````bash
git stash
````
- list stack-order of stashed file changes
````bash
git stash list
````
- write working from the top of the stash stack
````bash
git stash pop
````
- discard the changes from the top od the stash stack
````bash
git stash drop
````

#### Diff
- show alterations to be sent
````bash
git diff --stat
````
- show alterations in current branch of what is changed but not staged
````bash
git diff
````
- show alterations in currnt branch of what is staged but not yet commited
````bash
git diff --staged
````
- show alterations between files in current branch and remote
````bash
git diff -p file-name
````
- show alterations between files in current branch and remote specifying a commit
````bash
git diff -p file-name f90b0dd3949..70ad8038d0
````

#### Repository
- show repository url
````bash
git remote -v
````
- altering repository url
````bash
git remote set-url origin ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/foo
````
- upload a existent repository
````bash
git push ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/foo --all
````
