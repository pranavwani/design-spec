# 📘 Design Specs Repository (RFCs)

[![Docs Live](https://img.shields.io/badge/docs-live-brightgreen)](https://your-org.github.io/design-specs/)
[![RFCs](https://img.shields.io/badge/RFCs-3-blue)](./RFC_INDEX.md)
[![Active](https://img.shields.io/badge/Active-1-green)](./RFC_INDEX.md)
[![In Progress](https://img.shields.io/badge/In%20Progress-1-yellow)](./IN_PROGRESS_INDEX.md)
[![Archived](https://img.shields.io/badge/Archived-1-lightgrey)](./archive/RFC_ARCHIVE_INDEX.md)

This repository contains **design specifications (RFCs)** for features, architecture decisions, and technical improvements.
RFCs capture the **why and how** behind important changes and ensure cross-squad visibility.

---

## 📌 Purpose

* Provide a structured process for **submitting, reviewing, and maintaining** RFCs.
* Ensure **cross-squad participation** (Foundry, SDK, Iris, Flare).
* Maintain a **historical record** of design evolution.

---

## 📑 RFC Overview

* [Active RFCs](./RFC_INDEX.md)
* [In Progress RFCs](./IN_PROGRESS_INDEX.md)
* [Archived RFCs](./archive/RFC_ARCHIVE_INDEX.md)

👉 See the full [Process Guide](./PROCESS.md) for lifecycle details.

---

## 📝 How to Propose a New RFC

1. Open a new RFC proposal using the **[RFC Proposal Form](../../issues/new?template=rfc-proposal.yml)**.
2. Automation will:

   * Create a new branch + RFC skeleton folder in [`/rfcs/`](./rfcs/).
   * Pre-fill metadata (ID, title, author, date).
   * Open a **draft PR** and assign squad reviewers automatically.
3. Author updates the RFC doc + supporting files (`design/`, `diagrams/`, `notes/`).
4. PR goes through cross-squad review until all required squads approve.
5. Once merged → RFC is accepted and appears in the index.

---

## 📂 Repository Structure

```
design-specs/
├── README.md                # Overview (this file)
├── PROCESS.md               # Lifecycle & workflow details
├── TEMPLATE.md              # Base template for RFCs
├── CONTRIBUTING.md          # Quick-start guide for contributors
├── RFC_INDEX.md             # Auto-generated: Active RFCs
├── IN_PROGRESS_INDEX.md     # Auto-generated: In-progress RFCs
├── rfcs/                    # Active RFC folders
│   └── RFC-XYZ-title/
│       ├── RFC-XYZ-title.md
│       ├── design/
│       ├── diagrams/
│       └── notes/
└── archive/                 # Archived RFCs
    ├── RFC_ARCHIVE_INDEX.md
    └── RFC-000-old-approach/
```

---

## 📊 Status Legend

Each RFC has a **Status** field in its metadata:

* `Draft` – Initial proposal, not yet in review
* `In Review` – Under discussion with reviewers
* `Approved` – Accepted and merged into repo
* `Implemented` – Change has been delivered in codebase
* `Superseded` – Replaced by a newer RFC
* `Deprecated` – No longer relevant

---

## 📚 Documentation Portal

The full RFC repository is browsable on **GitHub Pages**:

👉 [RFC Docs Portal](https://your-org.github.io/design-specs/)

Built with **MkDocs + Material theme**, with:

* 🔍 Full-text search
* 📊 Auto-updating indexes
* 🖼️ Live Mermaid diagrams
* 📂 Navigation synced with repo structure

