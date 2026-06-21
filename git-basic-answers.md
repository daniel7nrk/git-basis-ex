## bundel 1
# exe 1
Q1.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git init
Reinitialized existing Git repository in C:/Users/IFAK/Desktop/git-exe-basic/.git/

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git branch
* main

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ echo "Hello this is a Git file" > app.txt

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        app.txt

nothing added to commit but untracked files present (use "git add" to track)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git branch
* main

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git branch -M master

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (master)
$ git branch
* master

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (master)
$ git branch -M main

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git branch
* main
```

q4.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git add ./
warning: in the working copy of 'app.txt', LF will be replaced by CRLF the next time Git touches it

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git commit -m "Initial project setup"
[main 93e6aa3] Initial project setup
 1 file changed, 1 insertion(+)
 create mode 100644 app.txt

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git log --oneline
93e6aa3 (HEAD -> main) Initial project setup
191c2fe (origin/main) first commit

```
q5.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git remote -v
origin  https://github.com/daniel7nrk/git-basis-ex.git (fetch)
origin  https://github.com/daniel7nrk/git-basis-ex.git (push)

```

q6. 
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 309 bytes | 309.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/daniel7nrk/git-basis-ex.git
   191c2fe..93e6aa3  main -> main

```

q7
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout -b dev
Switched to a new branch 'dev'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git branch
* dev
  main
```
q8.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git checkout -b test
Switched to a new branch 'test'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (test)
$ git branch
  dev
  main
* test
```
q9.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (test)
$ git switch dev
Switched to branch 'dev'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git branch
* dev
  main
  test
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
```
q10
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git branch -d test
Deleted branch test (was 93e6aa3).

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git branch
* dev
  main

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ 
```

# exercise 2
q1.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ echo "<h1>Home Page</h1>" > home.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash push -u -m "home page"
warning: in the working copy of 'home.html', LF will be replaced by CRLF the next time Git touches it
Saved working directory and index state On dev: home page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash list
stash@{0}: On dev: home page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git status
On branch dev
nothing to commit, working tree clean

```

q2.
```bash
```
q3.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ touch about.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash push -u -m "about page"
Saved working directory and index state On dev: about page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash list
stash@{0}: On dev: about page
stash@{1}: On dev: home page
```
q4.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ echo "<h1>Team Page</h1>" > team.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash push -u -m "team page"
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it
Saved working directory and index state On dev: team page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash list
stash@{0}: On dev: team page
stash@{1}: On dev: about page
stash@{2}: On dev: home page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ 
```
q5.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash pop stash@{1}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{1} (b0ed7e37fb1908e28667081c9391255ee103012e)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ ls
about.html  app.txt  README.md
```
q6.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash list
stash@{0}: On dev: team page
stash@{1}: On dev: home page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash pop stash@{1}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{1} (ce12c41dfd70dd527e7b3dc27e99c1b1e6f20ecf)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ ls
about.html  app.txt  home.html  README.md

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ 
```
q7
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git add .

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git commit -m "Add home and about pages"
[dev 8e0d0e5] Add home and about pages
 2 files changed, 2 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 394 bytes | 131.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/dev
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      dev -> dev

```

q8.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash list
stash@{0}: On dev: team page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash pop stash@{0}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{0} (57dab76918dbf8025fddb27b84b4454bb79d895d)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ 
```
q9.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git reset --hard HEAD
HEAD is now at 8e0d0e5 Add home and about pages

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git clean -fd
Removing team.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git status
On branch dev
nothing to commit, working tree clean

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ ls
about.html  app.txt  home.html  README.md

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash pop stash@{1}
error: stash@{1} is not a valid reference
```

```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git stash list

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ 
```

## bundle 2
# exe 1

q1.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git branch
* dev
  main

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ git branch
  dev
* ft/bundle-2
  main
```

q2. 
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ touch services.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ echo "<h1>Services Page</h1>" > services.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ cat services.html
<h1>Services Page</h1>
```
q3.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ git add services.html
warning: in the working copy of 'services.html', LF will be replaced by CRLF the next time Git touches it

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ git commit -m "Add services page"
[ft/bundle-2 a54d9bf] Add services page
 1 file changed, 1 insertion(+)
 create mode 100644 services.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ git log --oneline -3
