---
layout: page
title: Git
modified: 
excerpt: "Software development"
comments: false
share: false
image:
  feature: 
  credit: 
  creditlink: 
---

**Git is a distributed version control system for tracking changes in source code when developing software.**

#### Git basic command  
`git --version`

##### Set up  
`git config --global user.name "XXX"`
`git config --global user.email "XXX"`

##### Initialization  
`git init`

##### Stage  
`git status`

`git add YOUR CODE`

To add all change using
`git add .`

##### Commit  
`git commit -m "YOUR MESSAGE"`

##### Retrive   
 `git checkout -- .`

##### Pull  
git clone https://

##### A new project  
`git remote add origin <server>`

change origin

`git remote -v       // check the address
git remote set-url origin https://
git remote -v    //double check`

##### Push
`git push origin master
git push -f origin master, force to push.`


#### Efficient trick  
- Push with comments  
Create a file named 'git_commit_and_push.sh', and write the following inside:  
```
# Commit and push to repo
git add .

echo 'Enter the commit message:'
read commitMessage

git commit -m "$commitMessage"

git push -u origin master
```

- Push with default comment 'debug'
Create a file named 'git_commit_and_push_debug.sh' and write the following:  
```
# Commit and push to repo
git add .

git commit -m "debugging"

git push -u origin master
```

#### More commands can refer to:  
http://rogerdudler.github.io/git-guide/