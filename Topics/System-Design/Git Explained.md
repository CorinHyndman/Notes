___
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

> [!Tip]
> Use `git status` often it tells you what is going on in your repo.

___  
![[how-git-commands-work.png]]
![[git-merge-git-rebase.png]]
___
## Flashcards
#flashcards
**What is Git?** :: A distributed version control system that tracks changes in files, allowing multiple developers to collaborate efficiently.

**What’s the difference between Git and GitHub?** :: Git is the version control tool; GitHub is a platform for hosting and sharing Git repositories online.

**What is a repository?** :: A collection of files tracked by Git along with their complete version history.

**What is a branch?** :: A parallel line of development allowing you to work on features independently of the main codebase.

**What is a commit?** :: A snapshot of the repository at a specific point in time, recording changes made since the last commit.

**What does `git init` do?** :: Initializes a new Git repository in the current directory.

**What does `git clone` do?** :: Creates a copy of an existing remote repository locally.

**What does `git status` show?** :: Displays the state of the working directory and staging area—what’s modified, staged, or untracked.

**What does `git add` do?** :: Moves changes from the working directory to the staging area, preparing them for a commit.

**What’s the difference between `git add .` and `git add -u`?** :: `git add .` stages new and modified files; `git add -u` stages modified and deleted files (but not new ones).

**What does `git commit -m "message"` do?** :: Records the staged changes to the repository with a descriptive message.

**How do you create and switch to a new branch?** :: `git checkout -b branch_name`

**How do you list all branches?** :: `git branch -l`

**How do you delete a branch locally?** :: `git branch -d branch_name`

**What does `git merge branch_name` do?** :: Combines changes from another branch into the current branch.

**What’s the difference between `git merge` and `git rebase`?** :: Merge creates a new commit combining changes; rebase moves commits to appear on top of another branch’s history.

**When should you use rebase over merge?** :: Use rebase to keep a clean, linear history; use merge to preserve context of parallel development.

**What does `git remote -v` show?** :: Lists all remote connections associated with the repository.

**What does `git fetch` do?** :: Downloads changes from the remote without merging them.

**What does `git pull` do?** :: Fetches and automatically merges changes from the remote branch into your current branch.

**What does `git push` do?** :: Uploads local commits to a remote repository.

**What does `git push -f` do?** :: Force-pushes local commits, overwriting the remote branch (use with caution).

**What does `git restore` do?** :: Restores files in the working directory to their last committed state.

**What does `git reset --soft HEAD~1` do?** :: Moves the last commit’s changes back to the staging area (undo commit but keep staged).

**What does `git reset --hard HEAD~1` do?** :: Completely removes the last commit and discards all related changes.

**How do you undo a specific commit without losing history?** :: `git revert <commit_hash>`

**What’s the difference between reset and revert?** :: Reset rewrites history (destructive), revert adds a new commit that undoes previous changes (safe).

**How do you view the commit history?** :: `git log`

**How do you view a simplified one-line commit log?** :: `git log --oneline`

**How do you see changes between commits?** :: `git diff [commit1] [commit2]`

**How do you see what changed in the last commit?** :: `git show HEAD`

**How do you see which branch a commit belongs to?** :: `git branch --contains <commit_hash>`

**What does `git rebase -i HEAD~n` do?** :: Opens an interactive rebase editor for the last _n_ commits, allowing rewording, squashing, or reordering.

**What is `git stash` used for?** :: Temporarily saves uncommitted changes so you can switch branches safely.

**How do you reapply stashed changes?** :: `git stash pop`

**How do you apply changes from a specific stash without deleting it?** :: `git stash apply stash@{n}`

**What does `git cherry-pick <commit>` do?** :: Applies a specific commit from one branch onto another.

**What command should you run often to understand your repo’s state?** :: `git status`

**Why should you write meaningful commit messages?** :: They make it easier to understand the project history and reason about changes later.

**How often should you commit?** :: Commit early and often—each commit should represent a logical, small unit of change.

**Why avoid force-pushing to shared branches?** :: It rewrites history, potentially causing data loss for others.

---
