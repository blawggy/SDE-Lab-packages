<div align="center">

# 🧪 SDE-Lab-packages

**Effortlessly provision lab environments on Debian 13 (Trixie)**

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Debian%2013%20Trixie-red?logo=debian)](https://www.debian.org/)
[![Shell](https://img.shields.io/badge/shell-Bash-green?logo=gnu-bash)](https://www.gnu.org/software/bash/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

</div>

---

## 📖 Overview

**SDE-Lab-packages** is a lightweight toolset that automates the setup of reproducible, ready-to-use lab environments on **Debian 13 (Trixie)**. Whether you need a software-development workstation, a security-research sandbox, or a data-science environment, SDE-Lab-packages gets you from a bare Debian install to a fully configured lab in minutes.

---

## ✨ Features

- 🚀 **One-command setup** — bootstrap a complete lab environment with a single script
- 📦 **Curated package profiles** — pre-defined package lists for common lab types (development, security, data science, …)
- ⚙️ **Configurable** — override defaults via simple configuration files
- 🧹 **Clean & reproducible** — idempotent scripts that can be re-run safely
- 🐧 **Debian-native** — built specifically for Debian 13 Trixie using `apt` and official repositories

---

## 📁 Project Structure

```
SDE-Lab-packages/
├── configs/          # Environment-specific configuration files
├── docs/             # Guides, references, and architecture documentation
├── packages/         # Package manifests and dependency lists per lab profile
├── scripts/          # Installation and setup automation scripts
├── src/              # Core source code and helper modules
├── tests/            # Unit and integration tests
├── LICENSE           # GNU General Public License v3
└── README.md         # You are here
```

---

## 🚀 Getting Started

### Prerequisites

- A running **Debian 13 (Trixie)** installation (physical, VM, or container)
- `sudo` / root access
- Internet connectivity (for `apt` package downloads)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/blawggy/SDE-Lab-packages.git
   cd SDE-Lab-packages
   ```

2. **Run the setup script**

   ```bash
   sudo bash scripts/install.sh
   ```

3. **Select a lab profile** *(optional — defaults to `dev`)*

   ```bash
   lab create <Lab-project>
   ```

---

## ⚙️ Configuration

Configuration files live in the `configs/` directory. Copy the example config and adjust it to your needs:

```bash
cp configs/default.conf configs/local.conf
# Edit configs/local.conf to customise your environment
```

See [`configs/README.md`](configs/README.md) for a full description of all available options.

---

## 📦 Lab Profiles

Package lists are stored in the `packages/` directory. Each profile is a plain-text file with one Debian package name per line:

| Profile | Description |
|---|---|
| `dev.list` | General software-development tools |
| `security.list` | Security research and penetration-testing tools |
| `data-science.list` | Python, R, Jupyter, and data analysis libraries |

See [`packages/README.md`](packages/README.md) to learn how to create your own profile.

---

## 🧪 Running Tests

```bash
bash tests/run_tests.sh
```

See [`tests/README.md`](tests/README.md) for more information on the test suite.

---

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

Please make sure your changes pass existing tests and follow the project's code style.

---

## 📄 License

This project is licensed under the **GNU General Public License v3.0** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

Made with ❤️ for the Debian community

</div>
