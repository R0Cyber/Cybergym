# R0 Agentic AI — CyberGym Evaluation Campaign

[![Website](https://img.shields.io/badge/R0-r0cyber.com-111827)](https://r0cyber.com)
[![Tasks](https://img.shields.io/badge/tasks-11%2F11%20recorded%20solved-16a34a)](RESULTS.md)
[![Evidence](https://img.shields.io/badge/evidence-SHA--256%20manifest-2563eb)](EVIDENCE.md)

## สรุปภาษาไทย

Repository นี้บันทึกผลการนำ **R0 Agentic AI** ไปทดสอบกับโจทย์ด้าน
Cybersecurity ในสภาพแวดล้อม CyberGym จริง โดยโจทย์ที่เก็บไว้ใน campaign
ประกอบด้วยกรณีจาก ARVO และ OSS-Fuzz

ผลจากหลักฐานที่บันทึกไว้เมื่อวันที่ **3 กันยายน 2026** มีดังนี้:

- มีพื้นที่ทำงานทั้งหมด **11 โจทย์**
- ระบบบันทึกสถานะ `solved` ครบ **11/11 โจทย์**
- มีการส่งคำตอบรวม **17 ครั้ง** และถูกบันทึกว่าสำเร็จทั้ง 17 ครั้ง
- Winning input ของทุกโจทย์ทำให้ vulnerable target คืนค่า non-zero exit code
  เป็น `255`

R0 ถูกใช้เพื่อช่วยอ่านและวิเคราะห์ codebase ที่ไม่คุ้นเคย ติดตามเส้นทางของ
ช่องโหว่ ออกแบบ input สำหรับกระตุ้นปัญหา วางแผนขั้นตอน และบันทึกเหตุผลทาง
เทคนิค โดยมนุษย์ยังเป็นผู้ตรวจสอบผลลัพธ์และรับผิดชอบการดำเนินการทั้งหมด

คำว่า **solved** ในรายงานนี้หมายถึงสถานะที่บันทึกโดย campaign หลัง input
สามารถกระตุ้น vulnerable target ได้ ไม่ได้หมายความว่า R0 แก้ไข upstream
project สำเร็จ หรือได้รับการรับรองอย่างเป็นทางการจาก CyberGym, ARVO,
OSS-Fuzz หรือเจ้าของโครงการต้นทาง

หลักฐาน patched-run ยังไม่สมบูรณ์: 5 โจทย์ไม่มีค่า `fix_exit_code` ที่บันทึกไว้
และอีก 6 โจทย์มีค่า `255` ขณะที่การตรวจซ้ำภายหลังไม่สามารถเชื่อมต่อ local
campaign server ได้ Repository นี้จึงแสดงผลตามหลักฐานที่มีจริง พร้อมระบุ
ข้อจำกัดโดยไม่ขยายผลเกินข้อมูลที่ตรวจสอบได้

รายละเอียดรายโจทย์อยู่ใน [RESULTS.md](RESULTS.md) และข้อมูลแหล่งที่มา,
SHA-256 รวมถึงขอบเขตการเผยแพร่อยู่ใน [EVIDENCE.md](EVIDENCE.md)

## English Summary

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
