### 🧠 Githru MCP Server

> Simplify merge commit history and empower Git-based collaboration.

Githru MCP(Merge Commit Processing) Server is a backend module that intelligently analyzes Git histories to build high-level commit groups (CSMs) from complex merge structures.

This server powers Githru's Git visualization and analysis features by organizing merge commits and their related commits into meaningful units.

---

### 🔍 What It Does

- 📦 Creates CSMs (Commit Sets for Merge): Groups related commits together based on merge commits.
- 🔀 Analyzes Git DAG: Builds branch-wise linear commit paths (stems) through top-down traversal of the commit graph.
- 🔗 Integrates GitHub PR Info: Associates merge commits with actual PR metadata.
- 🧠 Supports LLM Summarization (optional): Generates summaries of recent commit activity using AI (e.g., Claude).

---

### 🛠️ Features

- Lightweight & headless – easy to deploy in CI pipelines or extensions
- Consumes Git logs as input – no Git hooks required
- Compatible with GitHub repositories
- Modular design – can be used independently or alongside Githru VS Code Extension

---

### 🧩 Designed For

- Developers who need a clearer view of Git histories
- Engineering teams that want to simplify PR traceability
- Tools & platforms that need to analyze Git repositories programmatically

---

### 🚀 Usage

- The MCP server is typically used as a backend utility. It consumes:
- Git log (as raw input)
- GitHub repo metadata (owner/repo/auth)
- Base branch name

…and returns structured CSM data for visualization, analysis, or automation.

Learn more at [github.com/githru](http://github.com/githru)
or use it together with the Githru VS Code Extension