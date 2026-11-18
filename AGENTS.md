# AGENTS.md — Clothing Color Extraction

## Mission
งานวิจัยวิธีจำแนกสีเสื้อผ้าส่วนบน/ส่วนล่างจาก mask และโมดูลที่ถูกเลือกใช้งานในระบบจริง

## Read before any change
1. `README.md`
2. `docs/SCOPE_AND_DELIVERABLES.md`
3. `docs/SOURCE_INVENTORY.md`
4. `docs/QUALITY_GATES.md`
5. `tasks/ACTIVE_TASK.md` if present
6. Corresponding source repos' own `AGENTS.md` and exact workspace files.

## Scientific and source integrity
- Confirm source file paths, git status, commit hashes, actual selected implementation, checkpoint/version and report provenance before claiming anything is final.
- Treat old experiments as **read-only evidence**. Preserve canonical metrics, raw annotations, source hashes, logs and model artifacts; do not delete or silently regenerate them.
- Do not assume the newest-named folder is what the final app runs. Verify actual imports/config/checkpoints in the running project.
- Preserve prior git histories; use links/evidence manifests rather than bulk-duplicating research data.
- Separate confirmed facts, derived analysis, inference and TODO/NOT_VERIFIED.

## Scope and permissions
- ไม่กล่าวอ้างว่า M1–M7 ทุกตัว train เหมือนกัน
- ไม่แก้ learned mapping matrix/prototypes หรือ GT labels เงียบ ๆ
- ไม่ประกาศสีที่มองไม่ชัดเป็นสีแน่นอนโดยไม่มี threshold
- Do not edit the Hub, Final repo or any other repository without a separate scoped task.
- Do not download large models/datasets, install packages, run full benchmarks/training, move/delete originals or change repository visibility without authorization.
- No API keys, passwords, tokens, DB credentials or company imagery in public commits. **PUBLIC — metadata and approved code/docs only.** Never publish restricted company footage or secrets.

## Required work product
- สำรวจ repo Garment-Color-Extractor และบันทึก M1–M7 ที่มีโค้ดและผลจริง
- ระบุ method และ parameters ที่ถูกเลือกไปในเว็บ demo โดยอ้าง commit
- เตรียม summary ไทยแบบ per-method, visual success/failure และ reproducibility
- ย้ายเฉพาะ code/config/tests ที่ใช้จริง; ไม่คัดลอก cache และ dataset

## Done means
- train/test split ไม่รั่วไหล; color categories และ background handling ตรง evaluator
- เปรียบเทียบ methods บน same GT/eval อย่างเป็นธรรม
- ขั้นตอน convert RGB to LAB/HSV และ mask region ไม่รวม background
- พิสูจน์ว่า output API ทำงานกับ parser-selected mask จริง
- Preserve a durable summary of findings, source SHAs, changed paths, test results, known issues and a reproducibility note.
- Record relevant decisions/limitations in docs and the Project Hub if authorized.
- Remove **only** `tasks/ACTIVE_TASK.md` after owner acceptance and saved evidence; never remove permanent `AGENTS.md`, provenance or historical artifacts.
