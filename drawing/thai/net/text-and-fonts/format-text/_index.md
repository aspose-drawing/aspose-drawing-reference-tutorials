---
date: 2026-07-17
description: เรียนรู้วิธีป้องกันการล้นของข้อความโดยการตั้งค่าการจัดแนวข้อความใน Aspose.Drawing
  สำหรับ .NET และเพิ่มข้อความลงในรูปภาพ คู่มือขั้นตอนโดยละเอียดพร้อมตัวอย่าง
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: ตั้งค่าการจัดแนวข้อความด้วย Aspose.Drawing สำหรับ .NET
og_description: ป้องกันการล้นของข้อความโดยการตั้งค่าการจัดแนวข้อความใน Aspose.Drawing
  สำหรับ .NET. เรียนรู้การวาดสตริงบนรูปภาพ, จัดข้อความให้อยู่กึ่งกลางในสี่เหลี่ยม,
  และแทนที่ System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: ป้องกันการล้นของข้อความ – ตั้งค่าการจัดแนวข้อความด้วย Aspose.Drawing สำหรับ
  .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: ป้องกันการล้นของข้อความ – ตั้งค่าการจัดแนวข้อความด้วย Aspose.Drawing สำหรับ
  .NET
url: /th/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ป้องกันการล้นของข้อความ – ตั้งการจัดแนวข้อความด้วย Aspose.Drawing

## บทนำ

เมื่อคุณต้องการ **ป้องกันการล้นของข้อความ** ขณะเรนเดอร์กราฟิกใน .NET, Aspose.Drawing จะให้การควบคุมที่ละเอียดในการวางตำแหน่งข้อความ, การจัดแนว, และการตัดบรรทัด. ไม่ว่าคุณจะสร้างเครื่องสร้างแบจ, รายงานแบบไดนามิก, หรือผลลัพธ์ที่เป็นภาพใด ๆ, การเชี่ยวชาญการจัดแนวข้อความจะทำให้ข้อความของคุณอยู่ภายในสี่เหลี่ยมที่กำหนดและดูเรียบร้อย. ในคู่มือนี้เราจะอธิบายขั้นตอนการสร้างแคนวาส bitmap, การกำหนดค่า `StringFormat`, การวาดสี่เหลี่ยมพร้อมข้อความกึ่งกลาง, การจัดการการล้น, และสุดท้ายการบันทึกรูปภาพ.

## คำตอบสั้น
- **“set text alignment” หมายความว่าอะไร?** มันกำหนดว่าข้อความถูกจัดตำแหน่งแนวนอนและแนวตั้งอย่างไรภายในสี่เหลี่ยมวาด.  
- **คลาสใดควบคุมการจัดแนว?** `StringFormat` ให้คุณตั้งค่า `Alignment` และ `LineAlignment`.  
- **ฉันสามารถวาดสตริงและสี่เหลี่ยมพร้อมกันได้หรือไม่?** ใช่—ใช้ `Graphics.DrawRectangle` แล้วตามด้วย `Graphics.DrawString`.  
- **ฉันจะป้องกันการล้นของข้อความได้อย่างไร?** ปรับขนาดสี่เหลี่ยมหรือแยกข้อความเป็นหลายบรรทัดด้วยตนเอง.  
- **ฉันต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.Drawing เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่การประเมินผล.

## **set text alignment** คืออะไรใน Aspose.Drawing

`set text alignment` กำหนดการวางตำแหน่งข้อความในแนวนอน (`StringAlignment`) และแนวตั้ง (`LineAlignment`) ภายใน `Rectangle` หรือพื้นที่วาด. โดยการปรับคุณสมบัติเหล่านี้คุณสามารถควบคุมว่าข้อความจะแสดงเป็นจัดชิดซ้าย, กึ่งกลาง, ชิดขวา, ชิดบน, กลาง, หรือชิดล่าง, ทำให้สามารถจัดวางกราฟิก, แบจ, และรายงานที่สร้างด้วย Aspose.Drawing ได้อย่างแม่นยำ.

