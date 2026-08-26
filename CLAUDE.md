<!-- BEGIN medsci-skills routing -->
## MedSci Skills

MedSci Skills is installed. When a request matches a row below, invoke that skill rather than
answering from scratch. When the right one is not obvious, invoke `orchestrate` — it classifies the
request and routes to the rest.

| Request | Skill |
|---|---|
| Find papers; check that a citation is real; build a reference list | `search-lit`, `verify-refs`, `manage-refs` |
| Plan a study; sample size; define variables; de-identify data | `design-study`, `calc-sample-size`, `define-variables`, `deidentify` |
| Run statistics; draw a publication figure | `analyze-stats`, `make-figures` |
| Draft or revise a manuscript; write an IRB protocol | `write-paper`, `revise`, `write-protocol` |
| Audit against a reporting guideline (STROBE, PRISMA, CONSORT, STARD, TRIPOD) or a risk-of-bias tool | `check-reporting` |
| Self-review before submitting; answer reviewers; review someone else's paper | `self-review`, `revise`, `peer-review` |
| Choose a journal; assemble a submission package | `find-journal`, `sync-submission` |
| Medical-research work that is not obviously one of the above | `orchestrate` |

How a skill is invoked depends on how it was installed: bare (`/write-paper`) for a skills-folder
install, namespaced (`/medsci-writing:write-paper`) for a plugin install. Skip any skill that is not
installed, and never invent one.

These skills draft and audit. They do not replace authors, statisticians, reviewers, or an IRB, and
every output needs human-expert verification.
<!-- END medsci-skills routing -->
