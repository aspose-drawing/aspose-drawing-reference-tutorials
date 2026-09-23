---
date: 2026-09-23
description: เรียนรู้วิธีวาดข้อความบนภาพโดยใช้ Aspose.Drawing for .NET. สร้างภาพพร้อมข้อความ,
  เพิ่มข้อความลงใน bitmap, และบันทึก bitmap เป็น PNG พร้อมฟอนต์ที่กำหนดเอง.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: วิธีวาดข้อความด้วย Aspose.Drawing
og_description: เรียนรู้วิธีวาดข้อความบนภาพโดยใช้ Aspose.Drawing for .NET. บทเรียนนี้แสดงวิธีสร้างภาพพร้อมข้อความ,
  เพิ่มข้อความลงใน bitmap, และบันทึก bitmap เป็น PNG พร้อมฟอนต์ที่กำหนดเอง.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: วาดข้อความบนภาพด้วย Aspose.Drawing for .NET – คู่มือด่วน
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: วิธีวาดข้อความบนภาพด้วย Aspose.Drawing for .NET
url: /th/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดข้อความบนภาพด้วย Aspose.Drawing สำหรับ .NET

## บทนำ

ในคู่มือแบบขั้นตอนนี้คุณจะได้เรียนรู้ **วิธีวาดข้อความบนภาพ** ด้วย Aspose.Drawing สำหรับ .NET ไม่ว่าคุณจะต้องการสร้าง *ภาพข้อความแบบไดนามิก*, เพิ่มข้อความลงในบิตแมพที่มีอยู่แล้ว, หรือสร้างกราฟิกด้วยฟอนต์ที่กำหนดเอง คู่มือนี้จะพาคุณผ่านทุกขั้นตอนเพื่อให้คุณเริ่มวาดข้อความได้ในไม่กี่นาที ไลบรารีนี้รองรับเมธอด GDI+ มากกว่า 30 วิธี, ทำงานบน Windows, Linux, และ macOS, และไม่มี **การพึ่งพา external ใดๆ**, ทำให้เป็นตัวเลือกที่เชื่อถือได้สำหรับการสร้างภาพบนเซิร์ฟเวอร์

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่ใช้คืออะไร?** Aspose.Drawing for .NET  
- **ภารกิจหลัก?** วาดข้อความบนภาพ (สร้างภาพพร้อมข้อความ)  
- **เมธอดสำคัญ?** `Graphics.DrawString` (วาดสตริงบนภาพ)  
- **รูปแบบผลลัพธ์?** PNG (บันทึกบิตแมพเป็น PNG)  
- **ข้อกำหนดเบื้องต้น?** สภาพแวดล้อมการพัฒนา .NET และไลบรารี Aspose.Drawing  

## การวาดข้อความด้วย Aspose.Drawing คืออะไร?
การวาดข้อความด้วย Aspose.Drawing หมายถึงการใช้ API ที่เข้ากันได้กับ GDI+ ของไลบรารีเพื่อเรนเดอร์สตริง Unicode ลงบนแคนวาสแบบแรสเตอร์ เมธอด `Graphics.DrawString` จะเขียนข้อความลงในบิตแมพ, ให้คุณควบคุมฟอนต์, สี, การจัดแนว, และการทำ anti‑aliasing วิธีนี้ช่วยให้คุณสร้างภาพคุณภาพสูงโดยไม่ต้องติดตั้ง System.Drawing.Common

## ทำไมต้องใช้ Aspose.Drawing เพื่อเพิ่มข้อความลงในภาพ?
Aspose.Drawing ให้วิธีที่เชื่อถือได้และข้ามแพลตฟอร์มเพื่อเรนเดอร์ข้อความบนภาพโดยไม่ต้องใช้ไลบรารี GDI+ แบบดั้งเดิม, ส่งมอบคุณภาพและประสิทธิภาพที่สม่ำเสมอบนทุกระบบปฏิบัติการ รองรับการทำ anti‑aliasing ขั้นสูง, ตัวอักษร Unicode, และฟอนต์กำหนดเอง, และผสานรวมอย่างราบรื่นกับแอปพลิเคชัน .NET ทำให้เหมาะสำหรับการสร้างภาพบนเซิร์ฟเวอร์และเครื่องมือเดสก์ท็อป

- **ความน่าเชื่อถือข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS  
- **การเรนเดอร์ขั้นสูง** – anti‑aliasing และการทำ smoothing ของข้อความระดับ sub‑pixel เพื่อผลลัพธ์คมชัด  
- **ไม่มีการพึ่งพา external** – ไลบรารีบรรจุทุกอย่างที่คุณต้องการเพื่อ *สร้างภาพพร้อมข้อความ*  

## ข้อกำหนดเบื้องต้น
ก่อนเริ่ม, โปรดตรวจสอบว่าคุณมี:

- **Aspose.Drawing for .NET** – ดาวน์โหลดจาก [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/)  
- **IDE ของ .NET** เช่น Visual Studio หรือ VS Code  

## นำเข้า namespace
เริ่มต้นด้วยการนำเข้า namespace ที่จำเป็น:

These namespaces provide the core GDI+ types such as `Bitmap`, `Graphics`, and text rendering utilities.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## ขั้นตอนที่ 1: สร้างอ็อบเจ็กต์ bitmap และ graphics
`Bitmap` เป็นคอนเทนเนอร์ภาพแรสเตอร์ของ Aspose.Drawing สำหรับข้อมูลพิกเซล, และ `Graphics` ให้เมธอดการวาดเพื่อเรนเดอร์รูปทรงและข้อความลงบนมัน  

`Bitmap` แสดงภาพในหน่วยความจำ, ส่วน `Graphics` ให้เมธอดการวาดเพื่อเรนเดอร์ลงบนบิตแมพนั้น  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

