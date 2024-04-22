# GIT EXERCISES

## Bundle1

### Exercise1

```bash


 ~
$ mkdir Bundle1Exercise1


 ~
$ cd Bundle1Exercise1



 ~/Bundle1Exercise1
$ ls
index.html  style.css


 ~/Bundle1Exercise1
$ git init
Initialized empty Git repository in C:/Users/LENOVO/Bundle1Exercise1/.git/


 ~/Bundle1Exercise1 (master)
$ ls
index.html  style.css



 ~/Bundle1Exercise1 (master)
$ git branch -m master main


 ~/Bundle1Exercise1 (main)
$ ls
index.html  style.css


 ~/Bundle1Exercise1 (main)
$ git add -A


 ~/Bundle1Exercise1 (main)
$ git commit -m 'Added index.html and style.css files'
[main (root-commit) 4be0fe5] Added index.html and style.css files
 2 files changed, 18 insertions(+)
 create mode 100644 index.html
 create mode 100644 style.css


 ~/Bundle1Exercise1 (main)
$ git remote add origin https://github.com/christellealexia/Git-Bundle1-Exercise1.git


 ~/Bundle1Exercise1 (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.



 ~/Bundle1Exercise1 (main)
$  git push --set-upstream origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 448 bytes | 448.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/christellealexia/Git-Bundle1-Exercise1.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.


 ~/Bundle1Exercise1 (main)
$ git add -A


 ~/Bundle1Exercise1 (main)
$ git commit -m 'Added a readme file'
[main ebc71f6] Added a readme file
 1 file changed, 1 insertion(+)
 create mode 100644 README..md



 ~/Bundle1Exercise1 (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 353 bytes | 353.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/christellealexia/Git-Bundle1-Exercise1.git
   4be0fe5..ebc71f6  main -> main


 ~/Bundle1Exercise1 (main)
$ git branch dev


 ~/Bundle1Exercise1 (main)
$ git branch
  dev
* main


 ~/Bundle1Exercise1 (main)
$ git checkout dev
Switched to branch 'dev'


 ~/Bundle1Exercise1 (dev)
$ git branch test


 ~/Bundle1Exercise1 (dev)
$ git branch
* dev
  main
  test


 ~/Bundle1Exercise1 (dev)
$ git branch -d test
Deleted branch test (was ebc71f6).


 ~/Bundle1Exercise1 (dev)
$ git branch
* dev
  main
  ```

  ### Exercise 2

  ```bash
   ~/Bundle1Exercise1 (dev)
$ touch home.html


 ~/Bundle1Exercise1 (dev)
$ ls
README..md  home.html  index.html  style.css


 ~/Bundle1Exercise1 (dev)
$ git stash save 'Added home.html file'
No local changes to save


 ~/Bundle1Exercise1 (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)


 ~/Bundle1Exercise1 (dev)
$ touch about.html


 ~/Bundle1Exercise1 (dev)
$ ls
README..md  about.html  home.html  index.html  style.css


 ~/Bundle1Exercise1 (dev)
$

 ~/Bundle1Exercise1 (dev)
$ git stash save about.html
No local changes to save


 ~/Bundle1Exercise1 (dev)
$ git stash pop
No stash entries found.


 ~/Bundle1Exercise1 (dev)
$ git add home.html


 ~/Bundle1Exercise1 (dev)
$ git stash save home.html
Saved working directory and index state On dev: home.html


 ~/Bundle1Exercise1 (dev)
$ git add about.html


 ~/Bundle1Exercise1 (dev)
$ git stash save about.html
Saved working directory and index state On dev: about.html


 ~/Bundle1Exercise1 (dev)
$ touch team.html


 ~/Bundle1Exercise1 (dev)
$ git stash save team.html
No local changes to save


 ~/Bundle1Exercise1 (dev)
$ git add team.html


 ~/Bundle1Exercise1 (dev)
$ git stash save team.html
Saved working directory and index state On dev: team.html


 ~/Bundle1Exercise1 (dev)
$ git stash list
stash@{0}: On dev: team.html
stash@{1}: On dev: about.html
stash@{2}: On dev: home.html


 ~/Bundle1Exercise1 (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (7e1a71ed613686bc03c42c5c6a06d41a8c2d9ba3)


 ~/Bundle1Exercise1 (dev)
$ git stash list
stash@{0}: On dev: team.html
stash@{1}: On dev: home.html


 ~/Bundle1Exercise1 (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (8bd824fac4f531ad131ec9520bc8036b0494bb13)    


 ~/Bundle1Exercise1 (dev)
$ git commit -m 'Restored about.html and home.html files'
[dev d2f1e94] Restored about.html and home.html files
 2 files changed, 10 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html


 ~/Bundle1Exercise1 (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use  

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.      



 ~/Bundle1Exercise1 (dev)
$  git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 499 bytes | 499.00 KiB/s, done.    
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)   
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:  
remote:      https://github.com/christellealexia/Git-Bundle1-Exercise1/pull/new/dev
remote:
To https://github.com/christellealexia/Git-Bundle1-Exercise1.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.


 ~/Bundle1Exercise1 (dev)
$ git stash list
stash@{0}: On dev: team.html


 ~/Bundle1Exercise1 (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (87563f48652cac5839cbefbeb432760e58070c5a)    


 ~/Bundle1Exercise1 (dev)
$ git reset --hard
HEAD is now at d2f1e94 Restored about.html and home.html files


 ~/Bundle1Exercise1 (dev)
$
```
## Bundle 2
### Exercise 1

