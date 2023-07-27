# git-exercises-allbundles

## BUNDLE 1

### Exercise 1

```bash
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

```

### Exercise 2

```bash
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
```

## BUNDLE 2

### Exercise 1

```bash
LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/bundle-2)
$ vi services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/bundle-2)
$ git add .
warning: in the working copy of 'services.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/bundle-2)
$ git commit -m 'added services page'
[ft/bundle-2 dae678f] added services page
 1 file changed, 9 insertions(+)
 create mode 100644 services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 352 bytes | 352.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/gitarecy/git-exercises-allbundles/pull/new/ft/bundle-2
remote:
To https://github.com/gitarecy/git-exercises-allbundles.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
```

### Exercise 2

```bash
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git checkout main\
> ^C

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git pull
remote: Enumerating objects: 19, done.
remote: Counting objects: 100% (19/19), done.
remote: Compressing objects: 100% (18/18), done.
remote: Total 18 (delta 5), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (18/18), 5.95 KiB | 96.00 KiB/s, done.
From https://github.com/gitarecy/git-exercises-allbundles
   1973994..ea6e06b  main       -> origin/main
Updating 1973994..ea6e06b
Fast-forward
 README.md | 297 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 297 insertions(+)
 create mode 100644 README.md

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git add .
warning: in the working copy of 'service.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git commit -m 'added new changes to service.html'
[ft/service-redesign 6fa8bbb] added new changes to service.html
 1 file changed, 8 insertions(+)
 create mode 100644 service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 351 bytes | 351.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/gitarecy/git-exercises-allbundles/pull/new/ft/service-redesign
remote:
To https://github.com/gitarecy/git-exercises-allbundles.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git add .
warning: in the working copy of 'service.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git commit -m 'added service.html'
[main d6f7b19] added service.html
 1 file changed, 10 insertions(+)
 create mode 100644 service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 427 bytes | 427.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/gitarecy/git-exercises-allbundles.git
   ea6e06b..d6f7b19  main -> main

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git diff main
diff --git a/README.md b/README.md
deleted file mode 100644
index f951d07..0000000
--- a/README.md
+++ /dev/null
@@ -1,297 +0,0 @@
-# git-exercises-allbundles
-
-## BUNDLE 1
-
-### Exercise 1
-
-```bash
-$ cd Desktop/Git-exercises/
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
-$ git init
-Initialized empty Git repository in C:/Users/LENOVO/Desktop/Git-exercises/.git/
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (master)
-$ git branch -m master main
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
:...skipping...
diff --git a/README.md b/README.md
deleted file mode 100644
index f951d07..0000000
--- a/README.md
+++ /dev/null
@@ -1,297 +0,0 @@
-# git-exercises-allbundles
-
-## BUNDLE 1
-
-### Exercise 1
-
-```bash
-$ cd Desktop/Git-exercises/
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
-$ git init
-Initialized empty Git repository in C:/Users/LENOVO/Desktop/Git-exercises/.git/
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (master)
-$ git branch -m master main
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
-$ touch file.txt
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ ls
README.md  file.txt  service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git commit -m 'added service.html'
[main 2219a87] added service.html
 1 file changed, 1 insertion(+), 1 deletion(-)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 283 bytes | 283.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/gitarecy/git-exercises-allbundles.git
   d6f7b19..2219a87  main -> main

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git diff main
diff --git a/README.md b/README.md
deleted file mode 100644
index f951d07..0000000
--- a/README.md
+++ /dev/null
@@ -1,297 +0,0 @@
-# git-exercises-allbundles
-
-## BUNDLE 1
-
-### Exercise 1
-
-```bash
-$ cd Desktop/Git-exercises/
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
-$ git init
-Initialized empty Git repository in C:/Users/LENOVO/Desktop/Git-exercises/.git/
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (master)
-$ git branch -m master main
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
-$ touch file.txt
-
-LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ ls
file.txt  service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git merge main
Auto-merging service.html
CONFLICT (add/add): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign|MERGING)
$ git merge main
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign|MERGING)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign|MERGING)
$ git commit -m 'Merged main branch into ft/service-redesign'
[ft/service-redesign f8f2a09] Merged main branch into ft/service-redesign

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
To https://github.com/gitarecy/git-exercises-allbundles.git
 ! [rejected]        ft/service-redesign -> ft/service-redesign (fetch first)
error: failed to push some refs to 'https://github.com/gitarecy/git-exercises-allbundles.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git diff main
diff --git a/service.html b/service.html
index 4711c12..bee656f 100644
--- a/service.html
+++ b/service.html
@@ -3,8 +3,12 @@
 <title>Service</title>
 </head>
 <body>
+<<<<<<< HEAD
+<h1>Our Service</h1>
+=======
 <h1>Our Services</h1>
 <p>We offer a wide range of services, including...</p>
 <p>We also offer...</p>
