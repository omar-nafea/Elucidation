# Elucidation 💡

> A curated collection of modular, portable **Agent Skills** for modern AI coding assistants and agents — including **Antigravity**, **Claude Code**, **OpenAI Codex**, **Cursor**, and more.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Standard: Agent Skills](https://img.shields.io/badge/standard-Agent%20Skills-purple.svg)](https://agentskills.io)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)

---

## 📖 What are Agent Skills?

Agent Skills are version-controlled, self-contained runbooks and knowledge modules. Using a **progressive disclosure** architecture, an agent only loads metadata (name & description) during discovery. When a relevant task is encountered, the agent automatically activates the full instruction set into its context window — keeping token usage minimal while providing production-grade procedural expertise.

---

## 🗂️ Skills Catalog

| Skill | Description | Compatibility |
| :--- | :--- | :--- |
| [**`explain-from-first-principles`**](./explain-from-first-principles/) | Teaches and demonstrates any technical concept from its core foundational problem through advanced production-grade implementations, cumulative code examples, tradeoffs, and decision rules. | Antigravity, Claude Code, Codex, Cursor |

---

## 🚀 Installation & Usage

You can install individual skills or clone the entire repository.

### Option 1: Install a Specific Skill (Recommended)

Using [`degit`](https://github.com/Rich-Harris/degit) or `git sparse-checkout`, download just the skill you need:

#### Antigravity / Gemini CLI
* **Project-local** (available in your current project):
  ```bash
  mkdir -p .agents/skills
  npx degit omar-nafea/Elucidation/explain-from-first-principles .agents/skills/explain-from-first-principles
  ```
* **Global** (available across all your projects):
  ```bash
  mkdir -p ~/.gemini/config/skills
  npx degit omar-nafea/Elucidation/explain-from-first-principles ~/.gemini/config/skills/explain-from-first-principles
  ```

#### Claude Code
```bash
mkdir -p ~/.claude/skills
npx degit omar-nafea/Elucidation/explain-from-first-principles ~/.claude/skills/explain-from-first-principles
```

#### OpenAI Codex / Operator
```bash
mkdir -p .codex/skills
npx degit omar-nafea/Elucidation/explain-from-first-principles .codex/skills/explain-from-first-principles
```

#### Cursor / Windsurf
```bash
mkdir -p .cursor/skills
npx degit omar-nafea/Elucidation/explain-from-first-principles .cursor/skills/explain-from-first-principles
```

---

### Option 2: Clone the Full Skills Collection

```bash
git clone https://github.com/omar-nafea/Elucidation.git
```

To link all skills globally into Antigravity:
```bash
# Link all skills in this repo to your global Antigravity config
for skill in Elucidation/*/; do
  skill_name=$(basename "$skill")
  if [ -f "$skill/SKILL.md" ]; then
    mkdir -p ~/.gemini/config/skills
    ln -sfn "$(realpath "$skill")" ~/.gemini/config/skills/"$skill_name"
  fi
done
```

---

## 🧠 Skill Spotlight: `explain-from-first-principles`

### When to Use
Triggered whenever you want deep understanding, progressive examples, the rationale behind each architectural decision, meaningful edge cases, and production relevance rather than high-level documentation summaries.

### Example Prompts
* *"Explain consensus algorithms from first principles with progressive code examples."*
* *"Teach me Dependency Injection in Go, starting from the real problem it solves to a production-ready container."*
* *"Break down how LSM Trees work from scratch, including edge cases and tradeoffs against B-Trees."*

---

## 📁 Repository Structure

Each skill follows the universal Agent Skill specification:

```text
Elucidation/
├── LICENSE
├── README.md
└── <skill-name>/
    ├── SKILL.md            # Required: YAML frontmatter + structured instructions
    ├── agents/
    │   └── openai.yaml     # Optional: Codex/OpenAI agent interface metadata
    ├── scripts/            # Optional: Automated verification or helper scripts
    ├── references/         # Optional: Extended reference docs
    └── examples/           # Optional: Sample implementations
```

---

## 🤝 Contributing

Contributions of new skills or enhancements to existing skills are welcome!

1. Fork the repository.
2. Create a new directory `<your-skill-name>/`.
3. Add a `SKILL.md` with proper YAML frontmatter (`name` in kebab-case and a third-person `description` specifying trigger conditions).
4. (Optional) Add `agents/openai.yaml` for Codex support.
5. Open a Pull Request.

---

## 📄 License

This repository is licensed under the [MIT License](LICENSE) © 2026 Omar Nafea.
