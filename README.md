# Vim Basic | คีย์พื้นฐานของ Vim สำหรับผู้เริ่มต้น ⌨️

สำหรับผู้เริ่มต้นหรือผู้ที่ต้องการทบทวน คีย์ Vim พื้นฐานที่ใช้บ่อยและเป็นหัวใจของการใช้งาน มีดังนี้:

---

## 1. โหมดการทำงาน (Modes)

ก่อนใช้งาน Vim ต้องเข้าใจ **4 โหมดหลัก**:

- **Normal Mode (โหมดปกติ):**  
  ใช้สำหรับนำทาง, ลบ, คัดลอก, วาง, และเรียกใช้คำสั่งต่างๆ

- **Insert Mode (โหมดแทรก):**  
  ใช้พิมพ์ข้อความเหมือนโปรแกรมแก้ไขข้อความทั่วไป

- **Visual Mode (โหมดเลือก):**  
  ใช้เลือกข้อความเพื่อนำไปดำเนินการ เช่น คัดลอกหรือลบ

- **Command-line Mode (โหมดคำสั่ง):**  
  ใช้พิมพ์คำสั่ง เช่น บันทึก, ออกจากโปรแกรม, ค้นหา

### การเปลี่ยนโหมด:

| คำสั่ง           | โหมดที่เข้าสู่                  |
|------------------|----------------------------------|
| `Esc` / `Ctrl + [` | กลับสู่ Normal Mode            |
| `i`              | Insert Mode (แทรกที่ตำแหน่งปัจจุบัน) |
| `a`              | Insert Mode (แทรกหลังตำแหน่งปัจจุบัน) |
| `o`              | Insert Mode (แทรกบรรทัดใหม่ด้านล่าง) |
| `O`              | Insert Mode (แทรกบรรทัดใหม่ด้านบน) |
| `v`              | Visual Mode (เลือกตัวอักษร)     |
| `V`              | Visual Mode (เลือกทั้งบรรทัด)   |
| `Ctrl + v`       | Visual Block Mode (เลือกเป็นบล็อกสี่เหลี่ยม) |
| `:`              | Command-line Mode                |

---

## 2. การนำทางใน Normal Mode

| คำสั่ง         | ความหมาย                          |
|----------------|-----------------------------------|
| `h`            | เลื่อนไปทางซ้าย                   |
| `j`            | เลื่อนลง                          |
| `k`            | เลื่อนขึ้น                        |
| `l`            | เลื่อนไปทางขวา                    |
| `w`            | ไปยังต้นคำถัดไป                   |
| `b`            | ไปยังต้นคำก่อนหน้า               |
| `e`            | ไปยังท้ายคำ                        |
| `0`            | ไปยังต้นบรรทัด                    |
| `^`            | ไปยังตัวแรกที่ไม่ใช่ช่องว่างของบรรทัด |
| `$`            | ไปยังท้ายบรรทัด                   |
| `gg`           | ไปยังต้นไฟล์                      |
| `G`            | ไปยังท้ายไฟล์                     |
| `10gg`         | ไปยังบรรทัดที่ 10                 |
| `Ctrl + f`     | เลื่อนหน้าลง                      |
| `Ctrl + b`     | เลื่อนหน้าขึ้น                    |
| `Ctrl + d`     | เลื่อนลงครึ่งหน้า                 |
| `Ctrl + u`     | เลื่อนขึ้นครึ่งหน้า               |

---

## 3. การแก้ไขข้อความใน Normal Mode

