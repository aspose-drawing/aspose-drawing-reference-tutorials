---
date: 2026-08-28
description: เรียนรู้บทแนะนำการแปลงเมทริกซ์สำหรับ Aspose.Drawing .NET นี้ ซึ่งครอบคลุมวิธีการวาด
  rotated rectangle, การใช้ matrix rotation, และการทำ matrix scaling ด้วย C#
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- matrix rotation c#
- matrix scaling c#
- Aspose.Drawing graphics
lastmod: 2026-08-28
linktitle: Matrix Transformations ใน Aspose.Drawing
og_description: บทแนะนำการแปลงเมทริกซ์สำหรับ Aspose.Drawing .NET. เรียนรู้วิธีการวาด
  rotated rectangle, apply matrix rotation, translate และ scale graphics ด้วย C# ภายในไม่กี่นาที
og_image_alt: Screenshot of a rotated rectangle created with Aspose.Drawing using
  matrix transformations
og_title: บทแนะนำการแปลงเมทริกซ์ – apply rotation, scaling and translation ใน Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  headline: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  type: TechArticle
- description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  name: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  steps:
  - name: set up the canvas
    text: Create a bitmap that will serve as the drawing surface. We also clear it
      with a neutral gray background so the transformed shapes stand out. > **Pro
      tip:** Using `Format32bppPArgb` ensures correct alpha handling when you later
      apply anti‑aliasing.
  - name: define the original rectangle
    text: This rectangle is the base shape we’ll transform. Its coordinates are chosen
      to keep it well within the canvas bounds.
  - name: rotate the rectangle (draw rotated rectangle)
    text: The `Matrix` class is Aspose.Drawing's representation of a 3 × 3 affine
      transformation matrix used for rotation, scaling and translation. We now **apply
      matrix rotation** of 15 degrees around the origin. The helper method `TransformPath`
      (shown later) takes a lambda that receives a `Matrix` instance
  - name: translate the rectangle
    text: Translation moves the shape without altering its size or orientation. Here
      we shift it left‑up by 250 pixels.
  - name: scale the rectangle (matrix scaling C#)
    text: Scaling changes the rectangle’s dimensions. A factor of `0.3f` reduces both
      width and height to 30 % of the original size.
  - name: save the result
    text: Finally, write the transformed image to disk. Adjust the path to point to
      a folder that exists on your machine. > **Note:** The `TransformPath` method
      (used in the steps above) creates a `GraphicsPath` from the rectangle, applies
      the supplied matrix, and draws the transformed shape. It’s a compact w
  type: HowTo
- questions:
  - answer: The documentation is available **[here](https://reference.aspose.com/drawing/net/)**.
    question: Where can I find the Aspose.Drawing documentation?
  - answer: Obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: How do I get a temporary license for Aspose.Drawing?
  - answer: Visit the Aspose.Drawing forum **[here](https://forum.aspose.com/c/drawing/44)**.
    question: Where can I seek support or connect with the community?
  - answer: Yes, download it from **[here](https://releases.aspose.com/drawing/net/)**.
    question: Can I download Aspose.Drawing for .NET?
  - answer: Purchase your license **[here](https://purchase.aspose.com/buy)**.
    question: How can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- matrix transformation
- Aspose.Drawing
- .NET graphics
- C# drawing
- cross‑platform rendering
title: 'บทแนะนำการแปลงเมทริกซ์: matrix transformations ใน Aspose.Drawing สำหรับ .NET'
url: /th/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บทแนะนำการแปลงเมทริกซ์: การแปลงเมทริกซ์ใน Aspose.Drawing สำหรับ .NET

## บทนำ

ใน **matrix transformation tutorial** นี้ คุณจะได้ค้นพบว่า class `Matrix` ของ Aspose.Drawing ช่วยให้คุณหมุน, ย้ายตำแหน่ง, และปรับขนาดวัตถกราฟิกด้วยความแม่นยำระดับพิกเซล ไม่ว่าคุณจะสร้างเครื่องมือแก้ไขแผนภาพ, สร้างรายงานอัตโนมัติ, หรือเพิ่มเอฟเฟกต์ภาพให้กับบริการฝั่งเซิร์ฟเวอร์ การเชี่ยวชาญการแปลงเมทริกซ์เป็นสิ่งสำคัญสำหรับการผลิตผลลัพธ์ที่ดูเป็นมืออาชีพบน Windows, Linux และ macOS  

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้ครอบคลุมอะไร?** แสดงวิธีการหมุน, ย้ายตำแหน่งและปรับขนาดสี่เหลี่ยมโดยใช้ matrix API ของ Aspose.Drawing.  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีทำงานได้สำหรับการพัฒนา; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์.  
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7 และต่อไป  
- **การดำเนินการจะใช้เวลานานเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับตัวอย่างเต็มรูปแบบ  
- **ฉันสามารถดูภาพผลลัพธ์ได้หรือไม่?** ได้ – บทเรียนบันทึกไฟล์ PNG ที่คุณสามารถเปิดได้ทันที  

## บทเรียนการแปลงเมทริกซ์คืออะไร?
บทเรียนการแปลงเมทริกซ์อธิบายวิธีใช้เมทริกซ์เชิง affine ขนาด 3 × 3 เพื่อย้าย, หมุน, ปรับขนาด หรือบิดรูปทรงกราฟิกพื้นฐาน ใน Aspose.Drawing class `Matrix` รวมเอาการดำเนินการเหล่านี้ไว้ด้วยกัน ทำให้ `GraphicsPath` หรือรูปทรงใด ๆ สามารถแปลงได้ด้วยอ็อบเจกต์เดียวที่ใช้ซ้ำได้  

## ทำไมต้องใช้ Aspose.Drawing สำหรับการแปลงเมทริกซ์?
Aspose.Drawing รองรับ **สามระบบปฏิบัติการหลัก** (Windows, Linux, macOS) และสามารถเรนเดอร์ภาพได้ถึง **10,000 × 10,000 px** ภายในเวลา **200 ms** ต่อการดำเนินการบนฮาร์ดแวร์เซิร์ฟเวอร์ทั่วไป ไลบรารีนี้ให้ **ความเข้ากันได้ 100 % กับ GDI+ API** ทำให้คุณสามารถย้ายโค้ด System.Drawing ที่มีอยู่เดิมโดยไม่ต้องเขียนตรรกะใหม่ พร้อมทั้งหลีกเลี่ยงข้อจำกัดด้านไลเซนส์ที่ส่งผลต่อ System.Drawing.Common บนแพลตฟอร์มที่ไม่ใช่ Windows  

## ข้อกำหนดเบื้องต้น
- สภาพแวดล้อมการพัฒนา C# ที่ทำงานได้ (Visual Studio, Rider, หรือ VS Code).  
- ติดตั้ง Aspose.Drawing สำหรับ .NET – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ **[here](https://releases.aspose.com/drawing/net/)** หรือ **[this link](https://releases.aspose.com/drawing/net/)** หากคุณยังไม่ได้ดาวน์โหลด.  
- ความเข้าใจพื้นฐานเกี่ยวกับบิตแมพแคนวาส, สี่เหลี่ยมและกราฟิกพาธ  

## นำเข้าเนมสเปซ
ก่อนอื่น นำเนมสเปซที่จำเป็นเข้ามาในสโคป:

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

เนมสเปซเหล่านี้ให้คุณเข้าถึง `Bitmap`, `Graphics` และ class `Matrix` ที่จำเป็นสำหรับการแปลง  

## คู่มือขั้นตอนต่อขั้นตอน
ต่อไปนี้เป็นการเดินผ่านแบบสั้น ๆ พร้อมหมายเลข แต่ละขั้นตอนมีคำอธิบายสั้น ๆ ตามด้วยโค้ดที่คุณต้องการ (บล็อกโค้ดจะไม่เปลี่ยนจากบทเรียนต้นฉบับ)  

### ขั้นตอนที่ 1: ตั้งค่าแคนวาส
สร้างบิตแมพที่จะทำหน้าที่เป็นพื้นผิวการวาด เราจะล้างพื้นหลังด้วยสีเทากลางเพื่อให้รูปทรงที่แปลงมามองเห็นชัดเจน  

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **เคล็ดลับ:** การใช้ `Format32bppPArgb` จะทำให้การจัดการอัลฟ่าถูกต้องเมื่อคุณใช้การแอนตี้‑อัลลิอซิ่งในภายหลัง  

### ขั้นตอนที่ 2: กำหนดสี่เหลี่ยมต้นฉบับ
สี่เหลี่ยมนี้เป็นรูปทรงฐานที่เราจะทำการแปลง พิกัดของมันถูกเลือกให้อยู่ภายในขอบเขตของแคนวาสอย่างเหมาะสม  

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### ขั้นตอนที่ 3: หมุนสี่เหลี่ยม (วาดสี่เหลี่ยมที่หมุนแล้ว)
class `Matrix` เป็นการแสดงของ Aspose.Drawing สำหรับเมทริกซ์เชิง affine ขนาด 3 × 3 ที่ใช้สำหรับการหมุน, การปรับขนาดและการย้ายตำแหน่ง เราจะ **ทำการหมุนเมทริกซ์** 15 องศารอบจุดต้นกำเนิด เมธอดช่วยเหลือ `TransformPath` (แสดงต่อไป) รับ lambda ที่รับอ็อบเจกต์ `Matrix`  

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### ขั้นตอนที่ 4: ย้ายตำแหน่งสี่เหลี่ยม
การย้ายตำแหน่งจะเคลื่อนรูปทรงโดยไม่เปลี่ยนขนาดหรือการวางแนว ที่นี่เราจะเลื่อนมันไปด้านซ้าย‑บน 250 พิกเซล  

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### ขั้นตอนที่ 5: ปรับขนาดสี่เหลี่ยม (matrix scaling C#)
การปรับขนาดจะเปลี่ยนมิติของสี่เหลี่ยม ตัวคูณ `0.3f` จะลดความกว้างและความสูงลงเหลือ 30 % ของขนาดต้นฉบับ  

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### ขั้นตอนที่ 6: บันทึกผลลัพธ์
สุดท้าย เขียนภาพที่แปลงแล้วลงดิสก์ ปรับเส้นทางให้ชี้ไปยังโฟลเดอร์ที่มีอยู่บนเครื่องของคุณ  

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **หมายเหตุ:** เมธอด `TransformPath` (ที่ใช้ในขั้นตอนข้างต้น) สร้าง `GraphicsPath` จากสี่เหลี่ยม, ใช้เมทริกซ์ที่ให้มา, และวาดรูปทรงที่แปลงแล้ว เป็นวิธีที่กระชับในการใช้ตรรกะการวาดเดียวกันสำหรับการแปลงแต่ละขั้นตอน  

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | วิธีแก้ |
|-------|----------|
| **ภาพปรากฏว่าง** | ตรวจสอบให้แน่ใจว่าไดเรกทอรีผลลัพธ์มีอยู่และคุณมีสิทธิ์เขียน |
| **การแปลงดูไม่ตรงศูนย์กลาง** | จำไว้ว่า `Matrix.Rotate` หมุนรอบจุดต้นกำเนิด (0,0). ย้ายรูปทรงไปยังจุดศูนย์กลางที่ต้องการก่อนหมุน |
| **ความล่าช้าของประสิทธิภาพบนภาพขนาดใหญ่** | ใช้ `graphics.SmoothingMode = SmoothingMode.AntiAlias;` เฉพาะเมื่อจำเป็นและทำการปล่อยอ็อบเจกต์ `Graphics` อย่างทันท่วงที |

## คำถามที่พบบ่อย
**Q: ฉันสามารถหาเอกสาร Aspose.Drawing ได้จากที่ไหน?**  
A: เอกสารมีให้ที่ **[here](https://reference.aspose.com/drawing/net/)**  

**Q: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.Drawing ได้อย่างไร?**  
A: รับไลเซนส์ชั่วคราว **[here](https://purchase.aspose.com/temporary-license/)**  

**Q: ฉันสามารถขอรับการสนับสนุนหรือเชื่อมต่อกับชุมชนได้จากที่ไหน?**  
A: เยี่ยมชมฟอรั่ม Aspose.Drawing **[here](https://forum.aspose.com/c/drawing/44)**  

**Q: ฉันสามารถดาวน์โหลด Aspose.Drawing สำหรับ .NET ได้หรือไม่?**  
A: ได้, ดาวน์โหลดจาก **[here](https://releases.aspose.com/drawing/net/)**  

**Q: ฉันจะซื้อ Aspose.Drawing ได้อย่างไร?**  
A: ซื้อไลเซนส์ของคุณ **[here](https://purchase.aspose.com/buy)**  

## สรุป
คุณได้ทำ **matrix transformation tutorial** อย่างครบถ้วนโดยใช้ Aspose.Drawing สำหรับ .NET แล้ว คุณรู้วิธี **วาดสี่เหลี่ยมที่หมุนแล้ว**, **ทำการหมุนเมทริกซ์**, และทำ **matrix scaling C#** บนรูปทรงใด ๆ ทดลองโดยเชื่อมต่อการแปลงหลายขั้นตอนหรือใช้จุดศูนย์กลางแบบกำหนดเองเพื่อเปิดศักยภาพของเอฟเฟกต์กราฟิกที่สร้างสรรค์ยิ่งขึ้น  

---

**อัปเดตล่าสุด:** 2026-08-28  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

## บทเรียนที่เกี่ยวข้อง
- [วิธีวาดสี่เหลี่ยม – การแปลงระบบพิกัด (การแปลงหน้า) ด้วย Aspose.Drawing API สำหรับ .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [วิธีบันทึก PNG ด้วย Aspose.Drawing – การแปลงโลก](/drawing/net/coordinate-transformations/world-transformation/)
- [การแปลงขั้นตอนต่อขั้นตอน – การแปลงระบบพิกัด](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}