a54d9bf (HEAD -> ft/bundle-2) Add services page
8e0d0e5 (origin/dev, dev) Add home and about pages
93e6aa3 (origin/main, main) Initial project setup

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 308 bytes | 154.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/ft/bundle-2
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ 
```

q4. 
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 892 bytes | 52.00 KiB/s, done.
From https://github.com/daniel7nrk/git-basis-ex
 * branch            main       -> FETCH_HEAD
   93e6aa3..9857500  main       -> origin/main
Updating 93e6aa3..9857500
Fast-forward
 about.html    | 1 +
 home.html     | 1 +
 services.html | 1 +
 3 files changed, 3 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ 
```

# ex2

q1.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git pull origin main
From https://github.com/daniel7nrk/git-basis-ex
 * branch            main       -> FETCH_HEAD
Already up to date.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ 
```
q2.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
```
q3.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/service-redesign)
$ git add services.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/service-redesign)
$ git commit -m "Redesign services page heading"
[ft/service-redesign d78fc1b] Redesign services page heading
 1 file changed, 1 insertion(+), 1 deletion(-)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/service-redesign)
$ git push -u origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 309 bytes | 154.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/ft/service-redesign
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/service-redesign)
$ 
```
## bundle 3

# ex 1

q1. 
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main|MERGING)
$ git checkout main
git pull origin main
Already on 'main'
Your branch is up to date with 'origin/main'.
From https://github.com/daniel7nrk/git-basis-ex
 * branch            main       -> FETCH_HEAD
Already up to date.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ 
```

the rest of the exercise 
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/team-page)
$ touch team.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/team-page)
$ echo "<h1>Our Team</h1>" > team.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/team-page)
$ git add team.html
git commit -m "Add team page"
git push -u origin ft/team-page
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it
On branch ft/team-page
nothing to commit, working tree clean
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 294 bytes | 98.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/ft/team-page
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/team-page)
$ git log --oneline -1
179be4c (HEAD -> ft/team-page, origin/ft/team-page, main, ft/contact-page) Add team page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/contact-page)
$ git cherry-pick 179be4c
On branch ft/contact-page
You are currently cherry-picking commit 179be4c.
  (all conflicts fixed: run "git cherry-pick --continue")
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git cherry-pick --skip'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/contact-page|CHERRY-PICKING)
$ git cherry-pick --skip

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/contact-page)
$ git status
On branch ft/contact-page
nothing to commit, working tree clean

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/contact-page)
$ touch contact.html
echo "<h1>Contact Us</h1>" > contact.html

git add contact.html
git commit -m "Add contact page"
git push -u origin ft/contact-page
warning: in the working copy of 'contact.html', LF will be replaced by CRLF the next time Git touches it
[ft/contact-page 7515c76] Add contact page
 1 file changed, 1 insertion(+)
 create mode 100644 contact.html
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 294 bytes | 147.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/ft/contact-page
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ git cherry-pick --skip
git status
error: no cherry-pick in progress
fatal: cherry-pick failed
On branch ft/faq-page
nothing to commit, working tree clean

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ touch faq.html
echo "<h1>Frequently Asked Questions</h1>" > faq.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ git add faq.html
git commit -m "Add FAQ page"
warning: in the working copy of 'faq.html', LF will be replaced by CRLF the next time Git touches it
[ft/faq-page fc30fff] Add FAQ page
 1 file changed, 1 insertion(+)
 create mode 100644 faq.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 308 bytes | 154.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/ft/faq-page
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ git revert 179be4c
[ft/faq-page aa6b320] Revert "Add team page"
 1 file changed, 1 deletion(-)
 delete mode 100644 team.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 277 bytes | 277.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/daniel7nrk/git-basis-ex.git
   fc30fff..aa6b320  ft/faq-page -> ft/faq-page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ git log --oneline --all --grep="team"
aa6b320 (HEAD -> ft/faq-page, origin/ft/faq-page) Revert "Add team page"
179be4c (origin/ft/team-page, main, ft/team-page) Add team page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ git push
Everything up-to-date

```

ex2

```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git pull origin main
From https://github.com/daniel7nrk/git-basis-ex
 * branch            main       -> FETCH_HEAD
Already up to date.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git add home.html
git commit -m "Update home page on main"
git push origin main
[main 48b62e0] Update home page on main
 1 file changed, 1 insertion(+), 1 deletion(-)
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 303 bytes | 151.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/daniel7nrk/git-basis-ex.git
   8e7c10c..48b62e0  main -> main

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout ft/home-page-redesign
error: Your local changes to the following files would be overwritten by checkout:
        home.html
Please commit your changes or stash them before you switch branches.
Aborting

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/home-page-redesign)
$ git add home.html
git commit -m "Redesign home page"
[ft/home-page-redesign 2ca5370] Redesign home page
 1 file changed, 2 insertions(+), 1 deletion(-)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/home-page-redesign)
