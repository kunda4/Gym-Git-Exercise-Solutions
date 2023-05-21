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
