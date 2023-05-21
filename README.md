# Gym-Git-Exercise-Solutions
## Bundle 1
### Exercice 1

```bash
Andelas-MBP:git-exercises andelarwanda$ git init
Initialized empty Git repository in /Users/andelarwanda/Desktop/TheGym/git-exercises/.git/
Andelas-MBP:git-exercises andelarwanda$ git branch -M master
Andelas-MBP:git-exercises andelarwanda$ git branch
Andelas-MBP:git-exercises andelarwanda$ git branch -M main
Andelas-MBP:git-exercises andelarwanda$ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
Andelas-MBP:git-exercises andelarwanda$ touch readme.md
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   readme.md

Andelas-MBP:git-exercises andelarwanda$ git commit -m "init project"
[main (root-commit) 67b6db9] init project
 1 file changed, 2 insertions(+)
 create mode 100644 readme.md
Andelas-MBP:git-exercises andelarwanda$ git remote add origin https://github.com/kunda4/git-exercises.git
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 281 bytes | 281.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/kunda4/git-exercises.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
Andelas-MBP:git-exercises andelarwanda$ git checkout -b dev
Switched to a new branch 'dev'
Andelas-MBP:git-exercises andelarwanda$ git branch
* dev
  main
Andelas-MBP:git-exercises andelarwanda$ git checkout -b test
Switched to a new branch 'test'
Andelas-MBP:git-exercises andelarwanda$ git branch
  dev
  main
* test
Andelas-MBP:git-exercises andelarwanda$ git checkout dev
Switched to branch 'dev'
Andelas-MBP:git-exercises andelarwanda$ git branch -d test
Deleted branch test (was 67b6db9).
Andelas-MBP:git-exercises andelarwanda$ git branch
* dev
  main
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$ git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/dev
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
Andelas-MBP:git-exercises andelarwanda$ 
```
## Bundle 1
### Exercice 2
```bash
Andelas-MBP:git-exercises andelarwanda$ touch home.html
Andelas-MBP:git-exercises andelarwanda$ git add .home.html
fatal: pathspec '.home.html' did not match any files
Andelas-MBP:git-exercises andelarwanda$ git add home.html
Andelas-MBP:git-exercises andelarwanda$ git stash save "home.html file"
Saved working directory and index state On dev: home.html file
Andelas-MBP:git-exercises andelarwanda$ touch about.html
Andelas-MBP:git-exercises andelarwanda$ git add about.html
Andelas-MBP:git-exercises andelarwanda$ git stash save "about.html file"
Saved working directory and index state On dev: about.html file
Andelas-MBP:git-exercises andelarwanda$ git stash list
stash@{0}: On dev: about.html file
stash@{1}: On dev: home.html file
Andelas-MBP:git-exercises andelarwanda$ touch team.html
Andelas-MBP:git-exercises andelarwanda$ git add team.html
Andelas-MBP:git-exercises andelarwanda$ git stash save "team.html file"
Saved working directory and index state On dev: team.html file
Andelas-MBP:git-exercises andelarwanda$ git stash list
stash@{0}: On dev: team.html file
stash@{1}: On dev: about.html file
stash@{2}: On dev: home.html file
Andelas-MBP:git-exercises andelarwanda$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (63e5c0e84d0c90ec7e85df78d8ad89fd0cd49ed4)
Andelas-MBP:git-exercises andelarwanda$ git stash list
stash@{0}: On dev: team.html file
stash@{1}: On dev: home.html file
Andelas-MBP:git-exercises andelarwanda$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (f0a6d2ca4207f044f2346e33ea9375f0d076a9d2)
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "unstash about and home page"
[dev 3d6fb62] unstash about and home page
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
Andelas-MBP:git-exercises andelarwanda$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 546 bytes | 546.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/kunda4/git-exercises.git
   67b6db9..3d6fb62  dev -> dev
Andelas-MBP:git-exercises andelarwanda$ git stash list
stash@{0}: On dev: team.html file
Andelas-MBP:git-exercises andelarwanda$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (39b8453c80a6cbc3c3e80cd78bc2e95363b96c9d)
Andelas-MBP:git-exercises andelarwanda$ git reset --hard
HEAD is now at 3d6fb62 unstash about and home page
Andelas-MBP:git-exercises andelarwanda$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
Andelas-MBP:git-exercises andelarwanda$ 
```
