---
date: 2026-06-23
description: เรียนรู้วิธีบันทึก PNG ด้วย Aspose.Drawing, ใช้การแปลงเชิงโลก, และแปลงกราฟิกเป็น
  PNG. รวมตัวอย่าง translate transform C# และการแปลงกราฟิกหลายแบบ.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: การแปลงเชิงโลกใน Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: วิธีบันทึก PNG ด้วย Aspose.Drawing – การแปลงเชิงโลก
url: /th/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีบันทึก PNG ด้วย Aspose.Drawing – การแปลงโลก

## บันทึก Bitmap เป็น PNG – แนะนำ

**How to save PNG** ด้วย Aspose.Drawing เป็นความต้องการทั่วไปเมื่อคุณต้องการภาพคุณภาพสูงและโปร่งใสที่สร้างแบบเรียลไทม์ ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **save bitmap as PNG**, ใช้การแปลงโลกเช่น translate, rotate, และ scale, และสุดท้ายแปลงกราฟิกเป็น PNG — ทั้งหมดด้วยโค้ด C# ที่สะอาดและดูแลง่าย ไม่ว่าคุณจะสร้างเครื่องมือรายงาน, คอมโพเนนต์แผนภูมิ, หรือเรนเดอร์ UI แบบกำหนดเอง การเชี่ยวชาญขั้นตอนเหล่านี้จะทำให้คุณสร้างภาพไดนามิกที่ดูดีบนอุปกรณ์ใดก็ได้.

## คำตอบสั้น
- **What does “world transformation” mean?** It maps your drawing’s logical (world) coordinates to the page (device) coordinates.  
- **Can I export the result as PNG?** Yes – after drawing you simply call `bitmap.Save(...)` with a `.png` extension.  
- **Do I need a license for Aspose.Drawing?** การทดลองใช้ฟรีทำงานสำหรับการพัฒนา; จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการผลิต.  
- **Is this compatible with .NET 6/7?** แน่นอน — Aspose.Drawing รองรับ .NET Framework 4.5+ และ .NET Core/5/6/7.  
- **How many transformations can I chain?** คุณสามารถใช้ **multiple graphics transformations** ตามลำดับ (translate, rotate, scale, ฯลฯ).

## การแปลงโลกใน Aspose.Drawing คืออะไร

การแปลงโลกเปลี่ยนระบบพิกัดที่คำสั่งการวาดของคุณใช้ โดยค่าเริ่มต้น (0,0) อยู่ที่มุมซ้าย‑บนของ bitmap ด้วย `TranslateTransform`, `RotateTransform`, หรือ `ScaleTransform` คุณสามารถย้ายจุดกำเนิดนั้น, หมุนรูปทรง, หรือปรับขนาดโดยไม่เปลี่ยนแปลงเรขาคณิตเดิม.

## วิธีบันทึก PNG ด้วย Aspose.Drawing?

โหลดอ็อบเจ็กต์ `Bitmap`, ตั้งค่าการแปลงโลกที่ต้องการบนอินสแตนซ์ `Graphics` ของมัน, วาดรูปทรงของคุณ, และสุดท้ายเรียก `bitmap.Save("output.png", ImageFormat.Png)`. คำสั่งบันทึกบรรทัดเดียวนี้จะเขียนไฟล์ PNG แบบไม่มีการสูญเสียที่คงความโปร่งใสและความแม่นยำของสี ทำให้เหมาะสำหรับทรัพยากรเว็บและการซ้อนทับ UI.

## ทำไมต้องใช้ตัวอย่าง Graphics Translate

ตัวอย่าง graphics translate ช่วยให้คุณย้ายจุดกำเนิดของการวาดเพียงครั้งเดียวแทนการคำนวณใหม่ทุกจุด วิธีนี้ลดความซับซ้อนของโค้ด, ปรับปรุงความอ่านง่าย, และให้เอนจินกราฟิกจัดการคณิตศาสตร์เมทริกซ์อย่างมีประสิทธิภาพ ซึ่งสามารถเพิ่มประสิทธิภาพการเรนเดอร์ได้ถึง 30 % บนแคนวาสขนาดใหญ่.

