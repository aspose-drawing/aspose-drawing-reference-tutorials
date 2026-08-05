---
date: 2026-05-24
description: เรียนรู้วิธีตั้งหน่วยใน Aspose.Drawing สำหรับ .NET, แปลงหน่วยกราฟิกได้อย่างง่ายดาย,
  และเชี่ยวชาญการวัดที่แม่นยำสำหรับการเรนเดอร์กราฟิก
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Units of Measure ใน Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: วิธีตั้งหน่วยใน Aspose.Drawing สำหรับ .NET – Units of Measure
url: /th/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีตั้งหน่วยใน Aspose.Drawing สำหรับ .NET – หน่วยวัด

## บทนำ

ยินดีต้อนรับสู่โลกของ Aspose.Drawing สำหรับ .NET ที่ซึ่งความแม่นยำและความยืดหยุ่นมาบรรจบกันในการจัดการกราฟิก ในบทแนะนำนี้คุณจะได้ค้นพบ **วิธีตั้งหน่วย** สำหรับการวาดของคุณ เรียนรู้การ **แปลงหน่วยกราฟิก** ระหว่าง points, millimeters, และ inches และดูตัวอย่างจริงที่ทำให้ภาพของคุณพิกเซล‑เพอร์เฟ็กต์ ไม่ว่าคุณจะสร้างรายงาน, รูปย่อ, หรือแผนภูมิแบบกำหนดเอง การเชี่ยวชาญหน่วยวัดเป็นสิ่งสำคัญสำหรับการเรนเดอร์ที่สม่ำเสมอบนอุปกรณ์ต่าง ๆ

## คำตอบอย่างรวดเร็ว
- **วิธีหลักในการเปลี่ยนหน่วยคืออะไร?** เรียก `graphics.PageUnit = PageUnit.Point` (หรือ `.Millimeter`, `.Inch`) บนวัตถุ `Graphics`.  
- **หน่วยใดเท่ากับ 1/72 นิ้ว?** Points.  
- **มิลลิเมตรกี่มม.ในหนึ่งนิ้ว?** 25.4 mm = 1 inch.  
- **ต้องใช้ไลบรารีเพิ่มเติมเพื่อใช้หน่วยหรือไม่?** No, the Aspose.Drawing core library provides all unit constants.  
- **ฉันสามารถผสมหน่วยในภาพเดียวได้หรือไม่?** Set the unit once per `Graphics` instance; draw everything using that unit for consistency.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกสู่บทแนะนำ โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งานแล้ว:

- Aspose.Drawing for .NET: ตรวจสอบว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/drawing/net/).
- Document Directory: มีโฟลเดอร์ที่กำหนดไว้สำหรับบันทึกเอกสารที่สร้างขึ้น
- Basic C# Knowledge: ความเข้าใจพื้นฐานของ C# แนะนำเพื่อให้คุณใช้คู่มือนี้ได้เต็มที่

## นำเข้า Namespaces

ก่อนเริ่ม เรามานำเข้า Namespaces ที่จำเป็นเพื่อใช้ Aspose.Drawing อย่างมีประสิทธิภาพ:

```csharp
using System.Drawing;
```

ตอนนี้เราจะทำการแยกแต่ละตัวอย่างออกเป็นหลายขั้นตอน:

## วิธีตั้งหน่วยเป็น Points?

คลาส `Bitmap` แสดงถึงภาพในหน่วยความจำที่ทำหน้าที่เป็นผ้าใบสำหรับการวาด โหลด bitmap ของคุณ สร้างวัตถุ `Graphics` แล้วตั้งหน่วยหน้าเป็น points — สิ่งนี้บอกให้ Aspose.Drawing ตีความพิกัดทั้งหมดเป็นค่า 1/72 inch การใช้ points ให้การควบคุมละเอียดสำหรับกราฟิกพร้อมพิมพ์และช่วยให้คุณระบุความกว้างของเส้นได้อย่างแม่นยำ

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### ขั้นตอน 1: สร้าง Bitmap  
คลาส `Bitmap` แสดงถึงภาพในหน่วยความจำที่ทำหน้าที่เป็นผ้าใบสำหรับการวาด

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### ขั้นตอน 2: สร้าง Graphics Object  
`Graphics` ให้เมธอดการวาดสำหรับเรนเดอร์รูปทรงและข้อความลงบน `Bitmap`

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### ขั้นตอน 3: ตั้ง Page Unit เป็น Points  
`PageUnit` เป็น enumeration ที่ระบุหน่วยวัดสำหรับพิกัดของหน้า `PageUnit.Point` กำหนด points เป็นหน่วยวัด (1 point = 1/72 inch) การตั้งค่านี้จะใช้กับการเรียกวาดทั้งหมดต่อไป

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### ขั้นตอน 4: วาดสี่เหลี่ยมในหน่วย Points  
เมื่อคุณวาดสี่เหลี่ยมหลังจากตั้งหน่วยแล้ว มิติที่คุณระบุจะถูกตีความเป็น points ทำให้ขนาดแม่นยำ

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## วิธีตั้งหน่วยเป็น Millimeters?

