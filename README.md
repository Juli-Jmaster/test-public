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

**signed commit**\
$ git commit -S -m "first commit"

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


## gpg
**generate gpg key**\
$ gpg --full-generate-key\
RSA and RSA\
real name = username\
email = email
pwd = gitH@sK1

**getting gpg key and subkeys**\
$ gpg --list-secret-keys --keyid-format LONG

**using signing key**\
$ git config user.signingkey \<gpg_uid sec> OR \<gpg_subkeys ssb>

**import public key to github settings**\
$ gpg --armor --export \<email> OR \<uid>

**using gpg other device**\
$ gpg --armor --export \[email] >> public.asc\
$ gpg --armor --export-secret-keys \[email] >> private.asc\
$ gpg --import public.asc\
$ gpg --import private.asc

**deleting gpg key**\
$ gpg --delete-secret-key \<uid>\
$ gpg --delete-key \<uid>

## other
**push changes from one branch to another**\
get short commit ID changes and go to the branch want to push them to\
$ git reset --hard \<CommitIDShort>

**show commits on branch**\
$ git log --pretty=format:"%h: %s %n%an, %ar %n%G?: %GK - %GS%n"

## update
**update windows**\
$ git update-git-for-windows


##FIX
Creating Stashes
git stash — Saves tracked uncommitted changes and resets the working directory.
git stash push -m "message" — Saves changes with a specific descriptive label.
git stash -u — Saves tracked changes along with any brand new untracked files.
git stash -a — Saves everything including untracked and completely ignored files.
git stash -p — Opens an interactive menu to choose specific changes block-by-block.

Listing & Inspecting Stashesgit stash list — Shows all saved stashes with their corresponding stash@{index} identifiers.
git stash show — Displays a file diff summary for your most recent stash entry.
git stash show -p — Shows the full layout of the code changes inside the latest stash.
git stash show stash@{2} -p — Shows the full detailed code diff for a specific older index.

Applying & Restoring Stashesgit stash pop — Restores the latest changes and permanently removes them from the stack.
git stash pop stash@{1} — Restores a targeted stash index and removes it from the list.
git stash apply — Restores the latest changes but keeps them safely backed up in the list.
git stash apply stash@{2} — Restores a targeted index but keeps it safely inside the list.
git stash branch <name> — Builds a brand new branch and instantly applies your latest stash to it.

Cleaning & Deleting Stashesgit stash drop — Permanently deletes the most recent stash entry from your stack.
git stash drop stash@{3} — Permanently deletes one specific targeted stash entry from your list.
git stash clear — Destroys every single stash entry
