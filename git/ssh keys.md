
#SSH Keys

-   You can copy your ssh keys from one environment to another.
-   After doing so you will need to reset the permissions within the new environment.

    chmod 600 ~/.ssh/id_rsa
    chmod 600 ~/.ssh/id_rsa.pub

##You may have to use sudo
    sudo chmod 600 ~/.ssh/id_rsa
    sudo chmod 600 ~/.ssh/id_rsa.pub


##Add, Commit & Push repo to the remote
	git status /check to make sure the .gitignore files are not included 
	git add .  /adds all files 
	git commit -m "uploaded project"
	git push -u origin master
