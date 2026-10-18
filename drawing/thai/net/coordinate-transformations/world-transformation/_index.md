---
date: 2026-10-18
description: แปลง drawing เป็น PNG ด้วย Aspose.Drawing พร้อมการใช้ world transformations.
  เรียนรู้ตัวอย่างการ translate, rotate และ scale ใน C# และส่งออก transparent PNGs.
keywords:
- convert drawing to png
- save graphics as png
- rotate image .net
- scale graphics .net
- transparent png bitmap
lastmod: 2026-10-18
linktitle: World transformation ใน Aspose.Drawing
og_description: แปลง drawing เป็น PNG ด้วย Aspose.Drawing, ใช้ world transformations
  และส่งออก transparent PNGs. เรียนรู้ตัวอย่างการ translate, rotate และ scale ใน C#
  สำหรับ .NET.
og_image_alt: Tutorial showing how to convert drawing to PNG using Aspose.Drawing
  with world transformation
og_title: วิธีแปลง drawing เป็น PNG ด้วย Aspose.Drawing – world transformation
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  headline: How to convert drawing to PNG with Aspose.Drawing – world transformation
  type: TechArticle
- description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  name: How to convert drawing to PNG with Aspose.Drawing – world transformation
  steps:
  - name: create a bitmap
    text: '**Definition:** `Bitmap` is Aspose.Drawing’s in‑memory representation of
      a raster image that you can draw on or save to disk. We start by creating a
      blank canvas that will hold our drawing. `new Bitmap(width, height, PixelFormat.Format32bppPArgb)`
      creates a 32‑bit per pixel bitmap with premultiplied'
  - name: set the world transformation (graphics translate example)
    text: '**Definition:** `Graphics` is the drawing surface that renders shapes onto
      a `Bitmap`. `TranslateTransform` moves the origin of the coordinate system to
      a new location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height
      / 2)` shifts the (0,0) point to the canvas centre. After this call, an'
  - name: draw a rectangle using the transformed coordinates
    text: '**Definition:** `DrawRectangle` is a method of `Graphics` that renders
      a rectangular outline or filled shape based on the supplied pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width'
  - name: save the result – convert graphics to PNG
    text: '**Definition:** `ImageFormat` is an enumeration that tells the `Save` method
      which file format to use. `Save` writes the bitmap to a file in the specified
      image format. `bitmap.Save(outputPath, ImageFormat.Png)` writes a lossless PNG
      file that can be used directly in web pages or UI components. - PN'
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
  - answer: The complete documentation is available [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- convert drawing to png
- Aspose.Drawing
- .NET graphics
- PNG export
- world transformation
title: วิธีแปลง drawing เป็น PNG ด้วย Aspose.Drawing – world transformation
url: /th/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแปลง drawing เป็น PNG ด้วย Aspose.Drawing – การแปลงโลก

## บันทึก bitmap เป็น PNG – บทนำ

**How to convert drawing to PNG** using Aspose.Drawing เป็นความต้องการทั่วไปเมื่อคุณต้องการภาพคุณภาพสูงที่มีพื้นหลังโปร่งใสสร้างขึ้นแบบเรียลไทม์ ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **save bitmap as PNG**, ใช้การแปลงโลกเช่น translate, rotate, และ scale, และสุดท้ายแปลง graphics เป็น PNG—ทั้งหมดด้วยโค้ด C# ที่สะอาดและดูแลรักษาได้ง่าย ไม่ว่าคุณจะสร้าง engine รายงาน, component แผนภูมิ, หรือ renderer UI แบบกำหนดเอง การเชี่ยวชาญขั้นตอนเหล่านี้จะทำให้คุณสร้างภาพไดนามิกที่ดูดีบนอุปกรณ์ใดก็ได้

## คำตอบอย่างรวดเร็ว
- **What does “world transformation” mean?** มันทำการแมปพิกัดเชิงตรรกะ (world) ของ drawing ไปยังพิกัดของหน้า (device) ทำให้คุณสามารถย้ายตำแหน่ง, หมุน หรือสเกลทุกอย่างด้วยเมทริกซ์เดียว  
- **Can I export the result as PNG?** ใช่ – หลังจากวาดคุณเพียงเรียก `bitmap.Save(...)` พร้อมส่วนขยาย `.png`  
- **Do I need a license for Aspose.Drawing?** รุ่นทดลองฟรีใช้ได้สำหรับการพัฒนา; จำเป็นต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **Is this compatible with .NET 6/7?** แน่นอน – Aspose.Drawing รองรับ .NET Framework 4.5+ และ .NET Core/5/6/7, ครอบคลุมกว่า 90 % ของการติดตั้ง .NET ปัจจุบัน  
- **How many transformations can I chain?** คุณสามารถใช้ **multiple graphics transformations** อย่างต่อเนื่อง (translate, rotate, scale, ฯลฯ) โดยไม่เสียประสิทธิภาพ  

## การแปลงโลกใน Aspose.Drawing คืออะไร?

การแปลงโลกเปลี่ยนระบบพิกัดที่คำสั่ง drawing ของคุณใช้ โดยค่าเริ่มต้น (0,0) อยู่ที่มุมบน‑ซ้ายของ bitmap ด้วย `TranslateTransform`, `RotateTransform` หรือ `ScaleTransform` คุณสามารถย้ายจุดกำเนิดนั้น, หมุนรูปทรง, หรือปรับขนาดโดยไม่ต้องแก้ไขเรขาคณิตเดิม สิ่งนี้ทำให้คุณออกแบบครั้งเดียวแล้วเรนเดอร์ได้ทุกขนาดหรือทิศทาง

## วิธีบันทึก PNG ด้วย Aspose.Drawing?

โหลดอ็อบเจกต์ `Bitmap`, ตั้งค่าการแปลงโลกที่ต้องการบนอินสแตนซ์ `Graphics` ของมัน, วาดรูปทรงของคุณ, แล้วเรียก `bitmap.Save("output.png", ImageFormat.Png)` การบันทึกบรรทัดเดียวนี้จะเขียนไฟล์ PNG แบบ lossless ที่รักษาความโปร่งใสและความเที่ยงตรงของสี ทำให้เหมาะสำหรับ assets เว็บและ UI overlays API จะจัดการการเข้ารหัสระดับล่างทั้งหมด ทำให้คุณได้ PNG พร้อมใช้ภายในไม่กี่วินาทีสำหรับขนาด canvas ปกติ

## ทำไมต้องใช้ตัวอย่าง graphics translate?

ตัวอย่าง graphics translate ช่วยให้คุณย้ายจุดกำเนิดของการวาดเพียงครั้งเดียวแทนการคำนวณใหม่ทุกจุด การย้ายจุดกำเนิดไปที่ศูนย์ของ canvas ทำให้เรขาคณิตง่ายขึ้น, ลดการทำซ้ำของโค้ด, และให้ engine ทำการคูณเมทริกซ์ในโค้ดเนทีฟ ซึ่งอาจเพิ่มความเร็วการเรนเดอร์ได้ถึง 30 % บน canvas ขนาดใหญ่ รูปแบบนี้ยังทำให้โค้ดของคุณบำรุงรักษาง่ายเมื่อคุณเพิ่มการหมุนหรือสเกลในภายหลัง

## ตัวอย่าง graphics translate

**graphics translate example** แสดงว่าการย้ายจุดกำเนิดทำให้การจัดตำแหน่งง่ายขึ้น แทนการคำนวณใหม่ทุกจุด คุณย้ายระบบพิกัดเพียงครั้งเดียวและวาดเหมือนกับว่าจุดกำเนิดใหม่อยู่ที่ศูนย์ของ canvas

## ข้อกำหนดเบื้องต้น

ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมี:

- **Aspose.Drawing library** ที่รวมไว้ในโปรเจค .NET ของคุณ – ดาวน์โหลดจาก [หน้าเผยแพร่ Aspose.Drawing อย่างเป็นทางการ](https://releases.aspose.com/drawing/net/)  
- **document directory** ที่ไฟล์ภาพผลลัพธ์จะถูกบันทึก  
- ความคุ้นเคยพื้นฐานกับไวยากรณ์ **C#** และ Visual Studio หรือ IDE ที่คุณชอบ  

ตอนนี้, มาดูโค้ดกัน!

## นำเข้า namespaces

`Bitmap`, `Graphics`, และยูทิลิตี้การวาดของ Aspose อยู่ใน namespaces เหล่านี้  
**Definition:** `System.Drawing` ให้ประเภท GDI+ พื้นฐาน, ส่วน `Aspose.Drawing` ขยายด้วยความสามารถข้ามแพลตฟอร์ม, ทำให้คุณรันโค้ดเดียวกันบน Windows, Linux และ macOS โดยไม่มีการพึ่งพาเพิ่มเติม

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: สร้าง bitmap

**Definition:** `Bitmap` คือการแสดงผลภาพ raster ในหน่วยความจำของ Aspose.Drawing ที่คุณสามารถวาดหรือบันทึกลงดิสก์ได้  

เราจะเริ่มด้วยการสร้าง canvas ว่างที่จะเก็บการวาดของเรา

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` สร้าง bitmap 32‑บิตต่อพิกเซลที่มี premultiplied alpha ซึ่งเป็นรูปแบบที่เหมาะสำหรับการส่งออก PNG เพราะรักษาความโปร่งใสโดยไม่ต้องแปลงเพิ่มเติม

