<div align="center">

# 🗄️ AI Skills Vault — Starter Skills

**A ready-to-use pack of AI agent skills, plus a gentle introduction to the AI Skills Vault plugin.**

[![Install from JetBrains Marketplace](https://img.shields.io/badge/JetBrains%20Marketplace-Install-000000?logo=jetbrains&logoColor=white)](https://plugins.jetbrains.com/plugin/io.github.dariotintore.ai-skills-vault)
[![Plugin version](https://img.shields.io/jetbrains/plugin/v/io.github.dariotintore.ai-skills-vault?label=plugin&color=3574F0)](https://plugins.jetbrains.com/plugin/io.github.dariotintore.ai-skills-vault)
[![SKILL.md](https://img.shields.io/badge/format-Agent%20Skills-7F52FF)](https://github.com/DarioTintore/AI-Skill-Vault)
[![Skills](https://img.shields.io/badge/skills-13-2EA043)](#-whats-inside)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

</div>

---

## 📖 Table of contents

- [What is this repository?](#-what-is-this-repository)
- [What is AI Skills Vault?](#-what-is-ai-skills-vault)
- [Quick start](#-quick-start)
- [What's inside](#-whats-inside)
- [How a skill works](#-how-a-skill-works)
- [Write your own skill](#-write-your-own-skill)
- [Repository layout](#-repository-layout)
- [Compatibility](#-compatibility)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 What is this repository?

This repository is a **starter pack of skills** for AI coding agents — the same
**Agent Skills** / `SKILL.md` format used by **pi**, **claude**, **opencode**, Kiro and many other
CLI agents.

It exists for two reasons:

1. **So you can download useful skills in one click.** Add this repository to
   [AI Skills Vault](#-what-is-ai-skills-vault) and the plugin clones, updates and lists every skill
   below — no manual copying.
2. **As a living introduction to the plugin.** The README you are reading explains what AI Skills
   Vault is, why it exists, and how these skills plug into your daily workflow inside the IDE.

The skills are plain Markdown files. You can use them with any agent that understands the
`SKILL.md` convention, with or without the plugin — but the plugin is what turns them into a
browsable, one-click library.

---

## 🧩 What is AI Skills Vault?

**AI Skills Vault** is a plugin for the **IntelliJ Platform** (IntelliJ IDEA, PyCharm, WebStorm,
GoLand, …) that treats your agent skills as a first-class IDE concept.

> Your skills are scattered in hidden folders. Your agents each have their own syntax. You paste the
> same context over and over. AI Skills Vault fixes all of that: **browse, search, run and share
> skills without leaving the IDE.**

It scans the folders where agents keep their skills, shows them in a searchable tree, and runs any
skill against your current work in a fresh terminal — automatically injecting the context you want:

- the **code selection** from the editor, or
- an uncommitted **`git diff`**, picked file-by-file in a commit-style dialog.

| | |
|---|---|
| 🌳 **Skill tree** | One tree aggregates every configured source, with folders and metadata. |
| 🔎 **Speed search** | Type anywhere to filter, exactly like the Project view. |
| ▶️ **One-click run** | Opens a terminal, launches your agent and runs the skill. |
| 🧩 **Context aware** | Injects the editor selection or a chosen `git diff` into the prompt. |
| 🗂️ **Context picker** | Commit-style dialog to pick exactly which changed files feed the skill. |
| ⚡ **Parallel runs** | One terminal per skill, each agent working independently. |
| 🌐 **GitHub sync** | Clone and install public skill repositories like this one. |
| 📁 **Organize** | Create folders, rename and drag & drop skills between categories. |
| 🤖 **Multi-agent** | Configurable templates for pi, claude, opencode and any custom CLI. |
| 🎨 **Native UI** | Tool window, toolbar, gear menu and Settings page under *Tools*. |

**Links**

- 🛒 Marketplace: <https://plugins.jetbrains.com/plugin/io.github.dariotintore.ai-skills-vault>
- 💻 Plugin source & issues: <https://github.com/DarioTintore/AI-Skill-Vault>
- 📚 Full project documentation: see [`docs/PROJECT.md`](https://github.com/DarioTintore/AI-Skill-Vault) in the plugin repository

---

## 🚀 Quick start

### 1. Install AI Skills Vault

**Settings → Plugins → Marketplace →** search for **AI Skills Vault** → **Install** → restart the IDE.

> Prefer the manual route? Download the latest zip from the
> [releases page](https://github.com/DarioTintore/AI-Skill-Vault/releases) and use
> **Settings → Plugins → ⚙ → Install Plugin from Disk…**

### 2. Load these skills

Pick whichever fits you best.

**Option A — GitHub sync (recommended, always up to date)**

1. **Settings → Tools → AI Skills Vault**
2. Under **GitHub repositories**, add:

   ```text
   DarioTintore/AI-Skill-Vault-Starter
   ```

3. The plugin clones the repository and lists every skill under a new source in the **Skills** tool
   window. Use **Install to local skills** if you want to edit a copy.

**Option B — clone locally**

```bash
git clone https://github.com/DarioTintore/AI-Skill-Vault-Starter.git
```

Then add the cloned folder as a skills source in **Settings → Tools → AI Skills Vault → Folders**.

### 3. Run a skill

1. Open the **Skills** tool window (right stripe).
2. Choose your agent in **⋮ gear menu → Agent**.
3. Select code in the editor (or leave the context empty to use the whole file).
4. Double-click a skill — or select several and press **▶ Run**.

A terminal opens, your agent starts, and the skill runs with your context attached. 🎉

---

## 📦 What's inside

**13 skills**, grouped into 6 categories. Every skill is a folder with a `SKILL.md` inside.

### 🔌 API

| Skill | What it does |
|---|---|
| [`api-endpoint`](api/api-endpoint/SKILL.md) | Designs a complete REST endpoint: route, request/response, validation, status codes, error handling and tests. |

### ✨ Code quality

| Skill | What it does |
|---|---|
| [`code-review`](code-quality/code-review/SKILL.md) | Senior-engineer review: bugs, edge cases, security, performance and style — with concrete fixes. |
| [`performance`](code-quality/performance/SKILL.md) | Finds bottlenecks: complexity, allocations, slow I/O, plus caching and parallelism opportunities. |
| [`refactoring`](code-quality/refactoring/SKILL.md) | Rewrites code applying Clean Code and SOLID, keeping the behavior unchanged. |
| [`security-audit`](code-quality/security-audit/SKILL.md) | Looks for injection, XSS, secret leaks and auth issues, each with severity and a fix. |

### 🗄️ Database

| Skill | What it does |
|---|---|
| [`sql-query`](database/sql-query/SKILL.md) | Generates a query from a description, or optimizes and explains an existing one (indexes, JOINs, N+1). |

### 🐳 DevOps

| Skill | What it does |
|---|---|
| [`dockerfile`](devops/dockerfile/SKILL.md) | Generates an optimized, multi-stage, non-root Dockerfile with a `.dockerignore` and build/run commands. |

### 📝 Docs

| Skill | What it does |
|---|---|
| [`commit-messages`](docs/commit-messages/SKILL.md) | Writes Conventional Commits messages from a diff, with alternatives. |
| [`documentation`](docs/documentation/SKILL.md) | Generates Javadoc / KDoc / JSDoc / docstrings for classes, methods and functions. |

### 🧪 Testing

| Skill | What it does |
|---|---|
| [`unit-tests`](testing/unit-tests/SKILL.md) | Writes a full unit-test suite: happy path, edge cases and error handling, in the right framework. |

### 🛠️ Utility

| Skill | What it does |
|---|---|
| [`bug-fix`](utility/bug-fix/SKILL.md) | Diagnoses a bug from the code and a stack trace, explains the cause and proposes a fix. |
| [`explain-code`](utility/explain-code/SKILL.md) | Explains a block of code step by step, in plain language suitable for a junior. |
| [`regex`](utility/regex/SKILL.md) | Generates a regex from a description, or explains one and flags catastrophic backtracking. |

---

## 🧠 How a skill works

A skill is just a folder containing a **`SKILL.md`** file. It has two parts: a small YAML
frontmatter and a Markdown body.

````markdown
---
name: code-review
description: Reviews the selected code for bugs, security issues, performance weaknesses and style improvements. Use before a pull request.
---

# Code Review

Act as a senior engineer. Review the following code and produce a report with:

1. Bugs and edge cases
2. Security issues
3. Performance issues
4. Style and readability suggestions

For each point, indicate the relevant line/portion and propose a concrete fix.

```$FILE_EXTENSION
$SELECTION
```
````

- **`name`** — the skill identifier, used by the agent (e.g. `/skill:code-review`).
- **`description`** — a one-liner shown in the tree and used by agents to decide when to use it.

### Placeholders resolved by AI Skills Vault

When the plugin sends the skill to your agent, it replaces these placeholders with your current
context:

| Placeholder | Replaced with |
|---|---|
| `$SELECTION` | The code selected in the editor, **or** the `git diff` when a context selection is active |
| `$GIT_DIFF` | `git diff HEAD` — the whole repository, or only the files you selected |
| `$FILE_NAME` | The active file's name |
| `$FILE_EXTENSION` | The active file's extension (used as the code-fence language) |
| `$PROJECT_NAME` | The project name |

> If a skill body contains no placeholders, it still works — the agent simply receives the
> instructions as-is.

---

## ✍️ Write your own skill

1. Create a folder with a descriptive name, e.g. `my-category/my-skill/`.
2. Add a `SKILL.md` inside it, starting with the frontmatter:

   ````markdown
   ---
   name: my-skill
   description: One line that says what it does and when to use it.
   ---

   # My Skill

   Instructions for the agent. Use $SELECTION to inject the code to work on:

   ```$FILE_EXTENSION
   $SELECTION
   ```
   ````

3. Drop the folder into a skills source the plugin scans, or open the picker and **Install** it from
   a GitHub repository.

**Tips for good skills**

- Write the **description as an instruction**: what it does *and* when to trigger it.
- Keep the body focused on a single task — small skills compose better.
- Use explicit, checkable outputs ("produce a report with…", "for each point…").
- Prefer placeholders over asking the user to paste code.

---

## 🗂️ Repository layout

```text
AI-Skill-Vault-Starter/
├── api/
│   └── api-endpoint/SKILL.md
├── code-quality/
│   ├── code-review/SKILL.md
│   ├── performance/SKILL.md
│   ├── refactoring/SKILL.md
│   └── security-audit/SKILL.md
├── database/
│   └── sql-query/SKILL.md
├── devops/
│   └── dockerfile/SKILL.md
├── docs/
│   ├── commit-messages/SKILL.md
│   └── documentation/SKILL.md
├── testing/
│   └── unit-tests/SKILL.md
├── utility/
│   ├── bug-fix/SKILL.md
│   ├── explain-code/SKILL.md
│   └── regex/SKILL.md
├── LICENSE
└── README.md
```

The top-level folders are the **categories** you see in the plugin's tree (`category → skill`).
When AI Skills Vault syncs this repository, each folder becomes a category folder.

---

## 🤝 Compatibility

These skills are **plain `SKILL.md` files** and are not tied to the plugin. They work with any tool
that follows the *Agent Skills* convention, including:

- pi — `/skill:name`
- claude — `/name`
- opencode — `/name`
- Kiro — skills folder
- any custom CLI configured in the plugin

AI Skills Vault is simply the nicest way to **browse, organize and run** them from your IDE, with
your editor selection or `git diff` attached automatically.

---

## 🤝 Contributing

Have a skill worth sharing? Contributions are welcome.

1. Fork this repository and create a topic branch.
2. Add your skill under the most appropriate category as `<category>/<skill-name>/SKILL.md`, with a
   valid frontmatter (`name` + `description`).
3. Keep the body focused and use the placeholders above where they help.
4. Open a pull request describing what the skill does and when to use it.

---

## 📄 License

The skills in this repository are released under the **MIT License** — see [LICENSE](LICENSE).

**AI Skills Vault** (the IDE plugin) is a separate product and is **not** covered by this license.

---

<div align="center">
  <sub>Made for the <a href="https://plugins.jetbrains.com/plugin/io.github.dariotintore.ai-skills-vault">AI Skills Vault</a> plugin · <a href="https://github.com/DarioTintore/AI-Skill-Vault">github.com/DarioTintore/AI-Skill-Vault</a></sub>
</div>
