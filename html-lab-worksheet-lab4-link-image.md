# ใบงานการทดลอง HTML

## การทดลองที่ 4: การสร้างลิงก์และการแทรกรูปภาพ

### การเตรียมโครงสร้างโฟลเดอร์และไฟล์
1. สร้างโครงสร้างโฟลเดอร์:
   ```
   html-workshop/
   ├── index.html
   ├── pages/
   │   ├── about.html
   │   └── contact.html
   ├── images/
   │   ├── logo.jpg
   │   └── products/
   │       ├── product1.jpg
   │       └── product2.jpg
   └── files/
       └── document.pdf
   ```

2. ขั้นตอนการสร้างโครงสร้าง:
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "pages"
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "images"
   - ในโฟลเดอร์ images > New Folder > สร้าง "products"
   - คลิกขวาในโฟลเดอร์ html-workshop > New Folder > สร้าง "files"

3. สร้างไฟล์ HTML:
   - ในโฟลเดอร์หลัก: สร้าง index.html (ใช้ไฟล์เดิมที่มีได้)
   - ในโฟลเดอร์ pages: สร้าง about.html และ contact.html

4. จัดเตรียมไฟล์:
   - นำรูปภาพที่ต้องการใช้ไปไว้ในโฟลเดอร์ images
   - นำรูปภาพสินค้าไปไว้ในโฟลเดอร์ products
   - นำไฟล์เอกสารไปไว้ในโฟลเดอร์ files

### ขั้นตอนการทดลอง

#### ส่วนที่ 1: การสร้างลิงก์
1. เปิดไฟล์ index.html และใส่โครงสร้างพื้นฐาน:
```html
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <title>หน้าหลัก</title>
</head>
<body>
    <!-- ส่วนของเนื้อหา -->
</body>
</html>
```

2. สร้างเมนูนำทางพื้นฐาน:
```html
<nav>
    <!-- ลิงก์ภายใน - ไปยังหน้าในเว็บไซต์เดียวกัน -->
    <a href="index.html">หน้าหลัก</a>
    <a href="pages/about.html">เกี่ยวกับเรา</a>
    <a href="pages/contact.html">ติดต่อเรา</a>
    
    <!-- ลิงก์ภายนอก - เปิดในแท็บใหม่ -->
    <a href="https://www.google.com" target="_blank">
        ไปยัง Google
    </a>
</nav>
```
คำอธิบาย:
- `href="..."` - กำหนดเส้นทางของลิงก์
- `target="_blank"` - เปิดลิงก์ในแท็บใหม่

3. สร้างลิงก์ภายในหน้าเดียวกัน:
```html
<!-- สร้างจุดเชื่อมโยง -->
<section id="top">
    <h1>เนื้อหาส่วนบน</h1>
</section>

<section id="products">
    <h2>สินค้าของเรา</h2>
</section>

<!-- ลิงก์ไปยังจุดเชื่อมโยง -->
<a href="#top">กลับด้านบน</a>
<a href="#products">ไปยังสินค้า</a>
```
คำอธิบาย:
- `id="..."` - กำหนดจุดเชื่อมโยง
- `href="#..."` - ลิงก์ไปยัง id ที่กำหนด

4. สร้างลิงก์พิเศษ:
```html
<!-- ลิงก์อีเมล -->
<a href="mailto:contact@example.com">ส่งอีเมลหาเรา</a>

<!-- ลิงก์โทรศัพท์ -->
<a href="tel:+66812345678">โทร 081-234-5678</a>

<!-- ลิงก์ดาวน์โหลด -->
<a href="files/document.pdf" download>
    ดาวน์โหลดเอกสาร
</a>
```
คำอธิบาย:
- `mailto:` - เปิดโปรแกรมอีเมล
- `tel:` - เปิดโปรแกรมโทรศัพท์
- `download` - ดาวน์โหลดไฟล์แทนการเปิด

#### ส่วนที่ 2: การแทรกรูปภาพ
1. แทรกรูปภาพพื้นฐาน:
```html
<!-- รูปภาพในโฟลเดอร์ images -->
<img src="images/logo.jpg" 
     alt="โลโก้บริษัท"
     width="200">

<!-- รูปภาพในโฟลเดอร์ย่อย products -->
<img src="images/products/product1.jpg" 
     alt="สินค้าชิ้นที่ 1"
     width="300"
     height="200">
```
คำอธิบาย:
- `src="..."` - ระบุตำแหน่งของรูปภาพ
- `alt="..."` - ข้อความทดแทนเมื่อไม่สามารถแสดงรูปได้
- `width="..."` - กำหนดความกว้าง
- `height="..."` - กำหนดความสูง

2. ใช้ figure และ figcaption:
```html
<figure>
    <img src="images/products/product2.jpg" 
         alt="สินค้าชิ้นที่ 2">
    <figcaption>
        รายละเอียดสินค้าชิ้นที่ 2
    </figcaption>
</figure>
```
คำอธิบาย:
- `<figure>` - จัดกลุ่มรูปภาพและคำอธิบาย
- `<figcaption>` - คำอธิบายประกอบรูปภาพ

