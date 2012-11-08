GIT CHEAT SHEET
Git is:
• A decentralized Version Control
•	It allows you to store, manage, update, & share code. 

Command Line: 
git <any git command> --help

1.	git commit:

	a.	Commits changes from your working directory to your staging area.

	b.	Every commit creates a unique hash code

	c.	.Commit messages should be very descriptive.

	d.	Test changes and commit frequently 

	i.	Don’t wait to commit, fix one bug at a time & commit accordingly.

	e.	If you’ve made a mistake, use git reset –-hard COMMIT_HASH_NUMBER.

	i.	This will completely delete the commit you’ve just made and take you to your desired commit.

	f.	Our Standard: git commit –m “#issue_number <describe what you did>

	i.	Expected output: https://gist.github.com/f5d9819b1c6fc2804ccf

2.	git branch:

	a.	Creates a new “tree” from the master’s HEAD.

	b.	All branches include a master branch after initial commit.

	c.	Create new branch == git checkout –b “new branch”

	d.	 Always include “README.md” in every branch. 

	e.	Every assigned repository owner MUST create a development branch and staging branch.

	i.	[i.e. git checkout -b <branch_name>]

	f.	Our Standard: git checkout <issue_number: Name-of-issue>

	i.	Expected output: https://gist.github.com/040dc5028a79b53ef3da

	3.	git add:

	a.	adds changes from your working directory to be committed to the staging enviornment.

	b.	“git add .” adds all changes not just the designated file.

	c.	Our Standard: git add <file_name>

	i.	Expected output: If done correctly, git commit will give you the expected output 
	linked above.

4.	git status:

	a.	Use this command prior to committing your new changes. 

	i.	This will show you any files that have been changed in reference to your last commit. 

	b.	Our Standard:  Use before “git add” & “git commit”

	i.	Expected output: https://gist.github.com/e1acdb7ab4db36f5acb7

	5.	git log:

	a.	Use this command that will display all prior commits.

	b.	Expected output: https://gist.github.com/c81f251aa357ee8b0d8e

Our Processes:

	1.	New Projects

	- Ask Belmer/Farsheed to Create Repository

	- Run these commands for brand new repo:

	- touch README.md

	- git init

	- git add README.md

	- git commit -m "first commit"

	- git remote add origin git@github.com:drumbi/project_name.git

	- git push -u origin master

	- Run these commands for existing files:

	- git remote add origin git@github.com:drumbi/project_name.git

	- git push -u origin master

2.	Adding Feature/Bugfix to existing Project

		a.	if you don't have copy of project
	
		i.	git clone git@github.com:drumbi/project_name.git
	
		b.	Checkout branch you like branch FROM
	
		- git checkout branch_name
	
		c.	Create New Branch with issue#-issue-title
	
		 - git checkout -b '01-descriptive-branch-title'
	
		d.	Make your changes, stage, and commit often (repeat as necessary)
	
		 - git add .
	
		i.	git commit -m 'useful commit msg'
	
		e.	Push and Pull Changes back to GitHub often (repeat as necessary)
	
		 - git push origin branch_name (pushes changes from local to github)
	
		i.	git pull origin other_branch_name_like_dev  (note: this will merge that branch's code into yours)
	
		f.	When code is tested and ready, go to github.com, go to project page, at top, tap Pull Request, and specify your branch to the “development” master repo. Include a meaningful description about why the merge is necessary. 
	
		g.	Maintainer of repository will ok changes in development branch and merge to the master branch. 
