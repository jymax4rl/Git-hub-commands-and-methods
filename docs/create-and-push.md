# Quick: Create a GitHub repo and push local project

1. Create a new repository on GitHub (use the web UI).
   - Name it e.g. `github-commands-cheatsheet`.

2. Locally (from your project folder)
```bash
git init
git add .
git commit -m "Initial commit"
# set your branch name to main (or master if you prefer)
git branch -M main
# add remote (replace with your repo URL)
git remote add origin https://github.com/<your-username>/github-commands-cheatsheet.git
# push and set upstream
git push --set-upstream origin main or git push -u origin main
    
```

Notes
- If your local branch is named master and you want main: `git branch -M main`
- If GitHub gives you instructions after creating the repo, follow the commands they show (they match the steps above).
- If push fails with authentication error on HTTPS, either:
  - configure a Personal Access Token (PAT) and use it for HTTPS, or
  - set up SSH keys and push using the SSH URL.

Optional: set up the GitHub CLI and create PRs from the command line:
```bash
# install and authenticate gh
gh auth login
# create a pull request from current branch
gh pr create --title "My change" --body "What I changed" --base main
```