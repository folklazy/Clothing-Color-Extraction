# Acceptance checklist — Clothing Color Extraction

## Content selection
- [ ] Confirm actual source workspace/repo inventories, branches and commits.
- [ ] Classify each candidate artifact: shipping / evidence / exploratory / obsolete / sensitive.
- [ ] Include only reviewed code, tests, configs, results and documentation.
- [ ] Link to original full experiment reports instead of copying large logs/caches.

## Domain gates
- [ ] train/test split ไม่รั่วไหล; color categories และ background handling ตรง evaluator
- [ ] เปรียบเทียบ methods บน same GT/eval อย่างเป็นธรรม
- [ ] ขั้นตอน convert RGB to LAB/HSV และ mask region ไม่รวม background
- [ ] พิสูจน์ว่า output API ทำงานกับ parser-selected mask จริง

## Engineering/provenance
- [ ] Ensure README is accurate and all internal/external links work.
- [ ] Record source SHA / release version / environment / license/rights where relevant.
- [ ] Verify all imported code has tests or an evidenced smoke run.
- [ ] No secrets, unauthorized CCTV imagery, unverifiable numbers or silently edited canonical metrics.
- [ ] Preserve originals and record a migration summary with before/after checks.
- [ ] Update status in Project Hub only after evidence exists.
- [ ] Delete temporary `tasks/ACTIVE_TASK.md` **only after** acceptance and durable handoff summary.
