# Commandline Git

### Step 1: Set Up Git Configuration
Before working with Git, you need to set up your name, email, and other essential configurations:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-username@users.noreply.github.com"
```

Verify the configuration:
```bash
git config --list
```

### Step 2: Initialize a Repository
To start tracking a project with Git:

1. Navigate to the directory where your project is:
   ```bash
   cd ~/your_project_directory
   ```
   
2. Initialize Git:
   ```bash
   git init
   ```

### Step 3: Add a Remote Repository
If you want to link your local repo to GitHub:

```bash
git remote add origin git@github.com:YOUR_USERNAME/YOUR_REPOSITORY.git
```

### Step 4: Create and Stage Files
Create or add a file to the repository, such as `README.md`:

```bash
echo "# My Project" > README.md
```

To add changes to the staging area:

```bash
git add README.md
```

To add all files in the directory:

```bash
git add .
```

### Step 5: Commit Changes
To save changes locally:

```bash
git commit -S -m "Initial commit"
```
`-S` signs the commit using your GPG key.

### Step 6: Push to GitHub
To push your changes to GitHub:

```bash
git push -u origin main
```
If your branch is still named `master`, use:
```bash
git push -u origin master
```

### Step 7: Making Changes and Updating
After making changes to any files:

1. **Check the Status**: To see what has changed:
   ```bash
   git status
   ```

2. **Add Changes to Staging**: Add files you changed:
   ```bash
   git add modified_file.txt
   ```

3. **Commit Changes**: Commit with a message describing what changed:
   ```bash
   git commit -S -m "Updated file with new information"
   ```

4. **Push Changes to GitHub**:
   ```bash
   git push
   ```

### Step 8: Pull Changes from GitHub
To keep your local repository up-to-date with the remote:

```bash
git pull origin main
```

### Step 9: Branching
Branches are useful for working on new features without affecting the main codebase.

1. **Create a New Branch**:
   ```bash
   git checkout -b new-feature
   ```
   
2. **Switch Between Branches**:
   ```bash
   git checkout main
   ```

3. **Merge Branch**:
   Once the feature is done, switch back to `main` and merge it:
   ```bash
   git checkout main
   git merge new-feature
   ```

### Step 10: Viewing the History
To see the commit history:

```bash
git log
```

To see a more concise version:

```bash
git log --oneline
```

### Step 11: Discarding Changes
1. **Remove Changes from Staging**:
   If you've staged a file but want to unstage it:
   ```bash
   git reset HEAD filename
   ```

2. **Discard Local Changes**:
   If you want to discard changes to a file:
   ```bash
   git checkout -- filename
   ```

### Step 12: Cloning a Repository
To clone an existing repository from GitHub:

```bash
git clone git@github.com:YOUR_USERNAME/YOUR_REPOSITORY.git
```

### Common Workflow Recap
1. **Initialize**: `git init`
2. **Create/Edit Files**: Add and edit your code or files.
3. **Stage**: `git add .` or `git add filename`
4. **Commit**: `git commit -S -m "Commit message"`
5. **Push**: `git push -u origin main`
6. **Update from GitHub**: `git pull origin main`
7. **Branch Management**: Create (`git checkout -b branch_name`), switch (`git checkout branch_name`), and merge (`git merge branch_name`).

This should give you a solid start with using Git on your Debian VM. If you need more in-depth explanations or examples on any specific command, just let me know!
