# test-public

## init
 **create git in the computer system** \
$ git init

**link to remote git**\
$ git remote add origin \<link with .git>


## stash
**show all stashes**\
$ git stash list

**show fies in stash**\
$ git stash show \<number> --name-only

**turn stash into branch**\
$ git stash branch \<branch> \<number>

**save stash with name**\
$ git stash save \<name>

## commit 
**add file for commit**\
$ git add README.md

**commit**\
$ git commit -m "first commit"

**list files commiting**\
$ git diff HEAD --name-only


## branch 
**make main branch**\
$ git branch -M \<name>

**make branch**\
$ git branch \<name>

**delete branch**\
$ git branch -d \<name>

**pull branch from remote git**\
$ git pull origin \<branch>

**switch to another branch**\
$ git switch \<branch>

**switch or go back to commit**
$ git switch \<COMMIT_ID> --detach

**push to branch online**\
adds a "(#1)" to the name at end
$ git push -u origin \<branch>

**push to branch online**\
$ git push origin \<branch>

**put the HEAD to a branch and push online**\
$ git push origin HEAD:\<branch>


## pull request 
**create pull request**\
$ gh pr create --base \<main branch(to)> --head \<commit branch(from)> --title "\<title>" --body "\<body>"

**squash merge request approve**\
$ gh pr merge -s \<request number>

**merge request approve**\
$ gh pr merge \<request number>

