#cloning

## get an existing repo
	$ git clone git://github.com/StreamlinedStudio/existing-project1.git

That creates a directory named project1, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version. If you go into the new project1 directory, you’ll see the project files in there, ready to be worked on or used. If you want to clone the repository into a directory named something other than grit, you can specify that as the next command-line option:

	$ git clone git://github.com/StreamlinedStudio/existing-repo.git newfolder
That command does the same thing as the previous one, but the target directory is called newfolder.


##clone an existing repo into a new folder
	git clone -b new-project git@github.com:User/YourProject.git newProject
	git clone -b <branch name> <remote repo> <new folder>



