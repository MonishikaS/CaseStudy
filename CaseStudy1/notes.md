
# Git and GitHub — Beginner Notes

## 1. What is Git?

Git is a **distributed version control system** used to track changes in files over time.

### Why do we use Git?

- To track changes in files.
- To maintain project history.
- To restore earlier versions of files.
- To work on projects safely.
- To collaborate with other developers.

## 2. What is GitHub?

GitHub is an online platform used to host Git repositories and collaborate with other developers.

### Why do we use GitHub?

- To store repositories online.
- To share projects with others.
- To collaborate on projects.
- To maintain code backups.
- To contribute to open-source projects.

## 3. Difference Between Git and GitHub

| Git | GitHub |
|---|---|
| A version control system | An online hosting platform |
| Works locally on your computer | Stores repositories online |
| Tracks changes and commits | Hosts repositories and collaboration tools |
| Can work without an internet connection for local operations | Requires internet access for online operations |
| Uses commands such as `git add` and `git commit` | Provides features such as pull requests and issues |

## 4. What is a Repository?

A **repository (repo)** is a location where Git manages project files and their version history.

There are two common types:

- **Local repository:** Stored on your computer.
- **Remote repository:** Hosted on a platform such as GitHub.

## 5. Basic Git Setup

### Check Git Installation

```bash
git --version
```

Displays the installed Git version.

### Configure Your Username

```bash
git config --global user.name "Your Name"
```

Sets the author name used in your commits.

### Configure Your Email

```bash
git config --global user.email "you@example.com"
```

Sets the author email used in your commits.

### View Configuration

```bash
git config --list
```

Displays Git configuration settings.

**Note:** Use an email appropriate for your commits. If you want to keep your personal email private on GitHub, you can configure a GitHub-provided no-reply email.

## 6. Basic Git Commands

### 6.1 git init

```bash
git init
```

Initializes a Git repository in the current directory.

### 6.2 git status

```bash
git status
```

Displays the current state of files, including untracked, modified, and staged files.

### 6.3 git add

Stage a specific file:

```bash
git add notes.txt
```

Stage changes in the current directory:

```bash
git add .
```

Staging prepares changes for the next commit.

### 6.4 git commit

```bash
git commit -m "Add initial notes"
```

Records the staged changes in the local repository history.

The `-m` option allows you to provide a commit message.

### 6.5 git log

```bash
git log
```

Displays commit history.

For a compact history:

```bash
git log --oneline
```

### 6.6 git branch

```bash
git branch
```

Lists local branches.

A branch is an independent line of development. Branch creation and merging will be covered in a later case study.

### 6.7 git clone

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```

Copies a remote repository to your computer, including its available Git history.

Replace `USERNAME` and `REPOSITORY` with the actual values.

### 6.8 git remote

```bash
git remote -v
```

Displays configured remote repositories and their URLs.

### 6.9 git push

```bash
git push
```

Uploads local commits to the configured remote branch.

### 6.10 git pull

```bash
git pull
```

Fetches remote changes and integrates them into the current branch.

## 7. Understanding the Git Workflow

Git commonly follows three stages:

1. **Working directory:** Where you create or modify files.
2. **Staging area:** Where you prepare changes for a commit.
3. **Repository history:** Where committed snapshots are recorded.

### Workflow Commands

```bash
git status
git add notes.txt
git commit -m "Update notes"
git push
```

Explanation:

- `git status` checks the current state.
- `git add` stages the changes.
- `git commit` records the changes locally.
- `git push` uploads commits to the remote repository.

**Important:** A commit does not automatically upload your changes to GitHub. You must push them separately.

## 8. Important Git and GitHub Terms

| Term | Meaning |
|---|---|
| Repository | Project files and their version history |
| Commit | A recorded snapshot of staged changes |
| Commit message | A short description of the changes |
| Working directory | The files you are currently working on |
| Staging area | The area where changes are prepared for a commit |
| Branch | An independent line of development |
| Remote | A reference to a repository hosted elsewhere |
| Origin | The conventional name for the primary remote |
| Main | A common default branch name |
| Clone | Copy a remote repository locally |
| Push | Upload commits to a remote repository |
| Pull | Fetch and integrate remote changes |

## 9. First-Time GitHub Repository Setup

### Step 1: Create a local folder

Create a folder named `git-practice` and open a terminal inside it.

### Step 2: Initialize Git

```bash
git init
```

### Step 3: Create a file

Create a file named `notes.txt` and add some text.

### Step 4: Stage and commit

```bash
git add notes.txt
git commit -m "Add initial notes"
```

### Step 5: Create a GitHub repository

Create a repository named `git-practice` on GitHub.

For this beginner workflow, leave the README, license, and `.gitignore` initialization options unchecked so the remote repository starts empty.

### Step 6: Connect the local repository

Copy the repository URL from GitHub.

```bash
git remote add origin https://github.com/USERNAME/git-practice.git
```

### Step 7: Set the branch name

```bash
git branch -M main
```

### Step 8: Push the code

```bash
git push -u origin main
```

The `-u` option sets the upstream branch so future pushes and pulls can usually use shorter commands.

## 10. Common Beginner Mistakes

### Mistake 1: Forgetting to stage files

**Problem:** You run `git commit`, but your new changes are not included.

**Solution:**

```bash
git add .
git commit -m "Describe changes"
```

### Mistake 2: Forgetting to push

**Problem:** Your commit exists locally but is not visible on GitHub.

**Solution:**

```bash
git push
```

### Mistake 3: Using the wrong repository URL

**Problem:** Git cannot connect to the remote repository.

**Solution:**

```bash
git remote -v
```

Check the URL and correct it if necessary.

### Mistake 4: Committing without a message

**Problem:** Git does not accept the commit because a message was not provided or the configured editor was not completed.

**Solution:**

```bash
git commit -m "Add project notes"
```

### Mistake 5: Running Git commands in the wrong folder

**Problem:** Git reports that the current directory is not a repository.

**Solution:** Navigate to the correct project directory before running repository commands.

## 11. Best Practices

- Write clear and meaningful commit messages.
- Check `git status` before committing.
- Commit related changes together.
- Push your work regularly.
- Do not commit passwords, API keys, or other secrets.
- Read error messages carefully before running additional commands.
- Keep your README updated so others understand the project.

## 12. Quick Revision

| Question | Answer |
|---|---|
| Which command initializes a repository? | `git init` |
| Which command checks file status? | `git status` |
| Which command stages a file? | `git add` |
| Which command records staged changes? | `git commit` |
| Which command displays history? | `git log` |
| Which command copies a remote repository? | `git clone` |
| Which command uploads commits? | `git push` |
| Which command fetches and integrates remote changes? | `git pull` |
| Which command displays remote URLs? | `git remote -v` |
| What is GitHub? | An online platform for hosting Git repositories and collaboration |

---

## Conclusion

Git helps developers track and manage changes, while GitHub allows them to host repositories online and collaborate.

Understanding `git init`, `git status`, `git add`, `git commit`, `git log`, `git clone`, `git push`, and `git pull` provides the foundation for learning branches, merging, pull requests, and collaborative development.
