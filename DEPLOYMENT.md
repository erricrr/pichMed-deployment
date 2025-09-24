# 🚀 GitHub Pages Deployment Guide

This guide will help you deploy your pygame project to GitHub Pages.

## 📋 Prerequisites

- GitHub repository (already set up)
- Python environment with pygame and pygbag installed

## 🛠️ Setup Steps

### 1. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** tab
3. Scroll down to **Pages** section in the left sidebar
4. Under **Source**, select **Deploy from a branch**
5. Select **main** branch and **/docs** folder
6. Click **Save**

### 2. Automatic Deployment (Recommended)

The repository is configured with GitHub Actions for automatic deployment:

- Every push to the `main` branch will automatically build and deploy
- The workflow is located in `.github/workflows/deploy.yml`
- No manual intervention required

### 3. Manual Deployment (Alternative)

If you prefer manual deployment:

```bash
# Build the game for web (preserves custom HTML files)
python build_for_github_pages.py

# Commit and push changes
git add docs/
git commit -m "Update game build"
git push origin main
```

**Note:** The build script automatically preserves your custom `index.html` and `game.html` files in the docs folder, so you don't need to worry about losing your customizations when rebuilding.

## 🌐 Access Your Game

Once deployed, your game will be available at:
```
https://yourusername.github.io/pichardoMedina/
```

Replace `yourusername` with your actual GitHub username.

## 🔧 Troubleshooting

### Build Issues
- Make sure you're in the project root directory
- Ensure all dependencies are installed: `pip install pygame pygbag`
- Check that the source directory contains `main.py`

### GitHub Pages Issues
- Verify the Pages source is set to `/docs` folder
- Check the Actions tab for any failed workflows
- Ensure the `docs` folder contains the necessary files:
  - `index.html` (landing page - can be custom)
  - `game.html` (game page - can be custom)
  - `source.apk` (game data)
  - `favicon.png` (icon)

### Game Not Loading
- Check browser console for errors
- Ensure all files are properly uploaded
- Verify the APK file is not corrupted

## 📁 File Structure

```
docs/
├── index.html                    # Landing page (can be custom)
├── game.html                     # Game page (can be custom)
├── source.apk                    # Game data
└── favicon.png                   # Site icon
```

## 🎮 Game Features

- Multiple themed levels
- Progressive difficulty
- Sound effects and music
- High score tracking
- Responsive controls

## 📞 Support

If you encounter any issues:
1. Check the GitHub Actions logs
2. Verify all files are in the docs folder
3. Test the game locally first
4. Check browser compatibility

Happy gaming! 🎉
