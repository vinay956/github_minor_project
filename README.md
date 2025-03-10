# GitHub Practice Guide

This guide will help you get familiar with Git, GitHub, and version control through a series of practical tasks. Follow the steps below to practice Git and GitHub workflows.

## 1. Setting Up Your GitHub Account and Git

If you haven't already, follow these steps to set up your GitHub and Git environment.

- **Create a GitHub Account:** If you don’t have one already, go to [GitHub](https://github.com) and sign up.
- **Install Git:** If Git is not installed on your system, install it.
  - On Linux (Ubuntu/Debian):
    ```bash
    sudo apt update
    sudo apt install git
    ```

## 2. Create a Local Git Repository

Start by creating a new project folder on your local system and initialize it with Git.

```bash
# Create a new folder for your project
mkdir MyFirstProject
cd MyFirstProject

# Initialize a Git repository
git init
```
3. Create a New File and Add Content
Create a simple text file to start practicing.

```bash
Copy
# Create a new text file
echo "Hello, GitHub!" > hello.txt
```
4. Add Files to Git and Commit
Now, let's add the new file to the Git repository and commit the changes.

```bash
Copy
# Add the file to Git
git add hello.txt

# Commit the changes
git commit -m "Initial commit with hello.txt"
```
5. Create a Remote GitHub Repository
Go to GitHub and create a new repository (without a README for now). Copy the repository URL for the next steps.

6. Link Local Repo to GitHub and Push
Now, let's push your local repository to GitHub.

```bash
Copy
# Add your remote GitHub repository
git remote add origin https://github.com/yourusername/MyFirstProject.git
# Push the local repository to GitHub
git push -u origin master
```
7. Make Changes Locally and Push
Make some changes to your file, and practice committing and pushing.

```bash
Copy
# Modify the file
echo "Welcome to GitHub!" >> hello.txt

# Stage the changes
git add hello.txt

# Commit the changes
git commit -m "Added welcome message"

# Push the changes to GitHub
git push origin master
```
8. Create a New Branch
Branches help in managing separate features or fixes. Create and switch to a new branch.

```bash
Copy
# Create a new branch
git checkout -b feature-branch

# Make changes to the file
echo "This is a feature branch" >> hello.txt

# Add and commit changes
git add hello.txt
git commit -m "Updated the file on feature-branch"
```
9. Push the New Branch to GitHub
Push your new branch to GitHub.

```bash
Copy
# Push the branch to GitHub
git push -u origin feature-branch
```
10. Create a Pull Request (PR)
Go to GitHub and open the repository.
You'll see a notification to compare and create a pull request for the feature-branch.
Click on "Compare & Pull Request".
Write a description of the changes you made and click "Create Pull Request".
After reviewing, you can merge the pull request.
11. Merge the Pull Request Locally
Once the PR is merged, you can pull the changes back to your local machine.

```bash
Copy
# Switch back to the master branch
git checkout master

# Pull the latest changes (including the merge from the PR)
git pull origin master
```
12. Delete the Feature Branch
After the PR is merged, you can delete the feature branch both locally and on GitHub.

```bash
Copy
# Delete the local branch
git branch -d feature-branch

# Delete the remote branch
git push origin --delete feature-branch
```
13. Fork and Clone a Repository (Collaboration Practice)
Collaborating on GitHub usually involves forking someone else’s repository and contributing to it. Here’s how to practice:

Fork a Repository:

Go to any public GitHub repository and click on the Fork button.
Clone Your Forked Repository:

After forking, clone your forked repository to your local machine.
bash
Copy
git clone https://github.com/yourusername/forked-repo.git
cd forked-repo
Make Changes, Commit, and Push to Your Forked Repo:

Make changes, add files, and commit them as shown in previous steps. Then, push to your forked repository:
bash
Copy
git push origin master
Create a Pull Request to the Original Repository:

Go back to the original repository (where you forked from) and create a pull request from your fork.
Wait for review and possibly merge your changes into the original project.
14. Pull Changes from the Original Repository (Sync Fork)
If you want to keep your fork up to date with the original repository, you can pull the latest changes from the original repository.

bash
Copy
# Add the original repository as an upstream remote
git remote add upstream https://github.com/original-owner/repo-name.git

# Fetch the latest changes from the original repository
git fetch upstream

# Merge the changes into your local master branch
git checkout master
git merge upstream/master

# Push the updated changes to your fork
git push origin master
15. Additional Git Commands for Practice
Check the status of your repository:

bash
Copy
git status
View the commit history:

bash
Copy
git log
Undo the last commit (but keep the changes):

bash
Copy
git reset --soft HEAD~1
Remove a file from the staging area:

bash
Copy
git reset <file>
Show the diff between changes:

bash
Copy
