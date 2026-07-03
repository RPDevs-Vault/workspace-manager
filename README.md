# Gemini Project Manager Toolchain

This directory contains the custom automation suite used by the Gemini CLI to manage the workspace, fully integrated with the **PMOSkills Architecture**.

## 🛠️ Tools

### `pm.py` / `bin/pm`
The primary CLI for workspace management.

**Commands:**
- `scan`: Scans all top-level directories and updates the master `INVENTORY.md`.
- `status`: Identifies and displays the top 5 most recently active projects based on file modifications (excluding documentation).
- `setup-pmo`: Initializes the workspace `.gemini/pmo` directory with the PMOSkills manuals and templates.
- `scaffold <name> [--tier {Hobbyist,Consulting,Gov}]`: Initializes a new project directory with standardized `.gemini/GEMINI.md` and `README.md`. If Tier > Hobbyist, injects PMOSkills A04 Project Charter.
- `audit <name>`: Audits a project for compliance and TIMWOODS waste (e.g., checks for uninstantiated `[...]` placeholders).

## 📁 Structure
- `bin/`: Executable shims for easy access.
- `core/`: The PMOSkills reference architecture (skills, artifacts, and routing governance).
- `templates/`: Standardized project templates.

## 🚀 Usage
```bash
./projectmanager/bin/pm scan
./projectmanager/bin/pm status
./projectmanager/bin/pm scaffold MyNewProject --tier Consulting
./projectmanager/bin/pm audit MyNewProject
```

---
*Managed by Gemini Project Manager*
