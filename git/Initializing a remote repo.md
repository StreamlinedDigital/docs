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
