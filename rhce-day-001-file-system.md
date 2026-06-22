# 🛠️ Day 1 Practical Lab: Navigating the File System

Linux organizes everything into a single, massive tree structure. There are no drive letters (like `C:` or `D:`). Everything starts at the **root directory**, represented by a single forward slash `/`.

---

## Step 1: Locate Yourself

Type this command and hit **Enter** to find your current coordinate in the system:

```bash
pwd
```

- **What it means:** Print Working Directory.
- **Expected Output:** If you are logged in as the `root` user, it will output `/root`. If you are a standard user, it will output `/home/username`.

---

## Step 2: List Contents and Reveal Hidden Configuration Files

To see what files exist in your current location, run:

```bash
ls -la
```

**The breakdown:**
- `ls` lists files.
- The `-l` flag turns on the **long list** format (showing sizes, owners, and permissions).
- The `-a` flag reveals **all** files, including hidden system files that start with a dot `.`.

---

## Step 3: Understand Relative vs. Absolute Paths

- An **absolute path** always starts from the root `/`.
- A **relative path** starts from where you are standing right now.

Let's create a training workspace to practice this:

```bash
mkdir rhce_course
cd rhce_course
pwd
```

**Observe:** Your path changes (e.g., `/root/rhce_course`).

Now, let's jump instantly to the system configuration directory using an **absolute path**:

```bash
cd /etc
pwd
```

Now, let's jump back to your previous folder using the shortcut for your home directory (`~`):

```bash
cd ~/rhce_course
pwd
```

---

## Step 4: The Directory Shortcut Dots

- `.` represents your **current** directory.
- `..` represents the **parent** directory (one level up).

Move up one level right now by typing:

```bash
cd ..
pwd
```

---

## 📝 Short Notes & Memorisation Summary

| Symbol / Command | Meaning |
|---|---|
| `/` (Root) | The parent directory of the entire operating system. |
| `~` (Tilde) | Shortcut for the current logged-in user's home directory. |
| `.` (Single Dot) | The directory you are currently inside. |
| `..` (Double Dot) | The directory directly above your current location. |
| `ls -lh` | Lists files in a "human-readable" format (showing file sizes in KB, MB, or GB instead of raw bytes). |

---

## 🃏 Permanent Memory Flashcards (Copy to Anki)

**Front:** What is the difference between an absolute path and a relative path in Linux?
**Back:** An absolute path always starts from the system root (`/`), while a relative path starts from the current working directory.

**Front:** Which `ls` flags display hidden files and detailed file properties simultaneously?
**Back:** `ls -la` (or `ls -l -a`).

**Front:** In a directory listing, what do the `.` and `..` listings represent?
**Back:** `.` represents the current working directory; `..` represents the parent directory one level up.

---

## 💬 Technical Interview Preparation

**Q:** A junior administrator claims a critical configuration file vanished because `ls` doesn't show it. What is the most likely issue, and how do you verify it?

**A:** The file likely begins with a dot (`.`), making it a **hidden file** in Linux. Standard `ls` ignores hidden files by design. The administrator must run `ls -a` or `ls -la` to see hidden files within that directory.

---

## 🎯 Official RHCSA / RHCE Exam Simulation

**Scenario:** The Red Hat exam grading scripts are entirely automated. They do not care *how* you navigate; they only check if your final configurations exist in the exact required directories.

**Exercise Objective:** Create a specific directory structure using a single command string without moving out of your home directory. Create a directory named `deployments` inside your home directory, and a directory named `production` inside that.

**Execution Command:**

```bash
mkdir -p ~/deployments/production
```

**Exam Tip:** The `-p` flag stands for **parents**. It commands Linux to automatically create any missing parent directories in the path. Without `-p`, the command will fail if the `deployments` folder doesn't already exist.

---

## 🛡️ Day 1 Completion Backup Token

Copy this entire response and save it as a PDF inside your Mac's `RHCE_120_Day_Course` folder.

Your progress validation token for today is:

```
TOKEN: RHCE_120_DAY_01_COMPLETE
```

Run these lab steps on your Windows machine's RHEL 10 terminal, then let me know if you encountered any errors or if you are completely ready to move on to **Day 2**.
