# Git & GitHub
## 1. Git

### Definition

**Git** is a distributed version control system used to track code changes, manage project history, and collaborate with other developers.

### Example

If you accidentally break your project, Git lets you view previous versions and restore a working state.

### Key Points

- Tracks changes in files.
- Maintains project history.
- Supports branching and merging.
- Enables safe collaboration.

---

## 2. GitHub

### Definition

**GitHub** is a cloud-based platform for hosting Git repositories and collaborating on software projects.

### Example

A developer pushes a local project to GitHub so teammates can access, review, and contribute to the code.

### Key Points

- Hosts Git repositories online.
- Enables collaboration.
- Provides backup and remote access.
- Supports features like Pull Requests and Issues.

---

## 3. Git vs GitHub

### Definition

**Git** is the version control tool, while **GitHub** is an online platform that hosts Git repositories.

### Example

```text
Git → Tracks changes locally
GitHub → Stores and shares the repository online
```

### Key Points

| Git                        | GitHub                       |
| -------------------------- | ---------------------------- |
| Version control system     | Code hosting platform        |
| Runs locally               | Cloud-based platform         |
| Tracks project history     | Hosts remote repositories    |
| Works through Git commands | Provides collaboration tools |

---

## 4. Repository (Repo)

### Definition

A **repository** is a project directory tracked by Git, including its files and version history.

### Example

A `portfolio` folder initialized with Git becomes a Git repository.

### Key Points

- Contains project files.
- Stores Git version history.
- Can exist locally or remotely.
- Commonly called a **repo**.

---

## 5. Working Directory

### Definition

The **working directory** is the local project folder where you create and modify files.

### Example

You edit `index.html` and `style.css` inside your project folder.

### Key Points

- Contains your current project files.
- Where you make code changes.
- Changes are initially untracked or modified.
- Git monitors changes in this area.

---

## 6. Staging Area

### Definition

The **staging area** is a temporary area where you select changes that should be included in the next commit.

### Visual

```text
Working Directory
      |
    git add
      v
Staging Area
      |
  git commit
      v
Repository
```

### Key Points

- Selects changes for the next commit.
- Created using `git add`.
- Allows partial changes to be committed.
- Sits between working files and commits.

---

## 7. Commit

### Definition

A **commit** is a saved snapshot of staged changes in a Git repository.

### Example

`git commit -m "Add login page"`

### Key Points

- Saves a version of the project.
- Contains a commit message.
- Creates a point in project history.
- Can be viewed or restored later.

---

## 8. Branch

### Definition

A **branch** is an independent line of development used to work on features or fixes without directly changing the main branch.

### Visual

```text
main ───●────●────────●
              \
feature ───────●────●
```

### Key Points

- Enables parallel development.
- Keeps features isolated.
- Useful for bug fixes and experiments.
- Can later be merged into another branch.

---

## 9. Main Branch

### Definition

The **main branch** is the primary branch of a Git repository and commonly contains the stable version of a project.

### Example

A team develops a feature on `feature-login` and merges it into `main` after completion.

### Key Points

- Usually represents the main codebase.
- Often contains stable code.
- Should be protected from accidental changes.
- Previously, `master` was also commonly used as the default name.

---

## 10. Remote Repository

### Definition

A **remote repository** is a Git repository hosted on another system or online platform such as GitHub.

### Example

Your local project is connected to a GitHub repository named `my-portfolio`.

### Key Points

- Stores project code remotely.
- Enables collaboration.
- Acts as an online backup.
- Commonly uses a remote name such as `origin`.

---

## 11. Git Workflow

### Definition

A **Git workflow** is the process of modifying files, staging changes, committing them, and optionally sharing them with a remote repository.

### Visual

```text
Edit Files
    |
    v
git add
    |
    v
Staging Area
    |
    v
git commit
    |
    v
Local Repository
    |
    v
git push
    |
    v
Remote Repository
```

### Key Points

- Modify project files.
- Stage changes with `git add`.
- Save changes with `git commit`.
- Upload commits using `git push`.

---

# 12. `git init`

### Definition

`git init` initializes a new Git repository in the current project directory.

### Example

```bash
git init
```

### Key Points

- Starts Git tracking for a project.
- Creates a hidden `.git` directory.
- Stores Git metadata and history.
- Usually run once when starting a new repository.

---

# 13. `git clone`

### Definition

`git clone` creates a local copy of an existing remote repository.

### Example

```bash
git clone https://github.com/user/repo.git
```

### Key Points

- Downloads a repository.
- Copies project files and Git history.
- Connects the local repository to the remote.
- Useful when starting work on an existing project.

---

# 14. `git status`

### Definition

`git status` shows the current state of your working directory and staging area.

### Example

```bash
git status
```

### Key Points

- Shows modified files.
- Shows staged files.
- Shows untracked files.
- Shows the current branch.

