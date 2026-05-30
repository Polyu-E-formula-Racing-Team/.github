# Introduction For New Member

This is the introduction document for new members. We highly recommend any new members to read this introduction to study the function of GitHub and our naming system.

## Table of Content

- [GitHub: What is it & How to use](#github-what-is-it--how-to-use)
- [Project structure](#project-structure)
---

## GitHub: What is it & How to use

### What is GitHub?

GitHub is a git-based code hosting platform that serves as our project version control system. We use Git to manage all our engineering files, including CAD drawings, source codes, and documentation.

#### Key Concepts

- **Repository (Repo)**: A collection of files with complete history
- **Commit**: A snapshot of changes saved to the repository
- **Push**: Uploading committed change to remote server (GitHub)
- **Pull**: Downloading committed change to local machine (Your PC)
- **Branch**: An alternate development path for a project
- **Merge**: Combining changes from one branch into another
- **Pull Request**: A request to merge changes, enabling code review

### How to use GitHub

We recommended using the simplified software from GitHub to manage the repo. You still use your preferred git software/plugin to manage repo.

#### GitHub Desktop: Installation & Setup

##### Step 1: Install GitHub Desktop

1. Download Git Desktop from the official website: https://desktop.github.com/
2. Run the installer and follow the setup wizard
3. Upon first launch, sign in with your GitHub account credentials

##### Step 2: Verify Git Configuration

GitHub Desktop automatically configures Git, but you can verify settings:

```bash
# Test the configuration
git --version
git config --list

# You should able to see the following lines
user.name=<Your username>
user.email=<12345678>+<Your username>@users.noreply.github.com
```

#### Core Operations: Clone, Commit, Push

##### Cloning the Repository

**Via GitHub Desktop:**

1. File → New Repository
2. Enter remote URL or select from recent repositories
3. Choose local folder location

**Via Terminal:**

```bash
git clone https://github.com/Polyu-E-formula-Racing-Team/Intro-for-new-member.git
cd Intro-for-new-member
```

##### Making Changes & Committing

1. Make your changes in any editor (VS Code, Notepad++, etc.)
2. In Git Desktop, you'll see changed files in the **Changes** section
3. Add all files: Click the **+** icon next to file type dropdown
4. Enter a descriptive commit message (e.g., "Added new documentation")
5. Click **Commit to main**

##### Pushing Changes to Remote Repository

After committing locally, you can push changes:

1. In Git Desktop: Right-click on the repository name and select **Push origin**
2. Or use terminal: `git push`

The pushed changes will appear in your GitHub web interface under **Contributors → [Your Name]**

##### Resolving Conflicts

If a conflict occurs during pull:

1. Git Desktop will mark conflicting files with yellow color
2. Open the file in your editor to resolve conflicts manually
3. Mark the conflict as resolved in Git Desktop once done
4. Commit your changes again

### Team Collaboration Tips

#### Before Making Changes

1. **Pull latest code**: Always sync before starting work
2. **Create a feature branch**: Don't modify main directly
3. **Use descriptive commit messages**: Explain what and why
4. **Test your changes**: Ensure no regressions are introduced

#### Commit Best Practices

- Be concise but informative in commit messages
- Group related changes in single commits
- Reference issue/PR numbers when applicable
- Keep atomic commits (one change per commit)