## ทำไมต้องใช้ Aspose.Drawing สำหรับการจัดแนวข้อความ?

Aspose.Drawing ขจัดข้อจำกัดของ GDI+ ที่ทำให้ `System.Drawing.Common` มีปัญหา. มันรองรับ **5 runtime ของ .NET หลัก** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6, และ .NET 7 – และสามารถเรนเดอร์ภาพได้สูงสุด **4000 × 4000 px** (≈ 100 MB) โดยไม่ทำให้หน่วยความจำหมด. การทำ Anti‑aliasing, การสเกลแบบ high‑DPI, และความเข้ากันได้เต็มรูปแบบกับคอนเทนเนอร์ Linux ทำให้คุณสร้างกราฟิกที่พิกเซล‑เพอร์เฟคในทุกสถานการณ์การปรับใช้.

## ข้อกำหนดเบื้องต้น

1. **Aspose.Drawing Library** – ดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/drawing/net/).  
2. **Development Environment** – Visual Studio 2022 (หรือ IDE C# ใดก็ได้).  
3. **Basic .NET knowledge** – คุณควรคุ้นเคยกับโครงการ C# และแพ็กเกจ NuGet.

## นำเข้า Namespaces

เพื่อเริ่มต้น ให้นำ Namespaces ที่จำเป็นเข้ามาในสโคป. สิ่งเหล่านี้จะให้คุณเข้าถึงกราฟิก, การเรนเดอร์ข้อความ, และ primitive การวาด.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## วิธีป้องกันการล้นของข้อความด้วย Aspose.Drawing?

`Bitmap` เป็นคลาสที่แสดงภาพที่เก็บในหน่วยความจำ, ในขณะที่ `RectangleF` กำหนดพื้นที่สี่เหลี่ยมแบบ floating‑point สำหรับการวาด. โดยการใช้ `StringFormat` ที่ตั้งค่า `Trimming` เป็น `StringTrimming.EllipsisCharacter` ตัวอักษรที่เกินจะถูกแทนที่ด้วยจุดไข่ปลาโดยอัตโนมัติ, ทำให้ข้อความไม่เกินขอบสี่เหลี่ยม. การวัดขนาดสตริงก่อนจะทำให้คุณตัดสินใจว่าจะลดขนาดสี่เหลี่ยมหรือแยกข้อความเป็นหลายบรรทัด, เพื่อให้ได้การจัดวางที่สะอาดโดยไม่มีการล้น.

โหลด bitmap ของคุณ, กำหนด `RectangleF` ที่มีขนาดเหมาะสม, และใช้ `StringFormat` ที่ตั้งค่า `Trimming` เป็น `StringTrimming.EllipsisCharacter` เพื่อทำการตัดอักขระที่เกินโดยอัตโนมัติ. หากต้องการควบคุมเต็มที่, วัดสตริงด้วย `Graphics.MeasureString` แล้วลดขนาดสี่เหลี่ยมหรือแยกข้อความเป็นบรรทัดก่อนการวาด. วิธีนี้รับประกันว่าจะไม่มีอักขระใดล้นออกนอกขอบมองเห็น.

## ขั้นตอนที่ 1: สร้างอ็อบเจ็กต์ Bitmap และ Graphics

`Bitmap` แสดงภาพในหน่วยความจำ, ในขณะที่ `Graphics` ให้เมธอดการวาดสำหรับ bitmap นั้น. การสร้าง bitmap จะให้แคนวาสที่คุณสามารถวาดบนมันได้. อ็อบเจ็กต์ `Graphics` คือพื้นผิวการวาด, และเราจะเปิดใช้งานการเรนเดอร์ข้อความคุณภาพสูงด้วย `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## ขั้นตอนที่ 2: กำหนด **StringFormat** และการจัดรูปแบบ

`StringFormat` ระบุตัวเลือกการจัดวางข้อความเช่นการจัดแนว, ระยะห่างบรรทัด, และการตัด. ที่นี่เราจะ **ตั้งค่าการจัดแนวข้อความ** โดยกำหนดค่าอินสแตนซ์ `StringFormat`. เรายังเตรียม brushes, pens, และฟอนต์ที่จะใช้เมื่อวาดสตริง.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## ขั้นตอนที่ 3: สร้างและจัดรูปแบบข้อความ – **วิธีวาดสตริง** และ **วาดสี่เหลี่ยมพร้อมข้อความ**

`Graphics.DrawString` แสดงข้อความบนแคนวาส, และ `Graphics.DrawRectangle` วาดรูปสี่เหลี่ยม. เราจัดเตรียมข้อความ, กำหนดสี่เหลี่ยมที่จะบรรจุข้อความ, แล้ววาดทั้งขอบสี่เหลี่ยมและสตริงเอง.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### วิธีจัดการการล้นของข้อความ

หาก `text` ที่ให้เกินขอบของสี่เหลี่ยม, คุณมีสองตัวเลือกทั่วไป:

1. **ปรับขนาดสี่เหลี่ยม** – เพิ่ม `rectangle.Width` หรือ `rectangle.Height`.  
2. **แยกข้อความ** – แบ่งสตริงเป็นบรรทัดที่พอดี, แล้วเรียก `DrawString` สำหรับแต่ละบรรทัดโดยปรับค่า Y‑coordinates.

## วิธีวาดสตริงบนภาพโดยใช้ Aspose.Drawing?

`Graphics.DrawString` วาดข้อความที่ระบุโดยใช้ฟอนต์และตัวเลือกการจัดรูปแบบ. สร้างอ็อบเจ็กต์ `Graphics` จาก bitmap ของคุณ, แล้วเรียก `DrawString` พร้อม `StringFormat` ที่เตรียมไว้. การเรียกเดียวนี้จะเรนเดอร์ข้อความตรงตำแหน่งที่คุณต้องการ, เคารพการจัดแนว, การตัด, และเมทริกซ์การแปลงใด ๆ ที่คุณได้ใช้. การเพิ่ม hint การเรนเดอร์คุณภาพสูงทำให้ผลลัพธ์คมชัดบนจอแสดงผล high‑DPI.

## วิธีจัดกึ่งกลางข้อความในสี่เหลี่ยม?

`StringAlignment` กำหนดการจัดแนวแนวนอนของข้อความภายในสี่เหลี่ยมการจัดวาง. ตั้งค่า `stringFormat.Alignment = StringAlignment.Center` และ `stringFormat.LineAlignment = StringAlignment.Center`. วิธีนี้จะทำให้ข้อความอยู่กึ่งกลางแนวนอนและแนวตั้งภายในสี่เหลี่ยม, เหมาะสำหรับแบจ, ปุ่ม, หรือการซ้อนป้าย. การจัดวางกึ่งกลางทำงานสอดคล้องกันในขนาดภาพและการตั้งค่า DPI ต่าง ๆ, ให้ลักษณะภาพที่สมดุล.

## วิธีทำให้ข้อความจัดแนวแนวตั้งได้?

`LineAlignment` ควบคุมการวางตำแหน่งแนวตั้งของข้อความภายในสี่เหลี่ยม. ใช้ `stringFormat.LineAlignment` กับค่า `StringAlignment.Near`, `Center`, หรือ `Far` เพื่อวางข้อความที่ด้านบน, กลาง, หรือด้านล่างของสี่เหลี่ยม. ผสานกับ `Graphics.TranslateTransform` หากคุณต้องการหมุนข้อความพร้อมคงการจัดแนวแนวตั้ง. การปรับ `LineAlignment` ทำให้บล็อกหลายบรรทัดจัดตำแหน่งตรงตามที่คุณคาดหวัง, แม้หลังการแปลง.

## ขั้นตอนที่ 4: บันทึกผลลัพธ์ – **เพิ่มข้อความลงในภาพ**

สุดท้าย, เขียน bitmap ลงดิสก์. ขั้นตอนนี้แสดงการ **เพิ่มข้อความลงในภาพ** ด้วยการเรียกเดียว.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## ปัญหาทั่วไปและวิธีแก้

| Issue | Solution |
|-------|----------|
| **ข้อความดูเบลอ** | ตรวจสอบให้แน่ใจว่าได้ตั้งค่า `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` |
| **ข้อความถูกตัด** | เพิ่มขนาดสี่เหลี่ยมหรือเปิดใช้งานตรรกะ word‑wrap โดยวัดขนาดสตริง (`Graphics.MeasureString`). |
| **ไม่พบฟอนต์** | ตรวจสอบว่าฟอนต์ได้ติดตั้งบนเครื่องโฮสต์หรือฝังฟอนต์ส่วนตัวด้วย `PrivateFontCollection`. |
| **สีที่ไม่คาดคิด** | ตรวจสอบสีของ brush และ pen อีกครั้ง; จำไว้ว่า `Color.FromKnownColor` ใช้สีที่กำหนดโดยระบบ. |

## คำถามที่พบบ่อย

**Q1: Aspose.Drawing รองรับทุกเวอร์ชันของ .NET หรือไม่?**  
A1: ใช่, Aspose.Drawing ถูกออกแบบให้เข้ากันได้กับหลายเวอร์ชันของ .NET, เพื่อความยืดหยุ่นสำหรับนักพัฒนา.

**Q2: ฉันสามารถปรับแต่งสไตล์ฟอนต์เพิ่มเติมได้หรือไม่?**  
A2: แน่นอน! ปรับพารามิเตอร์ของอ็อบเจ็กต์ `Font` เพื่อให้ได้ขนาด, สไตล์, และตระกูลฟอนต์ที่ต้องการ.

**Q3: ฉันจะจัดการการล้นของข้อความภายในสี่เหลี่ยมที่กำหนดได้อย่างไร?**  
A3: คุณสามารถจัดการการล้นของข้อความโดยปรับขนาดสี่เหลี่ยมหรือใช้ตรรกะแบบกำหนดเองเพื่อจัดการข้อความยาว.

**Q4: มีตัวเลือกการจัดรูปแบบอื่น ๆ ใน Aspose.Drawing หรือไม่?**  
A4: มี, Aspose.Drawing มีชุดเครื่องมือที่ครอบคลุมสำหรับการจัดการกราฟิก, รวมถึงตัวเลือกการจัดรูปแบบต่าง ๆ สำหรับข้อความ, รูปร่าง, และอื่น ๆ.

**Q5: ฉันจะหาการสนับสนุนเพิ่มเติมสำหรับ Aspose.Drawing ได้จากที่ไหน?**  
A5: สำรวจฟอรั่ม Aspose.Drawing [ที่นี่](https://forum.aspose.com/c/drawing/44) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

**Q: ฉันจะวาดสตริงโดยไม่มีสี่เหลี่ยมรอบ ๆ อย่างไร?**  
A: ไม่ต้องเรียก `DrawRectangle` และส่งตำแหน่ง `PointF` ที่ต้องการให้กับ `Graphics.DrawString`.

**Q: ฉันสามารถหมุนข้อความพร้อมคงการจัดแนวได้หรือไม่?**  
A: ใช่—ใช้การแปลง `Matrix` กับอ็อบเจ็กต์ `Graphics` ก่อนวาด, แล้วรีเซ็ตหลังจากนั้น.

**Q: สามารถส่งออกภาพเป็น JPEG แทน PNG ได้หรือไม่?**  
A: เพียงเปลี่ยนส่วนขยายไฟล์ใน `bitmap.Save` และอาจระบุ `ImageFormat.Jpeg` เพิ่มเติม.

**อัปเดตล่าสุด:** 2026-07-17  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [วิธีวาดข้อความด้วย Aspose.Drawing สำหรับ .NET](/drawing/net/text-and-fonts/draw-text/)
- [การเพิ่มข้อความบนภาพใน Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [วิธีวาดข้อความและฟอนต์ด้วย Aspose.Drawing สำหรับ .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}