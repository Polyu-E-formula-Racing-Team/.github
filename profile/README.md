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

## Project structure

### Repo naming

We use our race car code name as the prefix of our repo name, then follow with the project/system name. For example, `06E_VCU` is the repo of our VCU code for our 06E car. Sometimes, you will see the extra naming before the project/system name, like `06E_EEE_PCB` is for the PCB required by EEE sub-team for 06E.

### Repo Structure

We don't have strict requirement for repo structure, but we recommended you to follow the example below.

#### HW & SW project

For the project with both hardware and software design, we will put them in the same repo and store them in separated folders named `HW` and `SW`.

```plaintext
Repo
├── HW
│   ├── CAD files
│   ├── schematic files
│   ├── layout files
│   └── other documents
├── SW
│   ├── inc
│   ├── lib
│   ├── src
│   └── other documents
├── .gitignore
├── LICENSE
└── README.md
```

#### Solidworks Project

For the Solidworks project, the master assembly of the project shall be named as `Master Assembly.sldasm` or `<Project name>.sldasm`

```plaintext
Repo
├── Sub-project 1
│   ├── CAD files
│   ├── Sub-project 1.sldasm
│   └── other documents
├── Sub-project 2
│   ├── CAD files
│   ├── Sub-project 1.sldasm
│   └── other documents
├── Master Assembly.sldasm
├── CAD files
├── .gitignore
├── LICENSE
└── README.md
```

#### PCB project

For PCB project, we follow the following structure.

```plaintext
Repo
├── Documents                           # This where the Altium generate its files
│   ├── <Project name>-Gerber           # This where the Gerber file (for production) generated
│   |   └── Gerber format files 
│   ├── <Project name>-BOM.xlsx         # This is the BOM document (Bill of Material)
│   ├── <Project name>-Gerber.zip       # You need to manually zip the <Project name>-Gerber folder to zip file for submitting to manufactory.
│   ├── <Project name>-Description.zip  # This is generated by Draftman for describing the function of the PCB
│   └── <Project name>-Schematic.pdf    # This is schematic drawing in pdf for quick check
├── <Project name>.bomdoc
├── <Project name>.prjpcb
├── <Project name>.schdoc
├── <Project name>.pcbdoc
├── <Project name>.pcbdwf
├── <Project name>.outjob
├── .gitignore
├── LICENSE
└── README.md
```

#### C/C++ SW project

For the project of C/C++ software design, we follow the classic project structure.

```plaintext
Repo
├── .build          # temporary folder for building process and the binary output (don't upload to github)
├── doc             # folder of documentation and datasheet
├── inc             # folder for header files
├── lib             # folder for 3rd library
├── src             # c/c++ code files
├── .gitignore                    
├── LICENSE
└── README.md
```

#### Simulink project

For the project of Simulink design, we follow the project structure.

```plaintext
Repo
├── MeCa Interface              # telemetry config
├── <Project name>_ec55xx_cw   
|   ├── bin                     # complied binary folder
|   └── ...
├── <Project name>_ec55xx_rtw
├── <xxx>.slx                   # simulink library
├── <xxx>.m                     # matlab code
├── <Project name>.slx          # main simulink project
├── .gitignore                    
├── LICENSE
└── README.md
```

---

*Document Version: 1.0 | Last Updated: May 2026*


