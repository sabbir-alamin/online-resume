# Project Structure & Setup Guide

## Required Folder Structure

Create the following folder structure in your repository root:

```
portfolio/
│
├── index.html                    # Main resume page
├── contact.html                  # Contact information page
├── hobbies.html                  # Hobbies page
├── README.md                     # Project documentation
├── LICENSE                       # MIT License
├── .gitignore                    # Git ignore rules
│
└── assets/                       # Assets folder
    └── images/                   # Images subfolder
        └── photo.png             # Profile photograph
```

## Setup Instructions

### Step 1: Create the Project Directory
```bash
mkdir portfolio
cd portfolio
```

### Step 2: Create the Assets Folder Structure
```bash
mkdir -p assets/images
mkdir -p assets/css
mkdir -p assets/js
```

### Step 3: Copy Files
Copy the following files to your project root:
- `index.html`
- `contact.html`
- `hobbies.html`
- `README.md`
- `LICENSE`
- `.gitignore`

Copy `photo.png` to:
- `assets/images/photo.png`

### Step 4: Initialize Git Repository
```bash
cd portfolio
git init
git add .
git commit -m "Initial commit: Portfolio website"
```

### Step 5: Add Remote Repository (GitHub)
```bash
# Create a new repository on GitHub first, then:
git remote add origin https://github.com/yourusername/portfolio.git
git branch -M main
git push -u origin main
```

## Folder Descriptions

### Root Directory
Contains all HTML pages and configuration files:
- **index.html** - Main resume/homepage
- **contact.html** - Contact information
- **hobbies.html** - Personal interests

### assets/
Contains all project assets and resources.

#### assets/images/
Image files used throughout the website:
- **photo.png** - Profile photograph (currently 100px height)

#### assets/css/ (Future)
Where to place stylesheets when adding CSS styling:
- `style.css` - Main stylesheet
- `responsive.css` - Mobile responsiveness (optional)

#### assets/js/ (Future)
Where to place JavaScript files for interactivity:
- `script.js` - Main JavaScript file

## Future Enhancements

### Styling (CSS)
When you add CSS, create `assets/css/style.css` and uncomment the link in all HTML files:

```html
<link rel="stylesheet" href="./assets/css/style.css">
```

### JavaScript
When you add JavaScript, create `assets/js/script.js` and uncomment the script tag before closing `</body>`:

```html
<script src="./assets/js/script.js"></script>
```

### Additional Pages
For any new pages:
1. Create the `.html` file in the root directory
2. Add navigation links to `index.html`, `contact.html`, and `hobbies.html`
3. Follow the same HTML structure with semantic elements

## File Size Reference

- `photo.png` - Approximately 1.2 MB (Consider optimizing for web)

### Image Optimization Tips
```bash
# Using ImageMagick (if installed)
convert photo.png -resize 500x500 -quality 85 photo_optimized.png

# Using web tools
# - TinyPNG (tinypng.com)
# - Squoosh (squoosh.app)
```

## GitHub Repository Setup

### Create a New Repository

1. Go to [GitHub.com](https://github.com/new)
2. Repository name: `portfolio`
3. Description: "Personal portfolio and resume website"
4. Choose: Public (for portfolio showcase)
5. Add `.gitignore`: None (already included)
6. License: MIT

### Push to GitHub

```bash
git remote add origin https://github.com/yourusername/portfolio.git
git add .
git commit -m "Initial commit: Personal portfolio website"
git push -u origin main
```

## GitHub Pages Deployment (Recommended)

To make your portfolio live at `yourusername.github.io/portfolio`:

1. Go to repository Settings
2. Navigate to "Pages" section
3. Source: Deploy from a branch
4. Branch: main
5. Folder: / (root)
6. Save

Your site will be live at: `https://yourusername.github.io/portfolio`

## Updating Your Portfolio

To update your content:

```bash
# Make changes to HTML files
# Then commit and push:
git add .
git commit -m "Update: [description of changes]"
git push
```

Changes will be live on GitHub Pages within 1-2 minutes.

## Useful Git Commands

```bash
# Check status
git status

# View commit history
git log

# Create a new branch for changes
git checkout -b feature/new-feature

# Merge branch back to main
git checkout main
git merge feature/new-feature

# Delete a branch
git branch -d feature/new-feature
```

---

**Last Updated**: 2024
