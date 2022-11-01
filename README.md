
# Git Notes
Git Notes useful for keeping track of your project and take a reference from here
## Content
- Git Config
- Comman Git Commands
- Git Add and Commit
- Git Restore file
- Git Remove and Rename
- Git Differences of files
- Git Preety Print
- Git Remote
- Git Branch
- Git Branching Workflow


## Git Config
- Config Username
```
  git config --global user.name "omprakash2469"
```
- Config Email
```
  git config --global user.email "oprajapati249@gmail.com"
```

## Comman Git Commands

- Initialize a Git Repository
```
  git init
```
- Check Repo Status
```
  git status
```
- Clone git repo
```
  git clone URL-TO-CLONE
  git clone https://github.com/omprakash2469/sample.git
```
## Git Add and Commit

- Track All Files in Git
```
  git add
```
- Untrack file
```
  git rm --cached db.accdb
```
- Commit Files
```
  git commit -m "Initial Commit"
```
- Check commited Files
```
  git log
```
- Commits all tracked files skiping staging area
```
  git commit -a -m "Direct commit"
```
- Ignore Tracking files
- Create a .gitignore file
```
  touch .gitignore
```
- Add file names to ignore in .gitignore file
```
  /__pycache__
  /node_modules
  /env
```
## Git Restore file
- Unstage a staged file
```
  git restore --staged <filename>
```
- Restore previous version of file or unmodify a file
```
  git checkout --<filename.txt>
```

## Git Remove and Rename

- Delete folder from git
```
  rm -rf .git
```
- Remove file or folder
```
  git rm file.txt
```
- Rename file or folder
```
  git mv file.txt file2.txt
```
## Git Differences of files
- Compare working directory with staging area
```
  git diff
```
- Compare last commit with current staging area
```
  git diff --staged
```
- Git diff with all commits
```
  git log -p
```
- Git diff with number of given commits ( n for numbers )
```
  git log -p -n
```
## Git Preety Print
- Gives short definition of commit
```
  git log --stat
```
- Show all commit in oneline

```
  git log --pretty=oneline
```
- Show all commit in short

```
  git log --pretty=short
```
- Show all commit with some info

```
  git log --pretty=full
```
- Show all commit within the given time

```
  git log --since=2.days
```
- Show all commit in mentioned format

```
  git log --pretty=format:"%h -- %an"
```
## Git Remote
- Check if remote url is defined

```
  git remote -v
```
- Add remote url
```
  git remote add origin https://github.com/omprakash2469/gitnotes.git
```
- Update remote url
```
  git remote set-url origin REPO_URL
  git remote set-url origin https://github.com/omprakash2469/gitnotes.git
```
- Push Repo to remote url
```
  git push -u origin master
```
## Git Branch
### Create and Change Branch
- List all of the branches in your repository
```
  git branch
```
- Creating another git branch
```
  git checkout -b develop
```
- Change git branch
```
  git checkout BRANCH_NAME
  git checkout master
```
### Merge Branch
- Merge git in master branch
```
  git merge BRANCH_NAME
  git merge develop
```
### Delete Branch
- NOTE: Show error if not merged
```
  git branch -d BRANCH_NAME
  git branch -d develop
```
- Force delete branch without merging
```
  git branch -D BRANCH_NAME
  git branch -D develop
```
### Branch Logs
- Show all branches with hash and last commit
```
  git branch -v
```
- Show all merged branch
```
  git branch --merged
```
- Show all unmerged branch
```
  git branch --no-merged
```
## Git Branching Workflow
- Long Running Branches
```
  master
  develop
  PU ( proposed update )
```
- Topic Branches
```
  replaces text with js { TOPIC_NAME }
```
- Push branch to remote
```
  git push -u origin BRANCH_NAME
  git push -u origin master
```
- Push branch to remote alias
```
  git push origin BRANCH_NAME:BRANCH_ALIAS_IN_REMOTE
  git push origin master:main
```
- Delete branch in remote
```
  git push -d origin develop
```
