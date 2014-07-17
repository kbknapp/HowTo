# Git
## Config

	git config --global user.name "John Doe"

Sets the username for all repositories to John Doe.

	git config --global user.email "jdoe@mail.com"

Sets the user email for all repositories to jdoe@mail.com.

	git config --global color.ui true

Sets the ```git``` output to colorized.

## Initializing
    $ cd project
    $ git init
Creates a new repository inside the project directory.

## Misc
	$ git status
Checks the status of ```git``` repository

	$ git add some_file.txt
Adds some_file.txt to be tracked.

## Commiting
	$ git commit
Commits all files by showing a status and asking for a commit message.
### Flags
	$ git commit -a
Commits all currently tracked files with all current changes. Asks for a commit message by showing a status screen.

## Ignoring
	$ editor .gitignore
	.DS_Store
	tmp/*.txt
	!tmp/important.txt
A file that tells ```git``` what to ignore. One file/folder per line. Wildcards (```*```) are allowed. A line starting with ```!``` tels ```git``` to *include* such files and folders regardless of what other rules are listed in this file.