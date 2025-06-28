Git and GitHub in Action – A Step-by-Step Guide
1. Install Git CLI
Download and install the Git CLI from the official Git website if it’s not already installed.
To verify the installation:

Open a terminal (Command Prompt, PowerShell, or Terminal) and run:
git --version

This displays the installed Git version, confirming successful installation.



2. Configure Git
Set up your Git user information (run once per system):
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

To verify your configuration:
git config --global --list


3. Create a New GitHub Repository

Go to GitHub and sign in.
Click New to create a repository.
Name the repository, add an optional description, and choose visibility (public/private).
Optionally initialize with a README.md or .gitignore.
Click Create repository.


4. Initialize a Local Git Repository
Navigate to your project directory in the terminal and run:
git init

This creates a hidden .git folder, initializing a new Git repository.

5. Understand File States
Git tracks files in these states:

Untracked (U): Files not tracked by Git.
Staged (A): Files added to the staging area, ready to commit.
Committed: Changes saved to the local repository.
Modified (M): Tracked files with uncommitted changes.


6. Create a README.md File
Create a README.md file in your project directory to describe your project. Example:
# My Project
A brief description of your project.

Use a text editor or run:
echo "# My Project" > README.md


7. Check File Status
Check the status of files in your repository:
git status

This shows untracked, staged, or modified files.

8. Stage Files
To stage files for committing:

For a specific file:
git add README.md


For all files:
git add .




9. Commit Changes
Commit staged files to the local repository:
git commit -m "Initial commit with README"

Use descriptive commit messages to document changes.

10. Check or Create a Branch
View all branches:
git branch

The default branch is typically main. To rename it (if needed):
git branch -M main

Verify the current branch (marked with *):
git branch


11. Connect Local Repo to GitHub
Link your local repository to the GitHub repository:
git remote add origin https://github.com/username/repository-name.git

Verify the remote connection:
git remote -v


12. Push Code to GitHub
Push your local commits to the main branch on GitHub:
git push -u origin main

The -u flag sets the upstream branch for future pushes.

13. Add .gitignore File
Create a .gitignore file to exclude files/folders from being tracked. Example:
# .gitignore
venv/
node_modules/
*.log

Create it using:
echo "venv/" > .gitignore


14. Pull Updates from GitHub
Sync your local repository with GitHub:
git pull origin main

This fetches and merges changes from the remote main branch.

15. Create and Work on a Feature Branch
Create a new feature branch (e.g., for developer A):
git branch feature/dev_A

Switch to the branch:
git checkout feature/dev_A

Make changes, stage, and commit:
git add .
git commit -m "Add feature X"


16. Merge Changes to Main
Switch to the main branch:
git checkout main

Merge the feature branch:
git merge feature/dev_A

If no conflicts occur, delete the feature branch:
git branch -d feature/dev_A

Push updates to GitHub:
git push origin main


17. Handling Merge Conflicts
If a merge conflict occurs during git pull or git merge:

Run:
git pull origin main


Git marks conflicting files. Open them in a text editor to resolve conflicts, choosing or combining changes.

Mark resolved files:
git add .


Complete the merge:
git commit -m "Resolve merge conflict"


Push to GitHub:
git push origin main




18. View Commit History
View the commit history:
git log --oneline --graph

This shows a concise, visual history of commits.

19. Additional Tips

Undo Changes: To discard unstaged changes:
git restore .


Clone a Repository: To download an existing repository:
git clone https://github.com/username/repository-name.git


Best Practices:

Commit frequently with clear messages.
Use branches for features or bug fixes.
Regularly pull updates to avoid conflicts.


