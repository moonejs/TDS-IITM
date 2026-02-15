# TDS-IITM (Tools in Data Science)

A comprehensive repository for the Tools in Data Science course at IIT Madras, containing notes, resources, and a complete Git command reference.

##  Course Overview

This repository contains materials and resources for the Tools in Data Science (TDS) course, covering essential tools and techniques used in modern data science workflows.

##  Topics Covered

- **Version Control**: Git and GitHub fundamentals
- **Data Manipulation**: Python libraries (Pandas, NumPy)
- **Data Visualization**: Matplotlib, Seaborn
- **Command Line**: Unix/Linux shell commands
- **Development Tools**: Jupyter Notebooks, IDEs
- **Collaboration**: GitHub workflows, pull requests, code reviews

##  Git Quick Reference Guide

### Basic Git Commands

| Command | Purpose |
|---|---|
| `git init` | Initialize a new Git repository |
| `git clone <url>` | Copy a remote repository locally |
| `git status` | Show working directory status |
| `git add <file>` | Stage file for commit |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Create a commit |
| `git log` | Show commit history |
| `git log --oneline` | Compact commit history |
| `git diff` | Show unstaged changes |
| `git diff --staged` | Show staged changes |
| `git rm <file>` | Remove file from repo |
| `git mv <old> <new>` | Rename/move file |
| `git show <commit>` | Show commit details |
| `git help <command>` | Show help page |

### Branching & Merging

| Command | Purpose |
| --- | --- |
| `git branch` | List branches |
| `git branch <name>` | Create branch |
| `git checkout <branch>` | Switch branch |
| `git checkout -b <name>` | Create + switch branch |
| `git switch <branch>` | Switch branch (modern way) |
| `git switch -c <name>` | Create + switch branch |
| `git merge <branch>` | Merge branch |
| `git branch -d <name>` | Delete branch |
| `git rebase <branch>` | Reapply commits |
| `git cherry-pick <commit>` | Apply specific commit |
| `git merge --abort` | Cancel merge |
| `git rebase --abort` | Cancel rebase |

### Remote & Collaboration

| Command | Purpose |
| --- | --- |
| `git remote` | List remotes |
| `git remote -v` | Show remote URLs |
| `git remote add <name> <url>` | Add remote |
| `git fetch` | Download changes |
| `git pull` | Fetch + merge |
| `git push` | Upload changes |
| `git push -u origin <branch>` | Set upstream branch |
| `git push --force` | Force push |
| `git push --tags` | Push tags |
| `git clone --depth 1` | Shallow clone |

### Tags

| Command | Purpose |
| --- | --- |
| `git tag` | List tags |
| `git tag <name>` | Create tag |
| `git tag -a <name>` | Annotated tag |
| `git show <tag>` | Show tag details |
| `git tag -d <name>` | Delete tag |

### Stashing

| Command | Purpose |
|---|---|
| `git stash` | Save uncommitted changes |
| `git stash list` | List stashes |
| `git stash apply` | Apply stash |
| `git stash pop` | Apply + remove stash |
| `git stash drop` | Delete stash |
| `git stash clear` | Remove all stashes |

### Undo & Recovery

| Command | Purpose |
| --- | --- |
| `git reset <file>` | Unstage file |
| `git reset --soft HEAD~1` | Undo commit (keep changes) |
| `git reset --hard HEAD~1` | Undo commit (delete changes) |
| `git revert <commit>` | Create reverse commit |
| `git restore <file>` | Restore file |
| `git restore --staged <file>` | Unstage file |
| `git reflog` | Show reference history |
| `git fsck` | Check repository integrity |

### Inspection & Debugging

| Command | Purpose |
|---|---|
| `git blame <file>` | Show line authors |
| `git bisect start` | Start binary search |
| `git bisect good` | Mark good commit |
| `git bisect bad` | Mark bad commit |
| `git shortlog` | Commit summary by author |
| `git describe` | Show closest tag |

### Configuration

| Command | Purpose |
| --- | --- |
| `git config --global user.name` | Set username |
| `git config --global user.email` | Set email |
| `git config --list` | List configs |
| `git config --global alias.co checkout` | Create alias |

### Submodules

| Command | Purpose |
| --- | --- |
| `git submodule add <url>` | Add submodule |
| `git submodule init` | Initialize submodules |
| `git submodule update` | Update submodules |
| `git submodule foreach` | Run command in each submodule |

### Advanced / History Editing

| Command | Purpose |
| --- | --- |
| `git rebase -i HEAD~n` | Interactive rebase |
| `git commit --amend` | Modify last commit |
| `git filter-repo` | Rewrite history |
| `git replace` | Replace objects |
| `git worktree add` | Multiple working trees |

## ⭐ Most Important Commands (90% of Real Work)

```bash
git init
git add
git commit
git status
git branch
git switch
git merge
git pull
git push
git log --oneline --graph
git stash
git reset
git revert
```

##  Understanding the Pathspec Separator

```bash
git <command> [options] -- [file/path]
```

### `--` ← Very Important

This is called the **pathspec separator**.

It tells Git:

> "Everything after this is a file path, not an option."

Because Git can't always tell the difference between options and file paths, using `--` makes your commands unambiguous.

**Example:**
```bash
git checkout -- myfile.txt  # Restore myfile.txt from the index
git log -- src/  # Show commits that affected the src/ directory
```

##  Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Learning Lab](https://lab.github.com/)
- [Pro Git Book](https://git-scm.com/book/en/v2)

##  Contributing

Feel free to contribute to this repository by:
1. Forking the repository
2. Creating a feature branch (`git switch -c feature/amazing-feature`)
3. Committing your changes (`git commit -m 'Add amazing feature'`)
4. Pushing to the branch (`git push origin feature/amazing-feature`)
5. Opening a Pull Request

##  License

This repository is for educational purposes as part of the TDS-IITM course.

---

**Happy Learning! 🎓**
