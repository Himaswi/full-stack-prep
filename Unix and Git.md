## 1.Can you describe what Unix is?
**Unix** is a powerful, multi-user, multitasking operating system developed in the late 1960s at Bell Labs by Ken Thompson, Dennis Ritchie, and others. It was designed to be simple, portable, and efficient, and it became the foundation for many modern operating systems.
Today, many popular operating systems are either Unix or Unix-like systems, including:
- Linux
- macOS
- FreeBSD
- Solaris
- AIX
Unix follows the philosophy of building small programs that perform one task well and can be combined together to solve complex problems.
### Key Features
- Multi-user operating system
- Multitasking support
- Strong security and permissions
- Hierarchical file system
- Powerful command-line interface (Shell)
- Portability across different hardware

### Common Unix Commands

| Command | Purpose |
|----------|---------|
| pwd | Print current directory |
| ls | List files and folders |
| cd | Change directory |
| mkdir | Create a directory |
| rm | Remove files |
| cp | Copy files |
| mv | Move or rename files |
| cat | Display file contents |
| touch | Create an empty file |

## 2.Can you describe what relative and absolute paths are and the difference between them?

A **path** specifies the location of a file or folder in a file system.
There are two types:
1. Absolute Path
2. Relative Path
### Absolute Path
An absolute path starts from the root directory and specifies the complete location of a file.
Example:

```text
/home/himaswi/projects/react-app/src/App.js
```
### Relative Path
A relative path starts from the current working directory.
Example:
Suppose the current directory is:
```text
/home/himaswi/projects
```
Then:
```text
react-app/src/App.js
```
### Difference

| Absolute Path | Relative Path |
|---------------|--------------|
| Starts from root | Starts from current directory |
| Independent of current location | Depends on current location |
| Longer | Shorter |
| Always same | Changes based on current folder |

## 3.Do you know what CRUD is?
CRUD represents the four basic operations performed on data in software applications.

CRUD stands for:

- Create
- Read
- Update
- Delete

These operations are used in databases, REST APIs, and file systems.

## 4.Can you explain what version control is?
Version Control is a system that records changes made to files over time, allowing developers to track history, collaborate with others, and restore previous versions if needed.
It is especially useful when multiple developers work on the same project.
### Benefits
- Tracks changes
- Collaboration
- Restore previous versions
- Branching
- Merging
- Backup

## 5.Do you know what Git is and why is it used?
Git is a **distributed version control system** created by **Linus Torvalds** in 2005 to manage source code efficiently.
Git allows developers to:
- Track changes
- Collaborate
- Create branches
- Merge features
- Restore previous versions
- Resolve conflicts

## 6.Can you explain the three stages of Git?
Git manages changes using three stages.
### 1. Working Directory
Where you create and edit files.
### 2. Staging Area (Index)
Files selected to be included in the next commit.
```bash
git add file.txt
```
### 3.commit Area
### Flow

```text
Working Directory
       ↓
git add
       ↓
Staging Area
       ↓
git commit
       ↓
Git Repository
```
## 7.Can you check the logs of commits in Git?
Git stores the history of every commit.
Useful commands:
```bash
git log
```
Compact view
```bash
git log --oneline
```
Graph view
```bash
git log --graph --oneline
```
Show last 5 commits
```bash
git log -5
```

## 8.Can you explain the connection between Git and GitHub?
Git and GitHub are related but different.
### Git
- Version control system
- Installed locally
- Tracks project history
### GitHub
- Cloud platform
- Hosts Git repositories
- Enables collaboration
- Pull Requests
- Issues
- Actions

## 9.Can you explain what a repo is?
A **repository (repo)** is a storage location that contains a project's source code, history, branches, commits, and configuration files.
A Git repository includes:
- Source code
- Commit history
- Branches
- Tags
- Configuration
- README
- License

Repositories can be:
- Local Repository
- Remote Repository

## 10.Can you clone a GitHub repo locally?
Command:
```bash
git clone https://github.com/user/project.git
```
## 11.Can you create a branch, switch branches, and merge a branch into another branch in Git?
Branches allow developers to work independently without affecting the main code.
### Create Branch

```bash
git branch feature-login
```

### Switch Branch

```bash
git checkout feature-login
```

or

```bash
git switch feature-login
```

### Create and Switch

```bash
git checkout -b feature-login
```

### Merge

Switch to main

```bash
git checkout main
```

Merge

```bash
git merge feature-login
```

Delete merged branch

```bash
git branch -d feature-login
```

## 12. Can you send a pull request on GitHub and merge it locally? (Git commands)

A **Pull Request (PR)** is a request to merge changes from one branch into another (commonly into `main` or `develop`). It allows teammates to review code, discuss changes, and approve them before merging.

### Step 1: Create and switch to a new branch
```bash
git checkout -b feature-login
```
### Step 2: Make changes and commit
```bash
git add .
git commit -m "Add login feature"
```
### Step 3: Push the branch to GitHub
```bash
git push origin feature-login
```
### Step 4: Create a Pull Request

On GitHub:
1. Open the repository.
2. Click **Compare & pull request**.
3. Add a title and description.
4. Submit the Pull Request.
5. Wait for code review and approval.
6. Merge the Pull Request on GitHub.

### Step 5: Update your local `main` branch
```bash
git checkout main
git pull origin main
```
### If you merge locally instead of GitHub
```bash
git checkout main
git merge feature-login
git push origin main
```