| คำสั่ง         | ความหมาย                                    |
|----------------|---------------------------------------------|
| `x`            | ลบตัวอักษรใต้เคอร์เซอร์                    |
| `dd`           | ลบบรรทัดปัจจุบัน                            |
| `d{motion}`    | ลบจากตำแหน่งปัจจุบันถึงที่ระบุ เช่น `dw`, `d$` |
| `yy`           | คัดลอกบรรทัดปัจจุบัน                        |
| `y{motion}`    | คัดลอกตามช่วง เช่น `yw`                      |
| `p`            | วางหลังเคอร์เซอร์ หรือใต้บรรทัดปัจจุบัน    |
| `P`            | วางก่อนเคอร์เซอร์ หรือเหนือบรรทัดปัจจุบัน  |
| `u`            | ยกเลิกการกระทำล่าสุด (undo)                |
| `Ctrl + r`     | ทำซ้ำการยกเลิก (redo)                        |
| `r{char}`      | แทนที่ตัวอักษรใต้เคอร์เซอร์ด้วย `{char}`    |
| `s`            | ลบตัวอักษรและเข้าสู่ Insert Mode           |
| `c{motion}`    | ลบช่วงและเข้าสู่ Insert Mode เช่น `cw`     |
| `cc`           | ลบบรรทัดและเข้าสู่ Insert Mode              |
| `~`            | สลับตัวพิมพ์เล็ก/ใหญ่ของตัวอักษรใต้เคอร์เซอร์ |

---

## 4. การค้นหาและแทนที่ใน Command-line Mode

| คำสั่ง                         | ความหมาย                                                 |
|--------------------------------|----------------------------------------------------------|
| `/คำค้นหา`                    | ค้นหาคำไปข้างหน้า (ใช้ `n` เพื่อหาถัดไป, `N` เพื่อย้อนกลับ) |
| `?คำค้นหา`                    | ค้นหาคำย้อนกลับ                                         |
| `:%s/คำเก่า/คำใหม่/g`        | แทนที่ทุกคำเก่าด้วยคำใหม่ในทั้งไฟล์ (g = global)       |
| `:%s/คำเก่า/คำใหม่/gc`       | แทนที่พร้อมถามยืนยันก่อนเปลี่ยน (c = confirm)           |

---

## 5. การบันทึกและออกจาก Vim

| คำสั่ง     | ความหมาย                                      |
|------------|-----------------------------------------------|
| `:w`       | บันทึกไฟล์                                     |
| `:q`       | ออกจาก Vim                                     |
| `:wq`      | บันทึกและออก                                   |
| `:x`       | บันทึกและออก (เหมือน `:wq`)                  |
| `:q!`      | ออกโดยไม่บันทึก (force quit)                  |
| `:w!`      | บันทึกไฟล์แม้จะถูกล็อกหรือป้องกันการเขียน     |

---

## ตัวอย่างการใช้คำสั่งรวมกัน

- `d2w`: ลบ 2 คำ
- `y3j`: คัดลอก 3 บรรทัดถัดไป
- `5dd`: ลบ 5 บรรทัด
- `cib`: เปลี่ยนข้อความภายในวงเล็บ (inside block)
- `ciw`: เปลี่ยนข้อความภายในคำ (inside word)

---

# คำสั่ง Vim พื้นฐานที่มีประโยชน์กับ HTML, CSS, JS

คำสั่งพื้นฐานที่พูดถึงก่อนหน้านี้ใช้ได้ดีกับโค้ดแทบทุกภาษา รวมถึง HTML, CSS และ JavaScript ด้วย แต่ต่อไปนี้คือคำสั่งที่ **มีประโยชน์เป็นพิเศษ** เมื่อต้องจัดการกับโค้ดเว็บ:

---

## 📐 การจัดรูปแบบ (Formatting & Indentation)

| คำสั่ง        | ความหมาย                                                                 |
|---------------|--------------------------------------------------------------------------|
| `gg=G`        | จัดรูปแบบ (auto-indent) ทั้งไฟล์ (`gg` ไปต้นไฟล์, `=G` จัดรูปแบบจนถึงท้ายไฟล์) |
| `=motion`     | จัดรูปแบบบล็อกตามช่วง เช่น `={` จัดรูปแบบบล็อกปัจจุบัน                |
| `>motion`     | เพิ่มการเยื้อง เช่น `>}` เพิ่มเยื้องบล็อก                               |
| `<motion`     | ลดการเยื้อง เช่น `<}` ลดเยื้องบล็อก                                     |
| `>>`, `<<`    | เยื้อง/ลดเยื้องบรรทัดเดียวใน Normal Mode                               |

