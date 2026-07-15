# Repository Mirroring Between GitHub and GitLab Using Git

## Introduction

This project demonstrates a repository mirroring workflow where code developed on a local machine is synchronized with both GitHub and GitLab using multiple Git remotes. Changes made in the local repository are pushed to both platforms, ensuring that each repository remains consistent and up to date. This implementation provides a practical approach to maintaining identical codebases across multiple Git hosting platforms through manual repository mirroring.

#### This approach is commonly used for:
* Backup repositories
* Multi-platform availability
* Professional Git workflows

## Architecture Diagram

![alt text](<Images/Architecture Diagram.png>)

## Tools and Platforms Used

* Local Machine (Windows)
* Git Bash
* VS Code
* GitHub
* GitLab

## Step-by-Step Mirroring Workflow

### Step 1 : Create Repository on GitHub

1. Login to GitHub
2. Click New Repository
3. Enter repository name
4. Create repository

![alt text](<Images/Screenshot (1073).png>)

![alt text](<Images/Screenshot (1074).png>)

### Step 2 : Create Repository on GitLab

1. Login to GitLab
2. Click New Project / Repository
3. Enter repository name
4. Create repository

![alt text](<Images/Screenshot (1075).png>)

![alt text](<Images/Screenshot (1076).png>)

![alt text](<Images/Screenshot (1078).png>)

### Step 3 : Configure Repository Mirroring in GitLab (HTTPS URL)

1. Open your GitLab repository

2. Go to Settings → Repository

3. Scoll to Mirroring repositories

4. Select add new

5. Paste the GitHub repository HTTPS URL
6. Save the mirror configuration

![alt text](<Images/Screenshot (1079).png>)

![alt text](<Images/Screenshot (1080).png>)

![alt text](<Images/Screenshot (1081).png>)

### Step 4 : Create GitHub Personal Access Token
1. Login to GitHub
2. Go to Settings → Developer settings
3. Open Personal access tokens
4. Select Generate new token (Classic)
5. Give a token name
6. Set token expiration (limit days as required)
7. Set token visibility as private
8. Select all required permissions (check all boxes)
9. Generate the token, copy it, and paste this token into the GitLab repository mirroring authentication section

![alt text](<Images/Screenshot (1082).png>)

![alt text](<Images/Screenshot (1083).png>)

![alt text](<Images/Screenshot (1084).png>)

![alt text](<Images/Screenshot (1085).png>)

### Step 5 : Clone One Repository to Local Machine

You can clone either GitHub or GitLab repository

```bash
git clone https://gitlab.com/username/repo-name.git
cd repo-name
```
![alt text](<Images/Screenshot (1086).png>)

* Right-click inside the folder, click Show more options, then select Open Git Bash here to open Git Bash in this directory

![alt text](<Images/Screenshot (1087).png>)

![alt text](<Images/Screenshot (1088).png>)

### Step 6 : Open Project in VS Code

```bash
code . ; exit
```

![alt text](<Images/Screenshot (1089).png>)

---

### Step 7 : Create or Modify Files Locally
Examples:
* index.html
* README.md

##### Stage and Commit Changes
git status
git add .
git commit -m "Commit for mirroring to GitHub and GitLab"

### Step 8 : Push File into Gitlab and Github 

```bash
git push -u origin main

```
![alt text](image.png)

![alt text](<Images/Screenshot (1093).png>)

![alt text](<Images/Screenshot (1094).png>)


---
## Summary

This project demonstrates a repository mirroring workflow that synchronizes source code between GitHub and GitLab from a single local Git repository. The project is developed locally using Git and Visual Studio Code, while both remote repositories remain synchronized through GitLab Repository Mirroring and multiple Git remotes.

The implementation includes creating repositories on GitHub and GitLab, configuring GitLab Repository Mirroring using the GitHub HTTPS repository URL, generating a GitHub Personal Access Token (PAT) for secure authentication, and managing version control operations using Git. Code changes committed locally are pushed to both platforms, ensuring that the repositories remain consistent and up to date.

This solution enhances code redundancy, simplifies multi-platform repository management, and demonstrates practical Git workflows and repository synchronization techniques commonly adopted in modern software development and DevOps environments.