---

# 15. `git add`

### Definition

`git add` stages changes so they can be included in the next commit.

### Example

```bash
git add index.html
git add .
```

### Key Points

- Moves changes to the staging area.
- Can stage specific files.
- `git add .` stages changes in the current directory.
- Required before committing changes.

---

# 16. `git commit`

### Definition

`git commit` saves staged changes as a new snapshot in the local repository.

### Example

```bash
git commit -m "Add login form"
```

### Key Points

- Saves staged changes.
- Requires a commit message.
- Creates a new point in project history.
- Commits are stored locally until pushed.

---

# 17. `git push`

### Definition

`git push` uploads local commits to a remote repository such as GitHub.

### Example

```bash
git push origin main
```

### Key Points

- Sends local commits to a remote.
- Shares changes with collaborators.
- Updates the remote branch.
- Requires a configured remote repository.

---

# 18. `git pull`

### Definition

`git pull` downloads changes from a remote repository and integrates them into the current local branch.

### Example

```bash
git pull origin main
```

### Key Points

- Gets the latest remote changes.
- Updates the local branch.
- Helps keep your project synchronized.
- May result in merge conflicts.

---

# 19. `git fetch`

### Definition

`git fetch` downloads new commits and references from a remote repository without automatically merging them into the current branch.

### Example

```bash
git fetch origin
```

### Key Points

- Downloads remote updates.
- Does not modify your working files directly.
- Lets you inspect remote changes first.
- Useful before deciding to merge or rebase.

---

# 20. `git diff`

### Definition

`git diff` shows differences between versions of your files.

### Example

```bash
git diff
git diff --staged
```

### Key Points

- Shows what lines were added or removed.
- `git diff` shows unstaged changes.
- `git diff --staged` shows staged changes.
- Useful for reviewing code before committing.

---

# 21. `git restore`

### Definition

`git restore` is used to restore files or remove changes from the working directory or staging area.

### Example

```bash
git restore index.html
git restore --staged index.html
```

### Key Points

- Can discard local file changes.
- Can unstage files.
- `--staged` removes a file from staging.
- Use carefully because discarded changes may be lost.

---

# 22. `git log`

### Definition

`git log` displays the commit history of a Git repository.

### Example

```bash
git log
git log --oneline
```

### Key Points

- Shows previous commits.
- Displays commit messages and authors.
- `--oneline` provides a compact history.
- Useful for tracking project progress.

---

# 23. `git show`

### Definition

`git show` displays details and changes associated with a specific commit.

### Example

```bash
git show a1b2c3d
```

### Key Points

- Shows commit details.
- Displays the changes introduced by a commit.
- Uses a commit hash.
- Useful for inspecting specific changes.

---

# 24. `git branch`

### Definition

`git branch` is used to view, create, and manage branches in a Git repository.

### Example

```bash
git branch
git branch feature-login
```

### Key Points

- Lists available branches.
- Creates new branches.
- Shows the current branch.
- Helps organize parallel development.

---

# 25. `git checkout`

### Definition

`git checkout` is a Git command historically used to switch branches and restore files.

### Example

```bash
git checkout feature-login
git checkout -b new-feature
```

### Key Points

- Switches between branches.
- Can create and switch to a new branch.
- Older but still widely encountered command.
- Modern Git often uses `git switch` for branch operations.

---

# 26. `git merge`

### Definition

`git merge` combines the changes from one branch into another branch.

### Example

```bash
git checkout main
git merge feature-login
```

### Key Points

- Combines branch histories.
- Usually performed from the target branch.
- Can create a merge commit.
- May result in merge conflicts.

---

# 27. `git branch -d`

### Definition

`git branch -d` deletes a local branch that is no longer needed.

### Example

```bash
git branch -d feature-login
```

### Key Points

- Deletes a local branch.
- Commonly used after merging.
- Helps keep branch lists clean.
- `-D` can force deletion when necessary.

---

# 28. `git remote`

### Definition

`git remote` manages connections between a local Git repository and remote repositories.

### Example

```bash
git remote add origin https://github.com/user/repo.git
git remote -v
```

### Key Points

- Adds remote repositories.
- Displays configured remotes.
- `origin` is the common default remote name.
- Used with commands such as `push` and `pull`.

---

# 29. Merge Conflict

### Definition

A **merge conflict** occurs when Git cannot automatically combine conflicting changes from different branches.

### Visual

```text
Branch A → Changes same line ← Branch B
                    |
                    v
             Merge Conflict
                    |
                    v
           Manually Resolve
                    |
                    v
                  Commit
```

### Key Points

- Happens when changes conflict.
- Git marks the conflicting sections.
- Developer manually chooses the correct version.
- Resolved files must be staged and committed.

---

# 30. Feature Branch Workflow

