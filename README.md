# design-spec

A repository to propose, review, and track **RFCs (Request for Comments)** for our architecture and SDK designs.

---

## 📌 How it works
1. Submit a new RFC → creates a draft under `/rfcs/NNNN-slug/`.
2. Discuss and review via Pull Request.
3. When merged:
   - ✅ Accepted RFCs move to `/specs/NNNN-slug/`
   - ❌ Rejected RFCs move to `/rejected/NNNN-slug/`
   - Index is auto-updated in [`RFC_INDEX.md`](./RFC_INDEX.md)
   - Site is published at: [🌐 RFCs Portal](https://<username>.github.io/design-spec/)

---

## 📝 Submitting
- 👉 [Submit a new RFC](../../issues/new?template=new_rfc.yml&labels=rfc)
- Draft RFCs live under `/rfcs/NNNN-slug/`.

Each RFC folder should contain:
- `rfc.md` (the proposal itself, with metadata)
- Optionally: `hld.md`, `lld.md`, `api.md`, `security.md`, etc.

---

## 📂 Structure
```

design-spec/
├── rfcs/       # Draft RFCs
├── specs/      # Accepted RFCs
├── rejected/   # Rejected RFCs
├── RFC\_INDEX.md  # Auto-generated index of all RFCs
└── .github/workflows/  # Automation

```

---

## 🔧 Automation
- **RFC Bootstrap** → Creates new RFC folder + template.
- **RFC Finalize** → Moves RFCs to `specs/` or `rejected/` when PR closes.
- **RFC Index Generator** → Updates [`RFC_INDEX.md`](./RFC_INDEX.md).
- **Publish to Pages** → Publishes to [GitHub Pages](https://<username>.github.io/design-spec/).
