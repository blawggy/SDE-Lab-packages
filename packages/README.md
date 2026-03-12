# `packages/`

This directory contains package lists and definitions used to construct lab environments on **Debian 13 (Trixie)**.

## Contents

| File | Description |
|---|---|
| *(to be added)* | Package manifests and dependency lists per lab profile |

## Format

Package lists are plain-text files with one Debian package name per line:

```
build-essential
git
curl
wget
```

## Guidelines

- Organize packages by lab profile (e.g., `dev.list`, `security.list`, `data-science.list`).
- Pin package versions where stability is critical.
- Document why non-obvious packages are included with inline comments.
