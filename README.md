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