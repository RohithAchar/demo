GIT CHEAT SHEET (PLAIN TEXT)

----------------------------
BASIC SETUP
----------------------------
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global --list

----------------------------
CREATE / CLONE
----------------------------
git init                     # initialize new repo
git clone <url>               # clone remote repo

----------------------------
STATUS & HISTORY
----------------------------
git status                   # working tree status
git log                      # commit history
git log --oneline --graph    # compact history

----------------------------
STAGING & COMMIT
----------------------------
git add <file>               # stage file
git add .                    # stage all
git commit -m "message"      # commit staged changes
git commit -am "message"     # stage tracked + commit

----------------------------
BRANCHING
----------------------------
git branch                   # list branches
git branch <name>            # create branch
git checkout <name>          # switch branch
git checkout -b <name>       # create + switch
git branch -d <name>         # delete branch

----------------------------
MERGING
----------------------------
git merge <branch>           # merge into current branch
git rebase <branch>          # rebase current branch

----------------------------
REMOTE
----------------------------
git remote -v                # list remotes
git remote add origin <url>  # add remote
git push origin <branch>     # push to remote
git pull origin <branch>     # fetch + merge
git fetch                    # download refs only

----------------------------
UNDO / FIX
----------------------------
git restore <file>           # discard working changes
git restore --staged <file>  # unstage file
git reset --soft HEAD~1      # undo commit, keep changes
git reset --hard HEAD~1      # undo commit, lose changes

----------------------------
STASH
----------------------------
git stash                    # save work temporarily
git stash list               # list stashes
git stash pop                # apply + remove stash

----------------------------
DIFF
----------------------------
git diff                     # working vs staged
git diff --staged            # staged vs last commit

----------------------------
TAGS
----------------------------
git tag                      # list tags
git tag v1.0                 # create tag
git push origin v1.0         # push tag

----------------------------
CLEAN
----------------------------
git clean -n                 # preview untracked removal
git clean -f                 # delete untracked files
