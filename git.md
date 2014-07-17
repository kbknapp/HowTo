# Git
## Config


Set the username for all repositories to John Doe.

	git config --global user.name "John Doe"

Set the user email for all repositories to jdoe@mail.com.

	git config --global user.email "jdoe@mail.com"

Set the ```git``` output to colorized.

	git config --global color.ui true

## Initializing

Create a new repository.

    $ git init
    
The above is typically preceded by ```$ mkdir myproject && cd myproject``` which creates a directory called *myproject* and then changes into that directory.

## Misc
	$ git status
Checks the status of ```git``` repository

	$ git add some_file.txt
Adds some_file.txt to be tracked.

	$ git diff some_file.py
Displays the differences between the working directory *some_file.py* and the staging directory. Adding ```--staged``` compares the staging area to the repository.

	$ git diff HEAD some_file.py
Compares the file *some_file.py* in your working directory to the most recent commit version of the same file.

## Logging / History

Show a Tk GUI showing commit history

	$ gitk
	
Show a history of commits on the current repository.

	$ git log
	
### Flags

Adding the following flags changes the output of ```git log```

```--stats``` show's the history with some statistics of what was changed.

```--oneline``` shows single line version of commits history.

```--graph``` shows branch diagrams (may be combined with ```--oneline```)

```--pretty="%h, %cn, %cr"``` shows commit history in a formatted version (example uses abbreviated hash, commiter name, and relative commiter date seperated via commas)

### --pretty Formatter Values
| | | | |
|:--------:|:-------------------------|:----------|:-------------------------|
| ```%H``` | Commit Hash              | ```%ad``` | Author Date              |
| ```%h``` | Abbreviated Hash         | ```%ar``` | Author Date, Relative    |
| ```%T``` | Tree Hash                | ```%cn``` | Committer Name           |
| ```%t``` | Abbreviated Tree Hash    | ```%ce``` | Committer E-mail         |
| ```%P``` | Parent Hashes            | ```%cd``` | Committer Date           |
| ```%p``` | Abbreviated Parent Hashes| ```%cr``` | Committer Date, Relative |
| ```%an```| Author Name              | ```%s```  | Subject (Commit Message) |
| ```%ae```| Author E-mail            |

## Commiting

Commit all files by showing a status and asking for a commit message.

	$ git commit .

### Flags

Adding the following flags to ```git commit``` changes the functionality.

```-a``` Commits all tracked files with all current changes. Asks for a commit message by showing a status screen.

```-m "a message"``` Commits files with the specified message.
  
## Ignoring

To ignore files create a file named *.gitignore* inside the repository. Add one line per file (or folder) to ignore. Wildcards (```*```) are allowed. A line starting with ```!``` tels ```git``` to *include* such files and folders regardless of what other rules are listed in this file. Example:

	$ editor .gitignore
	.DS_Store
	tmp/*.txt
	!tmp/important.txt