+>>>>>>> main
 </body>
 </html>

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ ls
README.md  file.txt  service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git diff main
diff --git a/service.html b/service.html
index 4711c12..f0bec0a 100644
--- a/service.html
+++ b/service.html
@@ -3,8 +3,12 @@
 <title>Service</title>
 </head>
 <body>
+<<<<<<< HEAD
+<h1></h1>
+=======
 <h1>Our Services</h1>
-<p>We offer a wide range of services, including...</p>
-<p>We also offer...</p>
+<p></p>
+<p></p>
+>>>>>>> main
 </body>
 </html>

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git commit -m 'changes to service '
[ft/service-redesign 26607b7] changes to service
 1 file changed, 3 insertions(+), 3 deletions(-)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
To https://github.com/gitarecy/git-exercises-allbundles.git
 ! [rejected]        ft/service-redesign -> ft/service-redesign (fetch first)
error: failed to push some refs to 'https://github.com/gitarecy/git-exercises-allbundles.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git diff main
diff --git a/service.html b/service.html
index 4711c12..f0bec0a 100644
--- a/service.html
+++ b/service.html
@@ -3,8 +3,12 @@
 <title>Service</title>
 </head>
 <body>
+<<<<<<< HEAD
+<h1></h1>
+=======
 <h1>Our Services</h1>
-<p>We offer a wide range of services, including...</p>
-<p>We also offer...</p>
+<p></p>
+<p></p>
+>>>>>>> main
 </body>
 </html>

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git commit -m 'service update'
[ft/service-redesign 378e2ad] service update
 1 file changed, 2 deletions(-)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
To https://github.com/gitarecy/git-exercises-allbundles.git
 ! [rejected]        ft/service-redesign -> ft/service-redesign (fetch first)
error: failed to push some refs to 'https://github.com/gitarecy/git-exercises-allbundles.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git diff main
diff --git a/service.html b/service.html
index 4711c12..8a76686 100644
--- a/service.html
+++ b/service.html
@@ -3,8 +3,10 @@
 <title>Service</title>
 </head>
 <body>
+<<<<<<< HEAD
+<h1></h1>
+=======
 <h1>Our Services</h1>
-<p>We offer a wide range of services, including...</p>
-<p>We also offer...</p>
+>>>>>>> main
 </body>
 </html>

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git commit -m 'service update'
[ft/service-redesign 43cc854] service update
 1 file changed, 2 insertions(+), 5 deletions(-)
LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
To https://github.com/gitarecy/git-exercises-allbundles.git
 ! [rejected]        ft/service-redesign -> ft/service-redesign (fetch first)
error: failed to push some refs to 'https://github.com/gitarecy/git-exercises-allbundles.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git commit -m 'updates on service'
[main 05a99c3] updates on service
 1 file changed, 2 insertions(+), 3 deletions(-)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git push origin main
To https://github.com/gitarecy/git-exercises-allbundles.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/gitarecy/git-exercises-allbundles.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git push origin ft/service-redesign


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 1.29 KiB | 101.00 KiB/s, done.
From https://github.com/gitarecy/git-exercises-allbundles
   6fa8bbb..acd06ca  ft/service-redesign -> origin/ft/service-redesign
   2219a87..4459b04  main                -> origin/main
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> ft/service-redesign


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 1 and 3 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git pull
Auto-merging service.html
Merge made by the 'ort' strategy.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
To https://github.com/gitarecy/git-exercises-allbundles.git
 ! [rejected]        ft/service-redesign -> ft/service-redesign (non-fast-forward)
error: failed to push some refs to 'https://github.com/gitarecy/git-exercises-allbundles.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> ft/service-redesign


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git branch --set-upstream-to=origin/ft/service-redesign ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
To https://github.com/gitarecy/git-exercises-allbundles.git
 ! [rejected]        ft/service-redesign -> ft/service-redesign (non-fast-forward)
error: failed to push some refs to 'https://github.com/gitarecy/git-exercises-allbundles.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git branch --set-upstream-to=origin/ft/service-redesign ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git pull
Auto-merging service.html
Merge made by the 'ort' strategy.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 19, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 8 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (13/13), 1.25 KiB | 1.25 MiB/s, done.
Total 13 (delta 9), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (9/9), completed with 3 local objects.
To https://github.com/gitarecy/git-exercises-allbundles.git
   acd06ca..bb311bd  ft/service-redesign -> ft/service-redesign

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git merge main
Merge made by the 'ort' strategy.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git commit -m 'merging ft/service-redesign to main'
On branch ft/service-redesign
Your branch is ahead of 'origin/ft/service-redesign' by 4 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Desktop/Git-exercises (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 550 bytes | 550.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/gitarecy/git-exercises-allbundles.git
   bb311bd..548a8c5  ft/service-redesign -> ft/service-redesign

```

## Bundle 3
### Exercise 1

```bash

```