3. สร้างรูปภาพที่คลิกได้:
```html
<a href="images/products/product1.jpg">
    <img src="images/products/product1.jpg" 
         alt="คลิกเพื่อดูรูปขนาดใหญ่"
         width="200">
</a>
```

### หมายเหตุ
- ตรวจสอบการสะกดชื่อไฟล์และโฟลเดอร์ให้ถูกต้อง
- path ของรูปภาพต้องถูกต้องตามโครงสร้างโฟลเดอร์
- ทดสอบการทำงานของลิงก์ทุกจุด

### แบบฝึกหัด
1. สร้างแกลเลอรีสินค้า:
   - สร้างโฟลเดอร์ images/gallery
   - ใส่รูปภาพอย่างน้อย 4 รูป
   - แต่ละรูปต้องคลิกดูขนาดใหญ่ได้
   - มีคำอธิบายใต้รูป
   - มีปุ่มกลับด้านบน

### บันทึกผลการทดลอง
[<!DOCTYPE html>
<html lang="th">
    <div style="text-align: center;">
    <img src="image/Wave-125i-Logo-2012-(Medium).jpg" 
alt="โลโก้บริษัท"
width="150">
<div style="text-align: center;">
    <p>Honda thailand </p>
</div>

<head>
    <meta charset="UTF-8">
    <title>หน้าหลัก</title>
</head>
<nav>
    <!-- ลิงก์ภายใน - ไปยังหน้าในเว็บไซต์เดียวกัน -->
    <a href="https://www.thaihonda.co.th/honda/motorcycle/family/all-new-wave125i">หน้าหลัก</a>
    
    
    <!-- ลิงก์ภายนอก - เปิดในแท็บใหม่ -->
    <a href="https://www.motorshow.me/uploadImages/GalleryDocs/Doc6652.pdf" target="_blank">
        สเปค
    </a>
</nav>
</html>
<body>
    Honda Wave 125i 2023
</body>
</html>
<section id="top">
    <h1>เนื้อหาส่วนสำคัญ</h1>
</section>
โช๊คอัพถูกปรับปรุงใหม่ เพิ่มระยะยุบของโช้คอัพด้านหน้าและด้านหลัง สามารถซับแรงกระแทก ช่วยให้ทรงตัวดียิ่งขึ้น

ระบบเบรกด้านหน้า ใช้ดิสก์เบรกเดี่ยว พร้อมปั้มเบรก 1 พอต ส่วนล้อใช้เป็นล้ออัลลอยขนาด 17 นิ้ว รัดยางขนาด 70/90-17
<section id="products">
    <h2>สินค้าของเรา</h2>
</section>
<a href="https://www.motorshow.me/uploadImages/GalleryDocs/Doc6652.pdf" target="_blank">
    สเปค
</a>
<figure>
<img src="image/product/000000187306_7237487c_c4ea_4667_8681_38fa2c36fd10.jpg" 
     alt="สินค้าชิ้นที่ 1">
    <figcaption>
        All New Wave 125i มาพร้อมดีไซน์สปอร์ตด้วยเฟรมใหม่ ออกแบบวัสดุและเทคนิคการเชื่อมต่อตัวถังให้แข็งแรงทนทาน น้ำหนักเบาลง ควบคุมรถได้ง่ายและคล่องตัวกว่าเดิม 
    </figcaption>
<figure>
   
    <img src="image/product/05ThHonda_Wave125i-2022_WingCenter_Color_chart_Blue.png" 
         alt="สินค้าชิ้นที่ 2">
    <figcaption>
        All New Wave 125i มาพร้อมคอนเซปต์ “ผู้นำที่ทุกคนเชื่อมั่น” โดยมี “เวียร์-ศุกลวัฒน์ คณารส” เป็น พรีเซนเตอร์ เพื่อสะท้อนอัตลักษณ์ความเป็น “ผู้นำที่ทุกคนเชื่อมั่น” ทั้งตัวผลิตภัณฑ์และผู้ครอบครอง ให้สมกับเป็นรถจักรยานยนต์ครอบครัวระดับท็อปคลาสแห่งยุค

</figure>
<a href="https://www.motor1.com/reviews/738653/2025-bmw-m5-review/" target="_blank">
    สเปค
</a>
<figure>
<a href="image/product/8b05e021517888e1d14db53595303fa1.webp">
    <img src="image/product/8b05e021517888e1d14db53595303fa1.webp" 
         alt="คลิกเพื่อดูรูปขนาดใหญ่"
         width="200">
</figure>
</a>

<!-- ลิงก์ไปยังจุดเชื่อมโยง -->
<a href="http://127.0.0.1:5500/index.html">กลับสู่หน้าหลัก</a>
<a href="https://www.bmw.co.th/th/all-models.html">ไปยังสินค้า</a>

<!-- ลิงก์อีเมล -->
<a href="67030172@kmitl.ac.th">ส่งอีเมลหาเรา</a>

<!-- ลิงก์โทรศัพท์ -->
<a href="tel:+66955243927">โทร 099-287-8348</a>

<!-- ลิงก์ดาวน์โหลด -->
<a href="file/PGMFI.pdf" download>
    ดาวน์โหลดเอกสาร
</a>]
![image](https://github.com/user-attachments/assets/7265b16a-6203-4be5-986b-f1b8f1171bdd)




