# **Nathan's Most Excellent Cheatsheet** 

## **Table of Contents**
1. <a href="#keyboard-shortcuts">**Keyboard Shortcuts**</a>
2. <a href="#spectacle-shortcuts">**_Spectacle_ Shortcuts**</a>
3. <a href="#terminal-and-the-command-line-interface">**_Terminal_ and the Command Line Interface**</a>
4. <a href="#git-and-github">**Git and GitHub**</a>

## **Keyboard Shortcuts**
- Developers avoid using the mouse whenever possible and are more productive when their hands are on the keyboard. 
- Below is a list of commonly used keyboard shortcuts:

| Keys   |      Action      |  
|----------|-------------|
| `cmd+space` | Opens *Spotlight* search bar. | 
| `cmd+tab`   | Quickly switches between running apps. |
| `cmd+backtick` | Switch between multiple windows of same application. | 
| `cmd+'Z'` | Undo's last edit. |
| `cmd+'W'` | Close's current working window or tab. |
| `cmd+'Q'` | Close's current working application. |


>NOTE: it's best to minimize how many windows/applications you have open when developing to make switching between applications quicker and minimize distractions to the job at hand.

<a href="#nathans-most-excellent-cheatsheet">Back to Top</a>

---

## **_Spectacle_ Shortcuts**
- Application allows user to easily organize windows without using a mouse!
- Here is a list of basic commands below:

| Keys    |     Action     |
|----------|---------------|
| `opt+cmd+'F'` | Makes window full-size. |
| `opt+cmd+'Left'` | Moves window to left half. |
| `opt+cmd+'Right'` | Moves window to right half. |
| `opt+cmd+'Up'` | Moves window to top half. |
| `opt+cmd+'Down'` | Moves window to bottom half. |

<a href="#nathans-most-excellent-cheatsheet">Back to Top</a>

---

## **_Terminal_ and the Command Line Interface**

### **What is _Terminal_?**
- *Terminal* is the developers' choice for entering commands and navigating the filesystem and is also known as a *shell*. 
- Here's a list of basic commands below:

| Type   |      Action      |
|--------|------------------|
| `pwd`  | "Prints" the current working directory (or folder). | 
| `cd`  | Change directory. |
| `cd ~` | Change to logged user's *home* directory. |
| `cd /` | Change to *root* (top-level) directory on harddrive. |
| `cd ..` | Change to *parent* directory. | 
| `ls`  | Lists contents of current directory. | 
| `ls -a` | Displays *hidden* files in current directory. |
| `mkdir` | Creates a *directory* (or folder). |
| `touch` | Creates a *file* in current directory (i.e. `touch index.html`). |
| `mv`  | *Move* and *rename* files and directories (i.e. `mv style1.css style2.css`). |
| `cp`  | *Copy* files and directories. |
| `rm`  | *Deletes* files and directories. |
| `rm -r` | *Deletes* directories and contents within. |
>Note: be careful when deleting anything using the *Terminal* as it will be gone **FOREVER** (no trashcan, no undos).


### **Command History & Clearing the Window**
- Pressing the `'Up'` and `'Down'` arrow in *Terminal* will cycle through previously entered commands. This can be a huge time saver!
- To clear the *Terminal* window, simply press `cmd+k` or type `clear` in the window.

<a href="#nathans-most-excellent-cheatsheet">Back to Top</a>

---

## **Git and GitHub**
- **Git** provides us with local repositories on our computers. 
- **GitHub** provides us with remote repostories stored in the cloud. 
- A local repository is "linked" to a remote repository by adding a "remote" with the command `$ git remote add <name of remote> <URL of repo on GitHub>`. 

### **Configure Tooling**
_Configure user information for all local repositories._

| `$ git config --global user.name "[name]"` |
|---|
Sets the name you want attached to your commit transactions. 

| `$ git config --global user.email "[email address]"` |
|---|
Sets the email you want attached to your commit transactions. 

| `$ git confi --global color.ui auto` |
|---|
Enables helpful colorization of command line output. 

<br>

### **Create Repositories**
_Start a new repository or obtain one from an existing URL._

| `$ git init [project-name]` |
|---|
Creates a new local repository with the specified name.

| `$ git clone [url]` | 
|---| 
Downloads a project and its entire version history.

<br>

### **Make Changes**
_Review edits and craft a commit transaction._

| `$ git status` |
|---|
Lists all new or modified files to be committed. 

| `$ git diff` |
|---|
Shows file differences not yet stages.

| `$ git add [file]` |
|---|
Snapshots the file in preparation for versioning. 

| `$ git diff --staged` |
|---| 
Shows file differences between staging and the last file version.

| `$ git reset [file]` |
|---|
Unstages the file, but preserves its contents. 

| `$ git commit -m "[descriptive message]"` |
|---|
Records file snapshots permanently in version history. 

<br>

### **Group Changes**
_Name a series of commits and combine completed efforts._

| `$ git branch` |
|---| 
Lists all local branches inthe current repository. 

| `$ git branch [branch-name]` |
|---|
Creates a new branch. 

| `$ git checkout [branch-name]` |
|---|
Switches to the specified branch and updates the working directory. 

| `$ git merge [branch]` |
|---| 
Combines the specified branch's history into the current branch.

| `$ git branch -d [branch-name]` |
|---|
Deletes the specified branch. 

<br>

### **Refactor Filenames**
_Relocate and remove versioned files._

| `$ git rm [file]` |
|---|
Deletes the file from the working directory and stages the deletion. 

| `$ git rm --chached [file]` |
|---|
Removes the file from version control but preserves the file locally. 

| `$ git mv [file-original] [file-renamed]` |
|---|
Changes the file name and prepares it for commit. 

<br>

### **Suppress Tracking**
_Exclude temporary files and paths._

| `*.log build/temp-*` |
|---|
|A text file names `.gitignore` suppresses accidental versioning of files and paths matching the specified patterns. |

| `$ git ls-files --other --ignored --exclude-standard` |
|---|
Lists all ignored files in this project. 

<br>

### **Save Fragments**
_Shelve and restore incomplete changes._

| `$ git stash` |
|---|
Temporarily stores all modified tracked files. 

| `$ git stash pop` |
|---|
Restores the most recently stashed files. 

| `$ git stash list` |
|---|
Lists all stashed changesets.

| `$ git stash drop` |
|---|
Discards the most recently stashed changeset.

<br>

### **Review History**
_Browse and inspect the evolution of project files._

| `$ git log` |
|---|
Lists version history for the current branch. 

| `$ git log --follow [file]` |
|---|
Lists version history for a file, including renames. 

| `$ git diff [first-branch]...[second-branch]` |
|---|
Shows content differences between two branches. 

| `$ git show [commit]` |
|---|
Outputs metadata and content changes of the specified commit. 

<br>

### **Redo Commits**
_Erase mistakes and craft replacement history._

| `$ git reset [commit]` |
|---|
Undoes all commits after `[commit]`, preserving changes locally. 

| `$ git reset --hard [commit]` |
|---|
Discards all history and changes back to the specified commit. 

<br>

### **Synchronize Changes**
_Register a repository bookmark and exchange version history._

| `$ git fetch [bookmark]` |
|---|
Downloads all history from the repository bookmark.

| `$ git merge [bookmark]/[branch]` |
|---|
Combines bookmark's branch into current local branch. 

| `$ git push [alias] [branch]` |
|---|
Uploads all local branch commits to GitHub. 

| `$ git pull` |
|---|
Downloads bookmark history and incorporates changes. 

<a href="#nathans-most-excellent-cheatsheet">Back to Top</a>