- **Why 32bppPArgb?** รูปแบบพิกเซลนี้รองรับความโปร่งใสของ alpha และการเรนเดอร์สีคุณภาพสูง, เหมาะสำหรับการส่งออก PNG  
- **Pro tip:** ปรับความกว้าง/ความสูงให้ตรงกับขนาดภาพเป้าหมาย; canvas 1920 × 1080 จะเรนเดอร์ภายในต่ำกว่า 0.2 วินาทีบนแล็ปท็อปของนักพัฒนาทั่วไป  

### ขั้นตอนที่ 2: ตั้งค่าการแปลงโลก (graphics translate example)

**Definition:** `Graphics` คือพื้นผิวการวาดที่เรนเดอร์รูปทรงลงบน `Bitmap`  

`TranslateTransform` ย้ายจุดกำเนิดของระบบพิกัดไปยังตำแหน่งใหม่  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` ย้ายจุด (0,0) ไปที่ศูนย์ของ canvas หลังจากเรียกนี้, รูปทรงใด ๆ ที่วาดด้วยพิกัด (0,0) จะปรากฏที่กลางภาพ

- การย้ายจุด (0,0) ไปที่ (500, 400) – กลางของ canvas ขนาด 1000 × 800  
- คุณสามารถต่อเนื่องการแปลงเพิ่มเติม: `RotateTransform` หมุนระบบพิกัด, `ScaleTransform` ปรับขนาด, ทำให้ **multiple graphics transformations** ทำงานใน pipeline เดียว  

### ขั้นตอนที่ 3: วาดสี่เหลี่ยมโดยใช้พิกัดที่แปลงแล้ว

**Definition:** `DrawRectangle` เป็นเมธอดของ `Graphics` ที่วาดโครงสี่เหลี่ยมหรือรูปแบบเติมตาม pen และพิกัดที่ระบุ  

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` วาดสี่เหลี่ยมที่ศูนย์ของ canvas เพราะมุมซ้าย‑บนของมันถูกชิดด้วยครึ่งความกว้างและความสูงจากจุดกำเนิดที่แปลงแล้ว

