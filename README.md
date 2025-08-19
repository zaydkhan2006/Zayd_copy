# Github-Activity
# COMP301 Git Activity

Welcome to our collaborative Git exercise! In this activity, you will first work independently, then in pairs and teams, to practice branching, committing, resolving merge conflicts, and making pull requests.

---

## What You Will Learn

- Creating and pushing branches.  
- Making pull requests to a protected main branch.  
- Working with shared files in a team.  
- Encountering and resolving merge conflicts.  
- Organizing contributions from many people into one shared project.  

---


## Part 1: Individual Contribution (No Conflicts)

1. Clone this repository to your computer.
2. You will see folders for the morning section and the afternoon section.  Choose the appropriate folder to work in.
3. Create a new branch named `solo/<onyen>`. 
4. Now navigate to the `solo/` foldoer (unrelated to branch name).  Inside it, create a new text file named `<onyen>.txt`.  
5. Add your full name inside the file.  
6. Stage, commit, and push your branch to GitHub.  
7. Open a pull request from your branch to `main` with the title `solo: <onyen>`.  

Each student will have their own file, so there should be no conflicts in this step.

---

## Part 2: Pair and Team Contribution (Designed Conflicts)

1. Your group of 4–6 students is a **team**. Choose a unique team identifier (for example, `UNC-Alpha`, `Sharks`, `Team42`).  
2. One person in the team acts as **Integrator** and will create the team’s base branch `team/<team-id>/base`.  
3. The Integrator should create a new folder `teams/<team-id>/` and a file inside it called `roster.md`.  
   - The file should begin with:  
     `# Team <team-id> Roster (alphabetical by last name)`  
     followed by a line that says `Members:`.  
4. Within the team, split into pairs. Each pair creates their own branch from the base: `team/<team-id>/pair-<lastname1>-<lastname2>`.  
5. Each pair should edit the same line in `teams/<team-id>/roster.md`, directly under `Members:`.  
   - Add exactly one line with the format:  
     `<Name1> + <Name2> — Team name: <chosen team name>`  
   - Every pair must insert their line at the same place, so that conflicts are guaranteed.  
6. Commit and push your changes.  

---

## Part 3: Conflict Resolution and Integration

1. The Integrator should create a new branch `team/<team-id>/integration` from the base.  
2. Then, merge each pair branch into the integration branch, one by one.  
   - This will cause conflicts in the `roster.md` file.  
   - Resolve the conflicts by keeping only one `Members:` header, then making sure all lines are included.  
   - The final list of pairs must be in **alphabetical order by last name**.  
   - Each line must show both names and the team name.  
3. After all conflicts are resolved and merged, push the integration branch.  

---

## Part 4: Class Roster Pull Request

1. The Integrator should append the team’s final roster to the file `class-roster.md`.  
   - Add a section starting with `## <team-id>` followed by the list of pairs.  
2. Commit and push the update to the integration branch.  
3. Open a pull request from `team/<team-id>/integration` to `main` with the title `<team-id> → class-roster`.  

---

## Quick Reference (Commands in Alphabetical Order)

- `git add <file>` — stage changes to be committed.  
- `git checkout -b <new-branch>` — create and switch to a new branch.  
- `git checkout <branch>` — switch to an existing branch.  
- `git clean -fd` — remove untracked files and folders (use with caution).  
- `git clone <repo-url>` — clone the repository to your computer.  
- `git commit -m "<message>"` — commit staged changes with a message.  
- `git fetch --all` — fetch all updates from remote branches.  
- `git merge <branch>` — merge another branch into your current branch.  
- `git pull --ff-only` — update your branch with the latest changes from remote.  
- `git push -u origin <branch>` — push your branch to GitHub and set upstream.  
- `git reset --hard origin/main` — reset your branch to match the remote main branch.  



## Common Mistakes

1. **Confusing branch names with folder names.**  
Remember: `solo/{{ONYEN}}` is the branch name; `solo/` is the folder. Both are required.

2. **Forgetting to pull the latest changes before branching or merging.**  
Always run `git pull --ff-only` on `main` or your base branch to avoid diverging histories.

3. **Leaving merge conflict markers in files.**  
Always remove `<<<<<<<`, `=======`, and `>>>>>>>`. Ensure the final `roster.md` is clean and alphabetized.

---

## Extra Debugging Commands

- `git status` — check current branch and file state.  
- `git branch -vv` — show local branches and their remote tracking.  
- `git diff` — show unstaged changes.  
- `git diff --staged` — show staged but uncommitted changes.  
- `git log --oneline --graph --decorate --all` — visualize branch history.  
- `git reflog` — view recent HEAD movements to recover from mistakes.  
- `git merge --abort` — cancel a merge attempt.  
- `git restore <file>` — discard changes to a file before staging.  
- `git reset --hard origin/main` — reset your local branch to match the remote main branch.  

---
