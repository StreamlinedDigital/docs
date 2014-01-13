#cloning

## get an existing repo
	$ git clone git://github.com/schacon/grit.git

That creates a directory named grit, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version. If you go into the new grit directory, you’ll see the project files in there, ready to be worked on or used. If you want to clone the repository into a directory named something other than grit, you can specify that as the next command-line option:


	$ git clone git://github.com/schacon/grit.git mygrit
That command does the same thing as the previous one, but the target directory is called mygrit.


##clone an existing repo into a new folder
	git clone -b new-project git@github.com:User/YourProject.git newProject
	git clone -b <branch name> <remote repo> <new folder>



