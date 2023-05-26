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
## Bundle 2
### Exercice 1
```bash
Andelas-MBP:git-exercises andelarwanda$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
Andelas-MBP:git-exercises andelarwanda$ touch services.html
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "add services.html file"
[ft/bundle-2 a4a372a] add services.html file
 1 file changed, 12 insertions(+)
 create mode 100644 services.html
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$  git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 486 bytes | 486.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/ft/bundle-2
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```
## Bundle 2
### Exercice 2
```bash
Andelas-MBP:git-exercises andelarwanda$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit "feat: add changes to services.html"
error: pathspec 'feat: add changes to services.html' did not match any file(s) known to git
Andelas-MBP:git-exercises andelarwanda$ git commit -m "feat: add changes to services.html"
[ft/service-redesign 83e78a1] feat: add changes to services.html
 1 file changed, 7 insertions(+)
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 376 bytes | 376.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/ft/service-redesign
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
Andelas-MBP:git-exercises andelarwanda$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "add some changes on services.html"
[main 2817ff5] add some changes on services.html
 1 file changed, 7 insertions(+)
Andelas-MBP:git-exercises andelarwanda$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 358 bytes | 358.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kunda4/git-exercises.git
   dd64ec5..2817ff5  main -> main
Andelas-MBP:git-exercises andelarwanda$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
Andelas-MBP:git-exercises andelarwanda$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "feat: fix(conflict)"
[ft/service-redesign 688c2bb] feat: fix(conflict)
Andelas-MBP:git-exercises andelarwanda$ git push
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 252 bytes | 252.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/kunda4/git-exercises.git
   83e78a1..688c2bb  ft/service-redesign -> ft/service-redesign
```
## Bundle 3
### Exercice 1
```bash
Andelas-MBP:git-exercises andelarwanda$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
Andelas-MBP:git-exercises andelarwanda$ touch team.html
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "feat: Create team.html"
[ft/team-page 44a30ee] feat: Create team.html
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 483 bytes | 483.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/ft/team-page
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
Andelas-MBP:git-exercises andelarwanda$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
Andelas-MBP:git-exercises andelarwanda$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
Andelas-MBP:git-exercises andelarwanda$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
Andelas-MBP:git-exercises andelarwanda$ git log
commit 44a30ee06fd18c09986e8f4892509f9ca9277e84 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 03:11:33 2023 +0200

    feat: Create team.html

commit 688c2bb98abba46ec2bc0488f93145e8a86652a4 (origin/ft/service-redesign, ft/service-redesign)
Merge: 83e78a1 2817ff5
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:45:18 2023 +0200

    feat: fix(conflict)

commit 2817ff56691a594e61ddcec391d3fb452513d83b (origin/main, main, ft/contact-page)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:33:09 2023 +0200

    add some changes on services.html

commit 83e78a13c31348e631374059fa08f314e43e5c9c
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:28:19 2023 +0200

Andelas-MBP:git-exercises andelarwanda$ git branch
  dev
  ft/bundle-2
  ft/contact-page
  ft/service-redesign
* ft/team-page
  main
Andelas-MBP:git-exercises andelarwanda$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'
Andelas-MBP:git-exercises andelarwanda$ git cherry-pick 44a30ee06fd18c09986e8f4892509f9ca9277e84 
[ft/contact-page 04eae5a] feat: Create team.html
 Date: Mon May 22 03:11:33 2023 +0200
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
Andelas-MBP:git-exercises andelarwanda$ touch contact.html
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "feat: add contact.html file"
[ft/contact-page 0542558] feat: add contact.html file
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 2 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 765 bytes | 765.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/ft/contact-page
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
Andelas-MBP:git-exercises andelarwanda$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
Andelas-MBP:git-exercises andelarwanda$ touch faq.html
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "add new file faq.html"
[ft/faq-page 36d9361] add new file faq.html
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$  git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 477 bytes | 477.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/ft/faq-page
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
Andelas-MBP:git-exercises andelarwanda$ git log
commit 36d9361c2973b031bc95e5f5fce9cef171ab1918 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 03:44:15 2023 +0200

    add new file faq.html

commit 0542558304ba3e4f1fb85ce67858e4f21a43a0f9 (origin/ft/contact-page, ft/contact-page)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 03:35:33 2023 +0200

    feat: add contact.html file

commit 04eae5a279f2f12c5d5d9f8441906185b804299e
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 03:11:33 2023 +0200

    feat: Create team.html

commit 2817ff56691a594e61ddcec391d3fb452513d83b (origin/main, main)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:33:09 2023 +0200

    add some changes on services.html

commit dd64ec5e9678a6d870889c170737cf5ece5fd343
Merge: e8e872b a4a372a
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Andelas-MBP:git-exercises andelarwanda$ git revert 04eae5a279f2f12c5d5d9f8441906185b804299e
[ft/faq-page 9c1659f] Revert "feat: Create team.html"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html
Andelas-MBP:git-exercises andelarwanda$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 305 bytes | 305.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/kunda4/git-exercises.git
   36d9361..9c1659f  ft/faq-page -> ft/faq-page
   ```
