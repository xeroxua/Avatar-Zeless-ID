# 🎮 Zenless Zone Zero - Avatar ID Mapping Reference

## 🛠️ การนำไปใช้งาน (Usage)

ID เหล่านี้ใช้สำหรับระบุตัวละครในไฟล์ข้อมูล เพื่อแก้ไขค่าสถานะต่าง ๆ ดังนี้:

* **Character Stats:** แก้ไขระดับเลเวล (**level**), ประสบการณ์ (**exp**) และการเลื่อนขั้น (**rank**)
* **Skill Management:** ปรับระดับเลเวลของทักษะต่าง ๆ (**skill_type_level**) เช่น Common Attack หรือ Unique Skill
* **Talents:** ปลดล็อกและตั้งค่ากลุ่มดาวตัวละคร (**unlocked_talent_num**)
* **Equipment:** จัดการอาวุธและอุปกรณ์สวมใส่ผ่านรหัส UID

### 🌐 ช่องทางการแก้ไข (How to Edit)
1. **แก้ไขผ่านไฟล์โดยตรง:** ใช้รหัส ID เป็นชื่อไฟล์ (เช่น `1011`) และแก้ไขโครงสร้างข้อมูลภายใน
2. **เครื่องมือแก้ไขออนไลน์:** เพิ่ม/แก้ไข `Drive Discs` [PSConfig Editor](https://psconfig.zenlessfun.com/) แก้ไข/เพิ่ม เสร็จแล้วนำไปใส่ใน ``\state\player\{ID_Account}\equip\``

---

## 📄 ตัวอย่างโครงสร้างไฟล์ (File Structure Example)

ตัวอย่างการแก้ไขไฟล์ตัวละครโดยตรง (เช่นไฟล์ชื่อ **1011** สำหรับ **Anby Demara**):

```rust
# Name File: 1011
.{
    .level = 60,
    .exp = 0,
    .rank = 6,
    .unlocked_talent_num = 6,
    .talent_switch_list = .{
        false, false, false, true, true, true,
    },
    .passive_skill_level = 6,
    .cur_weapon_uid = 0,
    .is_favorite = false,
    .avatar_skin_id = 0,
    .is_awake_available = false,
    .awake_id = 0,
    .cur_form_id = 0,
    .is_awake_enabled = false,
    .dressed_equip = .{
        null, null, null, null, null, null,
    },
    .show_weapon_type = .active,
    .skill_type_level = .{
        .{ .type = .common_attack, .level = 12 },
        .{ .type = .special_attack, .level = 12 },
        .{ .type = .evade, .level = 12 },
        .{ .type = .cooperate_skill, .level = 12 },
        .{ .type = .unique_skill, .level = 12 },
        .{ .type = .core_skill, .level = 7 },
        .{ .type = .assist_skill, .level = 12 },
    },
}
```
---

## 📋 รายการ ID ตัวละคร (Avatar ID List)

| ID | ชื่อตัวละคร (Character Name) |
| :--- | :--- |
| **1011** | Anby Demara |
| **1021** | Nekomiya Mana |
| **1031** | Nicole Demara |
| **1041** | Soldier 11 |
| **1051** | Yidhari Murphy |
| **1061** | Corin Wicker |
| **1071** | Caesar King |
| **1081** | Billy Kid |
| **1091** | Hoshimi Miyabi |
| **1101** | Koleda Belobog |
| **1111** | Anton Ivanov |
| **1121** | Ben Bigger |
| **1131** | Soukaku |
| **1141** | Von Lycaon |
| **1151** | Luciana de Montefio |
| **1161** | Lighter |
| **1171** | Burnice White |
| **1181** | Grace Howard |
| **1191** | Ellen Joe |
| **1201** | Asaba Harumasa |
| **1211** | Alexandrina Sebastiane |
| **1221** | Tsukishiro Yanagi |
| **1241** | Zhu Yuan |
| **1251** | Qingyi |
| **1261** | Jane Doe |
| **1271** | Seth Lowell |
| **1281** | Piper Wheel |
| **1291** | Hugo Vlad |
| **1301** | Orphin Magnusson & Magus |
| **1311** | Astra Yao |
| **1321** | Evelyn Chevalier |
| **1331** | Vivian Banshee |
| **1341** | Xiao Zhao |
| **1351** | Pilchra Fellini |
| **1361** | Trigger |
| **1371** | Yixuan |
| **1381** | Soldier 0 - Anby |
| **1391** | Ju Fufu |
| **1401** | Alice Thymefield |
| **1411** | Ukinami Yuzuha |
| **1421** | Pan Yinhu |
| **1431** | Ye Shunguang |
| **1441** | Komano Manato |
| **1451** | Lucia Elowen |
| **1461** | Seed |
| **1471** | Banyue |
| **1481** | Dialyn |
| **1491** | Sunna |
| **1501** | Aria |
| **2071** | - |

---

## 💬 Community & Support
หากมีข้อสงสัยหรือต้องการพูดคุยเพิ่มเติม สามารถเข้าร่วมได้ที่ Discord:
* **OurServer:** [https://discord.gg/kWFnanUCvX](https://discord.gg/kWFnanUCvX)

## ✍️ ผู้จัดทำ (Author)
* **xeroxua**
* หากมีการอัปเดตตัวละครใหม่ จะมีการเพิ่มเติมข้อมูลในภายหลัง
