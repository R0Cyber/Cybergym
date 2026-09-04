# Evidence and Provenance

## Source

The public report was prepared from the preserved directory
`consolidated_summaries`, generated on 2026-09-03. The retained private export
contains a campaign overview, per-task summaries, status records, vulnerable
source snapshots, and winning inputs.

Only sanitized narrative and aggregate metadata are published here. Original
artifacts remain outside Git history.

## Task-summary SHA-256 Manifest

These hashes identify the exact per-task `SUMMARY.md` files used to prepare the
public report.

| Task | SHA-256 |
|---|---|
| `arvo:10400` | `fb847f08e9f87431c3f0a3e797fa35437ca4ff82d80747ce0b2ff7c6691607d6` |
| `arvo:1065` | `34e23a9bb305a4607c3733f1139e9507d2183b176d7f145ea6f38a4c95155b5c` |
| `arvo:24993` | `000265506663137c27dd7b2da1dfa69a8ea1f8ed439387ed1c1bbdee20d5e221` |
| `arvo:368` | `11bb8d76128c8ee58ee5eb9d7c6abc8db54c8e48550acf3b32d6333a195694b9` |
| `arvo:36861` | `f75806795bceb3b15facd472e249f21d01067a76867c33ff4cd2d45f5961a3e9` |
| `arvo:3938` | `4d4930fa5c60f56f7550b1f52c84b5511fc24055a0eb53b162a9a8c4db9b4d5d` |
| `arvo:47101` | `23b80df3ceabe5010f754611ee8f5992db4365753b7cd6673eb00799fd92ab04` |
| `oss-fuzz:370689421` | `7ee3e4ed56598d37cda2e5a68bdbeb0e45ddaea0d8d869f6b63e0144e40aa0ae` |
| `oss-fuzz:385167047` | `998ffad401c7fc3507405d79bf1c5a2f470ad54180ad2213bdcb5053e93a483e` |
| `oss-fuzz:42535201` | `caf73918edc1620dd27d03cf9ea9dc6ad147c77d4e149ad54dc0da0c245c931f` |
| `oss-fuzz:42535468` | `12be731d7d2be4f42dbdf831553fc692c8625f262b2514459d6839eecddbe903` |

## Public-release Exclusions

- `repo-vul.tar.gz` source snapshots (approximately 1.8 GB combined)
- Raw `status.json` and service-response data
- `submit.sh` files and environment-specific endpoints
- Winning PoC binaries and executable crash inputs
- Agent IDs, PoC IDs, and masked internal task identifiers

These exclusions reduce accidental disclosure, repository bloat, licensing
ambiguity, and unsafe redistribution while retaining an auditable campaign
record.

## Secret Scan

Before preparing this report, the retained text files were checked for common
GitHub token, personal access token, AWS access-key, credential assignment,
flag-assignment, and email-address patterns. No matches were found by that
pattern-based scan. This is a best-effort check, not a guarantee that every
possible sensitive value has been detected.