`PageUnit` เป็น enumeration ที่ระบุหน่วยวัดสำหรับพิกัดของหน้า การสลับเป็นมิลลิเมตรเป็นประโยชน์เมื่อคุณต้องการขนาดเมตริก เช่น การสร้างแผนผังวิศวกรรม Aspose.Drawing ปฏิบัติ 1 mm เป็น 1/25.4 inch ทำให้คุณสามารถจัดตำแหน่งกราฟิกกับการวัดจริงที่ใช้ในอุตสาหกรรมและเอกสารเทคนิคได้

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### ขั้นตอน 1: ตั้ง Page Unit เป็น Millimeters  
กำหนด `PageUnit.Millimeter` ให้กับวัตถุ `Graphics`; พิกัดทั้งหมดจะสอดคล้องกับระบบเมตริก

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### ขั้นตอน 2: วาดสี่เหลี่ยมในหน่วย Millimeters  
ความกว้างและความสูงของสี่เหลี่ยมตอนนี้แสดงเป็นมิลลิเมตร ทำให้การจัดตำแหน่งกับการวัดจริงเป็นเรื่องง่ายและรับประกันว่าผลลัพธ์ที่พิมพ์ออกมาจะตรงกับขนาดในโลกจริง

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## วิธีตั้งหน่วยเป็น Inches?

`Graphics` ให้เมธอดการวาดสำหรับเรนเดอร์รูปทรงและข้อความลงบน `Bitmap` นิ้วเป็นหน่วยเริ่มต้นสำหรับเครื่องมือออกแบบหลาย ๆ ตัวในสหรัฐ การตั้งหน่วยเป็นนิ้วทำให้คุณคิดในหน่วยที่คุ้นเคยเมื่อจัดวาง UI และช่วยให้การเปลี่ยนจากการออกแบบบนหน้าจอไปสู่การพิมพ์ที่ใช้หน่วยนิ้วเป็นเรื่องง่าย

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### ขั้นตอน 1: ตั้ง Page Unit เป็น Inches  
`PageUnit.Inch` เปลี่ยนระบบพิกัดให้ 1 หน่วยเท่ากับ 1 inch ให้วิธีที่ตรงไปตรงมาสำหรับการกำหนดขนาดองค์ประกอบในเลย์เอาต์ที่มุ่งเน้นการพิมพ์

CODE_BLOCK_PLACEHOLDER_10_END

### ขั้นตอน 2: วาดสี่เหลี่ยมในหน่วย Inches  
ตอนนี้รูปทรงใด ๆ ที่คุณวาดจะใช้หน่วยนิ้วเป็นฐานการวัด ซึ่งเหมาะสำหรับเลย์เอาต์การพิมพ์และการสื่อสารขนาดให้กับผู้ที่คุ้นเคยกับหน่วยอิมพีเรียล

CODE_BLOCK_PLACEHOLDER_11_END

## บันทึกผลลัพธ์

หลังจากทำตัวอย่างครบแล้ว ให้บันทึกภาพที่ได้ลงในโฟลเดอร์เอกสารของคุณ เมธอด `Bitmap.Save` จะเขียนไฟล์ในรูปแบบที่คุณระบุ (PNG, JPEG, ฯลฯ)

CODE_BLOCK_PLACEHOLDER_12_END

ตอนนี้คุณได้สำรวจหน่วยวัดที่หลากหลายใน Aspose.Drawing สำหรับ .NET แล้ว โดยสร้างภาพสี่เหลี่ยมในรูปแบบ points, millimeters, และ inches อย่างสมบูรณ์

## ทำไมต้องใช้ระบบหน่วยของ Aspose.Drawing?

Aspose.Drawing รองรับ **รูปแบบภาพกว่า 30 ประเภท** และสามารถประมวลผลภาพขนาดสูงสุด **5000 × 5000 พิกเซล** โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ ส่งมอบประสิทธิภาพสูงสำหรับการสร้างกราฟิกขนาดใหญ่ การตั้งหน่วยอย่างชัดเจนช่วยขจัดการคาดเดา ลดข้อผิดพลาดการแปลง และทำให้ผลลัพธ์ของคุณตรงกับมิติทางกายภาพที่แน่นอนบนทุกแพลตฟอร์ม

## ปัญหาทั่วไปและวิธีแก้

- **Unexpected size after saving** – ตรวจสอบว่าคุณได้ตั้งค่า `graphics.PageUnit` **ก่อน** การเรียกวาดใด ๆ; การเปลี่ยนหน่วยภายหลังจะไม่ปรับขนาดรูปทรงที่มีอยู่แล้วโดยอัตโนมัติ  
- **Blurry output on high‑DPI screens** – เพิ่มความละเอียดของ bitmap (เช่น `new Bitmap(width, height, 300)`) เพื่อให้ตรงกับ DPI เป้าหมาย  
- **Mixed units in one image** – สร้าง `Graphics` แยกต่างหากสำหรับแต่ละหน่วยหรือทำการแปลงด้วยตนเองก่อนวาด

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose. Drawing สำหรับ .NET กับ .NET Frameworks อื่นๆ ได้หรือไม่
คำตอบที่ 1: เป็นไปได้, Aspose. Drawing มีหลาย .NET frameworks ที่ยังคงมีการพัฒนาของคุณ

### Q2: มีการทดลองใช้ฟรีหรือไม่?
A2: พยายามตรวจสอบอย่างละเอียด Aspose. Drawing สามารถทำได้ [ที่นี่](https://releases.aspose.com/)

### Q3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose. Drawing สำหรับ .NET ได้อย่างไร
A3: จำเป็นต้องมี [Aspose. Drawing Forum](https://forum.aspose.com/c/drawing/44) เพื่อรับชุมชนและการเดินทาง

### Q4: ฉันสามารถซื้อใบอนุญาตชั่วคราวสำหรับโครงการระยะสั้นได้หรือไม่
A4: ทำได้, ไม่เคยรับมาก่อนชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q5: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose. Drawing ได้จากที่ไหน?
A5: เอกสารฉบับเต็มพร้อมให้บริการ [ที่นี่](https://reference.aspose.com/drawing/net/)

---

**อัปเดตล่าสุด:** 2026-05-24  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
