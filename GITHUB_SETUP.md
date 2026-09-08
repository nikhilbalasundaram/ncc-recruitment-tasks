# GitHub Repository Setup Guide

## 📦 How to Create a GitHub Repository for Submission

### **Step 1: Create a GitHub Account (if you don't have one)**
1. Go to https://github.com/join
2. Sign up with your email
3. Verify your email
4. Complete your profile

### **Step 2: Create a New Repository**

1. **Go to GitHub Homepage** - https://github.com
2. **Click the "+" icon** at the top right corner
3. **Select "New repository"**
4. **Fill in the repository details**:
   - **Repository name**: `ncc-recruitment-tasks` (or your preferred name)
   - **Description**: `Newton School Coding Club - Recruitment Tasks (1st Year Technical Domain)`
   - **Public/Private**: Select "Public" (required for submission)
   - **Initialize with README**: Leave unchecked (we'll add our README)
   - **Add .gitignore**: Not necessary for this project
   - **Add license**: You can choose MIT License

5. **Click "Create repository"**

### **Step 3: Upload Your Files to GitHub**

#### **Option A: Using GitHub Web Interface (Easiest)**

1. **Go to your repository** (e.g., github.com/yourusername/ncc-recruitment-tasks)
2. **Click "Add file" → "Upload files"**
3. **Drag and drop these files**:
   - `task1_signup.html`
   - `task2_personal_intro.html`
   - `README.md`
   - `GITHUB_SETUP.md` (optional)

4. **Add commit message**: "Initial commit: Add recruitment tasks"
5. **Click "Commit changes"**

#### **Option B: Using Git Command Line (Recommended)**

**If you have Git installed:**

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/ncc-recruitment-tasks.git
cd ncc-recruitment-tasks

# 2. Copy your HTML and README files into this folder
# (Copy task1_signup.html, task2_personal_intro.html, README.md)

# 3. Stage files for commit
git add .

# 4. Create initial commit
git commit -m "Initial commit: Add NCC recruitment tasks"

# 5. Push to GitHub
git push origin main
```

### **Step 4: Verify Files in Repository**

- Visit your repository URL
- You should see:
  ```
  ncc-recruitment-tasks/
  ├── README.md (displays automatically)
  ├── task1_signup.html
  ├── task2_personal_intro.html
  └── GITHUB_SETUP.md (optional)
  ```

---

## 📁 Repository Structure

```
ncc-recruitment-tasks/
│
├── README.md                    # Main documentation
├── GITHUB_SETUP.md             # This file
├── task1_signup.html           # Task 1: Signup Form
├── task2_personal_intro.html   # Task 2: Personal Introduction
│
└── (optional folders)
    ├── assets/                 # Images, screenshots
    │   └── demo-screenshot.png
    └── docs/                   # Additional documentation
        └── concepts.md
```

---

## 🎬 Create a Demo Video

### **What to Demonstrate**

#### **Task 1 Demo (2-3 minutes)**
1. Show the signup form
2. Fill in valid details (username, email, password)
3. Click signup button
4. Show success message
5. Switch to dashboard view
6. Show user data in table
7. Click delete button and show data removed
8. Fill another user and show in dashboard
9. Show dark mode toggle (if implemented)

#### **Task 2 Demo (2-3 minutes)**
1. Show the personal introduction page
2. Scroll through different sections (hero, skills, interests)
3. Demonstrate responsive design by resizing browser
4. Show hover effects on skill cards
5. Click social media links
6. Toggle dark/light mode
7. Show mobile view

### **Recording Tools**
- **Windows**: OBS Studio (free), Camtasia, ScreenFlow
- **Mac**: QuickTime, ScreenFlow, OBS Studio
- **Online**: Loom.com, Screencastify
- **Mobile**: Use built-in screen recording

### **Upload Video**
- Create a folder `videos/` in your repository
- Upload the demo video to your repository
- **OR** Upload to YouTube and link in README
- **OR** Create a `demo-video-link.txt` file with YouTube URL

---

## 📝 Create Comprehensive README

Your README should include:

```markdown
# Newton School Coding Club - Recruitment Tasks

## 📋 Overview
- Brief description of both tasks
- Links to live demos

## 🚀 How to Run
- Step-by-step instructions for each task
- No installation needed

## ✨ Features
- Task 1 features
- Task 2 features
- Bonus features (brownie subtasks)

## 💡 Technologies Used
- HTML5, CSS3, JavaScript
- Specific libraries/frameworks

## 📚 Concepts Learned
- Key learnings from each task
- Challenges overcome

## 🔗 Links
- Live demo (GitHub Pages - see below)
- Video demo link
- GitHub repository

## 📞 Contact
Your email and phone
```

---

## 🌐 Deploy with GitHub Pages (Optional)

This allows running the HTML files directly from GitHub:

### **Step 1: Enable GitHub Pages**
1. Go to repository settings
2. Scroll to "GitHub Pages" section
3. Select branch: `main`
4. Select folder: `/root` or `/(docs)`
5. Save

### **Step 2: Access Your Pages**
- **Task 1**: `https://yourusername.github.io/ncc-recruitment-tasks/task1_signup.html`
- **Task 2**: `https://yourusername.github.io/ncc-recruitment-tasks/task2_personal_intro.html`

### **Update README**
Add these links to your README:
```markdown
## 🌐 Live Demo

- [Task 1 - Signup Form](https://yourusername.github.io/ncc-recruitment-tasks/task1_signup.html)
- [Task 2 - Personal Introduction](https://yourusername.github.io/ncc-recruitment-tasks/task2_personal_intro.html)
```

---

## ✅ Final Checklist Before Submission

- [ ] Repository created and public
- [ ] All three files uploaded:
  - [ ] `task1_signup.html`
  - [ ] `task2_personal_intro.html`
  - [ ] `README.md`
- [ ] README contains:
  - [ ] How to run instructions
  - [ ] Features implemented
  - [ ] Technologies used
  - [ ] Concepts learned
  - [ ] Any additional features
- [ ] Code is clean and commented
- [ ] No sensitive information in repository
- [ ] Files are tested and working
- [ ] GitHub Pages enabled (optional but recommended)
- [ ] Demo video created and uploaded/linked
- [ ] Repository has proper description

---

## 📝 Sample Repository Description

```
Newton School Coding Club - 1st Year Recruitment Tasks
✨ Task 1: Signup Form with Validation & Dashboard
✨ Task 2: Personal Introduction Page with Dark Mode
🎯 HTML5 | CSS3 | Vanilla JavaScript | localStorage
🔗 Live Demo: [Link to GitHub Pages]
📹 Demo Video: [Link to YouTube]
```

---

## 🚨 Common Issues & Solutions

### **Issue: Files not showing in GitHub**
- **Solution**: Make sure files are in the root directory
- Check file extensions (.html, .md)
- Refresh your GitHub page

### **Issue: GitHub Pages not working**
- **Solution**: 
  - Go to Settings → Pages
  - Select `main` branch
  - Wait 1-2 minutes for deployment
  - Check if repository is public

### **Issue: How to edit files after upload**
- **Solution**:
  1. Click on file in repository
  2. Click the pencil icon (Edit)
  3. Make changes
  4. Commit directly to main branch

### **Issue: Need to update code**
- **Solution**: 
  - Click on file
  - Click pencil icon to edit
  - Make changes and commit
  - OR Re-upload the file and replace it

---

## 📚 Additional Resources

### **Git & GitHub Learning**
- GitHub Hello World: https://guides.github.com/activities/hello-world/
- Git Documentation: https://git-scm.com/doc
- GitHub Guides: https://guides.github.com/

### **Markdown Formatting**
- Markdown Guide: https://www.markdownguide.org/
- GitHub Flavored Markdown: https://github.github.com/gfm/

### **Demo Video Recording**
- OBS Studio Tutorial: https://obsproject.com/wiki/OBS-Studio-Overview
- Loom Tutorial: https://www.loom.com/
- ScreenFlow (Mac): https://www.telestream.net/screenflow/

---

## 🎯 Submission Steps Summary

1. ✅ Create GitHub repository
2. ✅ Upload all required files
3. ✅ Write comprehensive README
4. ✅ Create demo video
5. ✅ Enable GitHub Pages (optional)
6. ✅ Test all functionality
7. ✅ Copy repository URL
8. ✅ Submit via the form: https://forms.gle/6JBrPJCsQPzWjWKy6

---

## 📞 Need Help?

If you face any issues:
1. Check GitHub documentation
2. Review this guide again
3. Contact NCC organizers:
   - Email: nscc@srmist.edu.in
   - Phone: +91 8603405145

---

**Happy coding! Good luck with your recruitment! 🚀**
