<h1 align="center">
    HippoX Skills Market
</h1>
<p align="center">
<a href="./README_zh-CN.md">简体中文</a> | <a href="./README.md">English</a>
</p>

# Hippox Skills Market Rules

## Overview

Hippox Skills Market is a Git repository-based skill distribution platform. Any directory structure that follows the specifications below will be recognized by Hippox, displayed, and available for installation. </br>
Place your skill in the specified category.

---

## Skill classification

| Classification | Describe                         |
| :------------- | :------------------------------- |
| **email**      | Email-related skill categories.  |
| **code**       | Code-related skill categories.   |
| **file**       | File-related skill categories.   |
| **math**       | Math-related skill categories.   |
| **net**        | Net-related skill categories.    |
| **system**     | System-related skill categories. |
| **time**       | Time-related skill categories.   |
| **other**      | Other skill categories.          |

## Directory Structure

Each skill is an independent folder. The folder name is the skill ID.

```
skills-market/
├── web-search/
│ ├── SKILL.md
│ └── config.json
├── file-processor/
│ ├── SKILL.md
│ └── config.json
└── ...
```

---

## File Specifications

### 1. SKILL.md (Required)

Skill description file. The first line is used as the short description, and the remaining content serves as detailed documentation.

Example:

```markdown
Search the web, supports Baidu, Google, Bing and other search engines

## Detailed Description

This skill performs web search operations and returns relevant page titles, links, and summaries.
```

Rules:

- File must exist
- First line automatically becomes the skill's short description
- Remaining content is displayed as README

### 2. config.json (Required)

Skill configuration file that defines skill metadata.

Structure:

```json
{
  "author": "",
  "github": "",
  "website": ""
}
```

Field Description:

| Field   | Type   | Required | Description                     |
| ------- | ------ | -------- | ------------------------------- |
| author  | string | No       | Author name                     |
| github  | string | No       | GitHub Link                     |
| website | string | No       | Author or personal website link |

Rules:

- File must exist
- All fields can be empty strings
- The github link

Example:

```json
{
  "author": "Hippox Team",
  "github": "https://github.com/xxxxx",
  "website": "https://hippox.dev"
}
```

Or all fields empty:

```json
{
  "author": "",
  "github": "",
  "website": ""
}
```

---

## Complete Example

Skill directory: web-search/

SKILL.md content:

```markdown
Search the web, supports Baidu, Google, Bing and other search engines

## Features

- Supports multiple search engines
- Returns titles, links, and summaries
- Supports paginated results
```

config.json content:

```json
{
  "author": "Hippox Team",
  "github": "hippox",
  "website": "https://hippox.dev"
}
```
