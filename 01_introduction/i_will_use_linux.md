# Linux Setup

Oh! Nice, I see you've decided to use Linux. Excellent choice!

For this class, I recommend the use of Linux, preferably Debian-based systems like Ubuntu. Why? Because this is the system I am most familiar with, so I can effectively assist you with any problems.

## Installing Conda on Linux

1. **Download Miniconda Installer**:

   **Option A - Using wget (easiest method, recommended for CREMI machines):**

   On CREMI machines and Linux in general, the easiest way to download Miniconda is directly from the terminal using `wget`:
   ```bash
   wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
   ```
   This will download the installer to your current directory. Then skip to step 5 to run the installer.

   **Option B - Using a browser:**
   - Visit the [Miniconda download page](https://docs.conda.io/en/latest/miniconda.html).
   - Select the `Miniconda3 Linux 64-bit` installer for Linux.

2. **Open Terminal**:
   - Open your terminal after downloading.

3. **Navigate to the Download Directory**:
   - Use the `cd` command to go to the directory where Miniconda was downloaded, usually the `Downloads` folder:
     ```bash
     cd ~/Downloads
     ```

4. **Check if the .sh file is in the folder**:
   ```bash
   ls

   # Expected file:
   Miniconda3-latest-Linux-x86_64.sh
   ```

5. **Run the Installer**:
   - Execute the installer script:
     ```bash
     bash Miniconda3-latest-Linux-x86_64.sh
     ```

6. **Follow On-Screen Instructions**:
   - Accept the license agreement by pressing `Enter` continuously. (Note: you need to go through the entire license agreement, so just hold down `Enter`. I know, it's tedious.)
   - Type `yes` to proceed with the installation.
   - Press `Enter` to accept the default installation location.
   - The installation might take a few minutes.

7. **Initialize Conda**:
   - At the end, the installer will ask if you wish to initialize Miniconda. Type `yes`.
   - This adds Conda to your PATH and enables Conda commands from the terminal.

8. **Close and Reopen Terminal**:
   - Close the terminal and reopen it for changes to take effect.

9. **Verify Installation**:
   - Run `conda list` to confirm a successful installation.

## Install Essential Libraries

For this class, we will use the `base` environment that comes with Conda. If you see `(base)` at the beginning of your terminal prompt, it worked!

Now, install some essential libraries:

```bash
pip install pandas
pip install matplotlib
pip install ipykernel
```

If all goes well, you're ready to start!

## Installing Visual Studio Code

1. **Download the Visual Studio Installer**:
   - Go to the [Visual Studio Code download page](https://code.visualstudio.com/download).
   - Choose the Linux installer (the one with the penguin). For Debian systems, select the .deb installer.

2. **Open Terminal**:
   - Open your terminal after downloading.

3. **Navigate to the Download Directory**:
   - Use `cd` to go to the directory where the installer was downloaded, usually the `Downloads` folder:
     ```bash
     cd ~/Downloads
     ```

4. **Check if the .deb file is in the folder**:
   ```bash
   ls

   # Expected file:
   code_1.85.2-1705561292_amd64.deb
   ```

5. **Run the Installer**:
   - Execute the installer script. *Note: Superuser privileges are required to install VSCode.*:
     ```bash
     sudo dpkg -i code_1.85.2-1705561292_amd64.deb
     ```

6. **Open VSCode**:
   - After installation, open VSCode from the "Show Applications" menu or by typing `code` in the terminal.

## Setting up VSCode

1. **Create a project folder**: Create a folder for our first project and open it in VSCode (File -> Open Folder).

2. **Install extensions**: Click on the Extensions icon in the left sidebar (or press `Ctrl + Shift + X`) and install:
   - Python
   - Jupyter

3. **Select the Python interpreter**: Press `Ctrl + Shift + P`, type `select interpreter`, and choose the `base` environment.

4. **Test your setup**: Create a new file called `test.ipynb`. This is a Jupyter notebook. Click on a cell, type `print("Hello!")`, and press `Ctrl + Enter` to run it. If it asks you to select a kernel, choose `base`.

---

## Terminal Basics

The terminal is a text-based way to interact with your computer. Here are the essential commands:

| Command | What it does | Example |
|---------|--------------|---------|
| `pwd` | Shows your current location | `pwd` |
| `ls` | Lists files in current folder | `ls` |
| `cd` | Changes directory | `cd Documents` |
| `cd ..` | Goes up one folder | `cd ..` |
| `mkdir` | Creates a new folder | `mkdir my_project` |
| `cp` | Copies a file | `cp file.txt copy.txt` |
| `mv` | Moves or renames a file | `mv old.txt new.txt` |
| `rm` | Deletes a file (careful!) | `rm file.txt` |

**Tips:**
- Use `Tab` to autocomplete file names
- Use `↑` arrow to repeat previous commands
- `~` means your home folder (e.g., `cd ~`)

---

## Following the Class Materials

You have two options to access the class materials:

### Option A: Download directly (simple)

Just download each class directly from the course repository:
1. Go to [github.com/luanteylo/dm_web2026](https://github.com/luanteylo/dm_web2026)
2. Click the green "Code" button and select "Download ZIP"
3. Extract the files to your computer

Repeat this for each new class or when the teacher updates the materials.

### Option B: Fork the repository (recommended)

This option lets you keep your own copy, save your work online, and easily get updates from the teacher.

**1. Create a GitHub account**

Go to [github.com](https://github.com) and sign up for a free account.

**2. Fork the course repository**

1. Go to [github.com/luanteylo/dm_web2026](https://github.com/luanteylo/dm_web2026)
2. Click the "Fork" button (top right)
3. This creates your own copy of the repository

**3. Clone your fork**

```bash
git clone https://github.com/YOUR_USERNAME/dm_web2026.git
cd dm_web2026
```

**4. Set up to receive teacher updates**

```bash
git remote add upstream https://github.com/luanteylo/dm_web2026.git
```

**5. Get updates from the teacher (without losing your work)**

When the teacher adds new materials:
```bash
# Save your current work first
git add .
git commit -m "My work"

# Get updates from the teacher
git fetch upstream
git merge upstream/main

# Push everything to your fork
git push
```

---

## Git Quick Reference

| Command | What it does |
|---------|--------------|
| `git status` | Shows what changed |
| `git add .` | Stages all changes |
| `git commit -m "message"` | Saves your changes |
| `git push` | Uploads to your fork |
| `git fetch upstream` | Gets teacher updates |
| `git merge upstream/main` | Applies teacher updates |

---

Congratulations! You're all set!
