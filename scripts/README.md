# JSON-LD to Markdown Generator

This Python script processes [JSON-LD](https://json-ld.org/) files representing software tools and generates corresponding Markdown files for TechRadar dashboard. It is designed to support technology radar-style documentation by extracting metadata like tool name, category, tags, and description.

## 📂 Directory Structure

project/
│
├── data/
│ └── software-tools/ # Place your .json files here
│
├── radar/
│ └── YYYY-MM-DD/ # Markdown files will be generated here
│
├── script.py # The main script
└── README.md # You're here!


## 🧰 Features

- Extracts fields from JSON-LD files such as:
  - `schema:name`
  - `schema:applicationCategory`
  - `rs:hasQualityDimension`
  - `rs:howToUse`
  - `schema:license`
  - `schema:url`
  - `schema:description`
  - `rs:appliesToProgrammingLanguage`
- Automatically generates a markdown file for each JSON-LD entry.
- Stores the output in a timestamped folder under `radar/`.

## 🚀 Getting Started

### 1. Prerequisites

This script uses only the Python standard library, so no external packages are required.

Make sure you have Python 3.7 or later installed:

```bash
python3 --version
```

### 2. Prepare Input

Place your .json files inside the data/software-tools/ directory. Each file should follow the JSON-LD format with relevant metadata.


### 3. Run the Script

You can run the script from the terminal:

```bash
python3 generate_markdown.py
```

### 4. Output Format (Markdown)
Each generated file will contain:

markdown
---
title: "Tool Name"
ring: AnalysisCode/ResearchInfrastructureSoftware/PrototypeTool
segment: Quality dimension
tags: [QualityTag, UsageMethod, LicenseType, Programming language]
---
https://example.com
Tool description here.

