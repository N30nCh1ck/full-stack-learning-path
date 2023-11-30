%% Index %%
- [[Git I]]
- [[Git II]]

#### Initial Git Repo
Use `git init` command to creates a new Git repository within your directory.

#### Config Git User
The most basic use case for `git config` is to invoke it with a configuration name and email.

execute the following command in your root directory repository
`git config user.name "your_name"` to set user name
`git config user.email "your_email"` to set user email

> Both command above is IMPORTANT when you *initial git repo* or *clone new repo*. except you've configured your *user.name* and *user.email* as *global* configuration. If not, you are going to face the issue like *cannot commit git repo*.

to see your configuration run `git config --list` command then press *enter* to scroll down or *q* to quit the mode.

#### Add Changed Git
The git add command adds a change in the working directory to the staging area.

`git add <file>` Stage all changes in `<file>` for the next commit.
`git add <directory>` Stage all changes in `<directory>` for the next commit.

`git add .` add all changes in the working directory.

> you can use `git status` to check all files that just *added*, *deleted*, or *modified* in your git directory before commit your code. 

#### Git Commit Message
A shortcut command that immediately creates a commit with a passed commit message
`git commit -m "commit message"`

#### `git remote` 
The `git remote` command lets you create, view, and delete connections to other repositories. 

Create a new connection to a remote repository by using.
`git remote add <name> <url>`

>Create your new repo in GitHub then follow the readme.

#### `git push`
The `git push` command is used to upload local repository content to a remote repository.

command `git push <remote> <branch>` for push the specified branch to , along with all of the necessary commits and internal objects. This creates a local branch in the destination repository.
![[git-push.svg]]


#### `git clone`
`git clone` is primarily used to point to an existing repo and make a clone or copy of that repo at in a new directory, at another location.

`git clone <repo> <directory>`

#### `git branch`
Git branches are effectively a pointer to a snapshot of your changes. When you want to add a new feature or fix a bug—no matter how big or how small—you spawn a new branch to encapsulate your changes.

![[git-branch.svg]]
command `git branch` can list all of the branches in your repository.
and `git branch -a` command is gonna list all your remote branches. 

`git branch <branch>` Create a new branch called ＜branch＞. **This does not check out the new branch.**

`git branch -d <branch>` Delete the specified branch. This is a “safe” operation in that Git prevents you from deleting the branch if it has unmerged changes.

`git branch -D <branch>` Force delete the specified branch, even if it has unmerged changes.

`git branch -m <branch>` Rename the current branch to `<branch>`. After you change your local branch and want to change **Remote Branch Name** use `git push <remote> :<old_name> <new_name>` command.

>To change **Remote Branch** use `git branch --set-upstream <branch_name> <your_new_remote>/<branch_name>`

#### `git checkout`
 The `git checkout` command lets you navigate between the branches created by `git branch`.
 
 Additionally, The `git checkout` command accepts a `-b` argument that acts as a convenience method which will create the new branch and immediately switch to it.
 `git checkout -b ＜new-branch＞`

#### `git fetch`
he `git fetch` command downloads commits, files, and refs from a remote repository into your local repo.
![[git-pull-1.svg]]
use `git fetch <remote>` to download (C point) into your repository.

#### `git pull`
The `git pull` command is used to fetch and download content from a remote repository and immediately update the local repository to match that content.
![[git-pull-2.svg]]
use `git pull <remote>` to update your local repository.

#### `git merge`
The `git merge` command lets you take the independent lines of development created by `git branch` and integrate them into a single branch.

Use`git merge <feature_branch>` After you stay on your base branch e.g. "main" then type the merge command.