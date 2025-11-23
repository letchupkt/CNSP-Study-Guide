# GitHub Repository Setup Guide

Follow these steps to push this CNSP Study Guide to your GitHub account.

## Prerequisites

- Git installed on your system
- GitHub account (username: letchupkt)
- GitHub CLI or personal access token (for authentication)

## Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com)
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Fill in the details:
   - **Repository name**: `CNSP-Study-Guide` (or your preferred name)
   - **Description**: "Comprehensive study guide for CNSP exam - Passed with 83% merit"
   - **Visibility**: Public (recommended for sharing)
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
5. Click "Create repository"

## Step 2: Connect Local Repository to GitHub

The repository is already initialized with git. Now connect it to GitHub:

```bash
# Add your GitHub repository as remote
git remote add origin https://github.com/letchupkt/CNSP-Study-Guide.git

# Verify the remote was added
git remote -v
```

## Step 3: Push to GitHub

```bash
# Push your code to GitHub
git push -u origin master
```

If you encounter authentication issues, you may need to:

### Option A: Use GitHub CLI (Recommended)
```bash
# Install GitHub CLI if not already installed
# Then authenticate
gh auth login

# Push again
git push -u origin master
```

### Option B: Use Personal Access Token
1. Go to GitHub Settings → Developer settings → Personal access tokens
2. Generate new token with `repo` scope
3. Use token as password when prompted

## Step 4: Verify Upload

1. Go to your GitHub repository URL
2. Verify all files are uploaded
3. Check that README.md displays correctly

## Step 5: Add Repository Topics (Optional but Recommended)

On your GitHub repository page:
1. Click the gear icon next to "About"
2. Add topics:
   - `cnsp`
   - `cybersecurity`
   - `certification`
   - `study-guide`
   - `network-security`
   - `secops-group`
   - `exam-preparation`
   - `security-certification`

## Step 6: Enable GitHub Pages (Optional)

To create a website from your repository:
1. Go to repository Settings
2. Scroll to "Pages" section
3. Under "Source", select "main" branch
4. Click "Save"
5. Your guide will be available at: `https://letchupkt.github.io/CNSP-Study-Guide/`

## Repository Structure

```
CNSP-Study-Guide/
├── README.md                    # Main overview
├── AUTHOR.md                    # Your profile
├── LICENSE                      # MIT License
├── CONTRIBUTING.md              # Contribution guidelines
├── SETUP.md                     # This file
├── .gitignore                   # Git ignore rules
└── docs/
    ├── exam-overview.md         # Exam details
    ├── syllabus.md              # Topics covered
    ├── study-materials.md       # Resources
    ├── practice-questions.md    # 64 practice questions
    ├── quick-reference.md       # Cheat sheet
    ├── certification.md         # Passing criteria
    └── my-experience.md         # Your 83% merit story
```

## Sharing Your Repository

Once uploaded, share your repository:

### LinkedIn Post Example:
```
🎉 Excited to share my CNSP Study Guide! 

I recently passed the Certified Network Security Practitioner (CNSP) exam 
with 83% merit and created a comprehensive study guide to help others succeed.

📚 Includes:
✅ Complete syllabus breakdown
✅ 64 practice questions with answers
✅ Study materials and resources
✅ My personal exam experience
✅ Quick reference cheat sheet

Check it out: https://github.com/letchupkt/CNSP-Study-Guide

#Cybersecurity #CNSP #NetworkSecurity #CertificationPrep #InfoSec
```

### Instagram Post Caption:
```
🔐 Just published my CNSP Study Guide on GitHub! 

Passed with 83% merit and want to help others succeed 💪

Link in bio or search: letchupkt/CNSP-Study-Guide

#cybersecurity #cnsp #networksecurity #ethicalhacking #infosec #studyguide
```

### Twitter/X Post:
```
🎓 New open-source project: CNSP Study Guide

Comprehensive resource for the Certified Network Security Practitioner exam
- 64 practice questions
- Complete syllabus
- Study materials
- Personal 83% merit experience

https://github.com/letchupkt/CNSP-Study-Guide

#Cybersecurity #CNSP
```

## Maintaining Your Repository

### Adding Updates
```bash
# Make changes to files
# Then commit and push
git add .
git commit -m "Update: [describe your changes]"
git push
```

### Accepting Contributions
1. Review pull requests from contributors
2. Merge valuable additions
3. Thank contributors in README or CONTRIBUTING.md

## Star and Watch

Don't forget to:
- ⭐ Star your own repository (shows confidence!)
- 👁️ Watch for issues and pull requests
- 📢 Share with your network

## Need Help?

If you encounter issues:
1. Check GitHub documentation: https://docs.github.com
2. Search Stack Overflow
3. Contact GitHub Support

---

**Good luck with your repository! 🚀**

Created by: Lakshmikanthan K (letchupkt)  
Portfolio: https://letchupkt.vgrow.tech
