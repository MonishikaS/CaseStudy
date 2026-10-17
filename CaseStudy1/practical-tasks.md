
# Git and GitHub — Practical Tasks

**Case Study 01: Basic Git and GitHub Commands**

Difficulty: Beginner

## Objective

Learn to use basic Git commands and connect a local repository to GitHub.

## Task 1: Check Git Installation

### Instructions

Open your terminal or Git Bash and execute:

```bash
git --version
```

### Questions

1. What does this command display?
2. What should you do if Git is not installed?

### Expected Outcome

The terminal displays the installed Git version.

---

## Task 2: Configure Git

### Instructions

Configure your Git username and email.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Verify the configuration:

```bash
git config --list
```

### Questions

1. Why do we configure a username and email?
2. What does the `--global` option mean?
3. Which command displays Git configuration?

### Expected Outcome

Your Git username and email are configured for your user account.

---

## Task 3: Initialize a Repository

### Instructions

1. Create a folder named `git-practice`.
2. Open a terminal inside the folder.
3. Execute the following commands:

```bash
git init
git status
```

### Questions

1. What does `git init` do?
2. What information does `git status` display?
3. What is a local repository?

### Expected Outcome

Git initializes a repository in the folder.

---

## Task 4: Create and Stage a File

### Instructions

1. Create a file named `notes.txt`.
2. Write a few lines in the file.
3. Execute:

```bash
git status
git add notes.txt
git status
```

### Questions

1. What does Git report before staging the file?
2. What changes after running `git add notes.txt`?
3. What is the staging area?

### Expected Outcome

The file changes from untracked to staged.

---

## Task 5: Create Your First Commit

### Instructions

Execute:

```bash
git commit -m "Add initial notes"
git log --oneline
```

### Questions

1. What is a commit?
2. Why do we use commit messages?
3. Where is this commit stored?
4. Does committing automatically upload files to GitHub?

### Expected Outcome

Git records a snapshot of the staged changes in the local repository.

---

## Task 6: Modify and Commit Again

### Instructions

1. Add another line to `notes.txt`.
2. Execute:

```bash
git status
git add notes.txt
git commit -m "Update notes"
git log --oneline
```

### Questions

1. Why does Git detect the file as modified?
2. Why are there now two commits?
3. How can you view the commit history?

### Expected Outcome

The repository contains two commits documenting different versions of the file.

---

## Task 7: Create a GitHub Repository

### Instructions

1. Sign in to GitHub.
2. Create a repository named `git-practice`.
3. For this exercise, leave the README, license, and `.gitignore` initialization options unchecked.
4. Copy the repository URL.

### Questions

1. What is a remote repository?
2. What is the difference between a local repository and a remote repository?
3. Why do developers use GitHub?

### Expected Outcome

An empty remote repository is available on GitHub.

---

## Task 8: Connect Local Git to GitHub

### Instructions

From your local `git-practice` directory, execute the following command, replacing the example URL with your repository URL:

```bash
git remote add origin https://github.com/YOUR-USERNAME/git-practice.git
git remote -v
```

Then rename your current branch and push your commits:

```bash
git branch -M main
git push -u origin main
```

### Questions

1. What is the purpose of `git remote add origin`?
2. What does `git remote -v` display?
3. What does `git branch -M main` do?
4. What is the purpose of `git push -u origin main`?

### Expected Outcome

Your local commits appear in the `main` branch on GitHub.

---

## Task 9: Clone a Repository

### Instructions

Open a terminal in a different directory and execute:

```bash
git clone https://github.com/YOUR-USERNAME/git-practice.git
```

Replace the URL with your actual repository URL.

### Questions

1. What does `git clone` do?
2. How is `git clone` different from `git init`?
3. Why is cloning useful when working with an existing project?

### Expected Outcome

A local copy of the GitHub repository is created.

---

## Task 10: Pull Remote Changes

### Instructions

1. Open your repository on GitHub.
2. Add a new file named `remote-notes.txt` through the GitHub website.
3. Commit the file on GitHub.
4. Open the original local repository and execute:

```bash
git pull origin main
```

### Questions

1. What does `git pull` do?
2. Why might your local repository need to pull changes?
3. What happens to `remote-notes.txt` after a successful pull?

### Expected Outcome

The remote changes are integrated into your local repository, and the new file appears locally.

---

## Final Challenge

Complete the following checklist:

- [ ] Check Git installation.
- [ ] Configure Git username and email.
- [ ] Initialize a repository.
- [ ] Create and stage a file.
- [ ] Commit changes.
- [ ] Make a second commit.
- [ ] Create a GitHub repository.
- [ ] Connect the local repository to GitHub.
- [ ] Push commits to GitHub.
- [ ] Clone the repository.
- [ ] Pull remote changes.
- [ ] Verify the repository on GitHub.

## Submission Requirements

Submit the GitHub repository URL.

Ensure that:

1. The repository contains `notes.txt` and `remote-notes.txt`.
2. At least two meaningful commits are visible.
3. The repository is accessible to the intended reviewer.
4. You can explain the purpose of each command used.
