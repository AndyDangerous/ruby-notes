# Git

### What is source control?

-keep track of source code over time (avoid the email with attachment version bullshit, e.g. Document_2_final_revised_3)

-built by Linus mfn Torvalds for Linux kernel work

-tracks lines, not files

-competetive/collaborative

-decentralized
	DVCS - Distributed Version Control Service


### Why?
The ability to undo!
See change details - what, when, hopefully why, compare changes

### What are we using now?
Git, SVN, mercurial

### Repos, Branches, Commits
	- Repo - Repository
		1 x project
	-Branches -
		-Master - trunk of the tree - production-ready, etc
		-“feature branches” we’re working on them
		-merge branches back into master
	-Commits - unit of progress
		-commit allthegoddamtime
			-commit with every passing test
		-commit message:
			good: why the change was made, present tense
			bad: emotion, nothing, stuff that doesn’t matter
		-SHA (pronounced “shah") - big long hexadecimal number
			records changes, timestamp, name, email, MAC address
		-commits can and will include multiple files


### Screencast:
  https://www.dropbox.com/s/09lrmanjdacc5cz/source_control_made_easy.mov

-not a regular source control program

### Resources
f you're brand new to git, start with try.github: https://try.github.io/levels/1/challenges/1

If you've used git before (or complete try.github), work through Git Immersion: http://gitimmersion.com/

And, if you just can't get enough Git, check out the Pro Git book: http://git-scm.com/book




Cheat Sheet:

 | `git init`  |  sets up new repo | 
 | `git status`  |  status checkup |
 | `git add <file>`  |  git will start tracking file, git will update what will be committed |
 | `git commit -m “message”`  |  commits files from staging to repo. “message” is the message is present tense, describes change and why made |
 | `git log`  |  chronological “journal” of commit changes |
 | `git remote add <remote_name> <repo URL>`  |  connects to remote repo |
 | `git push -u <remote_name> <branch>`  |  pushes local repo to remote, -u flag tells git to remember parameters so you can just use ‘git push’ |
 | `git pull <remote_name> <branch>`  |  pulls from remote |
 | `git diff HEAD`  |  brings up changes, HEAD is most recent commit |
 | `git diff —staged`  |  shows differences staged |
 | `git reset <file>`  |  removes file from stage |
 | `git checkout — <target>`  |  returns target to last commit |
