# Git Basics: A Step-by-Step Curriculum

---

## Module 1: Setup
**Goal:** Get Git configured and ready

1. Set your name and email:
   ```
   git config --global user.name "Your Name"
   git config --global user.email "you@email.com"
   ```
2. Verify your config: `git config --list`

---

## Module 2: Cloning a Repo
**Goal:** Get someone else's code onto your machine

1. Find a repo on GitHub (try a public one)
2. Clone it: `git clone https://github.com/username/repo.git`
3. Move into it: `cd repo-name`
4. Look around: `ls`, `git log --oneline`, `git status`

---

## Module 3: Understanding the Workflow
**Goal:** Know the 3 stages of Git

```
Working Directory → Staging Area → Repository
   (edit files)      (git add)     (git commit)
```

- `git status` — see what's changed
- `git diff` — see exactly what changed line by line

---

## Module 4: Making Changes
**Goal:** Edit a file and save that change to Git

1. Open and edit a file (README.md is a safe bet)
2. Check what changed: `git status` and `git diff`
3. Stage it: `git add README.md` (or `git add .` for everything)
4. Commit it: `git commit -m "describe what you changed"`
5. Check history: `git log --oneline`

---

## Module 5: Pushing Changes
**Goal:** Send your changes back to GitHub

1. Push: `git push origin main`
2. Visit the repo on GitHub and confirm your changes appear

---

## Module 6: Pulling Changes
**Goal:** Get the latest changes from GitHub

1. Pull: `git pull origin main`
2. Practice this when changes exist on GitHub that aren't on your machine (e.g., edit a file directly on GitHub, then pull it down)

---

## Module 7: Branching
**Goal:** Work on something without breaking main

1. Create a branch: `git checkout -b my-feature`
2. Make some changes and commit them
3. Switch back to main: `git checkout main`
4. Merge your branch: `git merge my-feature`
5. Delete the branch: `git branch -d my-feature`

---

## Module 8: Handling Conflicts
**Goal:** Understand what happens when two changes clash

1. Make a change to the same line in two branches
2. Try to merge — Git will flag a conflict
3. Open the file, look for `<<<<<<`, `=======`, `>>>>>>>`
4. Manually pick the right version, save
5. Stage and commit the resolved file

---

## Module 9: Forking & Pull Requests
**Goal:** Contribute to someone else's repo

1. Fork a repo on GitHub (creates your own copy)
2. Clone your fork locally
3. Make changes, commit, push to your fork
4. Open a Pull Request on GitHub to propose your changes

---

## Suggested Practice Order

| Lesson | Practice on CleverGolem |
|--------|------------------------|
| Module 2 | Clone your own repo fresh |
| Module 4 | Edit README, commit |
| Module 5 | Push to GitHub |
| Module 6 | Edit on GitHub.com, then `git pull` |
| Module 7 | Create a `dev` branch, make changes, merge |
| Module 8 | Intentionally create a conflict and resolve it |
| Module 9 | Fork a friend's repo and open a PR |
