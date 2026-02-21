# Contributing to Tesseras Website

Thank you for your interest in contributing! This document explains how to get
started.

## Getting Started

### Prerequisites

- **Zola** — static site generator ([getzola.org](https://www.getzola.org/))
- **just** — task runner ([just.systems](https://just.systems/))
- **dprint** — formatter for Markdown and TOML

### Building

```sh
# List all available tasks
just

# Serve locally with live reload
just serve

# Build the site
just build
```

## Development Workflow

1. **Clone** the repository and create a feature branch from `main`.
2. **Write content** following the conventions below.
3. **Preview locally** with `just serve` and verify your changes look correct.
4. **Submit your contribution** using one of the methods below.

### Submitting via Email (preferred)

The primary way to contribute is by sending a patch to the SourceHut mailing
list using `git send-email`:

```sh
# One-time setup
git config sendemail.to "~ijanc/tesseras-devel@lists.sr.ht"
git config sendemail.annotate true

# Send your commits as a patch series
git send-email --to="~ijanc/tesseras-devel@lists.sr.ht" origin/main
```

If you are new to `git send-email`, see the
[git-send-email tutorial](https://git-send-email.io/) for setup instructions.

Tips for email patches:

- Write a clear cover letter (`--cover-letter`) for multi-commit series.
- Ensure your patches apply cleanly on top of `main`.
- Respond to review feedback by sending a revised series with
  `git send-email -v2` (or `-v3`, etc.).

### Submitting via GitHub

You can also open a pull request on the
[GitHub mirror](https://github.com/tesseras-net/tesseras-website). Fork the
repository, push your branch, and open a PR against `main`.

## Project Structure

```
config.toml          # Zola site configuration
content/             # Markdown pages and blog posts
  news/              # Blog posts (news section)
  _index.md          # Homepage
  about.md           # About page
  contact.md         # Contact page
  faq.md             # FAQ page
  releases.md        # Releases page
  subscriptions.md   # Mailing list subscriptions page
  *.pt-br.md         # Brazilian Portuguese translations
templates/           # Zola HTML templates
static/              # Static assets (images, CSS, etc.)
deploy.sh            # Build + rsync deployment script
announce.py          # Blog post announcement script
```

## Content Conventions

- **Language**: all content in English by default. Brazilian Portuguese
  translations use the `*.pt-br.md` suffix.
- **Formatting**: `dprint fmt` for Markdown and TOML. Config in `dprint.json`.
- **Posts**: news posts go in `content/news/` as Markdown files with Zola front
  matter.
- **Static assets**: images, CSS, and other static files go in `static/`.

## Commit Messages

We use [Conventional Commits](https://www.conventionalcommits.org/) with
[git-cliff](https://git-cliff.org/) for automated changelog generation.

```
feat: add FAQ entry about tessera size limits

Adds a new question to the FAQ page explaining the maximum size
for individual tesseras and how erasure coding affects storage.
```

Supported prefixes: `feat:`, `fix:`, `perf:`, `refactor:`, `doc:`, `test:`,
`audit:`, `style:`, `chore:`, `ci:`, `build:`.

Use scope when it adds clarity: `feat(news):`, `fix(template):`,
`doc(faq):`.

## Reporting Issues

File issues on the
[SourceHut ticket tracker](https://todo.sr.ht/~ijanc/tesseras).

- Search existing issues before opening a new one.
- For security issues, follow the process described in
  [SECURITY.md](SECURITY.md) — do not open a public issue.

## Code of Conduct

This project follows a [Code of Conduct](CODE_OF_CONDUCT.md). By participating
you agree to abide by its terms.
