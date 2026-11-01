# 🧭 The Interactive Nmap Guide & Field Manual

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![Category](https://img.shields.io/badge/Domain-Network%20Security%20%26%20Pentesting-red.svg?style=for-the-badge)](https://nmap.org)
[![Tech](https://img.shields.io/badge/Tech-TailwindCSS%20%7C%20Chart.js-38bdf8.svg?style=for-the-badge)](#tech-stack)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](https://github.com/Akhil-Binu/Nmap_Guide/pulls)

<p align="center">
  <b>A modern, high-velocity interactive single-page application (SPA) and field manual designed for security engineers, penetration testers, and network administrators navigating Nmap reconnaissance.</b>
</p>

</div>

---

## 📌 Overview

**The Interactive Nmap Guide** bridges the gap between raw man pages and actionable field tradecraft. Built with a sleek, responsive dark-mode cyber interface, it enables security practitioners to dynamically explore scanning methodologies, compare protocol behaviors side-by-side, configure evasion templates, and quickly construct targeted Nmap command pipelines.

---

## ✨ Key Features & Interactive Modules

- 🔍 **Interactive Scan Explorer**:
  - Compare TCP SYN (`-sS`), TCP Connect (`-sT`), UDP (`-sU`), TCP Null (`-sN`), FIN (`-sF`), and Xmas (`-sX`) scans.
  - Inspect packet headers, flag combinations, and target response signatures (SYN/ACK, RST, ICMP unreachable).
- ⚡ **Performance & Timing Engine**:
  - Deep-dive into timing templates from Paranoid (`-T0`) and Sneaky (`-T1`) to Insane (`-T5`).
  - Visual guidance on probe timeouts, packet rates, and parallelism tuning for IDS avoidance or high-speed sweeps.
- 📜 **Nmap Scripting Engine (NSE) Playbook**:
  - Curated cheat sheet covering vulnerability exploitation (`vuln`), brute-force authentication (`auth`), discovery (`discovery`), and malware detection (`malware`).
- 🛡️ **Firewall & IDS/IPS Evasion**:
  - Practical recipes for MTU packet fragmentation (`-f`, `--mtu`), IP decoys (`-D`), source port manipulation (`--source-port 53`), and data payload customization.
- 📊 **Dynamic Comparison Metrics**:
  - Built-in Chart.js visualizer rating stealth, speed, root-privilege requirements, and firewall detectability across each scanning category.

---

## 🛠️ Tech Stack

- **Frontend**: HTML5, Vanilla JavaScript (Modern ES6+)
- **Styling**: [TailwindCSS](https://tailwindcss.com/) (Dark Cyber Aesthetic)
- **Data Visualization**: [Chart.js](https://www.chartjs.org/)
- **Typography & Icons**: Inter, FontAwesome / Heroicons

---

## 🚀 Quickstart & Usage

### 1. Run Locally
Because this project is self-contained with CDN assets, you can run it immediately without complex build setups:

```bash
# Clone the repository
git clone https://github.com/Akhil-Binu/Nmap_Guide.git

# Navigate into the project directory
cd Nmap_Guide

# Open directly in any modern web browser
# On Windows:
start index.html

# On Linux:
xdg-open index.html

# Or serve via Python HTTP server:
python -m http.server 8000
```
Then visit `http://localhost:8000` in your browser.

### 2. Deploy to GitHub Pages
1. Go to repository **Settings** -> **Pages**.
2. Under **Build and deployment**, select `Deploy from a branch`.
3. Set branch to `main` and folder to `/ (root)`.
4. Click **Save**. Your interactive guide is instantly live worldwide!

---

## 📋 Essential Nmap Command Cheatsheet

| Purpose | Syntax | Privileges |
| :--- | :--- | :--- |
| **Stealth SYN Scan** | `nmap -sS -Pn <target>` | Root / Admin |
| **Full TCP Connect** | `nmap -sT <target>` | Unprivileged |
| **Comprehensive UDP** | `nmap -sU --top-ports 100 <target>` | Root / Admin |
| **Service & OS Detection**| `nmap -sV -O -T4 <target>` | Root / Admin |
| **Aggressive Security Audit** | `nmap -A -v <target>` | Root / Admin |
| **Vulnerability Sweep** | `nmap --script "vuln" -Pn <target>` | Root / Admin |

---

## ⚠️ Educational & Ethical Disclaimer

> [!WARNING]
> This guide and tool are developed exclusively for educational purposes, legitimate security assessments, and authorized penetration testing. Scanning network targets without explicit written authorization is unlawful under computer misuse and cybercrime legislation. Always secure proper authorization before testing any network or system.

---

## 📄 License

Distributed under the [MIT License](LICENSE). Built with ❤️ by [Akhil Binu](https://akhilbinu.in/).
