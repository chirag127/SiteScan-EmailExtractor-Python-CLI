# SiteScan: Recursive Email & URL Extractor CLI

<p align="center">
  <h1 align="center">SiteScan: Recursive Email & URL Extractor CLI</h1>
  <p align="center">
A robust Python CLI tool for extracting email addresses and URLs from websites via recursive crawling and depth-limited scanning. Supports full site crawls or specified URL depth.
</p>

  <p align="center">
    <a href="https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI/actions/workflows/ci.yml">
      <img src="https://img.shields.io/github/actions/workflow/status/chirag127/SiteScan-EmailExtractor-Python-CLI/ci.yml?style=flat-square&logo=githubactions&logoColor=white" alt="Build Status">
    </a>
    <a href="https://codecov.io/gh/chirag127/SiteScan-EmailExtractor-Python-CLI">
      <img src="https://img.shields.io/codecov/c/github/chirag127/SiteScan-EmailExtractor-Python-CLI?style=flat-square&logo=codecov&logoColor=white" alt="Code Coverage">
    </a>
    <a href="#">
      <img src="https://img.shields.io/badge/Python-3.10+-blue.svg?style=flat-square&logo=python&logoColor=white" alt="Python Version">
    </a>
    <a href="#">
      <img src="https://img.shields.io/badge/Ruff-0.4.0-success.svg?style=flat-square&logo=ruff&logoColor=white" alt="Linter">
    </a>
    <a href="https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI/blob/main/LICENSE">
      <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-orange.svg?style=flat-square&logo=creativecommons&logoColor=white" alt="License">
    </a>
    <a href="https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI/stargazers">
      <img src="https://img.shields.io/github/stars/chirag127/SiteScan-EmailExtractor-Python-CLI?style=flat-square&logo=github&logoColor=white" alt="GitHub Stars">
    </a>
  </p>
  <p align="center">
    <a href="https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI/issues">Report Bug</a>
    ·
    <a href="https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI/issues">Request Feature</a>
  </p>
</p>

## Project Overview

SiteScan is a powerful and efficient command-line interface (CLI) tool engineered in Python to recursively crawl websites and extract valuable data, specifically email addresses and URLs. It offers configurable depth-limited scanning, ensuring comprehensive or targeted data collection.

## 🚀 Key Features

*   **Recursive Crawling:** Navigate and process entire websites or specific sections.
*   **Depth Control:** Limit the crawl depth to manage scope and performance.
*   **Email Extraction:** Identify and collect valid email addresses found on pages.
*   **URL Extraction:** Gather all unique URLs encountered during the crawl.
*   **Python CLI:** Built with `Click` for an intuitive and user-friendly command-line experience.
*   **Modern Stack:** Leverages Python 3.10+, `uv` for dependency management, `Ruff` for linting/formatting, and `Pytest` for testing.

## 🏗️ Architecture

This project follows a **Modular Monolith** architectural pattern. This ensures clear separation of concerns for different functionalities (crawling, extraction, CLI interface) while maintaining a unified and manageable codebase.

mermaid
graph TD
    A[CLI Entrypoint] --> B(Crawler Service)
    B --> C{Page Fetcher}
    C --> D[HTML Parser]
    D --> E(Data Extractor)
    E --> F[Email Extractor]
    E --> G[URL Extractor]
    F --> H(Data Storage/Output)
    G --> H
    B --> I(Depth Manager)
    I --> B


## 📚 Table of Contents

