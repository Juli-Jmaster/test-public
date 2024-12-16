# test-public

# init
### create git in the computer system 
$ git init

### link to remote git
$ git remote add origin \<link with .git>


## commit 
### add file for commit 
$ git add README.md

### commit
$ git commit -m "first commit"

## branch 
### make main branch
$ git branch -M \<name>

### make branch
$ git branch \<name>

### delete branch
$ git branch -d \<name>

### pull branch from remote git
$ git pull origin \<branch>


## pull request 
### create pull request 
$ gh pr create --base \<main branch(to)> --head \<commit branch(from)> --title "\<title>" --body "\<body>"

### squash merge request approve
$ gh pr merge -s \<request number>

### merge request approve
$ gh pr merge -s \<request number>
