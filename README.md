# git-exercises-allbundles
BUNDLE 1
========
Exercise 1
=========
$ cd Desktop/Git-exercises/

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git init
Initialized empty Git repository in C:/Users/LENOVO/Desktop/Git-exercises/.git/

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (master)
$ git branch -m master main

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ touch file.txt

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git coomit -m 'added file'
git: 'coomit' is not a git command. See 'git --help'.

The most similar command is
        commit

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git commit -m 'added file'
[main (root-commit) 1973994] added file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file.txt

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git remote add origin git@github.com:gitarecy/git-exercises-allbundles.git

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git push -u origin main
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git remote set-url https://github.com/gitarecy/git-exercises-allbundles.git
usage: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

    --push                manipulate push URLs
    --add                 add URL
    --delete              delete URLs


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git remote set-url origin https://github.com/gitarecy/git-exercises-allbundles.git

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 208 bytes | 104.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/gitarecy/git-exercises-allbundles.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ sudo service ssh start
bash: sudo: command not found

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ ssh-keygen -t rsa -b 4096
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/LENOVO/.ssh/id_rsa):

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git checkout -b dev
Switched to a new branch 'dev'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git checkout -b test
Switched to a new branch 'test'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (test)
$ touch test.txt

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (test)
$ git checkout dev
Switched to branch 'dev'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git branch -d test
Deleted branch test (was 1973994).

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git commit -m 'new dev branch'
[dev bf8b086] new dev branch
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git push -u origin dev
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 242 bytes | 242.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/gitarecy/git-exercises-allbundles/pull/new/dev
remote:
To https://github.com/gitarecy/git-exercises-allbundles.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.


Exercise 2
==========

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ vi home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git add .
warning: in the working copy of 'home.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash save 'changes to home.html page'
Saved working directory and index state On dev: changes to home.html page

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ vi about.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git  add .
warning: in the working copy of 'about.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash save 'changes to about.html page'
Saved working directory and index state On dev: changes to about.html page

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ vi team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git add .
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash save 'changes to team.html page'
Saved working directory and index state On dev: changes to team.html page

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash list
stash@{0}: On dev: changes to team.html page
stash@{1}: On dev: changes to about.html page
stash@{2}: On dev: changes to home.html page

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is ahead of 'origin/dev' by 2 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (745061279a26c1536681b03e5b298f41d23bfcd4)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash list
stash@{0}: On dev: changes to team.html page
stash@{1}: On dev: changes to home.html page

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash pop stash@{1}
On branch dev
Your branch is ahead of 'origin/dev' by 2 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (43da3d1d0343ca2d01cc516c52552c48303bbb8c)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git commit -m 'changes to home and about pages'
[dev dec78d8] changes to home and about pages
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 822 bytes | 822.00 KiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/gitarecy/git-exercises-allbundles.git
   bf8b086..dec78d8  dev -> dev

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash list
stash@{0}: On dev: changes to team.html page

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (3a63958ee3a0209e2760dbca0e3c5433cc515911)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ git reset --hard HEAD
HEAD is now at dec78d8 changes to home and about pages

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (dev)
$ ls
about.html  file.txt  home.html  test.txt

