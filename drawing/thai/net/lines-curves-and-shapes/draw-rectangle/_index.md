---
date: 2026-08-01
description: เรียนรู้วิธีสร้าง bitmap image C# และวาด rectangle บน bitmap ด้วย Aspose.Drawing.
  คู่มือแบบ Step‑by‑step สำหรับนักพัฒนา .NET
keywords:
- create bitmap image c#
- draw rectangle on bitmap
- replace system.drawing
lastmod: 2026-08-01
linktitle: การวาด Rectangles ใน Aspose.Drawing
og_description: สร้าง bitmap image C# และวาด rectangle บน bitmap ด้วย Aspose.Drawing.
  บทแนะนำนี้แสดงวิธี generate, style, และ save rectangle graphics ใน .NET.
og_image_alt: Guide to drawing rectangles on a bitmap with Aspose.Drawing for .NET
og_title: สร้าง Bitmap Image C# – วาด Rectangle ด้วย Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to create bitmap image C# and draw rectangle on bitmap using
    Aspose.Drawing. Step‑by‑step guide for .NET developers.
  headline: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)`
      before or after drawing the outline.
    question: Can I fill the rectangle with a solid color?
  - answer: Loop through a collection of `Rectangle` structs and call `DrawRectangle`
      for each iteration.
    question: How do I draw multiple rectangles?
  - answer: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform
      after.
    question: Is there a way to rotate the rectangle?
  - answer: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat`
      parameter.
    question: What image formats are supported for saving?
  - answer: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and
      later versions.
    question: Does Aspose.Drawing work on .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- create bitmap image
- Aspose.Drawing
- .NET graphics
- draw rectangle
title: สร้าง Bitmap Image C# – วาด Rectangle ด้วย Aspose.Drawing สำหรับ .NET
url: /th/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดสี่เหลี่ยมผืนผ้าด้วย Aspose.Drawing สำหรับ .NET

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีวาดสี่เหลี่ยมผืนผ้า** พร้อมกับการเชี่ยวชาญวิธี **สร้างภาพบิตแมพ C#** ด้วย Aspose.Drawing ไม่ว่าคุณจะต้องการองค์ประกอบ UI แบบง่ายหรือกราฟิกความละเอียดสูงสำหรับรายงาน เราจะอธิบายขั้นตอนการสร้างบิตแมพ, การกำหนดค่าอ็อบเจกต์ Graphics, การวาดสี่เหลี่ยมผืนผ้า, และการบันทึกรูปภาพขั้นสุดท้าย วิธีนี้ทำงานบน Windows, Linux, และ macOS และแทนที่ API `System.Drawing.Common` รุ่นเก่าด้วยโซลูชันข้ามแพลตฟอร์มเต็มรูปแบบ  

## คำตอบสั้น
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.Drawing for .NET  
- **เมธอดใดที่ใช้วาดรูปทรง?** `Graphics.DrawRectangle`  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้งานฟรี; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการผลิต.  
- **ฉันสามารถเปลี่ยนขนาดสี่เหลี่ยมผืนผ้าได้หรือไม่?** ได้ – ปรับค่าความกว้าง, ความสูง, และพารามิเตอร์ตำแหน่ง.  
- **โค้ดนี้เข้ากันได้กับ .NET 6+ หรือไม่?** แน่นอน, Aspose.Drawing รองรับเวอร์ชัน .NET สมัยใหม่.  

## อะไรคือ “วิธีวาดสี่เหลี่ยมผืนผ้า” ในบริบทของ Aspose.Drawing?

การวาดสี่เหลี่ยมผืนผ้าด้วย Aspose.Drawing ใช้คลาส `Graphics` เพื่อเรนเดอร์เส้นขอบสี่เหลี่ยมหรือรูปแบบที่เติมเต็มบนแคนวาสบิตแมพ ซึ่งให้การควบคุมเต็มรูปแบบต่อขนาด, สี, ความหนาของเส้น, และรูปแบบภาพ ทำให้เหมาะสำหรับกราฟิกแบบเรียลไทม์ เนื่องจาก Aspose.Drawing ทำงานบนเอนจินที่จัดการโดยบริสุทธิ์ จึงหลีกเลี่ยงข้อจำกัดของ GDI+ ดั้งเดิมของ `System.Drawing.Common`  

## ทำไมต้องใช้ Aspose.Drawing สำหรับการสร้างสี่เหลี่ยมผืนผ้า?

