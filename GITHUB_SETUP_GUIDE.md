# GitHub Repository Setup with Preview as Main Branch

## Steps to Upload Local Project to New GitHub Repository

### 1. Create Repository on GitHub
- Go to GitHub and create a new repository
- Add a README.md file during creation
- Set the default branch name to `preview` (if available in settings)

### 2. Navigate to Your Local Project
```bash
cd /path/to/your/project
```

### 3. Initialize Git (if not already done)
```bash
git init
```

### 4. Add Remote Repository
```bash
git remote add origin https://github.com/username/repository-name.git
```

### 5. Stage All Files
```bash
git add .
```

### 6. Make Initial Commit
```bash
git commit -m "Initial commit: Project setup"
```

### 7. Rename Branch to Preview
```bash
git branch -M preview
```

### 8. Pull Remote Content and Merge
```bash
git pull origin preview --allow-unrelated-histories --no-rebase
```

### 9. Resolve Merge Conflicts (if any)
- Edit conflicted files (usually README.md)
- Combine content from both local and remote versions
- Stage resolved files:
```bash
git add filename.md
```

### 10. Complete Merge
```bash
git commit -m "Merge remote repository with local project"
```

### 11. Push to GitHub
```bash
git push -u origin preview
```

## Future Updates
After initial setup, use these commands for regular updates:
```bash
git add .
git commit -m "Your commit message"
git push
```

## Notes
- The `--allow-unrelated-histories` flag is needed when merging completely separate Git histories
- Always resolve merge conflicts carefully to preserve important information from both sources
- The `-u` flag in the initial push sets up tracking between local and remote branches