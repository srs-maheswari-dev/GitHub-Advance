# ITC Git and GitHub Advanced Workshop

This repository contains practice scripts and exercises. 

## Workshop Topics

This workshop covers:
- **Pull request** - Code revision with other collaborators
- **Git Stash** - Temporarily save uncommitted changes
- **Reset & Revert** - Undo changes safely
- **Interactive Rebase** - Clean up commit history
  - Squashing commits
  - Rewording commit messages

## Prerequisites

- Git installed on your system
- Basic understanding of Git commands (commit, push, pull)
- Code editor preferably Virtual Studio Code
- Terminal or PowerShell access

## What to Do with This Repository?

### 1. Fork It

Fork your own copy of this repository by clicking on the **Fork** button in the top-right corner of the GitHub page. This creates a copy under your GitHub account.
<img width="1231" height="136" alt="image" src="https://github.com/user-attachments/assets/26354e38-29f0-46c5-bca2-8c50da6e0399" />

### 2. Clone It

Before cloning the repository, navigate to your **Desktop** directory. We're doing this on the desktop for simplicity.

**For Windows:**
Open PowerShell and run:
```powershell
cd C:\Users\<username>\Desktop
```

**For macOS:**
Open Terminal and run:
```bash
cd ~/Desktop
```

Where to get your repository-url (**Do this in your own fork**):
<img width="909" height="128" alt="image" src="https://github.com/user-attachments/assets/6ba8792e-24a8-470b-b7da-4ea33f80913b" />

Then,

<img width="414" height="387" alt="image" src="https://github.com/user-attachments/assets/e5d7b38e-a2ce-4e6a-b0ae-830d3cdb3d98" />

Once you're on your Desktop, clone your forked repository:
```bash
git clone <your-forked-repository-url>
```

> **Note:** Make sure to use the URL from **your own fork**, not the original repository. You can find it by clicking the green "Code" button on your forked repository page.

### 3. Open It in Visual Studio Code

After cloning, a folder with the same name will appear on your Desktop. Open this folder in Visual Studio Code to start the exercises.

```bash
cd GitHub-Advance
code .
```

## Running the Scripts

The scripts inside this repo will populate your git log to set up your local repository for the exercises. Run the scripts in your editor terminal **🚨🗣️ONLY WHEN YOU ARE INSTRUCTED🗣️🚨.**

**For macOS/Linux:**
```bash
bash {script-name}.sh
```

**For Windows (PowerShell):**
```powershell
Set-ExecutionPolicy Bypass -Scope Process 
.\{script-name}.ps1
```

## What the Scripts Do

### populate_repo_squash.sh / populate_repo_squash.ps1

Creates a series of commits for practicing:
- **Squashing commits** - Multiple commits to `config.txt` that modify DEBUG and PORT settings
- **Rewording commits** - A commit with vague message ("update config") to practice better commit messages

After running the script, you'll have:
- 6 commits modifying `config.txt` (for squash practice)
- 1 commit creating `settings.txt` (for reword practice)

### populate_repo.sh / populate_repo.ps1

Creates an initial commit history on the main branch, then switches to a **chloe** branch for hotfix practice:

**Main branch (5 commits):**
- Add greeting feature
- Standardize greeting capitalization
- Add usage documentation
- Extract main entry point
- Add uppercase greeting helper

**Chloe branch (3 additional commits):**
- Add debug statement (app.py contains debug line for attendees to delete)
- Add error.py (dummy file for attendees to delete)
- Add README and gitignore (to avoid overwriting main branch files)

This simulates a hotfix scenario where attendees must clean up mistakes before merging back to main.

## Exercise Files

### From populate_repo_squash.sh:
- `config.txt` - Generated for squash exercises
- `settings.txt` - Generated for reword exercises

### From populate_repo.sh:
- `app.py` - Python application (with debug line to delete on chloe branch)
- `error.py` - Dummy file on chloe branch (for deletion practice)
- `README.md` - Generated on chloe branch
- `.gitignore` - Generated on chloe branch
- `USAGE.md` - Generated on main branch

Additionally, there's a pre-existing:
- `error.py` in the root for workshop warm-up deletion practice

## Useful Resources

- [Vim/NeoVim Cheat Sheet](https://www.notion.so/Vim-NeoVim-Cheat-cheats-2b1fa395dfdd800cb78afe0b69a53d06?source=copy_link) - Quick reference for vim commands

## Need Help?

Ask your facilatator for guidance on any Git operations!
