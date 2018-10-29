# Reminders

This is a set of reminder instructions for how to use Git.

## What is it?

Git is a decentralised version control system created by the inventor of linux.  It allows you to track changes from multiple remote develops into a master branch.

You can have a local repository (repo) and a remote one, hosted by something like Github.

The principle is you take snapshots of files using a process of 'commits'.

## Step 1

### Download Git:

http://git-scm.com/download/win

This automatically downloads a command line interface called GitBash.

## Step 2

Add a new project.  Create a folder in the file structure where you want to store the project.

Right click on the file and 'open bash here'.  This opens bash in the right working directory.

## Step 3

Create the files you need.

$ touch <filename.extension>

e.g. $ touch mywords.docx

## Step 4

Open the files in whatever editor you want e.g. Atom and make and save changes.

## Step 5

In Bash, initialise an empty local git repo.

$ git init

## Step 6

Add files to the repo:

- $ git add <filename>

or:

- $ git add .

To add all the files at the same time.
This moves files into the 'staging area'.  You can check which files are here using:

$ git status

To remove files from the staging area:

$ git rm <>

## Step 7

There may be files which you don't want to commit to the master branch, e.g. log files, error files etc.

In this case, create a .gitignore file:

$ touch .gitignore

Open the gitignore file within the editor, then list the names of the files you don't want committed e.g. log.txt

Save.

When you next commit the files inside the .gitignore won't be uploaded.

## Step 8

To create a branch:

$ git branch <name>

To switch branches:

$ git checkout <name>

To merge branches:

$ git merge <name of the branch to be merged with the master>

## Step 9

To commit the files in the staging area to the repo:

$ git commit

This brings up an editor which encourages you to comment on your commit changes.

Use 'i' to edit the text, then esc, then : wq to exit.

To not do this each time:

$ git commit -m 'comments in here'

## Step 10

For remote repos (Github).

Create an account and sign in.

Make a new repo.

When you create a new repo it lists the url which you can copy and paste into your local repo to link.

$ git remote **this lists the current remote links within the local repo**

$ git push -u origin master **this will push your local repo master to the remote github repo via a login screen**

## Step 11

Create a README.md file for your repo.

$ touch README.md

Then edit, add, commit, push.

$ git push

$ git pull **this will get all the changes made from your master remote repo to your local repo**

## Step 12

To clone a repo from github, click the clone button which gives you the url.

Create a folder where you want to store it, open gitbashhere +:

$ git clone <paste web url>