ที่นี่เราสร้าง `Bitmap` ที่จะเก็บภาพสุดท้ายและอ็อบเจ็กต์ `Graphics` ที่ให้เราวาดบนมัน คำแนะนำ anti‑aliasing จะทำให้ข้อความดูเรียบเนียน

## ขั้นตอนที่ 2: ตั้งค่า brush, pen, และ font
`Brush` กำหนดสีเติม, `Pen` วาดขอบรูปทรง, และ `Font` ระบุฟอนต์, ขนาด, และสไตล์สำหรับการเรนเดอร์ข้อความ  

`Brush` เติมสีให้รูปทรง, `Pen` วาดขอบรูปทรง, และ `Font` กำหนดฟอนต์และขนาดสำหรับการเรนเดอร์ข้อความ  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** กำหนดสีของข้อความ  
- **Pen** ใช้ในภายหลังเพื่อวาดสี่เหลี่ยมรอบข้อความ (ไม่บังคับ)  
- **Font** ระบุฟอนต์, ขนาด, และสไตล์สำหรับการ *วาดสตริงบนภาพ*  

## ขั้นตอนที่ 3: กำหนดข้อความและสี่เหลี่ยม
`Rectangle` กำหนดกล่องขอบเขตที่ข้อความจะถูกวาง, ระบุพิกัด X/Y และความกว้าง/สูง  

`Rectangle` ระบุตำแหน่งและขนาดของพื้นที่สี่เหลี่ยม, ใช้ที่นี่เพื่อจำกัดข้อความที่วาด  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` กำหนดตำแหน่งที่ข้อความจะถูกวาง ปรับพิกัดและขนาดให้เหมาะกับการจัดวางของคุณ

## ขั้นตอนที่ 4: วาดสี่เหลี่ยมและข้อความ
`Graphics.DrawString` เรนเดอร์ข้อความที่ระบุภายในสี่เหลี่ยมที่กำหนดโดยใช้ฟอนต์และ brush ที่ให้มา  

`Graphics.DrawString` เรนเดอร์สตริงข้อความภายในสี่เหลี่ยมที่ระบุโดยใช้ฟอนต์และ brush ที่ให้มา  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

แรกเราวาดขอบพื้นที่ด้วยสี่เหลี่ยมสีน้ำเงิน, จากนั้นเราจะ **เพิ่มข้อความลงในบิตแมพ** โดยเรียก `DrawString` นี่คือแกนหลักของ *การวาดข้อความ* บนภาพ

## ขั้นตอนที่ 5: บันทึกผลลัพธ์
ภาพจะถูกบันทึกเป็นไฟล์ PNG, ตอบสนองความต้องการ *บันทึกบิตแมพเป็น PNG* แทนที่เส้นทาง placeholder ด้วยโฟลเดอร์จริงที่คุณต้องการเก็บไฟล์  

`bitmap.Save` เขียนภาพลงไฟล์ในรูปแบบที่เลือก, เช่น PNG  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## กรณีการใช้งานทั่วไป
- **สร้างใบรับรอง** พร้อมชื่อส่วนบุคคล  
- **สร้างภาพย่อที่มีลายน้ำ** สำหรับแกลเลอรีเว็บ  
- **สร้างแผนภูมิกระแสไดนามิก** ที่รวมป้ายกำกับหรือคำอธิบาย  

## การแก้ไขปัญหาและเคล็ดลับ
- **ไม่พบฟอนต์?** ตรวจสอบว่าฟอนต์ได้ติดตั้งบนเครื่องโฮสต์หรือใช้คอลเลกชันฟอนต์ส่วนตัว  
- **ข้อความถูกตัด?** เพิ่มขนาดสี่เหลี่ยมหรือทำให้ฟอนต์เล็กลง  
- **กังวลเรื่องประสิทธิภาพ?** ใช้อ็อบเจ็กต์ `Graphics` เดียวกันสำหรับหลายการวาดเมื่อเป็นไปได้  

## คำถามที่พบบ่อย
**Q: จะเปลี่ยนรูปแบบผลลัพธ์เป็น JPEG ได้อย่างไร?**  
A: แทนที่ส่วนขยาย `.png` ด้วย `.jpg` ในเมธอด `Save` และอาจระบุ `ImageCodecInfo` สำหรับคุณภาพ JPEG  

**Q: สามารถวาดข้อความหลายบรรทัดได้หรือไม่?**  
A: ได้, ใส่ตัวอักษรขึ้นบรรทัดใหม่ (`\n`) ในสตริงหรือใช้ `StringFormat` กับ `FormatFlags.LineLimit`  

**Q: มีวิธีวัดขนาดข้อความก่อนวาดหรือไม่?**  
A: ใช้ `Graphics.MeasureString` เพื่อรับมิติที่แม่นยำของข้อความที่เรนเดอร์  

**Q: Aspose.Drawing รองรับอักขระ Unicode หรือไม่?**  
A: แน่นอน. ให้ฟอนต์ที่มี glyph ที่ต้องการและไลบรารีจะเรนเดอร์ได้อย่างถูกต้อง  

**Q: เวอร์ชันของ Aspose.Drawing ที่ใช้ในการทดสอบคืออะไร?**  
A: ตัวอย่างทดสอบด้วย Aspose.Drawing 24.11 สำหรับ .NET  

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

## บทแนะนำที่เกี่ยวข้อง
- [สร้างกราฟิก Bitmap C# – บันทึกภาพ PNG และทำงานกับฟอนต์ที่ติดตั้งใน Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [วิธีบันทึกบิตแมพเป็น PNG ด้วย Aspose.Drawing API สำหรับ .NET](/drawing/net/image-editing/display/)
- [ข้อความบนภาพ](/drawing/net/use-cases/text-on-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}