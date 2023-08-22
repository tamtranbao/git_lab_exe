# Git workshop

# Basic

## Exercise 1: Initializing a Repository

- Open your terminal and navigate to the desired directory where you want to create a new repository.
- Use the command git init to initialize a new repository.
- Use the git status command to check the status of your repository.

## Exercise 2: Adding and Committing Changes

- Create a new file in your repository (e.g., touch file.txt).
- Use the command git status to see the untracked file.
- Add the file to the staging area using the command git add file.txt.
- Use the command git status to ensure that the file has been added to the staging area.
- Commit the changes using the command git commit -m “Add new file”.
- Use the command git log to view the commit history.

## Exercise 3: Working with Branches

- Create a new branch using the command git branch new-branch.
- Switch to the new branch using the command git checkout new-branch.
- Make some changes to a file in this branch (e.g., modify file.txt).
- Add and commit your changes in this branch.
- Switch back to the main branch using the command git checkout main.
- Use the command git merge new-branch to merge the changes from the new branch into the main branch.
- Use the command git branch -d new-branch to delete the branch.

## Exercise 4: Working with Remote Repositories

- Create a new repository on a hosting service like GitHub.
- Link your local repository with the remote repository using the command git remote add origin <remote-repository-url>.
- Use the command git push -u origin main to push your local repository to the remote repository.
- Make some changes to the file on the remote repository using the web interface.
- Use the command git pull origin main to update your local repository with the remote changes.

# Advanced 1

## Exercise 1: Resolving Merge Conflicts

- Create a new branch called feature-branch using the command git checkout -b feature-branch.
- Make some changes to a file in this branch and commit the changes.
- Switch back to the main branch using the command git checkout main.
- Make different changes to the same file in the main branch and commit the changes.
- Attempt to merge the feature-branch into the main branch using the command git merge feature-branch.
- Resolve any merge conflicts that occur in the file.
- Use the command git status to ensure that all conflicts have been resolved.
- Commit the merge changes and continue with the merge process.

## Exercise 2: Reverting Commits

- Identify the commit you want to revert by using the command git log.
- Use the command git revert <commit-hash> to revert the commit identified in the previous step.
- Verify the changes by using the command git log and checking that the commit has been reverted.

## Exercise 3: Working with Stashes

- Make some changes to a file in your repository.
- Use the command git stash to temporarily save your changes.
- Make more changes to the same file.
- Use the command git stash list to see a list of all stashed changes.
- Apply the changes from the stash using the command git stash apply.
- Use the command git stash drop to remove the stash once you have applied the changes.

## Exercise 4: Using Git Cherry-pick

- Identify a specific commit that you want to apply to your current branch.
- Use the command git log to find the commit hash of the desired commit.
- Switch to the branch where you want to apply the commit using the command git checkout <target-branch>.
- Use the command git cherry-pick <commit-hash> to apply the changes from the desired commit.
- Resolve any conflicts that may arise during the cherry-pick process.
- Commit the cherry-picked changes to your branch.

# Advanced 2

## Exercise 1: Using Git Submodules

- Create a new repository called parent-repo.
- Initialize parent-repo as a Git repository using the command git init.
- Create a new repository called child-repo.
- Initialize child-repo as a Git repository using the command git init.
- Add child-repo as a submodule to parent-repo using the command git submodule add <child-repo-url>.
- Make some changes to files within child-repo.
- Commit the changes in child-repo using the command git commit -m "Commit message".
- Go back to parent-repo using the command cd ...
- Commit the change of adding child-repo as a submodule using the command git commit -m "Added child-repo submodule".
- Clone the parent-repo repository on another machine using the command git clone <parent-repo-url>.
- Initialize and update the submodule in the cloned repository using the commands git submodule init and git submodule update.

## Exercise 2: Using Git Hooks

- Navigate to your Git repository's .git/hooks directory.
- Create a new file called pre-commit (without any file extension).
- Add a hook script in the pre-commit file to execute a custom command, such as running tests or linting, before committing.
- Make the pre-commit file executable using the command chmod +x pre-commit.
- Make some changes to a file in your repository and attempt to commit them.
- Observe that the custom command defined in your pre-commit hook script is executed before the commit is made.

## Exercise 3: Using Git Reflog

- Make some changes to your repository and create some commits.
- Use the command git reflog to see a list of all previous HEAD positions and actions.
- Identify a previous HEAD position that you want to revisit.
- Use the command git checkout <commit-hash> to checkout the specific commit or HEAD position.
- Review your repository at that specific commit or HEAD position.

## Exercise 4: Using Git Rebase

- Create a new branch called feature-branch using the command git checkout -b feature-branch.
- Make some changes and commit them to the feature-branch.
- Switch back to the main branch using the command git checkout main.
- Make a new commit in the main branch.
- Use the command git rebase main feature-branch to rebase the feature-branch onto the main branch.
- Resolve any conflicts that may occur during the rebase process.
- Use the command git log to verify that the changes from the feature-branch have been applied to the main branch.
