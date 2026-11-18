# Scope & deliverables — Clothing Color Extraction

## Purpose
งานวิจัยวิธีจำแนกสีเสื้อผ้าส่วนบน/ส่วนล่างจาก mask และโมดูลที่ถูกเลือกใช้งานในระบบจริง

## Deliverables
- แยกการประเมินแบบใช้ GT clothing mask ออกจากการใช้ predicted Human Parsing mask บนเว็บจริง.
- จัดหมวดวิธีทดลองที่ใช้จริง (M1–M7 ตาม registry ที่ตรวจได้): rule/HSV/LAB reference mapping, learned prototypes, clothing-type prototypes, ensemble/MLP ตาม implementation.
- อธิบาย label space ของ GT 12 สีและ 11 LAB reference colors เท่าที่โค้ดและผลตรวจยืนยัน; ระวังอย่าสับสน training labels กับ fixed reference palette.
- ทดสอบ/reproduce metrics เดิมสำหรับ single-color vs multi-color, upper vs lower, unknown, shade, fold, logo, shadow.
- สรุป confusion matrix/per-class metrics, visual examples, error taxonomy, selected method and saved learned parameters.
- จัด color extractor interface ที่รับ RGB crop + clothing region mask แล้วคืน structured label/confidence/unknown พร้อม version.

## Out of scope / risks
- ไม่กล่าวอ้างว่า M1–M7 ทุกตัว train เหมือนกัน
- ไม่แก้ learned mapping matrix/prototypes หรือ GT labels เงียบ ๆ
- ไม่ประกาศสีที่มองไม่ชัดเป็นสีแน่นอนโดยไม่มี threshold

## Definition of done
- train/test split ไม่รั่วไหล; color categories และ background handling ตรง evaluator
- เปรียบเทียบ methods บน same GT/eval อย่างเป็นธรรม
- ขั้นตอน convert RGB to LAB/HSV และ mask region ไม่รวม background
- พิสูจน์ว่า output API ทำงานกับ parser-selected mask จริง

## Interface to the final project
Only export the minimal verified runtime module, configuration, schema, model/checkpoint manifest, test fixtures and documentation needed by [Final End-to-End Project](https://github.com/folklazy/A-Comparative-Study-of-YOLO-Based-Instance-Segmentation). Archive research outputs stay in their original repos unless there is a clear and approved reason to bundle them.

Before release, register exact source commits, package/API versions and rights in the [Project Hub](https://github.com/folklazy/Human-Body-Extraction).