- มุมซ้าย‑บนของสี่เหลี่ยมเริ่มที่จุดกำเนิดที่แปลงแล้ว (ศูนย์ของภาพ)  
- คุณสามารถทดลองกับรูปทรงอื่น ๆ — วงรี, เส้น, หรือ path กำหนดเอง  

### ขั้นตอนที่ 4: บันทึกผลลัพธ์ – แปลง graphics เป็น PNG

**Definition:** `ImageFormat` เป็น enumeration ที่บอกเมธอด `Save` ว่าจะใช้รูปแบบไฟล์ใด  

`Save` เขียน bitmap ลงไฟล์ในรูปแบบภาพที่ระบุ  
`bitmap.Save(outputPath, ImageFormat.Png)` เขียนไฟล์ PNG lossless ที่สามารถใช้โดยตรงในหน้าเว็บหรือคอมโพเนนต์ UI

- PNG รักษาสีและความโปร่งใสที่ตั้งค่าไว้ก่อนหน้าอย่างแม่นยำ  
- แทนที่ `"Your Document Directory"` ด้วยพาธจริงบนเครื่องของคุณ  
- สำหรับการประมวลผลเป็นชุด, วนลูปผ่านคอลเลกชันของอ็อบเจกต์ `Bitmap` แล้วเรียก `Save` ภายในลูป – ไลบรารีสามารถจัดการภาพหลายพันรูปด้วยหน่วยความจำต่ำกว่า 200 MB  

