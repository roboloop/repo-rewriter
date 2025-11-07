# 🧬 Repo-Rewriter

> ⚠️ It's an educational project about GIT internals.
> 
> It uses plumbing commands to achieve its goal.

`repo-rewriter` is a collection of small composable shell utilities designed to help you **explore, modify, and sign** Git repositories.
Everything is written in shell, with minimum external dependencies beyond Git itself.

## ✨ Features

- 🔍 **History exploration**
  - `find_in_*` – search in blobs, commits, or filepaths
  - `print_authors` – list all commit authors
  - `print_files` – show all tracked files

- 🪄 **Automated rewriting**
  - `drop_files` — drop files by patterns
  - `replace_in_*` – perform safe text replacements in blobs, commits, or filepaths
  - `rewrite_authors` – map and normalize author identities
  - `rewrite_timestamps` – unify all timestamps to UTC
  - `sign_commits` – cryptographically sign all commits with your GPG key

- 🧱 **Interactive history rebuild**
  - `rewrite_history` – step-by-step reconstruction of a linear repository
    (supports pick/commit/skip/rollback/finalize/abort flow)

- ⚙️ **Portable & transparent**
  - POSIX-compliant shell (works on macOS and Linux)
  - Self-documenting commands with `--help`

## 🚀 Quick Start

```bash
# clone repository
git clone https://github.com/roboloop/repo-rewriter
cd repo-rewriter

# run any command, check docs --help
REPO_DIR="$(pwd)" ./bin/rewriter --help
REPO_DIR="$(pwd)" ./bin/rewriter print_authors --help
REPO_DIR="$(pwd)" ./bin/rewriter print_authors
````

All commands respect a single required environment variable:

| Variable   | Description                     |
| ---------- | ------------------------------- |
| `REPO_DIR` | Path to the Git repository root |

## ✏️ TODO

- Installation script
- Reflog support
- Shellcheck
- Tests

## 🧾 License

MIT © 2025 — Crafted with ❤️ in pure shell.
