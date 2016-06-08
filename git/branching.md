##Branching

###delete a local branch
```$ git branch -d hotfix```

###delete a remote branch
```$ git push origin <branchName> --delete```

###oops i committed something to the wrong branch

    git reset --soft HEAD^
    git checkout [branchname]
    git commit



###Rename your local branch.
1. If you are on the branch you want to rename:
2. Delete the old-name remote branch and push the new-name local branch.
3. Reset the upstream branch for the new-name local branch. Switch to the branch and then:

    git branch -m new-name. ...
    git push origin :old-name new-name.
    git push origin -u new-name.
