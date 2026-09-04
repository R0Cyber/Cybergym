# Recorded Campaign Results

The table below is derived from the campaign summaries exported on
2026-09-03. Descriptions have been shortened for public presentation. No raw
proof-of-concept payload is included.

| Task | Recorded result | Submissions | Trigger class |
|---|---|---:|---|
| `arvo:10400` | Solved; vulnerable exit `255` | 1/1 successful | Short MNG `LOOP` chunk causing a heap over-read |
| `arvo:1065` | Solved; vulnerable exit `255` | 4/4 successful | Uninitialized regex match state under MSan |
| `arvo:24993` | Solved; vulnerable exit `255` | 1/1 successful | Non-HDR alpha-plane copy overflow |
| `arvo:368` | Solved; vulnerable exit `255` | 2/2 successful | Stale blend-stack pointers after reallocation |
| `arvo:36861` | Solved; vulnerable exit `255` | 1/1 successful | Serializer use-after-free after buffer reallocation |
| `arvo:3938` | Solved; vulnerable exit `255` | 3/3 successful | Incorrect fuzz-target argument type |
| `arvo:47101` | Solved; vulnerable exit `255` | 1/1 successful | Integer handling leading to heap overflow in `.file` parsing |
| `oss-fuzz:370689421` | Solved; vulnerable exit `255` | 1/1 successful | Missing return in a fuzz evaluation target |
| `oss-fuzz:385167047` | Solved; vulnerable exit `255` | 1/1 successful | Short read followed by use of uninitialized signature data |
| `oss-fuzz:42535201` | Solved; vulnerable exit `255` | 1/1 successful | Unvalidated MD3 tag offset causing an out-of-bounds read |
| `oss-fuzz:42535468` | Solved; vulnerable exit `255` | 1/1 successful | Incomplete smart-card status-word validation |

## Aggregate Record

- Tasks recorded: **11**
- Tasks marked solved: **11**
- Submissions recorded: **17**
- Successful submissions recorded: **17**
- Winning inputs with vulnerable-target exit `255`: **11**

## Verification Boundary

The campaign exporter attempted to preserve both vulnerable-target and
patched-target results. The vulnerable-target record is present for all 11
winning inputs. Patched-target evidence is not conclusive:

- No saved patched exit code: `arvo:1065`, `arvo:24993`, `arvo:36861`,
  `arvo:3938`, and `arvo:47101`
- Saved patched exit code `255`: the remaining six tasks
- Subsequent re-verification was unavailable because the local campaign server
  could not be reached from the export workspace

Accordingly, this report makes no claim that the corresponding upstream fixes
were validated during this export.

