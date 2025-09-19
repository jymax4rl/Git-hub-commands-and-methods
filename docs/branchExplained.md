# Git Branch Explained

## What is a Branch?
A **branch** in Git is essentially a **pointer** to a specific commit in the history.  
It represents a separate line of development where you can make changes without affecting other parts of the project.

Think of it as a timeline of work.

---

## Why Use Branches?
Branches allow you to:
1. **Work on new features safely**  
   Experiment with new code without breaking the `main` branch.

2. **Collaborate with others**  
   Each developer can have their own branch and later merge changes into the main project.

3. **Switch contexts easily**  
   Work on multiple tasks by switching between branches.

---

## Visual Example

Imagine the commit history:

```
A -- B -- C   (main)
```

Now you create a new branch `feature-x` starting from `C`:

```
A -- B -- C   (main)
             \
              D -- E   (feature-x)
```

- `main` is still at commit `C`.
- `feature-x` has new commits `D` and `E`.

---

## Local vs Remote Branches
- **Local branch**: Exists only on your computer (e.g., `main`, `feature-x`).
- **Remote branch**: A branch on a remote repository (e.g., `origin/main`).  
  `origin` is the default name for the remote (often GitHub, GitLab, etc.).

---

## Useful Commands
### check which branch you’re currently working on
   ```bash
   git branch
   ```

### Create a new branch
```bash
git branch feature-x
```

### Switch to the new branch
```bash
git checkout feature-x
# Or the modern way
git switch feature-x
```

### Create AND switch in one command
```bash
git checkout -b feature-x
# Or
git switch -c feature-x
```

### Add changes and commit
```bash
git add .
git commit -m "Start working on feature-x"
```

### Push the new branch to remote
```bash
git push -u origin feature-x
```

Now your branch exists both locally and on the remote.

---

✅ **Summary**:  
A branch is a pointer to commits. Use branches to isolate work, collaborate, and keep `main` stable.