### Definition

A **feature branch workflow** isolates new development from the main codebase until the feature is ready.

### Visual

```text
main
  |
  +----> feature branch
  |          |
  |       Develop
  |          |
  |       Commit
  |          |
  +<----- Merge
```

### Key Points

- Create a branch for the feature.
- Develop and commit changes.
- Push the branch to GitHub.
- Merge into `main` after review and testing.

---

# 31. GitHub Pull Request

### Definition

A **Pull Request (PR)** is a GitHub feature used to propose and review changes before merging them into another branch.

### Example

A developer opens a PR from `feature-login` to `main` for team review.

### Key Points

- Used for code review.
- Allows discussion and feedback.
- Automated checks can run on PRs.
- Approved changes can be merged.

---

# 32. GitHub Issues

### Definition

**GitHub Issues** are used to track bugs, tasks, feature requests, and project discussions.

### Example

Create an issue titled **"Fix mobile navigation menu"** to track a UI bug.

### Key Points

- Tracks tasks and bugs.
- Supports project organization.
- Can be assigned to contributors.
- Can be linked with Pull Requests.

---

# 33. `.gitignore`

### Definition

A **`.gitignore`** file tells Git which files and folders should not be tracked or committed.

### Example

```text
node_modules/
.env
dist/
```

### Key Points

- Prevents unwanted files from being tracked.
- Commonly excludes dependencies and build files.
- Helps protect sensitive configuration files.
- Must be created in the repository.

---

# 34. Git Configuration

### Definition

Git configuration stores settings such as the username and email associated with your commits.

### Example

```bash
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

### Key Points

- Sets the author information for commits.
- `--global` applies the setting to your user account.
- Can also be configured per repository.
- Usually configured when setting up Git.

---

# 35. Commit Message

### Definition

A **commit message** briefly describes the changes included in a commit.

### Example

```bash
git commit -m "Add responsive navbar"
```

### Key Points

- Should be clear and concise.
- Describes the purpose of the change.
- Helps understand project history.
- Avoid vague messages like `"updated files"`.

---

# 36. Good Git Practices

### Definition

Good Git practices make project history easier to understand, maintain, and collaborate on.

### Example

Instead of one huge commit, make separate commits such as `Add navbar`, `Add hero section`, and `Fix mobile layout`.

### Key Points

- Commit small, logical changes frequently.
- Write meaningful commit messages.
- Use branches for features and fixes.
- Pull or fetch updates before starting collaborative work.

---

# 37. Essential Git Commands Cheat Sheet

### Definition

The following commands cover the basic Git workflow used in everyday development.

### Example

```bash
# Start a repository
git init

# Clone a repository
git clone <repository-url>

# Check status
git status

# Stage changes
git add .
git add <filename>

# Commit changes
git commit -m "Your message"

# View history
git log --oneline

# Create a branch
git branch <branch-name>

# Switch branch
git checkout <branch-name>

# Create and switch branch
git checkout -b <branch-name>

# Merge a branch
git merge <branch-name>

# Add remote
git remote add origin <repository-url>

# Push changes
git push origin main

# Pull changes
git pull origin main

# Fetch remote changes
git fetch origin
```

### Key Points

- `init` → Start Git.
- `add` → Stage changes.
- `commit` → Save changes locally.
- `push` → Upload changes.
- `pull` → Get and integrate remote changes.

---

# 38. Basic Git Workflow — Quick Glance

### Definition

The basic Git workflow moves changes from your working directory to the local repository and finally to a remote repository.

### Visual

```text
Edit
  ↓
git status
  ↓
git add
  ↓
git commit
  ↓
git push
  ↓
GitHub
```

### Key Points

- **Edit:** Modify project files.
- **Stage:** `git add`
- **Commit:** `git commit`
- **Upload:** `git push`

---

# 39. Git & GitHub Collaboration Workflow

### Definition

A collaborative GitHub workflow allows developers to work independently on branches and combine their changes through Pull Requests.

### Visual

```text
Clone / Pull
     ↓
Create Branch
     ↓
Write Code
     ↓
Commit
     ↓
Push Branch
     ↓
Pull Request
     ↓
Code Review
     ↓
Merge
```

### Key Points

- Work on separate feature branches.
- Commit changes regularly.
- Push branches to GitHub.
- Use Pull Requests for review and merging.

---

# 40. Git vs GitHub — Quick Revision

### Definition

Git manages version control, while GitHub provides online hosting and collaboration features for Git repositories.

### Example

```text
Local Computer              GitHub
     |                         |
     | ---- git push --------> |
     | <--- git pull --------- |
     |                         |
    Git                    Remote Repo
```

### Key Points

- Git is a **tool**.
- GitHub is a **platform**.
- Git works locally without GitHub.
- GitHub makes sharing and collaboration easier.
