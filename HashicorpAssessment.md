# What is the difference between git push, git fetch, and git pull?

## git push

`git push` uses your current branch and checks if there is a tracking branch for a remote repository connected to it. If a tracking branch exists, then `git push` sends your changes from your branch to the remote branch.

Sharing code with a remote repository makes the remote branch resemble your local branch.

`git push` fails if the remote branch differs from your local branch because not all the commits in the remote branch are in your local branch.

If `git push` fails, then synchronize your local branch with the remote branch either by using `git pull` or by using `git fetch` and `git merge`.

## git fetch

`git fetch` uses your current branch and checks if there is a tracking branch. If a tracking branch exists, then `git fetch` pulls changes from the remote branch into your tracking branch. It does not change your local branch.

Then, use `git merge origin/main` to merge the changes into your `main` branch.

## git pull

`git pull` pulls changes from a remote branch into your tracking branch and also merges them into your local branch. 

`git pull` and `git fetch` seem equivalent. However, `git pull` performs the combined actions of `git fetch` and `git merge`.

If you prefer to understand the changes you are merging into your branch before merging, then use `git fetch` followed by `git merge` rather than `git pull`.