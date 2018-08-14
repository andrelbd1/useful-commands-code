### Git commands
````bash
# commiting
git commit -a -m " "
# upload
git push origin nome_branch
# checking branch status
git status
# download commits from remote branch
git pull origin nome_branch
# using tool to merge branches
git mergetool


# checking commit logs
git log
# checking operation logs
git reflog
# checking logs of specific file
git log -p file-name
git log --graph --oneline --all


# changing branches
git checkout nome_branch
# show branches
git branch
# create a branch
git branch nome_branch
# show all branches
git branch -a
# show remote branches
git branch -r


# show alterations to be sent
git diff --stat
# show alterations in current branch
git diff
# show alterations between files in current branch and remote
git diff -p file-name
# show alterations between files in current branch and remote specifying a commit
git diff -p nome-do-arquivo f90b0dd3949..70ad8038d0


# altering repository url 
git remote set-url origin ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/foo
# upload a existent repository
git push ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/foo --all
````

