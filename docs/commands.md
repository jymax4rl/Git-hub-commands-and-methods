# Git & GitHub Quick Commands Cheat-sheet

This file gives short, copy-pastable commands and short explanations. Use it while working locally.

Basics — local repo
```bash
# initialize a repo
git init

# check status
git status

# see commits log
git log --oneline --graph --decorate --all
```

Staging & committing
```bash
git add file.txt           # stage a file
git add .                  # stage all changes
git commit -m "Short message explaining change"
git commit --amend         # amend last commit (careful if already pushed)
```

Branching & switching
```bash
git branch                 # list local branches
git branch -a              # list local + remote branches
git checkout -b feature/x  # create and switch to feature branch
git switch feature/x       # newer switch command
git switch -c feature/x    # create and switch
git merge main             # merge main into current branch or merge current into main from main
```

Remotes & pushing
```bash
# add remote (only once)
git remote add origin https://github.com/<user>/<repo>.git

# check remotes
git remote -v

# push current branch and set upstream
git push --set-upstream origin feature/x
# subsequent pushes:
git push

# push main (if branch is main)
git push --set-upstream origin main
```

Cloning
```bash
git clone https://github.com/<user>/<repo>.git
# or with SSH
git clone git@github.com:<user>/<repo>.git
```

Pulling & fetching
```bash
git fetch origin                # fetch updates (no merge)
git pull origin main            # fetch + merge remote main into local main
git pull --rebase origin main   # pull with rebase to keep linear history
```

Undo & reset (use with caution)
```bash
git restore file.txt            # undo unstaged changes in working tree (git >= 2.23)
git checkout -- file.txt        # older form to discard local changes
git reset HEAD file.txt         # unstage a staged file
git reset --soft HEAD~1         # move HEAD back one commit, keep changes staged
git reset --hard HEAD~1         # destroy last commit and working changes (dangerous)
```

Revert (safe for published commits)
```bash
git revert <commit>             # create a new commit that undoes <commit>
```

Stash (temporary save)
```bash
git stash                       # save working changes
git stash list
git stash apply                 # reapply most recent stash (keeps stash)
git stash pop                   # reapply and remove stash
```

Tags
```bash
git tag v1.0.0
git push origin v1.0.0
```

Common patterns / PR workflow
1. git checkout -b feature/short-descriptive-name
2. make commits (small & focused)
3. git push --set-upstream origin feature/short-descriptive-name
4. Open a Pull Request on GitHub from the branch → main (or develop)
5. Address review comments, push additional commits
6. Merge using GitHub UI (Squash & merge / Rebase & merge / Create merge commit)
7. git pull origin main locally to update main

Handling remotes & upstream differences
```bash
# rename remote or fix URL
git remote set-url origin git@github.com:<user>/<repo>.git

# remove a remote
git remote remove origin
```

Working with forks
- Fork a repo on GitHub, then:
```bash
git clone git@github.com:<you>/<fork>.git
git remote add upstream git@github.com:<original-owner>/<repo>.git
git fetch upstream
git merge upstream/main
# or rebase:
git rebase upstream/main
```

GitHub-specific (web + gh CLI)
- Create PR using GitHub web UI or use gh CLI:
```bash
# create a PR from your branch (gh CLI)
gh pr create --title "My feature" --body "Describe changes" --base main
# checkout PR locally
gh pr checkout 123
```

Safety tips & best practices
- Make small, focused commits with meaningful messages.
- Use feature branches and PRs for review and history.
- Use .gitignore to avoid committing credentials.
- When collaborating, prefer pull + rebase workflow or agreed-upon merge strategy.
- Use `git status` often.

Troubleshooting
- "fatal: repository not found" -> check remote URL and GitHub repo exists / access rights.
- "The current branch X has no upstream branch" -> use git push --set-upstream origin X
- Authentication issues -> update credentials or use SSH keys / personal access tokens (PAT) for HTTPS.

Further reading
- Pro Git book: https://git-scm.com/book/en/v2
- GitHub Docs: https://docs.github.com/en