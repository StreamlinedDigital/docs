#Adding a remote repo

##Setup the repo
-	add the gitignore & readme

##Initialize the remote repo
	git init
	git remote add origin git@github.com:StreamlinedStudio/sellrstuff.git

##Pull the .gitignore and readme from the remote branch
	git pull origin master


##Add, Commit & Push repo to the remote
	git status /check to make sure the .gitignore files are not included
	git add .  /adds all files
	git commit -m "uploaded project"
	git push -u origin master

##Verify
-	go to the remote and verify



##Change to a different remote
	git remote set-url origin git@github.com:USERNAME/OTHERREPOSITORY.git



#Branching

###delete a local branch
`$ git branch -d hotfix`


###delete a remote branch
`$ git push origin <branchName> --delete`

###oops i committed something to the wrong branch
````
    git reset --soft HEAD^
    git checkout [branchname]
    git commit
````


###Rename a branch.
````
    git branch -m new-name. ...
    git push origin :old-name new-name.
    git push origin -u new-name.
````


http://nvie.com/posts/a-successful-git-branching-model/#why-git
## Git Branching

##Main Branches

###Master
We consider origin/master to be the main branch where the source code of HEAD always reflects a production-ready state.

###Develop
We consider origin/develop to be the main branch where the source code of HEAD always reflects a state with the latest delivered development changes for the next release. Some would call this the “integration branch”. This is where any automatic nightly builds are built from.  When the source code in the develop branch reaches a stable point and is ready to be released, all of the changes should be merged back into master somehow and then tagged with a release number.

##Supporting Branches

Unlike the main branches, these branches always have a limited life time, since they will be removed eventually.

###Feature branches
- May branch off from: develop
- Must merge back into: develop
- Branch Naming Convention: anything except master, develop, release-*, or hotfix-*

Used to develop new features for the upcoming or a distant future release.  The essence of a feature branch is that it exists as long as the feature is in development, but will eventually be merged back into develop or discarded.  Feature branches typically exist in developer repos only, not in origin.

###Release branches
- May branch off from: develop
- Must merge back into: develop and master
- Branch naming convention: release-*

The key moment to branch off a new release branch from develop is when develop (almost) reflects the desired state of the new release. At least all features that are targeted for the release-to-be-built must be merged in to develop at this point in time. All features targeted at future releases may not—they must wait until after the release branch is branched off.

When the state of the release branch is ready to become a real release, some actions need to be carried out. First, the release branch is merged into master.  Next, that commit on master must be tagged for easy future reference to this historical version. Finally, the changes made on the release branch need to be merged back into develop, so that future releases also contain these bug fixes.

###Hotfix branches
- May branch off from:master
- Must merge back into: develop and master
- Branch naming convention: hotfix-*

They arise from the necessity to act immediately upon an undesired state of a live production version. When a critical bug in a production version must be resolved immediately, a hotfix branch may be branched off from the corresponding tag on the master branch that marks the production version.

When finished, the bugfix needs to be merged back into master, but also needs to be merged back into develop, in order to safeguard that the bugfix is included in the next release as well.


#gitignore

To untrack a single file that has already been added/initialized to your repository, i.e., stop tracking the file but not delete it from your system use: git rm --cached filename

##  Ignore files that have already been committed to a Git repository
To untrack every file that is now in your .gitignore:

First commit any outstanding code changes, and then, run this command:

`git rm -r --cached .`
This removes any changed files from the index(staging area), then just run:

`git add .`
Commit it:

`git commit -m ".gitignore is now working"`
To undo git rm --cached filename, use git add filename.




#cloning

## get an existing repo
	$ git clone git@github.com:StreamlinedStudio/existing-project1.git

That creates a directory named project1, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version. If you go into the new project1 directory, you’ll see the project files in there, ready to be worked on or used. If you want to clone the repository into a directory named something other than grit, you can specify that as the next command-line option:

	$ git clone git@github.com:StreamlinedStudio/existing-repo.git newfolder
That command does the same thing as the previous one, but the target directory is called newfolder.


##clone an existing repo into a new folder
	git clone -b new-project git@github.com:User/YourProject.git newProject
	git clone -b <branch name> <remote repo> <new folder>
