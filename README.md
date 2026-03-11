# 🚫 Acronym Shamer

An Agent Skill for [Claude Code](https://code.claude.com) and compatible agents designed to minimize the use of unexplained acronyms and internal jargon.

This skill ensures your documentation, commits, and communication remain accessible by enforcing a **"define-first"** rule for all abbreviations.

---

## ✨ Features

* **Jargon Detection**: Automatically scans your responses and code comments for capitalized abbreviations.
* **Enforced Definitions**: Prompts the agent to define an acronym upon its first use in a session.
* **Inclusivity Focus**: Refines outgoing text to be more readable for external stakeholders and new team members.
* **ASU Alignment**: Tailored for the communication standards used by the [Arizona State University](https://github.com/asuwebdesign) web design community.

## 🚀 Installation

To add this skill to your Claude Code environment, follow these steps:

1.  **Create the skill directory** in your project or global configuration:
    ```bash
    mkdir -p .claude/skills/acronym-shamer
    ```

2.  **Download the skill definition**:
    ```bash
    curl -o .claude/skills/acronym-shamer/SKILL.md [https://raw.githubusercontent.com/asuwebdesign/acronym-shamer/main/SKILL.md](https://raw.githubusercontent.com/asuwebdesign/acronym-shamer/main/SKILL.md)
    ```

## 🛠 Usage

Once installed, Claude will automatically apply the logic from `SKILL.md` whenever it generates text. You can also explicitly trigger a review of existing files:

* *"Claude, run the acronym-shamer on this technical spec."*
* *"Check my PR description for any undefined jargon."*

### Example Behavior

> **User**: How do we handle authentication?
>
> **Claude (with Skill)**: We utilize a **JWT (JSON Web Token)** to manage session state. Once the **JWT** is verified by the server...

## 📂 Repository Structure

* `SKILL.md`: The core system instructions and logic for the agent.
* `README.md`: Project documentation and installation guide.
