# Practical 01: Project Folder and Terminal Navigation

## Aim
To set up a structured web project directory hierarchy using command-line interface (CLI) commands and demonstrate essential terminal navigation and file management operations.

---

## Environment & Prerequisites
- **Operating System:** macOS / Linux / Unix-based shell
- **Shell:** `zsh` / `bash`
- **Utility Tools:** Terminal, basic POSIX file utilities (`mkdir`, `cd`, `ls`, `touch`, `pwd`)

---

## Step-by-Step Terminal Execution

### 1. Identify Current Working Directory
Verify the starting location before creating project folders:
```bash
pwd
```
*Output:*
```text
/Users/nilayraj/Web_Dev_Lab
```

### 2. Scaffold the Project Directory Structure
Create a root project folder along with nested subdirectories for stylesheets, scripts, assets, and documentation using the `-p` (parents) flag:
```bash
mkdir -p dev-portfolio/{css,js,assets/images,docs}
```

### 3. Enter the Project Folder
Change directory into the newly created portfolio root:
```bash
cd dev-portfolio
```

### 4. Create Initial Project Files
Initialize boilerplate files across respective subdirectories:
```bash
touch index.html css/style.css js/main.js docs/README.md
```

### 5. Inspect Directory Contents and Permissions
List all files including hidden ones with long listing format to verify permissions and sizes:
```bash
ls -la
```

### 6. Subdirectory Navigation & Relative Path Traversal
Navigate through subdirectories and traverse back using relative paths:
```bash
# Move into css directory
cd css
pwd

# Traverse one level up back to dev-portfolio
cd ..
pwd

# Traverse directly into assets/images
cd assets/images
pwd

# Return to project root using relative parent path
cd ../..
pwd
```

### 7. Verify the Complete Folder Hierarchy
Display the directory tree structure:
```bash
find . -not -path '*/.*'
```

---

## Resulting Directory Hierarchy
```text
dev-portfolio/
├── assets/
│   └── images/
├── css/
│   └── style.css
├── docs/
│   └── README.md
├── js/
│   └── main.js
└── index.html
```

---

## Terminal Commands Reference

| Command | Syntax / Example | Purpose / Description |
|---|---|---|
| `pwd` | `pwd` | Print Working Directory — outputs the full absolute path of the current shell location. |
| `mkdir` | `mkdir -p dir/{sub1,sub2}` | Make Directory — creates new folders. Flag `-p` creates parent folders without error if they exist. |
| `cd` | `cd path/to/dir` | Change Directory — shifts the shell session to the target path. |
| `cd ..` | `cd ..` | Moves the current location one level up to the parent directory. |
| `ls` | `ls -la` | List — displays directory contents. `-l` gives detailed metadata; `-a` displays hidden files. |
| `touch` | `touch file.ext` | Creates an empty file or updates the access and modification timestamps of an existing file. |
| `find` | `find . -type f` | Searches for files and directories matching conditions within a hierarchy. |

---

## Learning Outcomes
1. Demonstrated fluency in CLI shell navigation without relying on graphical file managers.
2. Built an industry-standard directory scaffolding for web projects separating assets, scripts, styles, and documents.
3. Mastered relative vs. absolute path traversal in terminal sessions.