$ git push -u origin ft/home-page-redesign
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 8 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (11/11), 1.05 KiB | 179.00 KiB/s, done.
Total 11 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/ft/home-page-redesign
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/home-page-redesign)
$ git checkout ft/faq-page
git checkout -b ft/home-page-redesign
git checkout main
git pull origin main
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.
fatal: a branch named 'ft/home-page-redesign' already exists
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
From https://github.com/daniel7nrk/git-basis-ex
 * branch            main       -> FETCH_HEAD
Already up to date.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ 
```

## Bundle 4 
Exercise 1.
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git remote -v
origin  https://github.com/daniel7nrk/git-basis-ex.git (fetch)
origin  https://github.com/daniel7nrk/git-basis-ex.git (push)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git remote add git-copy https://github.com/daniel7nrk/git-basis-copy.git

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git remote -v
git-copy        https://github.com/daniel7nrk/git-basis-copy.git (fetch)
git-copy        https://github.com/daniel7nrk/git-basis-copy.git (push)
origin  https://github.com/daniel7nrk/git-basis-ex.git (fetch)
origin  https://github.com/daniel7nrk/git-basis-ex.git (push)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git add home.html
git commit -m "Update home page"
[main d8c9ce1] Update home page
 1 file changed, 1 insertion(+), 1 deletion(-)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 304 bytes | 152.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/daniel7nrk/git-basis-ex.git
   48b62e0..d8c9ce1  main -> main

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git push -u git-copy main
Enumerating objects: 32, done.
Counting objects: 100% (32/32), done.
Delta compression using up to 8 threads
Compressing objects: 100% (21/21), done.
Writing objects: 100% (32/32), 4.29 KiB | 231.00 KiB/s, done.
Total 32 (delta 8), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (8/8), done.
To https://github.com/daniel7nrk/git-basis-copy.git
 * [new branch]      main -> main
branch 'main' set up to track 'git-copy/main'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git remote -v
git-copy        https://github.com/daniel7nrk/git-basis-copy.git (fetch)
git-copy        https://github.com/daniel7nrk/git-basis-copy.git (push)
origin  https://github.com/daniel7nrk/git-basis-ex.git (fetch)
origin  https://github.com/daniel7nrk/git-basis-ex.git (push)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git branch -vv
  dev                   8e0d0e5 Add home and about pages
  ft/bundle-2           a54d9bf [origin/ft/bundle-2] Add services page
  ft/contact-page       7515c76 [origin/ft/contact-page] Add contact page
  ft/faq-page           aa6b320 [origin/ft/faq-page] Revert "Add team page"
  ft/home-page-redesign 2ca5370 [origin/ft/home-page-redesign] Redesign home page
  ft/service-redesign   d78fc1b [origin/ft/service-redesign] Redesign services page heading
  ft/team-page          179be4c [origin/ft/team-page] Add team page
* main                  d8c9ce1 [git-copy/main] Update home page

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ 
```
exercise 2
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/footer)
$ echo "<footer>Copyright 2026</footer>" > footer.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/footer)
$ git add footer.html
git commit -m "Add footer section"
warning: in the working copy of 'footer.html', LF will be replaced by CRLF the next time Git touches it
[ft/footer 7a0f8aa] Add footer section
 1 file changed, 1 insertion(+)
 create mode 100644 footer.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/footer)
$ echo "<p>All rights reserved</p>" >> footer.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/footer)
$ git add footer.html
git commit -m "Update footer section"
warning: in the working copy of 'footer.html', LF will be replaced by CRLF the next time Git touches it
[ft/footer 0957435] Update footer section
 1 file changed, 1 insertion(+)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/footer)
$ git push -u origin ft/footer
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 603 bytes | 201.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/ft/footer
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/footer)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'git-copy/main'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git merge --squash ft/footer
Updating d8c9ce1..0957435
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 2 ++
 1 file changed, 2 insertions(+)
 create mode 100644 footer.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git commit -m "footer changes squashing"
[main f870aa8] footer changes squashing
 1 file changed, 2 insertions(+)
 create mode 100644 footer.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git push -u origin ft/squashing
error: src refspec ft/squashing does not match any
error: failed to push some refs to 'https://github.com/daniel7nrk/git-basis-ex.git'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git push -u origin ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
Everything up-to-date

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout main
Already on 'main'
Your branch is ahead of 'git-copy/main' by 1 commit.
  (use "git push" to publish your local commits)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/squashing)