*   [Project Overview](#project-overview)
*   [🚀 Key Features](#key-features)
*   [🏗️ Architecture](#architecture)
*   [⚙️ Getting Started](#getting-started)
    *   [Prerequisites](#prerequisites)
    *   [Installation](#installation)
    *   [Usage](#usage)
*   [🧪 Testing](#testing)
*   [🤖 AI Agent Directives](#ai-agent-directives)
*   [💡 Development Principles](#development-principles)
*   [📜 License](#license)

## ⚙️ Getting Started

### Prerequisites

*   Python 3.10 or higher
*   `uv` installed (`pip install uv`)

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI.git
    cd SiteScan-EmailExtractor-Python-CLI
    

2.  **Install dependencies using uv:**
    bash
    uv install
    

### Usage

Run the CLI tool with your desired options:

bash
sitescan extract --start-url <URL> [--max-depth <INT>] [--output <FILEPATH>]


**Example:**

Crawl `example.com` up to a depth of 3 and save results to `output.json`:

bash
sitescan extract --start-url https://example.com --max-depth 3 --output results.json


## 🧪 Testing

Automated tests ensure the reliability and correctness of the tool. Use `pytest` for running the test suite.

bash
pytest


## 🤖 AI Agent Directives

<details>
<summary>View AI Agent Directives</summary>

### SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

#### 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

#### 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

#### 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type (`pyproject.toml` for Python) and apply the corresponding **Apex Toolchain**. This repository, `SiteScan-EmailExtractor-Python-CLI`, is a Python-based CLI tool.

*   **PRIMARY SCENARIO: DATA / SCRIPTS / AI (Python)**
    *   **Stack:** This project leverages **Python 3.10+**. Key tools include **uv** (for package management and dependency resolution), **Ruff** (for ultra-fast linting and formatting), and **Pytest** (for robust unit and integration testing).
    *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for features like data extraction, crawling logic, and the CLI interface, while maintaining a unified deployment.
    *   **CLI Framework:** Uses `Click` for a powerful and intuitive command-line interface.

---

#### 4. APEX NAMING CONVENTION (THE "STAR VELOCITY" ENGINE)
A high-performing name must instantly communicate **Product**, **Function**, **Platform** and **Type**.

**Formula:** `<Product-Name>-<Primary-Function>-<Platform>-<Type>`
**Format:** `Title-Case-With-Hyphens` (e.g., `SiteScan-EmailExtractor-Python-CLI`)

**Rules:**
1.  **Length:** 3 to 10 words.
2.  **Keywords:** MUST include high-volume terms.
3.  **Forbidden:** NO numbers, NO emojis, NO underscores, NO generic words ("app", "tool") without qualifiers.

---

#### 5. THE README REPLICATION PROTOCOL (THE ULTIMATE ARTIFACT)
The README is a self-contained **Project Operating System**.

**Required Sections:**
1.  **VISUAL AUTHORITY (Above the Fold):**
    *   Hero Banner/Logo (Placeholder).
    *   **Live Badges** (Shields.io):
        *   **Style:** `flat-square` (MANDATORY).
        *   **User:** `chirag127` (MANDATORY).
        *   **Required Badges:** Build Status (GitHub Actions), Code Coverage (Codecov), Tech Stack (Python), Lint/Format (Ruff), License (CC BY-NC 4.0), GitHub Stars.
    *   **Social Proof:** "Star ⭐ this Repo" button (Placeholder).

2.  **STRUCTURAL CLARITY:**
    *   **BLUF:** 2-sentence value proposition.
    *   **Architecture:** ASCII `tree` or Mermaid diagram.
    *   **Table of Contents.**

3.  **DEVELOPMENT STANDARDS:**
    *   Setup commands (`git clone` -> `uv install`).
    *   Scripts table.
    *   Principles (SOLID, DRY, YAGNI).

---

#### 6. CHAIN OF THOUGHT (CoT) PROTOCOL
Before generating JSON, perform deep analysis:
1.  **Audit:** Analyze repo content and purpose.
2.  **Pivot/Archive Decision:** Is it junk? If so, rename to `Archived-...`. If not, PIVOT to elite status.
3.  **Naming Strategy:** Apply `<Product>-<Function>-<Type>` formula.
4.  **Replication Protocol:** Draft the "AI Agent Directives" block.
5.  **File Generation:** Plan the content for all 11 required files (including `PROPOSED_README.md` and `badges.yml`).
6.  **Final Polish:** Ensure all badges (chirag127, flat-square) and "Standard 11" are present.
7.  **Strict Adherence:** Ensure `PROPOSED_README.md` strictly follows the `AGENTS.md` directives.

---

#### 7. DYNAMIC URL & BADGE PROTOCOL
**Mandate:** All generated files MUST use the correct dynamic URLs based on the **New Repository Name**.

**Rules:**
1.  **Base URL:** `https://github.com/chirag127/<New-Repo-Name>`
2.  **Badge URLs:** All badges (Shields.io) must point to this Base URL or its specific workflows (e.g., `/actions/workflows/ci.yml`).
3.  **Consistency:** Never use the old/original repository name in links. Always use the new "Apex" name.

</details>

## 💡 Development Principles

We adhere to established software development best practices:

*   **SOLID:** Designing robust and maintainable object-oriented systems.
*   **DRY (Don't Repeat Yourself):** Avoiding redundancy in code and configuration.
*   **YAGNI (You Ain't Gonna Need It):** Focusing on essential features and avoiding premature complexity.

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See the [LICENSE](LICENSE) file for more details.
