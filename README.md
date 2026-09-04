# R0 Agentic AI — CyberGym Evaluation Campaign

[![Website](https://img.shields.io/badge/R0-r0cyber.com-111827)](https://r0cyber.com)
[![Tasks](https://img.shields.io/badge/tasks-11%2F11%20recorded%20solved-16a34a)](RESULTS.md)
[![Evidence](https://img.shields.io/badge/evidence-SHA--256%20manifest-2563eb)](EVIDENCE.md)

This repository documents a real evaluation campaign in which **R0 Agentic AI**
was used to investigate and produce triggering inputs for CyberGym vulnerability
tasks derived from ARVO and OSS-Fuzz cases.

The preserved campaign export records:

- **11 task workspaces**
- **11/11 tasks marked `solved`** in the saved local campaign state
- **17 submissions**, all recorded as successful by the exported summaries
- A non-zero vulnerable-target exit code (`255`) for every recorded winning input

These figures describe the saved benchmark campaign evidence generated on
**2026-09-03**. They do not constitute independent certification or endorsement
by CyberGym, ARVO, OSS-Fuzz, or the affected upstream projects.

## What R0 Was Evaluated On

- Reading unfamiliar vulnerable codebases
- Tracing a vulnerability to a concrete code path
- Designing minimal or structured proof-of-concept inputs
- Iterating within submission constraints
- Preserving task-level results and technical reasoning
- Recognizing uncertainty when patched-target verification was unavailable

## Results at a Glance

| Dataset | Recorded tasks | Recorded solved | Submissions |
|---|---:|---:|---:|
| ARVO | 7 | 7 | 13 |
| OSS-Fuzz | 4 | 4 | 4 |
| **Total** | **11** | **11** | **17** |

See [RESULTS.md](RESULTS.md) for the task-level record and
[EVIDENCE.md](EVIDENCE.md) for provenance, hashes, and verification limits.

## Evidence Policy

This public repository intentionally excludes vulnerable source archives,
submission scripts, raw service logs, agent/session identifiers, and executable
or binary PoCs. The source export contains multi-hundred-megabyte archives and
crash-triggering inputs that are unnecessary for substantiating the campaign and
could create licensing or safety problems if republished without review.

Instead, this repository publishes a sanitized result ledger and SHA-256 hashes
of the preserved task summaries. The hashes allow the summaries to be matched to
the retained originals if an authorized audit is required.

## Interpreting “Solved”

In this repository, **solved** means that the saved campaign state marked the
task solved after a submitted input produced a non-zero result on the vulnerable
target. It does **not** mean that R0 independently fixed the upstream project or
that a patched target was conclusively re-verified.

Patched-run evidence is incomplete: five task summaries contain no saved
`fix_exit_code`, while six contain `255`. A later re-verification attempt could
not reach the local campaign server. These limitations are preserved rather
than silently converted into stronger claims.

## Responsible Use

All work described here was performed in an authorized benchmark environment.
The material is published for evaluation, research, and defensive learning.
Do not test crash inputs against systems you do not own or have permission to
assess.

## About R0

R0 is an Agentic AI initiative focused on practical cybersecurity operations,
research, automation, and human–AI collaboration.

Website: [r0cyber.com](https://r0cyber.com)

