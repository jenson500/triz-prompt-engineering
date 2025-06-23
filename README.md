# triz-prompt-engineering

**Universal TRIZ prompts for LLMs – open, structured, and future-proof**

This repository contains a growing collection of TRIZ-based prompts for large language models (LLMs) such as ChatGPT – with a focus on Function Oriented Search (FOS), Method Oriented Search (MOS), and related TRIZ applications in AI-supported innovation processes.

All prompts are written in a clean, structured **XML format**, which makes them easy to read, edit, and extend using any standard text editor (e.g. VS Code, Notepad++, BBEdit).

---

## 🌐 Purpose

Our goal is to make TRIZ knowledge usable and sustainable in the age of AI – in a way that is platform-independent, transparent, and free from proprietary constraints.

This approach allows for:
- Interoperability across different tools and LLM platforms
- Future-proof archiving and documentation
- Simplified integration into company-specific workflows

---

## 🔧 Key Features

- ✅ **Structured XML prompt format** – clear, modular, and machine-readable
- 📖 **Format guide** – for consistent prompt development
- ⚖️ **MIT License** – enables open use, including commercial applications
- 📁 **Git-based collaboration** – with versioning, issue tracking, and controlled main branch
- 🔀 **Pull‑request workflow** – all changes must be made in a feature branch and merged into main via PR
- 🤖 Compatible with LLMs like **ChatGPT, Claude, Gemini, Mistral**, and others

---

## 🤝 Collaboration Welcome

In line with the original spirit of the **ccTOPP** initiative, this project is open for contributions – while keeping the main branch curated to ensure quality, transparency, and traceability.

Whether you're an AI developer, TRIZ expert, educator, or prompt engineer – feel free to fork, improve, and suggest new ideas. Let’s build a shared, evolving toolkit for AI-enhanced TRIZ applications.

- 💡 **Before you get started:** Please check the [`prompt-format-guide.pdf`](docs/prompt-format-guide.pdf)  

- 🧩 **Tip:** Use [`template_triz_gpt.xml`](docs/template_triz_gpt.xml) as a starting point when creating a new prompt. It includes the basic structure and placeholders for metadata, logic, and prompt content.

- 🚩 **Contribution rule:** All commits must be made to a branch other than `main` (e.g. `development`) and submitted via a **pull request** before they can be merged into the `main` branch.

- 💡 **Playground:** This folder is intended for experimenting with Git and GitHub during training sessions. Please do not store any important files here. The playground folder is not present in the main branch but can be used in any other branch as needed.

---

## 📂 Directory Structure

```plaintext
triz-prompt-engineering/
│
├── docs/
│   └── prompt-format-guide.pdf
│   └── prompt-format-guide.tex
|   └── prompt-guide.bib
│   └── template_triz_gpt.xml
│
├── playground/ (not in 'main' branch, for training/testing)
│   
├── prompts/
│   ├── business_triz/
│   │   └── .../
│   └── technical_triz/
│       └── .../
│
├── LICENSE
└── README.md