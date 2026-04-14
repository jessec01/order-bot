# Git Commands Information (Guide to Command Information)

This guide will provide you with quick commands in **English** console format necessary for the operations you will execute in your development routines, such as handling bugs and commits.

## 1. Commands for Creating Branches (Commands to Create Branches)

To create a new branch and automatically switch to it (recommended):

```bash
git checkout -b <branch-name>
```

🔹 _Example:_ `git checkout -b fix/14-payment-bug`

To create the branch but stay on the current one (not recommended if you are going to work immediately):

```bash
git branch <branch-name>
```

To see the list of your local branches and know which one you are on:

```bash
git branch
```

## 2. Committing Bug Reports on a Branch (Committing reports on a branch)

First, you must prepare your fixed files (stage changes):

```bash
# Add a specific file
git add index.js

# Or add all files that have changes
git add .
```

Then, proceed to make the commit. It is preferable to use multiple commands if you are using a direct terminal. (Follow the convention of `commit_template.md`):

```bash
git commit -m "fix(scope): brief description in english" -m "And a longer explanation of what the bug caused and how to handle it here."
```

If you prefer to use a text editor that includes a complete paste of your template:

```bash
git commit
```

_Nano, vim or vs-code will open, where you will paste the entire translated template._

## 3. Viewing the Repository Log/History (View log of problems in the repository)

If you need to do an inspection and audit of your bot quickly checking when something broke (The History Log):

For a simple and clean log of 1 single line per commit:

```bash
git log --oneline
```

To see the structured log visually (Graphic Tree):

```bash
git log --graph --oneline --decorate --all
```

If you are looking for when a _bug or error_ was introduced or discussed in the history, search for a keyword:

```bash
git log --grep="bug"
# Or search for words like "error", "crash"
git log --grep="error"
```

To inspect what happened in an exact commit and the lines of code that changed (diff):

```bash
git show <commit-hash>
```

## 4. Default Branch Conflict and History Desynchronization

When initializing the repository using a template or when making the first push, GitHub automatically established a branch called docs-templates-github as the main branch (Default). This caused that, although locally one worked in main, the changes were not reflected correctly in the web interface or seemed "not to be saved" due to the discrepancy between the server's entry point and the local history.

🛠 Solution Applied (Step by Step)
Remote Pointer Change:

Settings > Branches was entered in GitHub to manually change the Default Branch from docs-templates-github to main.

Local References Cleanup:

```bash
git fetch --prune origin
```

Forced Synchronization (Overwriting):

To ensure that the local code (Node/TS) was the "only truth", a Forced Push was used:

```bash
git push origin main --force
```

This overwrote the branch history on the server with the current state of the local folder, eliminating any trace of the previous template files.
