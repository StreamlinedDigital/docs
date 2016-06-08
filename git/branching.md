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
If you are on the branch you want to rename:
    git branch -m new-name. ...
Delete the old-name remote branch and push the new-name local branch.
    git push origin :old-name new-name.
Reset the upstream branch for the new-name local branch. Switch to the branch and then:
    git push origin -u new-name.
