# SiteScan-EmailExtractor-Python-CLI

A Python CLI tool for extracting email addresses and URLs from websites via recursive crawling and depth-limited scanning. Supports full site crawls or specified URL depth.

<!-- BADGES SECTION START -->
[![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/SiteScan-EmailExtractor-Python-CLI/ci.yml?style=flat-square&logo=githubactions)](https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI/actions)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/SiteScan-EmailExtractor-Python-CLI?style=flat-square&logo=codecov)](https://codecov.io/gh/chirag127/SiteScan-EmailExtractor-Python-CLI)
[![Python Version](https://img.shields.io/badge/Python-3.10%2B-blue?style=flat-square&logo=python)](https://www.python.org/)
[![Linting](https://img.shields.io/badge/Linting-Ruff-E0500F?style=flat-square&logo=ruff)](https://github.com/astral-sh/ruff)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgray?style=flat-square&logo=creativecommons)](https://creativecommons.org/licenses/by-nc/4.0/)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/SiteScan-EmailExtractor-Python-CLI?style=flat-square&logo=github)](https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI/stargazers)
<!-- BADGES SECTION END -->

--- 

## ⭐ Star ⭐ This Repo

If you find this project useful, please consider starring it to show your support!

--- 

## :rocket: Project Overview

**SiteScan-EmailExtractor-Python-CLI** is a robust, Python-based command-line interface tool designed for efficient web crawling and data extraction. It specializes in recursively scanning websites to extract all valid email addresses and URLs. The tool offers flexible crawling depth, allowing for full site scans or targeted scans up to a specified number of links deep. It's built with a focus on developer productivity and data accuracy.

--- 

## :file_tree: Architecture

ascii
SiteScan-EmailExtractor-Python-CLI/
├── src/
│   ├── __init__.py
│   ├── crawler/
│   │   ├── __init__.py
│   │   ├── engine.py      # Core crawling logic
│   │   └── validators.py  # URL and email validation
│   ├── cli.py             # CLI entry point and argument parsing
│   └── utils.py           # General utility functions
├── tests/
│   ├── __init__.py
│   ├── test_crawler.py
│   └── test_cli.py
├── pyproject.toml       # Project configuration, dependencies, and build settings
├── LICENSE              # Project license file
├── README.md            # This README file
└── .gitignore           # Git ignore file


--- 

## :memo: Table of Contents

*   [🚀 Project Overview](#rocket-project-overview)
*   [🌳 Architecture](#file_tree-architecture)
*   [⭐ Star ⭐ This Repo](#star-star-this-repo)
*   [📦 Key Features](#key-features)
*   [🛠️ Getting Started](#getting-started)
    *   [Prerequisites](#prerequisites)
    *   [Installation](#installation)
*   [💡 Usage](#usage)
*   [🤖 AI AGENT DIRECTIVES](#ai-agent-directives)
*   [⚖️ License](#license)

--- 

## :package: Key Features

*   **Recursive Web Crawling:** Explores websites by following links.
*   **Depth-Limited Scanning:** Control the crawl depth to manage scope and resources.
*   **Email Extraction:** Identifies and extracts valid email addresses.
*   **URL Extraction:** Collects all unique URLs encountered during the crawl.
*   **Python CLI:** User-friendly command-line interface for easy operation.
*   **Robust Validation:** Ensures extracted data conforms to standard formats.
*   **Modern Python Stack:** Utilizes `uv`, `Ruff`, and `Pytest` for efficiency and maintainability.

--- 

## :hammer: Getting Started

### Prerequisites

*   **Python:** Version 3.10 or higher.
*   **pip/uv:** A package installer for Python. `uv` is recommended for optimal performance.

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/SiteScan-EmailExtractor-Python-CLI.git
    cd SiteScan-EmailExtractor-Python-CLI
    

2.  **Set up the development environment and install dependencies using uv:**
    bash
    # Create and activate a virtual environment (optional but recommended)
    python -m venv .venv
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`

    # Install project dependencies
    uv install
    

--- 

## :bulb: Usage

Run the CLI tool using the `python -m` command. The primary arguments are the starting URL and optional depth.

**Example:**

Extract emails and URLs from `example.com` with a crawl depth of 3:

bash
python -m sitescan_extractor --url http://example.com --depth 3


To perform a full site crawl (use with caution on large sites):

bash
python -m sitescan_extractor --url http://example.com --full-crawl


**Command-line arguments:**

*   `--url` (required): The starting URL for the crawl.
*   `--depth` (optional): The maximum crawl depth. Default is 1.
*   `--full-crawl` (optional): If set, performs a complete site crawl.
*   `--output-file` (optional): Path to save the extracted emails and URLs.

--- 

## 🤖 AI AGENT DIRECTIVES

<details>

<summary>View AI Agent Directives</summary>

This repository is designed to be processed and understood by AI agents. The following directives outline the core principles and technical stack:

*   **IDENTITY:** APEX TECHNICAL AUTHORITY & ELITE ARCHITECT
    *   **Role:** Senior Principal Software Architect, Master Technical Copywriter, DevOps Strategist with 40+ years of elite industry experience.
    *   **Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."
    *   **Output Standard:** EXECUTION-ONLY.

*   **TECH STACK (Python - Late 2025 Standard):**
    *   **Language:** Python 3.10+
    *   **Package Management:** `uv` (for dependency resolution and installation).
    *   **Linting & Formatting:** `Ruff` (Ultra-fast, comprehensive static analysis).
    *   **Testing:** `Pytest` (Robust unit and integration testing framework).
    *   **CLI Framework:** `Click` (or similar, for intuitive command-line interfaces).
    *   **Core Libraries:** `requests`, `BeautifulSoup4` (or similar for parsing).

*   **ARCHITECTURAL PATTERNS:**
    *   **Primary:** **Modular Monolith**. Ensure clear separation of concerns between modules (e.g., Crawler, CLI, Validators).
    *   **Principles:** Adhere to **SOLID**, **DRY (Don't Repeat Yourself)**, and **YAGNI (You Ain't Gonna Need It)** principles.
    *   **Data Handling:** Design for efficient, memory-conscious data processing, especially for large crawls.

*   **VERIFICATION COMMANDS:**
    *   **Install Dependencies:** `uv install`
    *   **Run Linters & Formatters:** `ruff check .` and `ruff format .`
    *   **Run Tests:** `pytest`
    *   **Run Specific Test File:** `pytest tests/test_crawler.py`
    *   **Check Coverage:** `pytest --cov=src`
    *   **Execute CLI:** `python -m sitescan_extractor --help`

*   **FUTURE-PROOFING:**
    *   Ensure all code is written with backward compatibility for Python 3.10+ in mind.
    *   Modular design should allow for easy integration of new extraction targets or scanning strategies.

</details>

--- 

## :balance_scale: License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**. You are free to:

*   **Share** — copy and redistribute the material in any medium or format.
*   **Adapt** — remix, transform, and build upon the material.

Under the following terms:

*   **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
*   **NonCommercial** — You may not use the material for commercial purposes.

For more details, see the full [LICENSE](LICENSE) file.
