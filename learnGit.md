
# **Learning Git**

*This version: 2014-11-20*

*Filename: learnGit.md*

Reference: http://git-scm.com/book/en/v2/Getting-Started-Git-Basics


### History
* local version control
* centralized version control
* distributed version contraol (every computer is a full mirror, preventing single point failure)
  * linux kernal & Bitkeeper -> Git (2005)

### How Git Works
* snapshots, local operation
* checksum - SHA-1 Hash
* everything is undoable
* states
  * committed: stored local
  * modified: file changed but not committed 
  * staged: mark a changed file to go into next commit snapshot

### Basic Commands
 $ git init

 $ git status -s

 $ git add filename

 $ vim .gitignore
  to tell git ignore certain files

 $ git diff
 to see what you've changed but not staged

 $ git diff --staged 
 what will go into next commit

 $ git commit -m 
 to commit with a message

 $ git commit -a
 stage all files that are already tracked

 $ git rm -f
 remove and stage the changes, -f to force removal of modified file

 $ git rm --cached filename
 untrack the file

 $ git mv old_name new_name
 rename to file

 $ git log -p -2, git log --stat, git log --pretty=oneline --graph
 to see commit history in a customized format

 $ git commit --amend 
 append some changes to this commit

 $ git reset HEAD filename
 unstage a file

 $ git checkout -- filename
 to discard changes

 $ git remote add [lieu] url
 to add a remote repository


 $ git fetch origin
 fetch any new work but don't merge

 $ git pull 
 fetch and merge

 $ git push [remote-name] [branch-name] 
 push to remote, e.g. git push origin master

 $ git remote show origin
 to investigate the remote repo

 $git remote rm reponame
 to remove a repo

 $ git remote rename old_name new_name
 to rename a repo

 $ git tag -a v0.1 -m 'message'
 to tag (annotated) a commit

 $ git tag v0.1-lw
 to simple tag a commit

 $ git show v0.1
 to see tag

 $ git config --global alias.unstage 'reset HEAD --'
 to set a name for a command