```bash
 ~/Bundle1Exercise1 (dev)
$ git branch ft/bundle-2

 ~/Bundle1Exercise1 (dev)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'

 ~/Bundle1Exercise1 (ft/bundle-2) 
$ touch services.html

 ~/Bundle1Exercise1 (ft/bundle-2) 
$ git add .

 ~/Bundle1Exercise1 (ft/bundle-2) 
$ git commit -m 'Added services.html file'
[ft/bundle-2 dc72be5] Added services.html file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 services.html

 ~/Bundle1Exercise1 (ft/bundle-2) 
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use  

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.      


 ~/Bundle1Exercise1 (ft/bundle-2) 
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 279 bytes | 279.00 KiB/s, done.    
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)   
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/christellealexia/Git-Bundle1-Exercise1/pull/new/ft/bundle-2
remote:
To https://github.com/christellealexia/Git-Bundle1-Exercise1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.  

 ~/Bundle1Exercise1 (ft/bundle-2) 
$ git add .


 ~/Bundle1Exercise1 (ft/bundle-2) 
$ git commit -m 'Updates'
[ft/bundle-2 b8ae7f5] Updates
 1 file changed, 10 insertions(+)


 ~/Bundle1Exercise1 (ft/bundle-2) 
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 353 bytes | 353.00 KiB/s, done.    
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)   
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/christellealexia/Git-Bundle1-Exercise1.git
   dc72be5..b8ae7f5  ft/bundle-2 -> ft/bundle-2


 ~/Bundle1Exercise1 (ft/bundle-2) 
$    

```
### Exercise 2

```bash

 ~/Bundle1Exercise1 (main)        
$ git pull
Updating ebc71f6..7c13e72
Fast-forward
 about.html    |  0
 home.html     | 10 ++++++++++
 services.html |  0
 3 files changed, 10 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

 
 ~/Bundle1Exercise1 (main)        
$ git branch
  dev
  ft/bundle-2
* main


 ~/Bundle1Exercise1 (main)        
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

 ~/Bundle1Exercise1 (ft/service-redesign)
$ git add .


 ~/Bundle1Exercise1 (ft/service-redesign)
$ git commit -m 'Updates on services.html'
[ft/service-redesign 9d55b60] Updates on services.html
 1 file changed, 13 insertions(+)


 ~/Bundle1Exercise1 (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use  

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.      



 ~/Bundle1Exercise1 (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 390 bytes | 390.00 KiB/s, done.    
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)   
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/christellealexia/Git-Bundle1-Exercise1/pull/new/ft/service-redesign
remote:
To https://github.com/christellealexia/Git-Bundle1-Exercise1.git
 * [new branch]      ft/service-redesign -> ft/service-redesign 
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.


 ~/Bundle1Exercise1 (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.


 ~/Bundle1Exercise1 (main)        
$ git commit -m 'Updates on services page'
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)    
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")


 ~/Bundle1Exercise1 (main)        
$ git push
Everything up-to-date


 ~/Bundle1Exercise1 (main)        
$ git add .


 ~/Bundle1Exercise1 (main)        
$ git commit -m 'Updates on services page'
[main 89042be] Updates on services page
 1 file changed, 14 insertions(+)


 ~/Bundle1Exercise1 (main)        
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 407 bytes | 407.00 KiB/s, done.    
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)   
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/christellealexia/Git-Bundle1-Exercise1.git
   7c13e72..89042be  main -> main


 ~/Bundle1Exercise1 (main)        
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.    


 ~/Bundle1Exercise1 (ft/service-redesign)
$ git diff
diff --git a/README..md b/README..md
deleted file mode 100644
index e011d03..0000000
--- a/README..md
+++ /dev/null
@@ -1 +0,0 @@
-This is for exercise 1 bundle 1
\ No newline at end of file


 ~/Bundle1Exercise1 (ft/service-redesign)
$ git merge
Already up to date.


 ~/Bundle1Exercise1 (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.


 ~/Bundle1Exercise1 (ft/service-redesign|MERGING)
$ git add .


 ~/Bundle1Exercise1 (ft/service-redesign|MERGING)
$ git commit -m 'Merge'
[ft/service-redesign e4509c7] Merge


 ~/Bundle1Exercise1 (ft/service-redesign)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 267 bytes | 267.00 KiB/s, done.    
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)   
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/christellealexia/Git-Bundle1-Exercise1.git
   9d55b60..e4509c7  ft/service-redesign -> ft/service-redesign 


 ~/Bundle1Exercise1 (ft/service-redesign)
$
```


