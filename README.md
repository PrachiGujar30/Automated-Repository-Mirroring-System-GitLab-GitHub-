# 🚀 DevOps Project: Automated Repository Mirroring System (GitLab → GitHub)
## Project Overview
This project demonstrates how to automate repository synchronization from GitLab to GitHub using push mirroring. The GitLab repository acts as the primary source, and all code changes are automatically mirrored to GitHub.
This ensures:
- Continuous backup of source code
- High availability across platforms
- Improved disaster recovery readiness
![Architecture](Architecture.png)
---
## Prerequisites
- Before starting, ensure you have:
- Active GitLab account
- Active GitHub account
- Repository access (Maintainer/Owner in GitLab)
- Git installed on your system

Check Git installation:
```bash
git --version
```
---
## Implementation Steps
### Step 1: Create Repository in GitLab
- Create a new project (blank repository)
- This will act as the primary repository
![gitlab1](1.png)
![gitlab2](2.png)
![gitlab3](3.png)
![gitlab4](4.png)

### Step 2: Create Repository in GitHub
- Create a new empty repository
- This will act as the mirror repository
![github](5.png)
![github](6.png)

### Step 3: Configure Push Mirroring in GitLab
1. Go to Settings → Repository
- Scroll to Mirroring repositories
![repo](7.png)
2. Copy https github URL and Paste in Gitlab 
![repo](8.png)
![repo](9.png)
3. Go to Github and Generate Token for password 
![token](10.png)
![token](11.png)
![token](12.png)
![token](13.png)
![token](14.png)
### Step 4: Clone GitLab Repository
![clone](15.png)
``` bash
git clone <gitlab-repo-url> 
```
``` bash
cd <repo-name>
```
![terminal](16.png)
### Step 5: Add Code and Push
1. Create a sample file
![sample file](17.png)
2. Push the file using Source Control
![Push](18.png)
![Push](19.png)
![gitlab](20.png)
### Step 6: Verify Mirroring
- Check GitHub repository
- All changes from GitLab should automatically reflect
![github](21.png)
## Summary
This project implements an automated repository mirroring system between GitLab and GitHub, where changes from GitLab are automatically synchronized to GitHub using push mirroring. It uses secure token-based authentication to ensure seamless and safe communication while eliminating manual effort. The system enhances code availability, provides backup across platforms, and supports disaster recovery, reflecting key DevOps practices like automation and reliability.