$ git merge --squash ft/footer
Squash commit -- not updating HEAD
Automatic merge went well; stopped before committing as requested

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/squashing)
$ git commit -m "footer changes squashing"
On branch ft/squashing
nothing to commit, working tree clean

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/squashing)
$ git push -u origin ft/squashing
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 331 bytes | 165.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-basis-ex/pull/new/ft/squashing
remote: 
To https://github.com/daniel7nrk/git-basis-ex.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/squashing)
$ git log --oneline -5
f870aa8 (HEAD -> ft/squashing, origin/ft/squashing, main) footer changes squashing
d8c9ce1 (origin/main, origin/HEAD, git-copy/main, git-copy/HEAD) Update home page
48b62e0 Update home page on main
179be4c (origin/ft/team-page, ft/team-page) Add team page
8e7c10c message: Update services.html title

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/squashing)
$ git log --oneline -5
f870aa8 (HEAD -> ft/squashing, origin/ft/squashing, main) footer changes squashing
d8c9ce1 (origin/main, origin/HEAD, git-copy/main, git-copy/HEAD) Update home page
48b62e0 Update home page on main
179be4c (origin/ft/team-page, ft/team-page) Add team page
8e7c10c message: Update services.html title

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-exe-basic (ft/squashing)
$ 
```
## Bundle 5
# ex 1 
# ex 2
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (main)
$ git add ./

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html


IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (main)
$ git commit -m "Update welcome message"
[main a1883d8] Update welcome message
 1 file changed, 1 insertion(+), 1 deletion(-)

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 328 bytes | 328.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/daniel7nrk/git-cafe-exercise.git
   d1d3f9c..a1883d8  main -> main
```

## bundle 6
# ex 1
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (main)
$ git checkout -b feature/menu-page
Switched to a new branch 'feature/menu-page'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (feature/menu-page)
$ touch menu.html

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (feature/menu-page)
$ git add .
git commit -m "Add menu page"
git push -u origin feature/menu-page
[feature/menu-page cd1560d] Add menu page
 1 file changed, 12 insertions(+)
 create mode 100644 menu.html
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 462 bytes | 231.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'feature/menu-page' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-cafe-exercise/pull/new/feature/menu-page
remote: 
To https://github.com/daniel7nrk/git-cafe-exercise.git
 * [new branch]      feature/menu-page -> feature/menu-page
branch 'feature/menu-page' set up to track 'origin/feature/menu-page'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (feature/menu-page)
$ 
``` 
# ex2 
```bash 
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (main)
$ git checkout -b bugfix/contact-title
Switched to a new branch 'bugfix/contact-title'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (bugfix/contact-title)
$ git add index-4.html
git commit -m "Fix contact page title"
git push -u origin bugfix/contact-title
[bugfix/contact-title a50e5f7] Fix contact page title
 1 file changed, 1 insertion(+), 1 deletion(-)
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 311 bytes | 311.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'bugfix/contact-title' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-cafe-exercise/pull/new/bugfix/contact-title
remote: 
To https://github.com/daniel7nrk/git-cafe-exercise.git
 * [new branch]      bugfix/contact-title -> bugfix/contact-title
branch 'bugfix/contact-title' set up to track 'origin/bugfix/contact-title'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (bugfix/contact-title)
$ 
```

# ex 3
```bash
IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (bugfix/contact-title)
$ git checkout main
git pull origin main

git checkout -b hotfix/contact-phone
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
From https://github.com/daniel7nrk/git-cafe-exercise
 * branch            main       -> FETCH_HEAD
Already up to date.
Switched to a new branch 'hotfix/contact-phone'

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (hotfix/contact-phone)
$ git add index-4.html
git commit -m "Fix contact phone number"
git push -u origin hotfix/contact-phone
[hotfix/contact-phone 559fb1c] Fix contact phone number
 1 file changed, 1 insertion(+), 1 deletion(-)
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 307 bytes | 153.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'hotfix/contact-phone' on GitHub by visiting:
remote:      https://github.com/daniel7nrk/git-cafe-exercise/pull/new/hotfix/contact-phone
remote: 
To https://github.com/daniel7nrk/git-cafe-exercise.git
 * [new branch]      hotfix/contact-phone -> hotfix/contact-phone
branch 'hotfix/contact-phone' set up to track 'origin/hotfix/contact-phone'.

IFAK@Daniel-Ngaruka MINGW64 ~/Desktop/git-cafe-exercise/git-cafe-exercise (hotfix/contact-phone)
$ 
```
