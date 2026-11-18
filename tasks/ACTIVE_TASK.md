# ACTIVE TASK — Initial curated handoff for Clothing Color Extraction

**Status:** OPEN (temporary task brief; do not delete until validation + acceptance).

## Objective
Build the clean delivery package for Clothing Color Extraction from the owner's completed but mixed historical VS Code/SSH workspaces and GitHub evidence. This repo was newly created and is **not** proof that the original work has migrated.

## Sources to inspect
- [Garment Color Extractor](https://github.com/folklazy/Garment-Color-Extractor)

The owner may also have local-only files on the SSH machine. Find paths only by read-only inspection; do not assume or invent them.

## Work sequence
1. สำรวจ repo Garment-Color-Extractor และบันทึก M1–M7 ที่มีโค้ดและผลจริง
2. ระบุ method และ parameters ที่ถูกเลือกไปในเว็บ demo โดยอ้าง commit
3. เตรียม summary ไทยแบบ per-method, visual success/failure และ reproducibility
4. ย้ายเฉพาะ code/config/tests ที่ใช้จริง; ไม่คัดลอก cache และ dataset

## Mandatory restrictions
- ไม่กล่าวอ้างว่า M1–M7 ทุกตัว train เหมือนกัน
- ไม่แก้ learned mapping matrix/prototypes หรือ GT labels เงียบ ๆ
- ไม่ประกาศสีที่มองไม่ชัดเป็นสีแน่นอนโดยไม่มี threshold
- This task does not authorize deleting experiment directories, modifying original benchmark values, uploading restricted company CCTV, changing visibility, full retraining or large downloads.
- If a choice changes the selected model, interface, source-of-truth or rights exposure, stop and get owner approval.

## Final evidence to leave behind
- `docs/SOURCE_INVENTORY.md` completed with exact paths/commits/hashes
- Updated curated README/scope/quality checklist
- Relevant source files/tests/evidence index with verified links
- Short handoff summary: changed files, verifications, limitations, unresolved tasks
- Update Hub if separately authorized

## Cleanup after verified completion
After owner acceptance, preserve findings in permanent documents and delete **this task file only**. Do not delete `AGENTS.md`, results, provenance or audit files.
