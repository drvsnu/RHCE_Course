# RHCE_Course

Practical RHCE (Red Hat Certified Engineer) study lab materials and day-by-day practical exercises designed for hands-on exam preparation. Each lesson is a standalone Markdown lab with step-by-step instructions, exam tips, and short exercises.

## Repository contents (high-level)

- rhce-day-001-file-system.md — Day 1 practical lab covering the Linux filesystem: absolute vs relative paths, hidden files, directory navigation, and common `ls` usage. Includes flashcards and exam tips.
- rhce-day-002-navigating-filesystem.md — Day 2 practical lab about creating and editing files, using `touch`, `cp`, `mv`, and basic vim editor workflow; includes exam simulation tasks and recovery tips.

(If you add more `rhce-day-*.md` files, update this section or open a PR to expand the table of contents.)

## How to use

- Read the lesson files directly on GitHub or clone the repository:

```bash
git clone https://github.com/drvsnu/RHCE_Course.git
cd RHCE_Course
ls -1
```

- Open any lesson with your preferred Markdown viewer or in the terminal with `less`/`vim`:

```bash
less rhce-day-001-file-system.md
vim rhce-day-002-navigating-filesystem.md
```

## Suggested study workflow

1. Clone the repo and create a dedicated practice directory in your home: `~/rhce_course`.
2. Work through each `rhce-day-*.md` in order. Perform every command in a disposable VM or container to mimic exam constraints.
3. Make notes, create flashcards (Anki), and repeat tasks until they are muscle memory.

## Contributing

Contributions are welcome. Please follow these guidelines:

- Add new day files as `rhce-day-XXX-topic.md` with a clear title and objectives.
- Keep exercises reproducible and include expected commands and outcomes.
- Open an issue first if you plan larger restructuring.

## License

Add a LICENSE file to this repository if you want to declare terms. If you're not sure, consider using an OSI-approved license such as MIT or CC-BY-SA for educational content.

---

Generated/updated automatically to summarize existing lab files and provide usage/contribution guidance.
