
---
## Overview
Git is a [[Distributed Version Control|distributed version control]] software system. It allows multiple developers to work on projects simultaneously and track changes efficiently. Git is best learnt through practice [here](https://learngitbranching.js.org/)
___
###### Keywords  
- ``add``
	- ``Optional flags``
	- ``-u`` update all tracked files and move to git staging area.
- ``apply``
- ``branch``
	- ``Optional flags``
	- ``-l`` list all local git branches.  
	- ``-d`` delete branches locally.  
- ``commit``
- ``checkout``
	- ``Optional flags``
	- ``-b`` checkout onto a newly created branch.  
- ``diff``
- ``fetch``
- ``git`` 
- ``log``
- ``push``
	- ``Optional flags``
	- ``-f`` force override remote branch.  
- ``pull``
- ``rebase``
	- ``Optional flags``
	- ``-i`` Make a list of the commits which are about to be rebased. Let the user edit that list before rebasing. This mode can also be used to split, reword and reorder commits.  
- ``restore``
- ``reset``
	- ``Optional flags``  
	- ``--soft`` does not touch the index file or the working tree at all but resets index to target. This leaves all your changed files to be committed.  
	- ``--hard`` resets the index and working tree. Any changes to tracked files in the working tree since target are discarded.  
- ``status``
___  
###### Commonly used commands  
| Command                   | Description                                               |
| ------------------------- | --------------------------------------------------------- |
| `git log`                 | Displays log messages of previous commits                 |
| `git status`              | Shows the current status of the repo                      |
| `git add [FILEPATH]`      | Moves a file from untracked to tracked (staging)          |
| `git commit -m "MESSAGE"` | Commits staged files with a message                       |
| `git push`                | Pushes local commits to the remote repository             |
| `git pull`                | Fetches and merges remote changes into local repo         |
| `git fetch`               | Fetches remote changes without applying them              |
| `git diff HEAD~1`         | Shows differences between current repo and one commit ago |
___
## Flashcards
#flashcards
What is Git? :: A distributed version control system used to track and manage changes in files or codebases.

What does git add do? :: Moves changes to the staging area.

What’s the difference between git fetch and git pull? :: fetch downloads changes without applying them whereas pull downloads and merges them.

How do you create and switch to a new branch in one command? :: git checkout -b branch_name

What does git reset --hard do? :: Resets the index and working tree, discarding all changes.

What does the -i flag in git rebase enable? :: Interactive mode for editing, rewording, splitting, or reordering commits.

How do you view the commit history? :: git log

How do you see changes between commits? :: git diff [commit1] [commit2]

---
> [!Tip]
> Use `git status` often it tells you what is going on in your repo.