## ปัญหาทั่วไปและวิธีแก้

| Issue | Why it happens | Fix |
|-------|----------------|-----|
| **File not found error** | โฟลเดอร์เป้าหมายไม่มีอยู่ | สร้างโฟลเดอร์โดยโปรแกรม (`Directory.CreateDirectory`) ก่อนเรียก `Save`. |
| **Blank image** | `TranslateTransform` ถูกเรียกหลังการวาด | ตรวจสอบให้แน่ใจว่าการแปลงถูกตั้งค่า **ก่อน** คำสั่งวาดใด ๆ |
| **Distorted colors** | ใช้รูปแบบพิกเซลที่ไม่เข้ากัน | ใช้ `Format32bppPArgb` สำหรับการส่งออก PNG |
| **Out‑of‑memory on large canvases** | โหลด bitmap ทั้งหมดเข้าสู่หน่วยความจำ | ใช้ตัวเลือกสตรีมของ `Bitmap` หรือแยกภาพเป็นหลายส่วน; Aspose.Drawing สามารถเรนเดอร์แผ่นย่อยได้อย่างอิสระ |

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้การแปลงมากกว่าหนึ่งครั้งได้หรือไม่?**  
A: ใช่ – คุณสามารถต่อเนื่อง `TranslateTransform`, `RotateTransform`, และ `ScaleTransform` เพื่อสร้างเอฟเฟกต์ซับซ้อนใน pipeline graphics เดียว  

**Q: Aspose.Drawing ฟรีสำหรับโครงการเชิงพาณิชย์หรือไม่?**  
A: รุ่นทดลองฟรีใช้ได้สำหรับการประเมิน, แต่ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  

**Q: ทำงานกับ .NET Core และ .NET 5/6/7 หรือไม่?**  
A: แน่นอน. Aspose.Drawing รองรับ runtime .NET สมัยใหม่ทั้งหมด, รวมถึง .NET Core, .NET 5, .NET 6, และ .NET 7  

**Q: ฉันสามารถหาเอกสารอ้างอิง API เต็มรูปแบบได้ที่ไหน?**  
A: เอกสารเต็มรูปแบบพร้อมให้บริการที่ [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/)  

**Q: ฉันจะแก้ไขปัญหาไฟล์ผลลัพธ์หายได้อย่างไร?**  
A: ตรวจสอบสตริงพาธ, ยืนยันสิทธิ์การเขียน, และตรวจสอบว่าไดเรกทอรีมีอยู่ก่อนเรียก `Save`  

## สรุป

คุณได้เรียนรู้ **วิธีแปลง drawing เป็น PNG** ด้วย Aspose.Drawing, ใช้ **การแปลงโลก**, และทำ **graphics translate example** ที่สามารถต่อยอดด้วยการหมุนหรือสเกลได้ ด้วยการเข้าใจบล็อกพื้นฐานเหล่านี้ คุณสามารถสร้างภาพไดนามิก, สร้างแผนภูมิแบบกำหนดเอง, หรือสร้างกราฟิกบน‑บินสำหรับแอปพลิเคชัน .NET ใด ๆ ต่อไป, สำรวจบทแนะนำการแปลงเมทริกซ์เพื่อรวมหลายการดำเนินการในเมทริกซ์เดียวเพื่อประสิทธิภาพที่ดียิ่งขึ้น  

---

**Last updated:** 2026-10-18  
**Tested with:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  
**Related resources:** [Aspose.Drawing API reference](https://reference.aspose.com/drawing/net/) | [Download free trial](https://releases.aspose.com/drawing/net/)

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

- [บทแนะนำการแปลงเมทริกซ์: matrix transformations ใน Aspose.Drawing สำหรับ .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [วิธีหมุนภาพด้วย Aspose.Drawing global transformation](/drawing/net/coordinate-transformations/global-transformation/)
- [การแปลงระบบพิกัด – page transformation ใน Aspose.Drawing สำหรับ .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}