Aspose.Drawing ให้คุณ **วาดสี่เหลี่ยมผืนผ้าบนบิตแมพ** โดยไม่ต้องใช้ DLL ที่เฉพาะแพลตฟอร์มใด ๆ และรองรับ **รูปแบบผลลัพธ์กว่า 30 แบบ** (รวมถึง PNG, JPEG, BMP, GIF, และ TIFF) สามารถประมวลผลภาพได้สูงสุด **10,000 × 10,000 พิกเซล** พร้อมการใช้หน่วยความจำน้อยกว่า **100 MB**, ซึ่งมีประสิทธิภาพ 2‑3× มากกว่าการใช้งาน System.Drawing รุ่นเก่า  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Aspose.Drawing Library** – ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการ [here](https://releases.aspose.com/drawing/net/).  
- **Development Environment** – Visual Studio 2022 หรือ IDE ที่รองรับ .NET ใด ๆ.  
- **Basic .NET Knowledge** – ความคุ้นเคยกับไวยากรณ์ C# และโครงสร้างโปรเจกต์.  

## นำเข้า Namespaces

`using` directives นำคลาสที่จำเป็นเข้าสู่สโคป จำเป็นสำหรับการดำเนินการวาดใด ๆ.

```csharp
using System.Drawing;
```

## ขั้นตอนที่ 1: สร้างภาพ Bitmap

`Bitmap` แสดงถึงภาพแรสเตอร์ในหน่วยความจำที่คุณสามารถวาดบนได้ การสร้างมันกำหนดขนาดแคนวาสและรูปแบบพิกเซล.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## ขั้นตอนที่ 2: สร้างอ็อบเจกต์ Graphics

`Graphics` เป็นเอนจินที่ดำเนินการคำสั่งวาดทั้งหมดบนพื้นผิวบิตแมพ เมื่อคุณได้มามันแล้ว คุณสามารถเรนเดอร์รูปทรง, ข้อความ, และภาพได้.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## ขั้นตอนที่ 3: กำหนด Pen สำหรับสี่เหลี่ยมผืนผ้า

`Pen` ระบุสีเส้นขอบและความหนาสำหรับสี่เหลี่ยมผืนผ้า นอกจากนี้ยังควบคุมรูปแบบ dash และการเชื่อมต่อของเส้น.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## ขั้นตอนที่ 4: วาดสี่เหลี่ยมผืนผ้าบน Bitmap

`Graphics.DrawRectangle` วาดสี่เหลี่ยมผืนผ้าโดยใช้ Pen ที่กำหนดไว้ก่อนหน้านี้ คุณต้องระบุพิกัด X, Y พร้อมกับความกว้างและความสูงเพื่อกำหนดตำแหน่งรูปทรงอย่างแม่นยำ.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## ขั้นตอนที่ 5: บันทึกรูปภาพที่วาด

เมธอด `Bitmap.Save` เขียนภาพลงดิสก์ในรูปแบบที่คุณเลือก (เช่น PNG, JPEG) ขั้นตอนนี้แสดงความสามารถในการ **บันทึกรูปภาพที่วาด** และสรุปบิตแมพเพื่อการใช้งานต่อ.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

ยินดีด้วย! คุณได้ทำ **วิธีวาดสี่เหลี่ยมผืนผ้า** ด้วย Aspose.Drawing สำหรับ .NET สำเร็จแล้วและได้เรียนรู้วิธี **สร้างภาพบิตแมพ C#** ในกระบวนการ.  

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| ภาพว่างเปล่า | Bitmap ไม่ได้ถูกทำลายหรือ graphics ไม่ได้ flush | เรียก `graphics.Dispose();` ก่อนบันทึก หรือใช้บล็อก `using`. |
| ขอบภาพคุณภาพต่ำ | โหมด smoothing เริ่มต้น | ตั้งค่า `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`. |
| ข้อผิดพลาดเส้นทางไฟล์ | ไดเรกทอรีไม่ถูกต้อง | ตรวจสอบให้โฟลเดอร์เป้าหมายมีอยู่หรือใช้ `Path.Combine` เพื่อสร้างเส้นทางที่ปลอดภัย. |

## คำถามที่พบบ่อย

**Q: ฉันสามารถเติมสีเต็มสี่เหลี่ยมผืนผ้าด้วยสีทึบได้หรือไม่?**  
A: ได้, สร้าง `SolidBrush` แล้วเรียก `graphics.FillRectangle(brush, …)` ก่อนหรือหลังการวาดเส้นขอบ.  

**Q: ฉันจะวาดสี่เหลี่ยมผืนผ้าหลายรูปได้อย่างไร?**  
A: วนลูปผ่านคอลเลกชันของโครงสร้าง `Rectangle` แล้วเรียก `DrawRectangle` สำหรับแต่ละรอบ.  

**Q: มีวิธีหมุนสี่เหลี่ยมผืนผ้าไหม?**  
A: ใช้ `graphics.RotateTransform(angle)` ก่อนวาด แล้วรีเซ็ตการแปลงหลังจากนั้น.  

**Q: รูปแบบภาพใดบ้างที่รองรับการบันทึก?**  
A: PNG, JPEG, BMP, GIF, และ TIFF ทั้งหมดรองรับผ่านพารามิเตอร์ `ImageFormat` ที่เหมาะสม.  

**Q: Aspose.Drawing ทำงานบน .NET Core หรือไม่?**  
A: ใช่, ไลบรารีนี้เข้ากันได้เต็มที่กับ .NET Core, .NET 5, .NET 6, และเวอร์ชันต่อ ๆ ไป.  

---

**อัปเดตล่าสุด:** 2026-08-01  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

## บทแนะนำที่เกี่ยวข้อง

- [วิธีวาดวงรีด้วย Aspose.Drawing สำหรับ .NET](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [วาดหลายเส้นด้วย Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [วิธีสร้างบิตแมพ aspose.drawing – วาดหลายเหลี่ยมใน .NET](/drawing/net/lines-curves-and-shapes/draw-polygon/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}