**ตัวอย่างใช้งานใน Visual Mode:**

- เลือกข้อความด้วย `v` หรือ `V` แล้วกด `>` เพื่อเพิ่มเยื้อง หรือ `<` เพื่อลดเยื้อง

---

## 🧭 การนำทางเฉพาะโค้ด (Code-specific Navigation)

| คำสั่ง   | ความหมาย |
|----------|-----------|
| `%`      | กระโดดระหว่างวงเล็บคู่ (), {}, [], <> หรือแท็ก HTML ที่จับคู่กันได้ |
| `shift + [`, `shift + ]` / `[[`, `]]` / `][`, `[]` | กระโดดระหว่างฟังก์ชัน/บล็อก (ขึ้นอยู่กับไฟล์และการตั้งค่า filetype) |
| `gf`     | เปิดไฟล์ที่อยู่ใต้เคอร์เซอร์ เช่นชื่อไฟล์ใน `<script src="...">` หรือ `import` |

> 💡 *`%` มีประโยชน์มากสำหรับ HTML tag pairing, JS blocks และ CSS selectors*

---

## ✏️ การแก้ไขที่มีประสิทธิภาพ (Efficient Editing)

### การเปลี่ยนข้อความภายในบล็อก:

| คำสั่ง     | ความหมาย |
|------------|-----------|
| `ci{`, `ca{` | เปลี่ยนข้อความ **ภายใน** / **รวมถึง** วงเล็บปีกกา `{}` |
| `ci(`, `ca(` | สำหรับวงเล็บ () |
| `ci[`, `ca[` | สำหรับวงเล็บ [] |
| `ci"`, `ca"` | สำหรับข้อความใน `"` |
| `ci'`, `ca'` | สำหรับข้อความใน `'` |
| `cit`, `cat` | สำหรับ tag HTML เช่น `<div></div>` (ต้องใช้ปลั๊กอินเช่น `vim-surround`) |

### อื่นๆ:

| คำสั่ง      | ความหมาย |
|-------------|-----------|
| `.`         | ทำซ้ำคำสั่งล่าสุด เช่น ลบคำเดิม, แก้ไขเดิม |
| `Ctrl + a`  | เพิ่มค่าตัวเลขใต้เคอร์เซอร์ เช่น `margin: 10px;` → `11px` |
| `Ctrl + x`  | ลดค่าตัวเลขใต้เคอร์เซอร์ เช่น `10px` → `9px` |

---

## 🔍 การค้นหาและแทนที่ด้วย Regular Expressions

| คำสั่ง                           | ความหมาย |
|----------------------------------|-----------|
| `:s/pattern/replace/g`           | แทนที่ `pattern` ด้วย `replace` ในบรรทัดปัจจุบัน |
| `:%s/pattern/replace/g`          | แทนที่ทั้งหมดในไฟล์ |
| `:%s/pattern/replace/gc`         | แทนที่ทั้งหมดในไฟล์พร้อมยืนยันทุกครั้ง |
| `\v`                             | เปิด "very magic mode" ให้ใช้ regex ได้ง่ายขึ้น |

### ตัวอย่าง Regex:

```vim
:%s/\v<div class="old">/<div class="new">/g
```

---

💡 **เคล็ดลับ:**  
- การฝึกฝนเป็นกุญแจสำคัญในการใช้ Vim ให้คล่อง พยายามใช้คีย์บอร์ดแทนเมาส์ และเรียนรู้คำสั่งใหม่ๆ ทีละน้อย แล้วคุณจะใช้งาน Vim ได้อย่างชำนาญ