## ตัวอย่าง Graphics Translate

ตัวอย่าง **graphics translate example** แสดงว่าการย้ายจุดกำเนิดทำให้การจัดตำแหน่งง่ายขึ้นอย่างไร แทนการคำนวณใหม่ทุกจุด คุณเพียงเปลี่ยนระบบพิกัดครั้งเดียวและวาดเหมือนว่าจุดกำเนิดใหม่อยู่ที่ศูนย์กลางของแคนวาส.

## ข้อกำหนดเบื้องต้น

- **Aspose.Drawing library** ที่รวมไว้ในโปรเจกต์ .NET ของคุณ – ดาวน์โหลดจาก [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/) อย่างเป็นทางการ.  
- **document directory** ที่ไฟล์ภาพผลลัพธ์จะถูกบันทึก.  
- ความคุ้นเคยพื้นฐานกับไวยากรณ์ **C#** และ Visual Studio หรือ IDE ที่คุณชอบ.  

ตอนนี้, มาดูโค้ดกัน!

## นำเข้า Namespaces

`Bitmap`, `Graphics` และยูทิลิตี้การวาดของ Aspose อยู่ใน namespaces เหล่านี้  
**Definition:** `System.Drawing` ให้ประเภทหลักของ GDI+, ส่วน `Aspose.Drawing` ขยายด้วยความสามารถข้ามแพลตฟอร์ม.

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: สร้าง Bitmap

เราเริ่มด้วยการสร้างแคนวาสเปล่าเพื่อเก็บการวาดของเรา  

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` สร้าง bitmap 32‑บิตต่อพิกเซลพร้อมอัลฟ่าที่ทำล่วงหน้า ซึ่งเป็นรูปแบบที่เหมาะที่สุดสำหรับการส่งออก PNG เนื่องจากคงความโปร่งใสโดยไม่ต้องแปลงเพิ่มเติม.

- **Why 32bppPArgb?** รูปแบบพิกเซลนี้รองรับความโปร่งใสของอัลฟาและการแสดงสีคุณภาพสูง เหมาะอย่างยิ่งสำหรับการส่งออก PNG.  
- **Pro tip:** ปรับความกว้าง/ความสูงให้ตรงกับขนาดภาพเป้าหมายของคุณ.

### ขั้นตอนที่ 2: ตั้งค่าการแปลงโลก (Graphics Translate Example)

`TranslateTransform` ย้ายจุดกำเนิดของระบบพิกัดไปยังตำแหน่งใหม่  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` ย้ายจุด (0,0) ไปยังศูนย์กลางของแคนวาส หลังจากเรียกนี้ รูปทรงใด ๆ ที่คุณวาดด้วยพิกัด (0,0) จะปรากฏที่กลางภาพ.

- นี้ย้ายจุด (0,0) ไปยัง (500, 400) – กลางของแคนวาสขนาด 1000 × 800.  
- คุณสามารถต่อเนื่องการแปลงเพิ่มเติม: `RotateTransform` หมุนระบบพิกัด, และ `ScaleTransform` ปรับขนาด, ทำให้สามารถใช้ **multiple graphics transformations**.

### ขั้นตอนที่ 3: วาดสี่เหลี่ยมโดยใช้พิกัดที่แปลงแล้ว

