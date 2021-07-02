---
title: Repository organization
keywords: [documentation, example, git, cheatsheet]
tags: [documentation]
summary: "Cheatsheet for git usage"
sidebar: documentation_sidebar
permalink: docs_git_cheat_sheet.html
folder: tutorials
---

## Not sure what to do?

If you're unsure of what to do or unsure of the state of your repository, run `git status`. The first few lines will almost always tell you what you need to do to incorporate some upstream updates, continuing rebasing, etc.

## Work flow for new code:

a) update your GIT
```bash      
    git checkout master 
    git pull --rebase
```      

  other options
```bash      
    git fetch $RepoName
```      

b) create new branch or checkout existing
  new branch
```bash      
    git checkout -b NewFeature
```      
  new branch tracking remote
  
```bash      
    git checkout -b NewFeature REMOTEBRANCH/NewFeature
```      
  existing branch
```bash      
    git checkout Feature
    git pull --rebase
    git rebase master
```      

c) write code
  -> edit files
  -> add modified/new files to history

```bash      
  git add $MODFILENAME
  git commit -m "meaningful commit message"
```      

d) make sure your repo is still up to date

```bash    
  git checkout master
  git pull --rebase
  git checkout $BRANCHNAME
  git rebase master
```      

  -> if conflicts arise:
  file.cxx is in conflict appears in command line message
    -> edit file.cxx and resolve conflict (search for ">>>>" to find conflicting lines)
    -> add to history

```bash    
      git add file.cxx
      git rebase --continue
```      

f) push to remote
  git push MYREMOTE $BRANCHNAME
  
  -if rewrite of history is needed:
  
```bash
       git push -f MYREMOTE $BRANCHNAME
```


## Merging commits

  - if you want to merge i.e the last 3 commits as they were all things needed for the same thing but were just commited one adter another
  - rewind to before the 3 commits:

```bash
      git reset HEAD~3
      git add $CHANGEDFILE
      git commit -m "meaningful commit message"
```

  - if something really went bananas and you need to clear you history from the last changes (loosing the changed files)

```bash
      git reset --hard HEAD~1
```
   *careful this command will delete all changes in the previous commit locally*

    
  

{% include links.html %}
