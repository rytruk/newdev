ttps://github.com/rytruk/example_repo.git

rhyme@ip-172-31-131-101:~$ cd ~/dev/
rhyme@ip-172-31-131-101:~/dev$ git clone https://github.com/rytruk/example_repo.git
Cloning into 'example_repo'...
remote: Enumerating objects: 14, done.
remote: Total 14 (delta 0), reused 0 (delta 0), pack-reused 14
Unpacking objects: 100% (14/14), done.
rhyme@ip-172-31-131-101:~/dev$ ls
example_repo
rhyme@ip-172-31-131-101:~/dev$ git branch 
fatal: not a git repository (or any of the parent directories): .git
rhyme@ip-172-31-131-101:~/dev$ git config --global user.name "Rytis Rukstele"
rhyme@ip-172-31-131-101:~/dev$ git config --global user.email jambas@gmail.com
rhyme@ip-172-31-131-101:~/dev$ git branch

rhyme@ip-172-31-131-101:~/dev/example_repo$ git branch rhyme-init
rhyme@ip-172-31-131-101:~/dev/example_repo$ git branch 
* master
  rhyme-init
rhyme@ip-172-31-131-101:~/dev/example_repo$ git checkout rhyme-init 
Switched to branch 'rhyme-init'
rhyme@ip-172-31-131-101:~/dev/example_repo$ git branch 
  master
* rhyme-init
rhyme@ip-172-31-131-101:~/dev/example_repo$ git checkout -b rhyme2
Switched to a new branch 'rhyme2'
rhyme@ip-172-31-131-101:~/dev/example_repo$ git branch 
  master
  rhyme-init
* rhyme2
rhyme@ip-172-31-131-101:~/dev/example_repo$ 

Edit helloword.c in C and
rhyme@ip-172-31-131-101:~/dev/example_repo$ git status
On branch rhyme2
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   c/helloworld.c

no changes added to commit (use "git add" and/or "git commit -a")
rhyme@ip-172-31-131-101:~/dev/example_repo$ cd c/
rhyme@ip-172-31-131-101:~/dev/example_repo/c$ git add helloworld.c 
rhyme@ip-172-31-131-101:~/dev/example_repo/c$ git commit -m "Adding a comment"
[rhyme2 8d4afcd] Adding a commenth
 1 file changed, 2 insertions(+)
rhyme@ip-172-31-131-101:~/dev/example_repo/c$ git status
On branch rhyme2
nothing to commit, working tree clean

rhyme@ip-172-31-131-101:~/dev/example_repo/c$ git remote -v
origin  https://github.com/rytruk/example_repo.git (fetch)
origin  https://github.com/rytruk/example_repo.git (push)
rhyme@ip-172-31-131-101:~/dev/example_repo/c$ git remote add upstream https://github.com/therealslimgrady/example_repo.git
rhyme@ip-172-31-131-101:~/dev/example_repo/c$ git remote -vorigin  https://github.com/rytruk/example_repo.git (fetch)
origin  https://github.com/rytruk/example_repo.git (push)
upstream        https://github.com/therealslimgrady/example_repo.git (fetch)
upstream        https://github.com/therealslimgrady/example_repo.git (push)

rhyme@ip-172-31-131-101:~/dev/example_repo/c$ git push origin rhyme2
….
Total 4 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'rhyme2' on GitHub by visiting:
remote:      https://github.com/rytruk/example_repo/pull/new/rhyme2
remote: 
To https://github.com/rytruk/example_repo.git
* [new branch]      rhyme2 -> rhyme2

rhyme@ip-172-31-131-101:~/dev/example_repo$ git fetch --all
Fetching origin
Fetching upstream
From https://github.com/therealslimgrady/example_repo
* [new branch]      master     -> upstream/master
rhyme@ip-172-31-131-101:~/dev/example_repo$ git pull origin master
From https://github.com/rytruk/example_repo
 * branch            master     -> FETCH_HEAD
Already up to date.
rhyme@ip-172-31-131-101:~/dev/example_repo$ git pull upstream master
From https://github.com/therealslimgrady/example_repo
 * branch            master     -> FETCH_HEAD
Already up to date.

Edit Readme file
rhyme@ip-172-31-131-101:~/dev/example_repo$ git stash
Saved working directory and index state WIP on rhyme2: 8d4afcd Adding a comment
rhyme@ip-172-31-131-101:~/dev/example_repo$ git stash pop
On branch rhyme2
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (e18cc149d79e7bd2b95f5bf068583ed133db5016)
rhyme@ip-172-31-131-101:~/dev/example_repo$ git rebase origin/master rhyme2
Cannot rebase: You have unstaged changes.
Please commit or stash them.
rhyme@ip-172-31-131-101:~/dev/example_repo$ git stash
Saved working directory and index state WIP on rhyme2: 8d4afcd Adding a comment
rhyme@ip-172-31-131-101:~/dev/example_repo$ git rebase origin/master rhyme2
Current branch rhyme2 is up to date.

rhyme@ip-172-31-131-101:~/dev/example_repo$ git merge upstream/master 
Already up to date.
rhyme@ip-172-31-131-101:~/dev/example_repo$ git merge --abort 
fatal: There is no merge to abort (MERGE_HEAD missing).

LOG usage

git log
……
git log –stat
git log –graph
….
git log –oneline
git log --oneline –decorate=no
git log --walk-reflogs 
git reflog

git show HEAD@{2}~
git commit –amend (Edit commit)

git log –online
git rebase -i 9a168f4
….. galima redaguoti, pvz pakeisti I “squash” ir issaugoti
git log


...jei norime panaikinti kuri nors commita
git log –online
git reset --hard b5910f6


NEW Branch – create a folder 
in the folder
$git init .

...Create branch on github and
git remote add origin https://github.com/rytruk/newdev.git
git puch -u origin master
git status
Galima susikuti  sarasa kuriuos failus ignoruoti
vi .gitignore
vi .git/info/exclude 



