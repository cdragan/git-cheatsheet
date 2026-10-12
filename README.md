This is a list of my most commonly used git commands, sorted from the ones used most frequently to the ones used once in a blue moon.

# Looking around

* `git status`
  - Shows which files have been modified locally.
* `git diff`
  - By default shows the diff between HEAD commit or index and the state of the tree.
  - Can be used to diff against branches, commits, etc.
* `git loog`
  - `loog` is my alias for an improved `git log` command, the alias is configured in `.gitconfig`:
  ```
  [alias]
      loog = log --graph --all --pretty='format:%C(auto)%h %ad%d %C(auto)%s' --date=short
  ```
* `git show`
  - Shows contents of HEAD commit, or specific commit.

# Making changes

* `git add`
  - Adds files to staging index.
* `git commit`
  - Creates a new commit from changes staged in index.

# Communicating with remote repository

* `git push`
  - Pushes local commits to remote repository.
* `git pull`
  - Downloads commits from remote repository.

# Updating local files and index

* `git restore`
  - Restores file contents to the state from index or HEAD.
* `git reset`
  - On its own, removes files from index.
  - `git reset --soft` moves HEAD to a different commit, but keeps working tree intact.
    Can be used to collapse or rewrite commits.

# Managing branches

* `git rebase`
  - Rebases current branch on top of another one.
* `git merge`
  - Merges another branch into current branch.
* `git switch`
  - Switches HEAD to a different branch or commit.
* `git branch`
  - Can create or delete branches.

# Various management commands

* `git cherry-pick`
  - Makes a copy of another commit on top of HEAD.
* `git stash`
  - Saves local changes into stash and clears local modifications.
    `git stash pop` can do the reverse.
* `git tag`
  - Manages tags.
* `git remote`
  - Manages remote repositories.
  - `git remote -v` displays info about remote repositories.
  - `git remote prune origin` updates visibility of remote branches, esp. if remote branches
    were delete on the remote repository.
* `git rm`
  - Deletes files locally and stages them for removal.

# Worktrees and submodules

* `git worktree`
  - Manages worktrees.
* `git submodule`
  - Manages submodules.

# Repository and configuration

* `git init`
  - Initializes a new repository in the current directory.
* `git clone`
  - Clones a remote repository into a new directory.
* `git config`
  - Manages git configuration.

# Other commands

* `git apply`
  - Applies a patch to the tree.
* `git bisect`
  - Performs binary search to find a commit which introduced a regression using provided script to reproduce the regression.
* `git blame`
  - Lists last commit and author for each line in a file.
* `git fetch`
  - Downloads data from remote repository without updating files locally.
* `git gc`
  - Removes dangling commits.
* `git reflog`
  - Inspects the history of where HEAD has been, useful to recover commits from mistakenly deleted branches.
* `git revert`
  - Creates a revert for a commit.
* `git maintenance`
  - Various maintenance operations.
* `git checkout`
  - Older command superseded by `git switch` and `git restore`.
