### Git commands

#### General
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
- show all branches
````bash
git branch -a
````
- show remote branches
````bash
git branch -r
````

#### Diff
- show alterations to be sent
````bash
git diff --stat
````
- show alterations in current branch
````bash
git diff
````
- show alterations between files in current branch and remote
````bash
git diff -p file-name
````
- show alterations between files in current branch and remote specifying a commit
````bash
git diff -p nome-do-arquivo f90b0dd3949..70ad8038d0
````

#### Repository
- altering repository url
````bash
git remote set-url origin ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/foo
````
- upload a existent repository
````bash
git push ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/foo --all
````