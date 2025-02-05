# ใบงานการทดลอง HTML

## การทดลองที่ 5: การสร้างตารางและรายการ
### วัตถุประสงค์
- เรียนรู้การสร้างตารางข้อมูล
- เรียนรู้การสร้างรายการแบบต่างๆ

### ขั้นตอนการทดลอง
1. สร้างไฟล์ tablelist.html ดังตัวอย่าง:
```html
<table border="1">
    <thead>
        <tr>
            <th>Header 1</th>
            <th>Header 2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Row 1, Cell 1</td>
            <td>Row 1, Cell 2</td>
        </tr>
        <tr>
            <td>Row 2, Cell 1</td>
            <td>Row 2, Cell 2</td>
        </tr>
    </tbody>
</table>
```

### คำอธิบายเพิ่มเติม
- `<table>` กำหนดขอบเขตของตาราง
- `<thead>` สำหรับส่วนหัวตาราง
- `<tbody>` สำหรับเนื้อหาตาราง
- `<tr>` แทนแถว
- `<th>` แทนเซลล์หัวตาราง
- `<td>` แทนเซลล์ข้อมูล

2. การสร้างรายการ โดยเพิ่มเติม Code ในไฟล์ tablelist.html :
```html
<ul>
    <li>Unordered item 1</li>
    <li>Unordered item 2</li>
</ul>

<ol>
    <li>Ordered item 1</li>
    <li>Ordered item 2</li>
</ol>

<dl>
    <dt>Term 1</dt>
    <dd>Definition 1</dd>
    <dt>Term 2</dt>
    <dd>Definition 2</dd>
</dl>
```

### คำอธิบายเพิ่มเติม
- `<ul>` สำหรับรายการแบบไม่เรียงลำดับ
- `<ol>` สำหรับรายการแบบเรียงลำดับ
- `<dl>` สำหรับรายการแบบคำจำกัดความ
- `<li>` แทนรายการแต่ละรายการ

### แบบฝึกหัด
1. สร้างตารางแสดงข้อมูลส่วนตัว
2. สร้างรายการเมนูอาหาร

[<table border="4">
    <h1>routine</h1>
    <thead>
        <tr>
            <th>เวลาตื่น</th>
            <th>เวลาเรียน</th>
            <th>กินข้าว</th>
            <th>เวลาเรียน</th>
            <th>กลับบ้าน</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>05.00-08.00</td>
            <td>09:00</td>
            <td>12:30</td>
            <td>14.00</td>
            <td>18.30</td>
        </tr>
        <tr>
            <td></td>
            <td>Net work</td>
            <td>lunch</td>
            <td>digital</td>
            <td>backhome</td>
        </tr>
    </tbody>
</table>
<h1>ต้อบตามสั่ง</h1>
<ul>
    <li>กระเพราหมูสับไข่ดาว 50 baht</li>
    <li>กระเพราหมูกรอบไข่ดาว 75 baht</li>
    <li>กระเพราปลาหมึกไข่ดาว 80 baht</li>
    <li>กระเพราเครื่องในไก่ไข่ดาว 300 baht</li>
</ul>

<ol>
    <li>กระเพราหมูสับไข่ดาว 50 baht</li>
    <li>กระเพราหมูกรอบไข่ดาว 75 baht</li>
    <li>กระเพราปลาหมึกไข่ดาว 80 baht</li>
    <li>กระเพราเครื่องในไก่ไข่ดาว 300 baht</li>
</ol>

<dl>
    <dt>โจจีโร่</dt>
    <dd>สั่งกระเพราหมูกรอบไข่ดาว</dd>
    <dt>บิ้กแป้ม</dt>
    <dd>สั่งกระเพราหมูสับไข่ดาว</dd>
</dl>]
```html

```
- ภาพผลลัพธ์:
[![image](https://github.com/user-attachments/assets/af24d3a8-0971-40f6-a864-4fae0a7bbeb4)
]

