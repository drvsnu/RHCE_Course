# 🛠️ Day 2 Practical Lab: Creating and Editing Files

In Linux, configuration files are plain text. To manage a server, you must be able to create, copy, move, and edit these files entirely through the command line.

---

## Step 1: Create Blank Files

Let's enter your training directory and create some empty files using the `touch` command:

```bash
cd ~/rhce_course
touch config.txt server.conf notes.log
ls -l
```

**What it means:** `touch` instantly creates empty files if they do not exist. If they do exist, it updates their timestamp.

---

## Step 2: Copy and Move Files

Let's make a backup copy of your configuration file and then rename a file:

```bash
cp config.txt config.txt.bak
mkdir backups
mv config.txt.bak backups/
mv notes.log daily_notes.txt
ls -l
ls -l backups/
```

**The breakdown:**
- `cp [source] [destination]` — copies a file.
- `mv [source] [destination]` — moves a file, or renames it if the destination is a new name in the same directory.

---

## Step 3: Master the Vim Text Editor (Crucial Exam Skill)

RHEL 10 uses **vim** as its primary terminal text editor. It has two main modes:

- **Command Mode** — for navigating/deleting.
- **Insert Mode** — for typing.

When you open a file, you start in **Command Mode**.

### Open the file:

```bash
vim server.conf
```

### Switch to Insert Mode

Press the `i` key on your keyboard. You will see `-- INSERT --` appear at the bottom of the screen.

### Type text

Type the following two lines:

```text
PORT=8080
ENVIRONMENT=PRODUCTION
```

### Exit Insert Mode

Press the `Esc` key. The `-- INSERT --` text at the bottom will disappear.

### Save and Exit

Type `:wq` and press **Enter**.

> **Note:** `:` enters command-line mode, `w` means **write** (save), and `q` means **quit**.

---

## Step 4: View File Content without Opening It

To verify your work without opening the editor again, use the `cat` command:

```bash
cat server.conf
```

---

## 📝 Short Notes & Memorisation Summary

| Command | Purpose |
|---|---|
| `touch [filename]` | Creates an empty file. |
| `cp -r [dir1] [dir2]` | Copies an entire directory (the `-r` flag means **recursive**). |
| `mv [old_name] [new_name]` | Renames a file or folder. |
| `cat [file]` | Displays the entire contents of a file on the screen. |

### Vim Basics

| Keys | Action |
|---|---|
| `i` | Enter **Insert Mode** (to type text). |
| `Esc` | Return to **Command Mode**. |
| `:wq` | Save and quit. |
| `:q!` | Quit without saving (destroys accidental changes). |

---

## 🃏 Permanent Memory Flashcards (Copy to Anki)

**Front:** What is the purpose of the `-r` flag when using the `cp` command?\
**Back:** It stands for **recursive**, which is required to copy a directory and all of its contents.

**Front:** How do you exit a Vim file without saving any changes you made?\
**Back:** Press `Esc` to enter Command Mode, then type `:q!` and press **Enter**.

**Front:** Which Linux command displays the content of a text file directly to the terminal screen?\
**Back:** `cat`

---

## 💬 Technical Interview Preparation

**Q:** You need to quickly verify if a configuration file contains a specific setting, but the file is massive. Opening it in an editor is risky. How do you safely view its contents?

**A:** I would use the `cat` command to print the contents to stdout safely without risking accidental modification, or combine it with a tool like `grep` or `less` to scan the file without opening an active text editor session.

---

## 🎯 Official RHCSA / RHCE Exam Simulation

**Scenario:** The official Red Hat exam environment relies heavily on configuring text files located in `/etc`. If you forget to save, or if you accidentally format a configuration file incorrectly, services will fail to start, resulting in an automatic **0** for that task.

**Exercise Objective:** Create a folder at `~/exam_practice`. Inside it, create a file named `hosts.txt` using Vim. Write the text `127.0.0.1 localhost` inside it, save it, and make a copy of that file named `hosts.txt.backup` in the same directory.

### Execution Checklist

1. `mkdir ~/exam_practice`
2. `vim ~/exam_practice/hosts.txt`
   *(Press `i`, type the text, press `Esc`, type `:wq`)*
3. `cp ~/exam_practice/hosts.txt ~/exam_practice/hosts.txt.backup`

---

## 🛡️ Day 2 Completion Backup Token

```
TOKEN: RHCE_120_DAY_02_COMPLETE
```
