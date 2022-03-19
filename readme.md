## create a new repository on the command line
	echo "# git-learning" >> README.md
	git init -> initialize the current directory as git repository
	git add README.md -> add file to staging area
	commit the file
	git commit -m "first commit"
	git branch -M main -> 
	git remote add origin https://github.com/DevangJayswal/git-learning.git
	git push -u origin main
	
## push an existing repository from the command line
	git remote add origin https://github.com/DevangJayswal/git-learning.git
	git branch -M main
	git push -u origin main
	
	git -> all commands
	git status -> to know status of files in all areas
	git ls-files -> list all files which are tracked by git or in staging area	
	git -a -m "commit message" -> stage and commit
	
## to add all files in current working directory, git add start tracking file and add it to staging area
	git add .
	git add *
	git add -A 
	
	git add file1.txt file2.txt 
	git add *.java 
	git add *.txt 
	
	git config
	git config --list
	git config user.name
	git config user.email
	git config user.name "NewLocalUsername"
	git config --global user.name "NewGlobalUsername"
	
	git log
	git log --help
	git log . 
	git log file1.txt
	git log --oneline
	git log -n 2
	git log -n 2 --oneline
	
	git diff --name-only --cached -> show file that are in staging area
	
	git show <commit_id>
	
	git clone -b <branchname> <remote-repo-url>
	
	change default branch name
	git config --global init.defaultBranch main
	
	display what we can checkout
	git checkout
	
	$ git checkout
	M       f1
	A       f2
	A       f3	
	
	M = modified
	A = added
	D = deleted
	R = renamed
	C = copied
	U = updated but unmerged
	
	
	create-a-new-and-empty-root-branch	
	git checkout --orphan YourBranchName
	This will create a new branch with zero commits on it, however all of your files will be staged. At that point you could just remove them.
	("remove them": A git reset --hard will empty the index, leaving you with an empty working tree)

## remove untracked directories [read more](https://stackoverflow.com/questions/1499157/git-checkout-pull-doesnt-remove-directories)
`git clean -fd`

## as the files in `.gitignore` are not being tracked, you can use the git clean command to recursively remove files that are not under version control. [read more](https://stackoverflow.com/questions/13541615/how-to-remove-files-that-are-listed-in-the-gitignore-but-still-on-the-repositor)
*  to perform a dry run and see what will be removed
	* `git clean -xdn`
* to execute it
	* `git clean -xdf`

Be aware that this command will also remove new files that are not in the staging area
