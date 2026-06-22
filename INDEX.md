# RHCE Course — Index & Navigation

This index page is formatted like a textbook front-matter or a Confluence summary page: a single place to find lessons, concise learning objectives, estimated time, difficulty level, quick links, and a recommended study flow for the RHCE_Course repository.

> Tip: Open any lesson by clicking its link or view it in your editor: `less rhce-day-001-file-system.md`.

---

## Course at a glance

- Audience: System administrators preparing for Red Hat certification (RHCSA / RHCE).
- Format: Day-by-day Markdown practical labs. Each `rhce-day-XXX-*.md` file is a standalone lesson with hands-on commands, exam tips, and memory aids.
- Goal: Convert repeated hands-on practice into exam-ready muscle memory.

---

## Prerequisites & Safe Practice (short)

Before running any lesson commands, prepare a disposable practice environment. Recommended options:

- Quick container (requires Podman/Docker):

```bash
# start an interactive RHEL-like container (use one you have access to)
podman run -it --rm --name rhce-practice registry.access.redhat.com/ubi9/ubi:9.0 /bin/bash
```

- Virtual machine with a RHEL/CentOS stream image (recommended for full exam parity):
  - Create a VM in VirtualBox / KVM and install RHEL or CentOS Stream.
  - Snapshot the VM before practising so you can revert between exercises.

Safety tips:
- Never run destructive commands on production hosts; use `--dry-run` where available or test in a sandbox VM.
- Use `git` to version your practice configs and keep backups (`git init`, `git add`, `git commit`).

---

## Table of Contents (Lessons)

Each entry includes: objective, est. time, difficulty, and a link.

1. Day 1 — Navigating the File System
   - File: [rhce-day-001-file-system.md](./rhce-day-001-file-system.md)
   - Objective: Understand absolute vs relative paths, navigation shortcuts, and hidden files; use `ls` effectively.
   - Estimated time: 20–30 minutes
   - Difficulty: Beginner
   - Anchor: #day-1---navigating-the-file-system

2. Day 2 — Creating and Editing Files
   - File: [rhce-day-002-navigating-filesystem.md](./rhce-day-002-navigating-filesystem.md)
   - Objective: Create, copy, move, and edit files; basic vim workflow and safe viewing commands.
   - Estimated time: 30–45 minutes
   - Difficulty: Beginner–Intermediate
   - Anchor: #day-2---creating-and-editing-files

---

## How to use this index

- Clone the repository and work through lessons in numeric order.
- Run commands in a disposable environment and snapshot state frequently.
- When adding a new lesson file, follow the filename pattern `rhce-day-XXX-topic.md` and add an entry here with objective, time, and difficulty.

---

## Commands Appendix (Quick Reference)

Grouped cheat-sheet for common tasks used across lessons.

Navigation & listing
- pwd — show current directory
- ls -la — list files (including hidden) with details
- cd [path], cd ~, cd ..

File operations
- touch file — create empty file
- cp [src] [dst] — copy file
- mv [src] [dst] — move/rename
- rm [file] — remove file
- mkdir -p [dir] — create directory and parents

Viewing & searching
- cat file, less file, head -n N file, tail -n N file
- grep 'pattern' file

Editors
- vim file (Insert mode: i, save & quit: :wq, quit without saving: :q!)

Exam tips
- Practice commands until they are muscle memory; small typos cost time under exam conditions.

---

## Glossary (short)

- Absolute path: A path that begins with `/` and uniquely identifies a file or directory from root.
- Relative path: Location relative to the current working directory.
- Hidden file: A filename that starts with `.` and is not shown by `ls` without `-a`.
- Snapshot: VM snapshot or container image used to restore a known-good state quickly.

---

## Recommended study schedule (textbook-style)

- Week 1: Days 1–5 — Core filesystem, files & editors, users and permissions, processes, package management.
- Week 2: Days 6–10 — Network basics, services, firewalls, SELinux, systemd services.
- Week 3: Days 11–15 — Storage, LVM, backups, troubleshooting scenarios, exam practice.

Adjust pace to your experience level. Short daily practice (30–90 minutes) recommended.

---

## Contributing to this index (Confluence-like edits)

1. Add a new lesson file: `rhce-day-XXX-topic.md`.
2. Update this INDEX.md with a numbered entry and one-line summary (objective, time, difficulty).
3. Open a pull request describing the new content.

Guidelines
- Keep lesson titles short and descriptive.
- Provide reproducible commands and expected outcomes in lesson content.
- Use issues to discuss larger restructuring.

---

## Revision history / Changelog

| Date | Change | Author |
|---|---|---|
| 2026-06-22 | INDEX.md created and expanded with TOC, metadata, prerequisites, appendix, changelog | drvsnu |

---

Back to repository README: [README.md](./README.md)
