# git-base: Esame pratico

Si richiede di creare un fork del presente progetto.

Dovranno poi essere eseguite le seguenti operazioni:

* Staccare il branch exam a partire dal branch develop.
* Modificare il file commedia/canto1.md modificando la prima riga con il testo "Provando a imparar a usar lo Git"
* Comittare la modifica
* Pushare la modifica
* Mergiare il branch exam su master
* Risolvere eventuali conflitti in modo che sul branch master locale sia presente il testo inserito al punto 2
* Pushare su master.

Riportare i comandi git usati sul file onenote dell'esame insieme all'url del repository creato

************
LOG COMPLETO
************

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git
$ git clone https://github.com/christiansanfi/git-base-exam.git
Cloning into 'git-base-exam'...
remote: Enumerating objects: 20, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 20 (delta 3), reused 2 (delta 2), pack-reused 15 (from 1)
Receiving objects: 100% (20/20), 7.10 KiB | 3.55 MiB/s, done.
Resolving deltas: 100% (3/3), done.

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git
$ git init
Initialized empty Git repository in C:/Users/sanch/OneDrive/Desktop/Lavoro/Esame git/.git/

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git (master)
$ cd git-base-exam/

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam (master)
$ git log
commit a33de0a814b61d416809a3838a4ce6f25a6f7989 (HEAD -> master, origin/master, origin/HEAD)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:17:49 2021 +0100

    Update canto1.md

commit 6ce703891cfc55ccddd6344bf9d1cc1a64f438ea (origin/develop)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:15:44 2021 +0100

    Update README.md

commit 3a7ca6778a0fb9f3c11c6cc3bd84caed1927369c
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:12:26 2021 +0100

    Create canto1.md

commit 65e2d99dffdba559733f31ccf2204395449ced38
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:05:30 2021 +0100

    Update README.md

commit 220c84bb4ce9b27ca99628d863c4bc8db258cef7
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:03:30 2021 +0100

    Update README.md

commit 17008f53f36acf324ecf84da151cd50cc4ef3286
Author: Grimstack <gabry.grillo@alice.it>
Date:   Wed Nov 3 15:55:23 2021 +0100

    Initial commit

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam (master)
$ git checkout -b develop origin/develop
Switched to a new branch 'develop'
branch 'develop' set up to track 'origin/develop'.

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam (develop)
$ git log
commit 6ce703891cfc55ccddd6344bf9d1cc1a64f438ea (HEAD -> develop, origin/develop)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:15:44 2021 +0100

    Update README.md

commit 3a7ca6778a0fb9f3c11c6cc3bd84caed1927369c
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:12:26 2021 +0100

    Create canto1.md

commit 65e2d99dffdba559733f31ccf2204395449ced38
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:05:30 2021 +0100

    Update README.md

commit 220c84bb4ce9b27ca99628d863c4bc8db258cef7
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:03:30 2021 +0100

    Update README.md

commit 17008f53f36acf324ecf84da151cd50cc4ef3286
Author: Grimstack <gabry.grillo@alice.it>
Date:   Wed Nov 3 15:55:23 2021 +0100

    Initial commit

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam (develop)
$ git checkout -b exam
Switched to a new branch 'exam'

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam (exam)
$ git branch
  develop
* exam
  master

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam (exam)
$ ls
README.md  commedia/

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam (exam)
$ cd commedia

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ ls
canto1.md

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ nano canto1.md

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git status
On branch exam
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   canto1.md

no changes added to commit (use "git add" and/or "git commit -a")

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git add canto1.md

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git status
On branch exam
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   canto1.md


sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git commit -m Edit first canto1.md row
error: pathspec 'first' did not match any file(s) known to git
error: pathspec 'row' did not match any file(s) known to git

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git commit -m "Edit first canto1.md row"
[exam 0d8d5c4] Edit first canto1.md row
 1 file changed, 1 insertion(+), 1 deletion(-)

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git status
On branch exam
nothing to commit, working tree clean

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git log
commit 0d8d5c4258b76d8c9153367572a82b58109e16b5 (HEAD -> exam)
Author: Christian Sanfilippo <san.chri@tutanota.com>
Date:   Thu Aug 29 11:41:51 2024 +0200

    Edit first canto1.md row

commit 6ce703891cfc55ccddd6344bf9d1cc1a64f438ea (origin/develop, develop)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:15:44 2021 +0100

    Update README.md

commit 3a7ca6778a0fb9f3c11c6cc3bd84caed1927369c
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:12:26 2021 +0100

    Create canto1.md

commit 65e2d99dffdba559733f31ccf2204395449ced38
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:05:30 2021 +0100

    Update README.md

commit 220c84bb4ce9b27ca99628d863c4bc8db258cef7
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:03:30 2021 +0100

    Update README.md

commit 17008f53f36acf324ecf84da151cd50cc4ef3286
Author: Grimstack <gabry.grillo@alice.it>
Date:   Wed Nov 3 15:55:23 2021 +0100

    Initial commit

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git push origin exam
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 401 bytes | 401.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'exam' on GitHub by visiting:
remote:      https://github.com/christiansanfi/git-base-exam/pull/new/exam
remote:
To https://github.com/christiansanfi/git-base-exam.git
 * [new branch]      exam -> exam

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git status
On branch exam
nothing to commit, working tree clean

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git log
commit 0d8d5c4258b76d8c9153367572a82b58109e16b5 (HEAD -> exam, origin/exam)
Author: Christian Sanfilippo <san.chri@tutanota.com>
Date:   Thu Aug 29 11:41:51 2024 +0200

    Edit first canto1.md row

