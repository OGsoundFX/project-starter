### Git Commands Cheat Sheet for Team Collaboration

#### 1. **Creating and Switching to a New Branch**
   ```bash
   git checkout -b NAME_OF_BRANCH
   ```
   - Creates a new branch and switches to it. Use a descriptive name for your branch (e.g., `feature/login-page`).

#### 2. **Checking the Status of Your Repository**
   ```bash
   git status
   ```
   - Displays the status of your working directory and staging area. Shows which files are modified, staged for commit, or untracked.

#### 3. **Viewing Differences Between Files**
   ```bash
   git diff
   ```
   - Shows changes between your working directory and the staging area. Useful to review what changes you’ve made before committing.

#### 4. **Adding Changes to the Staging Area**
   ```bash
   git add FILES_TO_ADD
   ```
   - Stages specific files for commit. Replace `FILES_TO_ADD` with the file names.

   ```bash
   git add .
   ```
   - Stages all changes (new, modified, and deleted files) in the current directory.

#### 5. **Committing Your Changes**
   ```bash
   git commit -m "YOUR_COMMIT_MESSAGE"
   ```
   - Commits the staged changes with a descriptive message. The message should explain the purpose of the changes.

#### 6. **Pushing Your Branch to the Remote Repository**
   ```bash
   git push origin NAME_OF_BRANCH
   ```
   - Pushes your local branch to the remote repository on GitHub. This makes your changes available to others.

#### 7. **Switching Back to the Main Branch**
   ```bash
   git checkout master
   ```
   - Switches to the `master` branch (use `main` if your repository uses `main` as the default branch).

   ```bash
   git checkout main
   ```

#### 8. **Pulling the Latest Changes from the Main Branch**
   ```bash
   git pull origin master
   ```
   - Fetches and merges the latest changes from the remote `master` branch into your local `master` branch.

   ```bash
   git pull origin main
   ```
   - Fetches and merges the latest changes from the remote `main` branch into your local `main` branch.

#### 9. **Merging a Branch into the Main Branch (Optional)**
   ```bash
   git checkout master
   git pull origin master
   git merge NAME_OF_BRANCH
   ```
   - Switch to the `master` branch, pull the latest changes, and merge your branch into it. Replace `master` with `main` if needed.

#### 10. **Deleting a Branch (Optional)**
   ```bash
   git branch -d NAME_OF_BRANCH
   ```
   - Deletes the branch after it has been merged. Use `-D` instead of `-d` to force delete a branch that hasn’t been merged.

#### 11. **In case of an emergency (optional)**
   To cancel a commit (before pushing), every changes from the last commit will be put back into the staging area:
   ```bash
   git reset --soft HEAD~1
   ```
   To remove everything from the staging area but keep your chages:
   ```bash
   git reset .
   ```

### Tips for Working in Teams
- **Commit Often**: Make small, frequent commits with descriptive messages.
- **Pull Regularly**: Always pull the latest changes from the `master/main` branch before starting new work.
- **Use Pull Requests**: Before merging your branch into `master/main`, create a pull request on GitHub and ask a teammate to review it.
- **Resolve Conflicts Carefully**: If you encounter merge conflicts, resolve them thoughtfully, ensuring you’re not overwriting someone else's work.

This cheat sheet should help your students navigate Git as they work in teams, ensuring a smoother collaboration experience.
