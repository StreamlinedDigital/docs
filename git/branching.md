##Branching

###delete a local branch
```$ git branch -d hotfix```

###delete a remote branch
```$ git push origin <branchName> --delete```

###oops i committed something to the wrong branch

    git reset --soft HEAD^
    git checkout [branchname]
    git commit