`DrawRectangle` วาดสี่เหลี่ยมโดยใช้ปากกาที่ระบุและพิกัด  

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` วาดสี่เหลี่ยมที่อยู่กึ่งกลางแคนวาส เนื่องจากมุมซ้าย‑บนของมันถูกเลื่อนออกจากจุดกำเนิดที่แปลงแล้วครึ่งหนึ่งของความกว้างและความสูง.

- มุมซ้าย‑บนของสี่เหลี่ยมเริ่มที่จุดกำเนิดที่แปลงแล้ว (ศูนย์กลางของภาพ).  
- อย่าลังเลที่จะทดลองรูปทรงอื่น ๆ — วงรี, เส้น, หรือพาธที่กำหนดเอง.

### ขั้นตอนที่ 4: บันทึกผลลัพธ์ – แปลงกราฟิกเป็น PNG

`Save` เขียน bitmap ไปยังไฟล์ในรูปแบบภาพที่ระบุ  
`ImageFormat` ระบุรูปแบบไฟล์สำหรับบันทึกภาพ เช่น PNG  

`bitmap.Save(outputPath, ImageFormat.Png)` เขียนไฟล์ PNG แบบไม่มีการสูญเสียที่สามารถใช้โดยตรงในหน้าเว็บหรือคอมโพเนนต์ UI  

- PNG คงสีและความโปร่งใสที่ตั้งค่าไว้ก่อนหน้าอย่างแม่นยำ.  
- แทนที่ `"Your Document Directory"` ด้วยเส้นทางจริงบนเครื่องของคุณ.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **File not found error** เมื่อบันทึก | โฟลเดอร์เป้าหมายไม่มีอยู่. | สร้างโฟลเดอร์โดยโปรแกรม (`Directory.CreateDirectory`) ก่อนเรียก `Save`. |
| **Blank image** หลังการแปลง | `TranslateTransform` ถูกเรียกหลังการวาด. | ตรวจสอบให้แน่ใจว่าการแปลงตั้งค่า **ก่อน** คำสั่งวาดใด ๆ. |
| **Distorted colors** | ใช้รูปแบบพิกเซลที่ไม่เข้ากัน. | ใช้ `Format32bppPArgb` สำหรับการส่งออก PNG. |

## คำถามที่พบบ่อย

**Q: Can I apply more than one transformation?**  
A: ใช่ — คุณสามารถต่อเนื่อง `TranslateTransform`, `RotateTransform`, และ `ScaleTransform` เพื่อสร้างเอฟเฟกต์ซับซ้อนใน pipeline กราฟิกเดียว.

**Q: Is Aspose.Drawing free for commercial projects?**  
A: มีการทดลองใช้ฟรีสำหรับการประเมิน, แต่ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์.

**Q: Does this work with .NET Core and .NET 5/6/7?**  
A: แน่นอน. Aspose.Drawing รองรับรันไทม์ .NET สมัยใหม่ทั้งหมด รวมถึง .NET Core, .NET 5, .NET 6, และ .NET 7.

**Q: Where can I find the full API reference?**  
A: เอกสารเต็มสามารถดูได้ที่ [here](https://reference.aspose.com/drawing/net/).

**Q: How do I troubleshoot a missing output file?**  
A: ตรวจสอบสตริงของพาธ, ยืนยันสิทธิ์การเขียน, และยืนยันว่าโฟลเดอร์มีอยู่ก่อนเรียก `Save`.

## สรุป

คุณได้เรียนรู้ **how to save PNG** ด้วย Aspose.Drawing, ใช้ **world transformation**, และทำ **graphics translate example** ที่สามารถขยายด้วยการหมุนหรือการสเกลได้ ด้วยการเชี่ยวชาญบล็อกเหล่านี้ คุณสามารถสร้างภาพไดนามิก, สร้างแผนภูมิแบบกำหนดเอง, หรือสร้างกราฟิกแบบเรียลไทม์สำหรับแอปพลิเคชัน .NET ใดก็ได้.

---

**อัปเดตล่าสุด:** 2026-06-23  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  
**แหล่งข้อมูลที่เกี่ยวข้อง:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## บทแนะนำที่เกี่ยวข้อง

- [บทแนะนำการแปลงเมทริกซ์: การแปลงเมทริกซ์ใน Aspose.Drawing สำหรับ .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [วิธีหมุนภาพด้วย Aspose.Drawing Global Transformation](/drawing/net/coordinate-transformations/global-transformation/)
- [การแปลงระบบพิกัด – การแปลงหน้าใน Aspose.Drawing สำหรับ .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}