commit 6ce703891cfc55ccddd6344bf9d1cc1a64f438ea (origin/develop, develop)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:15:44 2021 +0100

    Update README.md

commit 3a7ca6778a0fb9f3c11c6cc3bd84caed1927369c
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:12:26 2021 +0100

    Create canto1.md

commit 65e2d99dffdba559733f31ccf2204395449ced38
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:05:30 2021 +0100

    Update README.md

commit 220c84bb4ce9b27ca99628d863c4bc8db258cef7
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:03:30 2021 +0100

    Update README.md

commit 17008f53f36acf324ecf84da151cd50cc4ef3286
Author: Grimstack <gabry.grillo@alice.it>
Date:   Wed Nov 3 15:55:23 2021 +0100

    Initial commit

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git logh
git: 'logh' is not a git command. See 'git --help'.

The most similar command is
        log

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git log
commit a33de0a814b61d416809a3838a4ce6f25a6f7989 (HEAD -> master, origin/master, origin/HEAD)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:17:49 2021 +0100

    Update canto1.md

commit 6ce703891cfc55ccddd6344bf9d1cc1a64f438ea (origin/develop, develop)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:15:44 2021 +0100

    Update README.md

commit 3a7ca6778a0fb9f3c11c6cc3bd84caed1927369c
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:12:26 2021 +0100

    Create canto1.md

commit 65e2d99dffdba559733f31ccf2204395449ced38
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:05:30 2021 +0100

    Update README.md

commit 220c84bb4ce9b27ca99628d863c4bc8db258cef7
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:03:30 2021 +0100

    Update README.md

commit 17008f53f36acf324ecf84da151cd50cc4ef3286
Author: Grimstack <gabry.grillo@alice.it>
Date:   Wed Nov 3 15:55:23 2021 +0100

    Initial commit

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git checkout exam
Switched to branch 'exam'

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git log
commit 0d8d5c4258b76d8c9153367572a82b58109e16b5 (HEAD -> exam, origin/exam)
Author: Christian Sanfilippo <san.chri@tutanota.com>
Date:   Thu Aug 29 11:41:51 2024 +0200

    Edit first canto1.md row

commit 6ce703891cfc55ccddd6344bf9d1cc1a64f438ea (origin/develop, develop)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:15:44 2021 +0100

    Update README.md

commit 3a7ca6778a0fb9f3c11c6cc3bd84caed1927369c
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:12:26 2021 +0100

    Create canto1.md

commit 65e2d99dffdba559733f31ccf2204395449ced38
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:05:30 2021 +0100

    Update README.md

commit 220c84bb4ce9b27ca99628d863c4bc8db258cef7
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:03:30 2021 +0100

    Update README.md

commit 17008f53f36acf324ecf84da151cd50cc4ef3286
Author: Grimstack <gabry.grillo@alice.it>
Date:   Wed Nov 3 15:55:23 2021 +0100

    Initial commit

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (exam)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git pull origin master
From https://github.com/christiansanfi/git-base-exam
 * branch            master     -> FETCH_HEAD
Already up to date.

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git log
commit a33de0a814b61d416809a3838a4ce6f25a6f7989 (HEAD -> master, origin/master, origin/HEAD)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:17:49 2021 +0100

    Update canto1.md

commit 6ce703891cfc55ccddd6344bf9d1cc1a64f438ea (origin/develop, develop)
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:15:44 2021 +0100

    Update README.md

commit 3a7ca6778a0fb9f3c11c6cc3bd84caed1927369c
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:12:26 2021 +0100

    Create canto1.md

commit 65e2d99dffdba559733f31ccf2204395449ced38
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:05:30 2021 +0100

    Update README.md

commit 220c84bb4ce9b27ca99628d863c4bc8db258cef7
Author: Grimstack <gabriele.grillo@aitho.it>
Date:   Wed Nov 3 16:03:30 2021 +0100

    Update README.md

commit 17008f53f36acf324ecf84da151cd50cc4ef3286
Author: Grimstack <gabry.grillo@alice.it>
Date:   Wed Nov 3 15:55:23 2021 +0100

    Initial commit

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git merge exam
Auto-merging commedia/canto1.md
CONFLICT (content): Merge conflict in commedia/canto1.md
Automatic merge failed; fix conflicts and then commit the result.

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master|MERGING)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   canto1.md

no changes added to commit (use "git add" and/or "git commit -a")

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master|MERGING)
$ nano canto1.md

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master|MERGING)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   canto1.md

no changes added to commit (use "git add" and/or "git commit -a")

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master|MERGING)
$ git add canto1.md

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master|MERGING)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   canto1.md


sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master|MERGING)
$ git commit
[master 2c8af9c] Merge branch 'exam'

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git push origin master
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 232 bytes | 232.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/christiansanfi/git-base-exam.git
   a33de0a..2c8af9c  master -> master

sanch@PChris MINGW64 ~/OneDrive/Desktop/Lavoro/Esame git/git-base-exam/commedia (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