## Bundle 3
### Exercice 2
```bash
Andelas-MBP:git-exercises andelarwanda$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
Andelas-MBP:git-exercises andelarwanda$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "add homepage content"
[main e588c26] add homepage content
 1 file changed, 4 insertions(+), 1 deletion(-)
Andelas-MBP:git-exercises andelarwanda$ git push origin main
To https://github.com/kunda4/git-exercises.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/kunda4/git-exercises.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
Andelas-MBP:git-exercises andelarwanda$ git push origin main --force
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 401 bytes | 401.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kunda4/git-exercises.git
 + 244319e...e588c26 main -> main (forced update)
Andelas-MBP:git-exercises andelarwanda$ git branch
  dev
  ft/bundle-2
  ft/contact-page
  ft/faq-page
  ft/home-page-redesign
  ft/service-redesign
  ft/team-page
* main
Andelas-MBP:git-exercises andelarwanda$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
Andelas-MBP:git-exercises andelarwanda$ git log
commit 9c1659f83d40334e5c7d1ccc1837a2d584398d16 (HEAD -> ft/home-page-redesign, origin/ft/faq-page, ft/faq-page)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 03:51:05 2023 +0200

    Revert "feat: Create team.html"
    
    This reverts commit 04eae5a279f2f12c5d5d9f8441906185b804299e.

commit 36d9361c2973b031bc95e5f5fce9cef171ab1918
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 03:44:15 2023 +0200

    add new file faq.html

commit 0542558304ba3e4f1fb85ce67858e4f21a43a0f9 (origin/ft/contact-page, ft/contact-page)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 03:35:33 2023 +0200

    feat: add contact.html file

commit 04eae5a279f2f12c5d5d9f8441906185b804299e
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 03:11:33 2023 +0200

    feat: Create team.html

commit 2817ff56691a594e61ddcec391d3fb452513d83b
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:33:09 2023 +0200

    add some changes on services.html

commit dd64ec5e9678a6d870889c170737cf5ece5fd343
Merge: e8e872b a4a372a
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:23:35 2023 +0200

    Merge pull request #2 from kunda4/ft/bundle-2
    
    Bundle2 #Exercise1

commit e8e872bd4ab5baa17a85351ff122e353bed7dc5f
Merge: 67b6db9 3d6fb62
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:10:42 2023 +0200

    Merge pull request #1 from kunda4/dev
    
    feat: stash files and retore

commit a4a372a5a7501a95f8fc4cd802f75286d4c5b98a (origin/ft/bundle-2, ft/bundle-2)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:09:26 2023 +0200

    add services.html file

commit 3d6fb62673354abf7fd3fcc03b4a1b9023bb0eec (origin/dev, dev)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 01:48:44 2023 +0200

    unstash about and home page

commit 67b6db9e44541ceb7842c34ce8deb5ede21234d2
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 01:22:57 2023 +0200

    init project
Andelas-MBP:git-exercises andelarwanda$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "feat: rebase and add change to home page"
[ft/home-page-redesign ff98592] feat: rebase and add change to home page
 1 file changed, 5 insertions(+)
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$  git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 2 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.91 KiB | 1.91 MiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), done.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/ft/home-page-redesign
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
Andelas-MBP:git-exercises andelarwanda$ 
```
## Bundle 4
### Exercice 1
```bash
Andelas-MBP:git-exercises andelarwanda$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
Andelas-MBP:git-exercises andelarwanda$ git remote add git-copy https://github.com/kunda4/git-exercises-clone.git
Andelas-MBP:git-exercises andelarwanda$ git remote
git-copy
origin
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   home.html

Andelas-MBP:git-exercises andelarwanda$ git commit -m "modify home.html"
[main c37fadc] modify home.html
 1 file changed, 1 insertion(+)
Andelas-MBP:git-exercises andelarwanda$ git push origin
To https://github.com/kunda4/git-exercises.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/kunda4/git-exercises.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
Andelas-MBP:git-exercises andelarwanda$ git push git-copy
Enumerating objects: 21, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 2 threads
Compressing objects: 100% (19/19), done.
Writing objects: 100% (21/21), 2.92 KiB | 1.46 MiB/s, done.
Total 21 (delta 12), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (12/12), done.
To https://github.com/kunda4/git-exercises-clone.git
 * [new branch]      main -> main
Andelas-MBP:git-exercises andelarwanda$ git push origin
To https://github.com/kunda4/git-exercises.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/kunda4/git-exercises.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
Andelas-MBP:git-exercises andelarwanda$ git push origin --force
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 340 bytes | 340.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kunda4/git-exercises.git
 + a3fff70...c37fadc main -> main (forced update)
Andelas-MBP:git-exercises andelarwanda$ 
```
## Bundle 4
### Exercice 2
```bash
Andelas-MBP:git-exercises andelarwanda$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'
Andelas-MBP:git-exercises andelarwanda$ touch footer.html
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "create footer.html"
[ft/footer 6ce70f4] create footer.html
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 footer.html
Andelas-MBP:git-exercises andelarwanda$ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add
Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "Add contents in footer.html"
[ft/footer 35c2f21] Add contents in footer.html
 1 file changed, 17 insertions(+)
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch ft/footer has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/footer

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$  git push --set-upstream origin ft/footer
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 2 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 819 bytes | 819.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/ft/footer
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
Andelas-MBP:git-exercises andelarwanda$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
Andelas-MBP:git-exercises andelarwanda$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
Andelas-MBP:git-exercises andelarwanda$ git merge --squash ft/footer
Updating c37fadc..35c2f21
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 17 +++++++++++++++++
 1 file changed, 17 insertions(+)
 create mode 100644 footer.html
Andelas-MBP:git-exercises andelarwanda$ git log
commit c37fadcb988c4b297903891f5facc76cf81c4434 (HEAD -> ft/squashing, origin/main, git-copy/main, main)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 04:35:21 2023 +0200

    modify home.html

commit e588c268f5ba0d39875ee216f83573ea5b6b3b18
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 04:08:04 2023 +0200

    add homepage content

commit 2817ff56691a594e61ddcec391d3fb452513d83b
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:33:09 2023 +0200

    add some changes on services.html

commit dd64ec5e9678a6d870889c170737cf5ece5fd343
Merge: e8e872b a4a372a
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:23:35 2023 +0200

Andelas-MBP:git-exercises andelarwanda$ git add .
Andelas-MBP:git-exercises andelarwanda$ git commit -m "footer changes squashing"
[ft/squashing 8747673] footer changes squashing
 1 file changed, 17 insertions(+)
 create mode 100644 footer.html
Andelas-MBP:git-exercises andelarwanda$ git log
commit 87476734317722786c4ab6810c4b4285cdb88b33 (HEAD -> ft/squashing)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 04:54:21 2023 +0200

    footer changes squashing

commit c37fadcb988c4b297903891f5facc76cf81c4434 (origin/main, git-copy/main, main)
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 04:35:21 2023 +0200

    modify home.html

commit e588c268f5ba0d39875ee216f83573ea5b6b3b18
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 04:08:04 2023 +0200

    add homepage content

commit 2817ff56691a594e61ddcec391d3fb452513d83b
Author: Agnes IRADUKUNDA <101483232+kunda4@users.noreply.github.com>
Date:   Mon May 22 02:33:09 2023 +0200

    add some changes on services.html
Andelas-MBP:git-exercises andelarwanda$ git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-exercises andelarwanda$  git push --set-upstream origin ft/squashing
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 546 bytes | 546.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/kunda4/git-exercises/pull/new/ft/squashing
remote: 
To https://github.com/kunda4/git-exercises.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
Andelas-MBP:git-exercises andelarwanda$ 
```
## Bundle 5
### Exercice 2
```bash
Andelas-MBP:git-cafe-exercise andelarwanda$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .vscode/

no changes added to commit (use "git add" and/or "git commit -a")
Andelas-MBP:git-cafe-exercise andelarwanda$ git add .
Andelas-MBP:git-cafe-exercise andelarwanda$ git commit -m "modify index.html"
[main 2c13946] modify index.html
 2 files changed, 4 insertions(+), 1 deletion(-)
 create mode 100644 .vscode/settings.json
Andelas-MBP:git-cafe-exercise andelarwanda$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 483 bytes | 483.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kunda4/git-cafe-exercise.git
   d1d3f9c..2c13946  main -> main
Andelas-MBP:git-cafe-exercise andelarwanda$ 
```
## Bundle 6
### Exercice 1
```bash
Andelas-MBP:git-cafe-exercise andelarwanda$ git branch
* main
Andelas-MBP:git-cafe-exercise andelarwanda$ git checkout -b feature
Switched to a new branch 'feature'
Andelas-MBP:git-cafe-exercise andelarwanda$ touch Menu.html
Andelas-MBP:git-cafe-exercise andelarwanda$ git status
On branch feature
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Menu.html

nothing added to commit but untracked files present (use "git add" to track)
Andelas-MBP:git-cafe-exercise andelarwanda$ git add Menu.html
Andelas-MBP:git-cafe-exercise andelarwanda$ git commit -m "Add menu.html file"
[feature b1636df] Add menu.html file
 1 file changed, 18 insertions(+)
 create mode 100644 Menu.html
Andelas-MBP:git-cafe-exercise andelarwanda$ git push
fatal: The current branch feature has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feature

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Andelas-MBP:git-cafe-exercise andelarwanda$  git push --set-upstream origin feature
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 527 bytes | 527.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'feature' on GitHub by visiting:
remote:      https://github.com/kunda4/git-cafe-exercise/pull/new/feature
remote: 
To https://github.com/kunda4/git-cafe-exercise.git
 * [new branch]      feature -> feature
branch 'feature' set up to track 'origin/feature'.
Andelas-MBP:git-cafe-exercise andelarwanda$ 
```
