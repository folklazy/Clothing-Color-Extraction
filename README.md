# Clothing Color Extraction

> **Curated delivery repository — content migration pending verification.** The project owner reports that implementation/research work was completed in older VS Code/SSH workspaces and source repos, but this new repository does not yet claim a fully packaged release.

งานวิจัยวิธีจำแนกสีเสื้อผ้าส่วนบน/ส่วนล่างจาก mask และโมดูลที่ถูกเลือกใช้งานในระบบจริง

**PUBLIC — metadata and approved code/docs only.** Never publish restricted company footage or secrets.

## เป้าหมายการส่งมอบ

- แยกการประเมินแบบใช้ GT clothing mask ออกจากการใช้ predicted Human Parsing mask บนเว็บจริง.
- จัดหมวดวิธีทดลองที่ใช้จริง (M1–M7 ตาม registry ที่ตรวจได้): rule/HSV/LAB reference mapping, learned prototypes, clothing-type prototypes, ensemble/MLP ตาม implementation.
- อธิบาย label space ของ GT 12 สีและ 11 LAB reference colors เท่าที่โค้ดและผลตรวจยืนยัน; ระวังอย่าสับสน training labels กับ fixed reference palette.
- ทดสอบ/reproduce metrics เดิมสำหรับ single-color vs multi-color, upper vs lower, unknown, shade, fold, logo, shadow.
- สรุป confusion matrix/per-class metrics, visual examples, error taxonomy, selected method and saved learned parameters.
- จัด color extractor interface ที่รับ RGB crop + clothing region mask แล้วคืน structured label/confidence/unknown พร้อม version.

## Existing sources (read-only starting points)

- [Garment Color Extractor](https://github.com/folklazy/Garment-Color-Extractor)

**Important:** these references are candidates, not proof that all content is current, supported or safe to move. Agent must verify files and commits before copying.

## เอกสารสำคัญ

- [AGENTS.md](AGENTS.md) — read first; permanent agent rules
- [Scope & deliverables](docs/SCOPE_AND_DELIVERABLES.md) — exact responsibilities and exclusions
- [Source inventory](docs/SOURCE_INVENTORY.md) — existing source pointers and audit template
- [Quality gates](docs/QUALITY_GATES.md) — acceptance checklist
- [Active task](tasks/ACTIVE_TASK.md) — first-pass work brief; delete **only after** verified completion and durable handoff
- [Project Hub](https://github.com/folklazy/Human-Body-Extraction)
- [Final End-to-End Repository](https://github.com/folklazy/A-Comparative-Study-of-YOLO-Based-Instance-Segmentation)

## Release status

| Stage | Status |
|---|---|
| Historical experiments / implementation | Reported complete by project owner; specific commits to be audited |
| Clean delivery repository | Initialized |
| Source migration and code/package verification | **Pending** |
| Actual tests and release evidence in this repository | **Not verified yet** |

Only claim numbers and performance backed by linked canonical files. Do not make up final file counts, model parameters or deployment commands.
