# 🤝 Contributing to Design Specs (RFCs)

Thank you for contributing!
This repo manages **design specifications (RFCs)** for features, architecture changes, and improvements across squads.

RFCs follow a **structured, automated workflow**.
This document explains how you can submit and maintain one.

---

## 📌 Before You Start

* Read the [Process Guide](./PROCESS.md) → explains full lifecycle.
* Familiarize yourself with the [RFC Template](https://github.com/pranavwani/design-spec/blob/main/.github/templates/RFC_TEMPLATE.md).

---

## 📝 Submitting a New RFC

1. Open a new issue using the **[RFC Proposal Form](https://github.com/pranavwani/design-spec/issues/new?template=rfc-proposal.yml)**.

   * Provide Title, Summary, Authors, Impacted Squads.

2. Automation will:

   * Assign the next RFC ID.
   * Create a **new branch** and **RFC skeleton folder** under `/rfcs/`.
   * Pre-fill metadata (ID, Title, Author, Date, Status = Draft).
   * Open a **draft PR** and auto-assign squad reviewers.

3. You will see your RFC PR with a structure like:

   ```
   rfcs/
   └── RFC-XYZ-title/
       ├── RFC-XYZ-title.md     # Main spec
       ├── design/              # HLD, LLD, Deployment details
       ├── diagrams/            # Architecture/flow diagrams
       ├── notes/               # Meeting notes & decisions
       └── README.md
   ```

---

## ✍️ Writing the RFC

* Fill in `RFC-XYZ-title.md`.
* Use subfolders for supporting material:

  * **`/design/`** → HLD.md, LLD.md, Deployment.md
  * **`/diagrams/`** → architecture, sequence, flow diagrams
  * **`/notes/`** → meeting-notes.md, decisions-log.md

⚡ Keep small RFCs simple (just edit the main `.md`).
For larger RFCs, split into supporting files.

---

## 👥 Review Process

* Once PR is open, Status = **In Review**.
* At least **one reviewer from each impacted squad** must approve.
* The PR will **fail checks** until all required squads approve.

Automation will update the PR timeline with status updates, e.g.:

```
🔄 RFC status updated: In Review
✅ All required squads approved!
```

---

## ✅ Approval & Merge

* After all squads approve → PR can merge.
* Status auto-updates to **Approved**.
* RFC appears in the [Active Index](./RFC_INDEX.md).

---

## 📦 Archival

* If an RFC becomes **Superseded** or **Deprecated**:

  * Update its metadata status in the RFC `.md`.
  * Automation will **move the RFC folder to `/archive/`**.
  * Indexes and badges auto-refresh.

---

## 📊 Indexes & Badges

* **Active RFCs** → [`RFC_INDEX.md`](./RFC_INDEX.md)
* **In Progress RFCs** → [`IN_PROGRESS_INDEX.md`](./IN_PROGRESS_INDEX.md)
* **Archived RFCs** → [`archive/RFC_ARCHIVE_INDEX.md`](./archive/RFC_ARCHIVE_INDEX.md)

Badges in the [README](./README.md) always reflect reality.

---

## 📌 Status Legend

* `Draft` → Skeleton created, not yet reviewed
* `In Review` → PR open, reviewers assigned
* `Approved` → PR merged, RFC accepted
* `Implemented` → Delivered in product code
* `Superseded` → Replaced by newer RFC
* `Deprecated` → Obsolete, moved to archive

---

## 🚀 Quick Summary for Authors

1. Open RFC Proposal Issue.
2. Edit your draft PR.
3. Get approvals from all squads.
4. Merge → Status = Approved.
5. Update later → Implemented / Deprecated / Superseded.

---

✅ With this setup:

* Authors focus on **content**, not process.
* Squads ensure **alignment**.
* Automation enforces **consistency**.
