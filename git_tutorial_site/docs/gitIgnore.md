# .gitignore

**Purpose:** A `.gitignore` file tells Git which files or folders to **ignore** and not track. It keeps your repository clean and safe.

**Why Use It?**

- Avoid tracking unnecessary files (logs, build folders, OS files)
- Prevent accidentally committing secrets (API keys, passwords)
- Reduce repository size and clutter

**How It Works:**

1.  Create a file named `.gitignore` in your project's root directory.
2.  Add patterns for files/directories to ignore.
3.  Git automatically excludes them from tracking.

**Common Patterns:**

- `*.log` - Ignore all files with `.log` extension
- `node_modules/` - Ignore entire directory
- `.env` - Ignore environment files (often contain secrets)
- `!important.log` - Exception: do NOT ignore this file

**Key Rule:** If a file is already tracked by Git, adding it to `.gitignore` won't stop tracking. Use `git rm --cached <file>` to remove it first.

**Pro Tip:** Use templates from [gitignore.io](https://www.tgitignore.io/) for your programming language or IDE.
