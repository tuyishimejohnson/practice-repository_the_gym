# practice-repository_the_gym



yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -HEAD~2
error: unknown switch `H'
usage: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
   or: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase>] --root [<branch>]
   or: git rebase --continue | --abort | --skip | --edit-todo

    --[no-]onto <revision>
                          rebase onto given branch instead of upstream
    --[no-]keep-base      use the merge-base of upstream and branch as the current base
    --no-verify           allow pre-rebase hook to run
    --verify              opposite of --no-verify
    -q, --[no-]quiet      be quiet. implies --no-stat
    -v, --[no-]verbose    display a diffstat of what changed upstream
    -n, --no-stat         do not show diffstat of what changed upstream
    --stat                opposite of --no-stat
    --[no-]signoff        add a Signed-off-by trailer to each commit
    --[no-]committer-date-is-author-date
                          make committer date match author date
    --[no-]reset-author-date
                          ignore author date and use current date
    -C <n>                passed to 'git apply'
    --[no-]ignore-whitespace
                          ignore changes in whitespace
    --[no-]whitespace <action>
                          passed to 'git apply'
    -f, --[no-]force-rebase
                          cherry-pick all commits, even if unchanged
    --no-ff               cherry-pick all commits, even if unchanged
    --ff                  opposite of --no-ff
    --continue            continue
    --skip                skip current patch and continue
    --abort               abort and check out the original branch
    --quit                abort but keep HEAD where it is
    --edit-todo           edit the todo list during an interactive rebase
    --show-current-patch  show the patch file being applied or merged
    --apply               use apply strategies to rebase
    -m, --merge           use merging strategies to rebase
    -i, --interactive     let the user edit the list of commits to rebase
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible
    --empty (drop|keep|stop)
                          how to handle commits that become empty
    --[no-]autosquash     move commits that begin with squash!/fixup! under -i
    --[no-]update-refs    update branches that point to commits that are being rebased
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG-sign commits
    --[no-]autostash      automatically stash/stash pop before and after
    -x, --[no-]exec <exec>
                          add exec lines after each commit of the editable list
    -r, --[no-]rebase-merges[=<mode>]
                          try to rebase merges instead of skipping them
    --[no-]fork-point     use 'merge-base --fork-point' to refine upstream
    -s, --[no-]strategy <strategy>
                          use the given merge strategy
    -X, --[no-]strategy-option <option>
                          pass the argument through to the merge strategy
    --[no-]root           rebase all reachable commits up to the root(s)
    --[no-]reschedule-failed-exec
                          automatically re-schedule any `exec` that fails
    --[no-]reapply-cherry-picks
                          apply all changes, even those already present upstream


yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~2
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git add .

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~2
error: cannot rebase: Your index contains uncommitted changes.
error: Please commit or stash them.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log 
commit 509361b1a9c5bef317a2f59b60a44db21eddf0b5 (HEAD -> main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Mon May 20 18:09:28 2024 +0200

    Readme

commit 3cd5ebd91c912e33b3a64c1d2b9c9ae89f4e0fcf
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Mon May 20 17:37:16 2024 +0200

    Test 2

commit 355243be3c603610b90ad574283ccc60ecec8b07
Author: tuyishime johnson <j.tuyishime4@alustudent.com>

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~3
error: cannot rebase: Your index contains uncommitted changes.
error: Please commit or stash them.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git stash
Saved working directory and index state WIP on main: 509361b Readme

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git stash pop
On branch main
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
pick 3cd5ebd Test 2

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (f6236d2856011a507c66c0374dc4d12177b176b7)

pick 355243b chore: Create second file
yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git add README.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
pick 9478a9a chore: Create initial file
chore: Create initial file
$ git commit -m "Outputs from git commands"
[main a02dc0a] Outputs from git commands
 1 file changed, 173 insertions(+), 1 deletion(-)

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~3
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~4
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~6
[detached HEAD 43e3c11] chore: Create initial file
 Date: Mon May 20 17:35:11 2024 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 firstFile.html
 create mode 100644 test1.md
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log
commit 428d26891c4e25b1a7fdb710942b4c9a26db2e6e (HEAD -> main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 11:08:55 2024 +0200

    Outputs from git commands

commit a82985d6f89596286b4cbfb3eb816ca137b969d1
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Mon May 20 18:09:28 2024 +0200

    Readme

commit 980b33b9e144d83673f3e9d7f462b98fcc19830a
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Mon May 20 17:37:16 2024 +0200

    Test 2

commit cf9a0e5eee74b4705f0e8fec95f1efe06644af16
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Mon May 20 17:36:37 2024 +0200

    chore: Create second file

commit 43e3c1116459fd85fd0caeca9119949cd231b47c
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Mon May 20 17:35:11 2024 +0200

    chore: Create initial file

    chore: Create another file

    Combination of two commits

commit 08dce5b711a664d342976ed262354f02c36dfb61 (origin/main, origin/HEAD)
Author: Tuyishime Noe Johnson <116555479+tuyishimejohnson@users.noreply.github.com>
Date:   Mon May 20 17:24:00 2024 +0200

    Initial commit

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$


yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~1
Successfully rebased and updated refs/heads/main.

pick eaa2c1e chore: Create third and fourth files
yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~1
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 6 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~1
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git reset HEAD~
Unstaged changes after reset:
M       README.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test3.md
        test4.md

no changes added to commit (use "git add" and/or "git commit -a")

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git add test3.md 

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log
commit 428d26891c4e25b1a7fdb710942b4c9a26db2e6e (HEAD -> main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 11:08:55 2024 +0200

    Outputs from git commands

commit a82985d6f89596286b4cbfb3eb816ca137b969d1
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Mon May 20 18:09:28 2024 +0200

    Readme

commit 980b33b9e144d83673f3e9d7f462b98fcc19830a
Author: tuyishime johnson <j.tuyishime4@alustudent.com>

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git commit -m "Create Third File"
[main 68e0b3f] Create Third File
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git add test4.md 

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git commit -m "Create fourth file"
[main 0e3df41] Create fourth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log
commit 0e3df4180503b1f137ba4e4e2aa9b6ce181f558e (HEAD -> main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 12:23:44 2024 +0200

    Create fourth file

commit 68e0b3f9ceeb2ec17f006c782829234c8080f7db
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 12:23:09 2024 +0200

    Create Third File

commit 428d26891c4e25b1a7fdb710942b4c9a26db2e6e
Author: tuyishime johnson <j.tuyishime4@alustudent.com>

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 7 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase --HEAD~4
error: unknown option `HEAD~4'
usage: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
   or: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase>] --root [<branch>]
   or: git rebase --continue | --abort | --skip | --edit-todo

    --[no-]onto <revision>
                          rebase onto given branch instead of upstream
    --[no-]keep-base      use the merge-base of upstream and branch as the current base
    --no-verify           allow pre-rebase hook to run
    --verify              opposite of --no-verify
    -q, --[no-]quiet      be quiet. implies --no-stat
    -v, --[no-]verbose    display a diffstat of what changed upstream
    -n, --no-stat         do not show diffstat of what changed upstream
    --stat                opposite of --no-stat
    --[no-]signoff        add a Signed-off-by trailer to each commit
    --[no-]committer-date-is-author-date
                          make committer date match author date
    --[no-]reset-author-date
                          ignore author date and use current date
    -C <n>                passed to 'git apply'
    --[no-]ignore-whitespace
                          ignore changes in whitespace
    --[no-]whitespace <action>
                          passed to 'git apply'
    -f, --[no-]force-rebase
                          cherry-pick all commits, even if unchanged
    --no-ff               cherry-pick all commits, even if unchanged
    --ff                  opposite of --no-ff
    --continue            continue
    --skip                skip current patch and continue
    --abort               abort and check out the original branch
    --quit                abort but keep HEAD where it is
    --edit-todo           edit the todo list during an interactive rebase
    --show-current-patch  show the patch file being applied or merged
    --apply               use apply strategies to rebase
    -m, --merge           use merging strategies to rebase
    -i, --interactive     let the user edit the list of commits to rebase
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible
    --empty (drop|keep|stop)
                          how to handle commits that become empty
    --[no-]autosquash     move commits that begin with squash!/fixup! under -i
    --[no-]update-refs    update branches that point to commits that are being rebased
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG-sign commits
    --[no-]autostash      automatically stash/stash pop before and after
    -x, --[no-]exec <exec>
                          add exec lines after each commit of the editable list
    -r, --[no-]rebase-merges[=<mode>]
                          try to rebase merges instead of skipping them
    --[no-]fork-point     use 'merge-base --fork-point' to refine upstream
    -s, --[no-]strategy <strategy>
                          use the given merge strategy
    -X, --[no-]strategy-option <option>
                          pass the argument through to the merge strategy
    --[no-]root           rebase all reachable commits up to the root(s)
    --[no-]reschedule-failed-exec
                          automatically re-schedule any `exec` that fails
    --[no-]reapply-cherry-picks
                          apply all changes, even those already present upstream


yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
pick 43e3c11 chore: Create initial file
$ git rebase -i HEAD~4
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.

pick 0e3df41 Create fourth file
yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git add README.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
pick 428d268 Outputs from git commands
$ git commit -m "Readme changes"
[main db47b24] Readme changes
 1 file changed, 128 insertions(+), 109 deletions(-)

pick 68e0b3f Create Third File
# This is a combination of 2 commits.
yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~4
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~3
[detached HEAD c247a26] Create Third File
 Date: Tue May 21 12:23:09 2024 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ ls
firstFile.css  firstFile.html  README.md  test1.md  test2.md  test3.md  test4.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log
commit bd5a1250a546db20e0bf46d0f070f30e5f96f339 (HEAD -> main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 12:28:22 2024 +0200

    Readme changes

commit c247a265eaa1e29ae81c81eccb6f7bc288bb2326
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 12:23:09 2024 +0200

    Create Third File

    Create fourth file


yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$



yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~4
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~3
[detached HEAD c247a26] Create Third File
 Date: Tue May 21 12:23:09 2024 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ ls
firstFile.css  firstFile.html  README.md  test1.md  test2.md  test3.md  test4.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log
commit bd5a1250a546db20e0bf46d0f070f30e5f96f339 (HEAD -> main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 12:28:22 2024 +0200

    Readme changes

commit c247a265eaa1e29ae81c81eccb6f7bc288bb2326
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 12:23:09 2024 +0200

    Create Third File

    Create fourth file


yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ touch unwanted.txt

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git add unwanted.txt 

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git commit -m "Unwanted commit"
[main dd75969] Unwanted commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 unwanted.txt

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log
commit dd75969af560f652356008c6ebc5279d3696d4eb (HEAD -> main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 12:39:03 2024 +0200

    Unwanted commit

commit bd5a1250a546db20e0bf46d0f070f30e5f96f339
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 12:28:22 2024 +0200

    Readme changes

commit c247a265eaa1e29ae81c81eccb6f7bc288bb2326
Author: tuyishime johnson <j.tuyishime4@alustudent.com>

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
pick eeb289f Readme changes
$ git rebase -i HEAD~
error: cannot rebase: You have unstaged changes.
error: Please commit or stash them.

pick bd5a125 Readme changes
yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git add README.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git commit -m "Readme changes"
[main eeb289f] Readme changes
 1 file changed, 237 insertions(+)

pick c247a26 Create Third File
yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~
Successfully rebased and updated refs/heads/main.

pick 980b33b Test 2
yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~3
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ ls
firstFile.css  firstFile.html  README.md  test1.md  test2.md  test3.md  test4.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~3
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git rebase -i HEAD~6
Successfully rebased and updated refs/heads/main.

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ ls 
firstFile.css  firstFile.html  README.md  test1.md  test2.md  test3.md  test4.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git branch
* main

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git branch ft/branch

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git branch
  ft/branch
* main

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git checkout ft/branch 
Switched to branch 'ft/branch'

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (ft/branch)
$ touch test5.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (ft/branch)
$ git add test5.md 

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (ft/branch)
$ git commit -m "Implemented test 5"
[ft/branch b547548] Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (ft/branch)
$ git log
commit b5475484d4a8e7262f5b0e5a136161672005d42c (HEAD -> ft/branch)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 22:17:40 2024 +0200

    Implemented test 5

commit 77707846e5e278f6c1e17f983652ce98aa0f8e0a (main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (ft/branch)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 8 commits.
  (use "git push" to publish your local commits)

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git cherry-pick b547548
[main 7121736] Implemented test 5
 Date: Tue May 21 22:17:40 2024 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log
commit 7121736898629b3afbfae6ee55121458e964c71a (HEAD -> main)
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 22:17:40 2024 +0200

    Implemented test 5

commit 77707846e5e278f6c1e17f983652ce98aa0f8e0a
Author: tuyishime johnson <j.tuyishime4@alustudent.com>

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log --graph
* commit 7121736898629b3afbfae6ee55121458e964c71a (HEAD -> main)
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Tue May 21 22:17:40 2024 +0200
|
|     Implemented test 5
|
* commit 77707846e5e278f6c1e17f983652ce98aa0f8e0a
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Tue May 21 12:42:51 2024 +0200
|
|     Readme changes
|
* commit bd5a1250a546db20e0bf46d0f070f30e5f96f339
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Tue May 21 12:28:22 2024 +0200
|
|     Readme changes
|
* commit c247a265eaa1e29ae81c81eccb6f7bc288bb2326
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Tue May 21 12:23:09 2024 +0200
|
|     Create Third File
|
|     Create fourth file
|
* commit 428d26891c4e25b1a7fdb710942b4c9a26db2e6e
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Tue May 21 11:08:55 2024 +0200
|
|     Outputs from git commands
|
* commit a82985d6f89596286b4cbfb3eb816ca137b969d1
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Mon May 20 18:09:28 2024 +0200
|
|     Readme
|
* commit 980b33b9e144d83673f3e9d7f462b98fcc19830a
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Mon May 20 17:37:16 2024 +0200
|
|     Test 2
|
* commit cf9a0e5eee74b4705f0e8fec95f1efe06644af16
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Mon May 20 17:36:37 2024 +0200
|
|     chore: Create second file
|
* commit 43e3c1116459fd85fd0caeca9119949cd231b47c
| Author: tuyishime johnson <j.tuyishime4@alustudent.com>
| Date:   Mon May 20 17:35:11 2024 +0200
|
|     chore: Create initial file
|
|     chore: Create another file
|
|     Combination of two commits
|
* commit 08dce5b711a664d342976ed262354f02c36dfb61 (origin/main, origin/HEAD)
  Author: Tuyishime Noe Johnson <116555479+tuyishimejohnson@users.noreply.github.com>
  Date:   Mon May 20 17:24:00 2024 +0200

      Initial commit

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git checkout -b ft/new-feature
Switched to a new branch 'ft/new-feature'

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (ft/new-feature)
$


yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git branch
  ft/branch
  ft/new-branch-from-commit
* main

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git branch -m ft/new-branch-from-commit ft/improved-branch-name

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git branch
  ft/branch
  ft/improved-branch-name
* main

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log --oneline
2abefda (HEAD -> main, ft/improved-branch-name) Merge branch 'ft/new-feature'
f4117a4 Updated project readme
05eff70 Implemented core functionality for new feature
7121736 Implemented test 5
7770784 Readme changes
bd5a125 Readme changes
c247a26 Create Third File
428d268 Outputs from git commands
a82985d Readme
980b33b Test 2
cf9a0e5 chore: Create second file
43e3c11 chore: Create initial file
08dce5b (origin/main, origin/HEAD) Initial commit

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git log
commit 2abefdac4308bd18db440a4f6a72710d0e55d1d6 (HEAD -> main, ft/improved-branch-name)
Merge: f4117a4 05eff70
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 22:51:53 2024 +0200

    Merge branch 'ft/new-feature'

commit f4117a44ef3ef7ee4da23037862ea2580cbc7c3e
Author: tuyishime johnson <j.tuyishime4@alustudent.com>
Date:   Tue May 21 22:44:48 2024 +0200

    Updated project readme

commit 05eff70590e70a2adf7530da475678afa5c9d65e

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$ git checkout 2abefda
M       README.md
M       readme.txt
Note: switching to '2abefda'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 2abefda Merge branch 'ft/new-feature'

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym ((2abefda...))
$

$ git tag v1.0 f4117a4
fatal: tag 'v1.0' already exists

yiish@DESKTOP-MFHFU23 MINGW64 ~/Documents/MYPROJECTS/practice-repository_the_gym (main)
$