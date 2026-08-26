# Toolchain: MedSci Skills

This review is run with the [MedSci Skills](https://github.com/Aperivue/medsci-skills)
agent-skill bundle (MIT; some bundled reporting-checklist summaries are CC BY-NC —
see the upstream `THIRD-PARTY-NOTICES.md`).

## Pinned version

| Field | Value |
|---|---|
| Repository | `https://github.com/Aperivue/medsci-skills` |
| Commit | `c393809e67f480b776f60a1a5a4efbc47a632c3c` |
| Installed | 2026-08-26 |
| Skills installed | 59 |

Recording the commit keeps the review reproducible: the QUADAS-3 / PRISMA-DTA
checklists and the extraction-form schema used here are the versions at that commit.

## Reinstall

```bash
git clone https://github.com/Aperivue/medsci-skills
cd medsci-skills && git checkout c393809e67f480b776f60a1a5a4efbc47a632c3c
python3 installers/install.py --target claude --claude-project /path/to/Project2
```

Restart Claude Code afterwards so the skills are enumerated.

## Skills used in this review

| Phase | Skill |
|---|---|
| Protocol + PROSPERO | `meta-analysis` |
| Search execution, verified citations | `search-lit`, `verify-refs` |
| Full-text retrieval (OA only) | `fulltext-retrieval` |
| Synthesis code | `analyze-stats` |
| PRISMA flow, forest / SROC plots | `make-figures` |
| PRISMA-DTA + QUADAS-3 audit | `check-reporting` |
| Manuscript | `write-paper`, `self-review` |
