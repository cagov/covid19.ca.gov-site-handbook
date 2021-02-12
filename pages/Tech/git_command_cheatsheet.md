---
title: Git Command Cheatsheet
date: 2021-02-11
permalink: /tech/git/
toc: true
eleventyNavigation:
  key: Git Command Cheatsheet
  order: 40
  parent: Tech
---

These are some handy utility git functions to do useful things with command line git.

## Understanding the status and changes in the repo

### See status of current git branch


```
git status
```


### See all full log of commit history


```
git log
```


### See short version of git commits


```
git log --oneline
```


### Search for specific commits that mention a string


```
git log -S 'Covid'
```


### Search for specific commits that mention a string


```
git log --all --grep="CCG-434"
```


### Checkout commit before a certain date in a given branch


```
git checkout git rev-list -1 --before="Jul 2 2020" master
```


### Generate a CSV from git commit history
This saves a csv file called `history.csv` to the relative root folder.

Then, using 
```
ls-files
```
finds any pdf files (upper or lower case).

For each record found, read a repository & build a history with links to the source files.

<!-- @TODO We also have a bash script version of this that is more detailed. -->

```
echo 'Date, Filename, Author, Github URL, Direct Download URL' > ./history.csv && git ls-files '*.pdf' '*.PDF' -z | xargs -0 -L1 -I'{}' git log --date=short --format='%ad, {}, %an, [https://github.com/cagov/covid19/blob/%H/{}](https://github.com/cagov/covid19/blob/%25H/%7B%7D), [https://github.com/cagov/covid19/raw/%H/{}](https://github.com/cagov/covid19/raw/%25H/%7B%7D)' -- '{}' >> ./history.csv
```


### See last updated date for all branches


```
git for-each-ref --sort='-committerdate:iso8601' --format=' %(committerdate:iso8601)%09%(refname)' refs/heads
```


### Get first commit ever


```
git rev-list --max-parents=0 HEAD
```


### Search full logs history for file that was renamed

Note, github's history view doesn't use this command, so logs for renamed filed may be cut off at the date of renaming. (There is [debate](https://stackoverflow.com/questions/2314652/is-it-possible-to-move-rename-files-in-git-and-maintain-their-history) as to whether or not git mv preserves the history or not.)


```
git log --follow --find-copies-harder filename
```
 

### See changes from a particular commit


```
git show commitguid
```
 e.g. git show 92a830e9f110fe1379621e835374b3ea76cda792

### Compare current branch to another (diff)


```
git diff other_branch_name
```


### Compare current branch to another, but only see the names of files


```
git diff other_branch_name --name-only
```


### Compare two commits or branches


```
git diff commit_guid..other_commit_guid
```
 


```
git diff branch..otherbranch
```


### See all remote branches


```
git remote show origin
```


---

## Working with changes

### Update all checked out branches since last fetch


```
git fetch --all
```
 

This puts the other branches in the memory of git, and able to checkout out by calling the checkout without creating a new branch.

### Fetch all updated data from origin, but doesn’t merge it into your working branch


```
git fetch origin
```


### List all branches


```
git branch
```


### List all remote branches


```
git branch -r
```


### Checkout a remote branch

(Assuming origin is called origin.) 


```
git checkout --track origin/branch_name
```


### Checkout files from another branch


```
git checkout branch_name
```


### Checkout a branch


```
git checkout branch_name
```


### Create a branch


```
git checkout -b new_branch_name
```


### Delete a branch


```
git branch -D desired_branch_name
```


### Delete a remote branch

(Assuming “origin” is called “origin.”) 


```
git push origin --delete feature/login
```


### Get data from remote server and merge it into your working branch


```
git pull origin main
```
 
```
git pull origin feature/2020-11-13-feature-name
```


### Save a commit message


```
git commit -m "Descriptive text of your commit message."
```


### Save a commit message and link to Jira ticket

If Jira and Github repository are connected, adding the ticket name in the commit message can automatically link the tickets. 


```
git commit -m "Descriptive text of your commit message. CCG-434"
```


### Edit a commit message for the last commit

This only works for local edits. 


```
git commit --amend "New text"
```


See: https://docs.github.com/en/free-pro-team@latest/github/committing-changes-to-your-project/changing-a-commit-message

---

## Undoing commits & changes

### Totally reset your branch back to the origin of the current branch

(Lose any changes)


```
git reset --hard HEAD
```


### Revert to a prior commit


```
git revert commit_guid
```


---

## Managing tags

### List tags


```
git tag
```


### Tag a commit


```
git tag v1.x.x
```
 

You will need to have an established version naming pattern for any releases.

### Push tag


```
git push origin tagname
```


### Rename a tag


```
git tag new old
```
 
```
git tag -d old
```
 
```
git push origin :refs/tags/old
```
 
```
git push --tags
```


### Delete remote tags


```
git push --delete origin tagname
```
 
```
git push origin :tagname
```


---

## Manage remotes

### Show all remote branches in your git config


```
git remote
```


### Add remote origin


```
git remote add path_to_origin
```
 

e.g. git remote add https://github.com/cagov/covid19.git

## Create a fork


```
git remote add fork git@github.com:username/covid19.git
```


### See urls for remote origins


```
git remote -v
```


---

### Apply a change from the tip of another branch

This would apply the last commit from one branch to another branch.


```
git cherry-pick other_branch_name
```


### Update a local branch, applying all changes from remote and replaying your changes back from the point at which they diverged

1. current branch: 
```
ticket/CCG-434-menu
```


2. Apply all changes from master branch to current branch
 
```
git rebase master
```


3. This will lead you through an interactive dialog that plays all changes from master and your changes, ideally leaving your commits as the most recent commits.

4. If there are merge conflicts, you will need to resolve them. This can get tricky the longer time has gone on.

5. If it fails, you can 
```
git rebase --abort
```
 to back out of it.

### Advanced Rebasing

You can also rebase off a branch, or a commit. 
```
git rebase --onto commitguid
```


### Look up the parent commit

If you’ve really got a mess, it can be helpful to look up the parent commit 


```
git rev-list --parents -n 1 commitguid
```


### Remove untracked files


```
git clean
```


### Sources & Resources

- https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes
- https://www.datree.io/resources/git-commands
- https://www.freecodecamp.org/news/10-important-git-commands-that-every-developer-should-know/
- https://medium.com/flawless-app-stories/useful-git-commands-for-everyday-use-e1a4de64037d