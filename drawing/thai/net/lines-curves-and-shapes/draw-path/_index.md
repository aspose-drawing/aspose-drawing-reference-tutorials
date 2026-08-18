---
date: 2026-07-22
description: เรียนรู้วิธีบันทึก bitmap เป็น PNG และส่งออกภาพเป็น JPEG ด้วย Aspose.Drawing
  คู่มือทีละขั้นตอนแสดงการวาด paths, การสร้างภาพ, และการส่งออกรูปแบบต่างๆ
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: การวาด Paths ใน Aspose.Drawing
og_description: บันทึก bitmap เป็น PNG และส่งออกภาพเป็น JPEG ด้วย Aspose.Drawing สำหรับ
  .NET ทำตามบทเรียนนี้เพื่อวาด paths ซับซ้อน, สร้างภาพคุณภาพสูง, และส่งออกหลายรูปแบบ
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: บันทึก Bitmap เป็น PNG – การวาด Paths ด้วย Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: บันทึก Bitmap เป็น PNG – ใช้ GraphicsPath ใน Aspose.Drawing
url: /th/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วาดเส้นทางใน Aspose.Drawing

## วิธีใช้ GraphicsPath – บทนำ

**บันทึกบิตแมพเป็น PNG** มักเป็นขั้นตอนแรกเมื่อคุณต้องการภาพที่ไม่มีการสูญเสียข้อมูลสำหรับการประมวลผลต่อหรือการเผยแพร่ ในบทเรียนนี้คุณจะได้เรียนรู้วิธีวาดเส้นเวกเตอร์ที่ซับซ้อนด้วย `GraphicsPath` เรนเดอร์ลงบนบิตแมพ และจากนั้น **บันทึกบิตแมพเป็น PNG** หรือแม้กระทั่ง **ส่งออกภาพเป็น JPEG** ไม่ว่าคุณจะสร้างเครื่องมือรายงาน ไลบรารีแผนภูมิแบบกำหนดเอง หรือแค่ต้องการสร้างกราฟิกแบบไดนามิก Aspose.Drawing จะมอบ API ที่จัดการเต็มรูปแบบและข้ามแพลตฟอร์มที่แทนที่ System.Drawing.Common

## คำตอบสั้น ๆ
- **GraphicsPath สามารถวาดอะไรได้บ้าง?** เส้น, สี่เหลี่ยม, วงรี, โค้ง, และรูปร่างกำหนดเอง.  
- **ต้องการไลเซนส์หรือไม่?** ทดลองใช้ฟรี; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **ต้องใช้ System.Drawing.Common หรือไม่?** ไม่จำเป็น, Aspose.Drawing ทำงานอิสระ.  
- **สามารถบันทึกเป็นรูปแบบต่าง ๆ ได้หรือไม่?** ได้ – PNG, JPEG, BMP, GIF, และอื่น ๆ.

## GraphicsPath คืออะไร?
`GraphicsPath` คือคอนเทนเนอร์เวกเตอร์ของ Aspose.Drawing ที่เก็บลำดับของ primitive การวาดเช่น เส้น, โค้ง, และวงกลมเป็นอ็อบเจ็กต์เดียวโดยการจัดกลุ่ม primitive เหล่านี้ คุณสามารถใช้การแปลง, กฎการเติม, และการตั้งค่าสไตล์เส้นอย่างสอดคล้องกัน ซึ่งทำให้การสร้างกราฟิกที่ซับซ้อนง่ายขึ้นและรับประกันการเรนเดอร์ที่สอดคล้องกันในรูปแบบผลลัพธ์ต่าง ๆ

## ทำไมต้องใช้ GraphicsPath กับ Aspose.Drawing?
การใช้ GraphicsPath กับ Aspose.Drawing ให้ความสามารถในการวาดเวกเตอร์ที่แม่นยำ ยืดหยุ่น และประสิทธิภาพสูง มันช่วยให้คุณสร้างรูปร่างซับซ้อน, ใช้การแปลง, และเรนเดอร์อย่างมีประสิทธิภาพ พร้อมคงความสอดคล้องข้ามแพลตฟอร์มและรองรับการประมวลผลภาพขนาดใหญ่ นอกจากนี้ยังทำงานร่วมกับไลบรารี .NET อื่น ๆ อย่างไร้รอยต่อ ทำให้คุณสามารถรวมเวิร์กโฟลว์แบบแรสเตอร์และเวกเตอร์ในแอปพลิเคชันเดียวได้

- **ความแม่นยำ:** รองรับ primitive เวกเตอร์กว่า 50 รายการด้วยความแม่นยำระดับ sub‑pixel, ทำให้เมื่อคุณ **บันทึกบิตแมพเป็น PNG** ผลลัพธ์คมชัดที่ความละเอียดใดก็ได้.  
- **ความยืดหยุ่น:** รวมเส้น, โค้ง, และ Bezier curve เป็นเส้นทางเดียว, แล้วเรนเดอร์ด้วยการเรียก `Graphics.DrawPath` ครั้งเดียว.  
- **ประสิทธิภาพ:** ท่อการเรนเดอร์ที่ปรับแต่งทำงานกับภาพขนาดสูงสุด 400 MP โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ, ทำให้งานแบตช์ขนาดใหญ่เป็นไปได้.  
- **ข้ามแพลตฟอร์ม:** ผลลัพธ์เดียวกันบน Windows, Linux, และ macOS, ขจัดบั๊กที่เจาะจงแพลตฟอร์ม.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มบทเรียน โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้:

- **ไลบรารี Aspose.Drawing:** ดาวน์โหลดและติดตั้งไลบรารี Aspose.Drawing คุณสามารถหาไลบรารีได้ [ที่นี่](https://releases.aspose.com/drawing/net/).
- **ผลิตภัณฑ์ Aspose อื่น ๆ:** สำรวจข้อเสนอเพิ่มเติมของ Aspose [ที่นี่](https://releases.aspose.com/).
- **สภาพแวดล้อมการพัฒนา:** ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ของคุณพร้อมเครื่องมือที่จำเป็น (Visual Studio, .NET SDK, ฯลฯ).

## นำเข้า Namespaces

เริ่มต้นด้วยการนำเข้า namespaces ที่จำเป็นในโปรเจกต์ของคุณ:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## ขั้นตอนที่ 1: สร้าง Bitmap และ Graphics

Bitmap แสดงภาพในหน่วยความจำ, ในขณะที่ Graphics ให้เมธอดการวาดเพื่อเรนเดอร์ลงบนภาพนั้น เริ่มต้นด้วยการสร้าง `Bitmap` และอ็อบเจ็กต์ `Graphics` เพื่อทำงานกับมัน Bitmap นี้จะเป็นแคนวาสที่ `GraphicsPath` จะถูกเรนเดอร์ลงไป และต่อมาคุณจะ **บันทึกบิตแมพเป็น PNG**:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## ขั้นตอนที่ 2: กำหนด Pen และ GraphicsPath

Pen กำหนดสี, ความกว้าง, และสไตล์ของเส้น; GraphicsPath เก็บคอลเลกชันของ primitive การวาดเป็นอ็อบเจ็กต์เวกเตอร์เดียว ต่อไปให้กำหนด `Pen` เพื่อระบุคุณลักษณะการวาดและสร้างอินสแตนซ์ของ `GraphicsPath` อ็อบเจ็กต์ `GraphicsPath` จะเก็บข้อมูลเวกเตอร์ก่อนที่จะแสดงผล:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## ขั้นตอนที่ 3: เพิ่มเส้นและรูปร่าง

AddLine, AddRectangle, และ AddEllipse จะเพิ่มรูปร่างที่สอดคล้องลงใน GraphicsPath เพื่อการเรนเดอร์ในภายหลัง เพิ่มเส้น, สี่เหลี่ยม, และวงรีลงใน `GraphicsPath` เพื่อสร้างเส้นทางซับซ้อน คุณยังสามารถเพิ่ม Bezier curve กำหนดเองเพื่อให้ได้รูปร่างที่เรียบได้:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## ขั้นตอนที่ 4: วาดเส้นทาง

DrawPath เรนเดอร์ข้อมูลเวกเตอร์จาก GraphicsPath ลงบนพื้นผิว Graphics โดยใช้ Pen ที่ระบุ วาดเส้นทางลงบนอ็อบเจ็กต์ `Graphics` ด้วย `Pen` ที่กำหนด การดำเนินการนี้จะทำให้ข้อมูลเวกเตอร์แปลงเป็นภาพแรสเตอร์บนแคนวาสบิตแมพ:

```csharp
graphics.DrawPath(pen, path);
```

## ขั้นตอนที่ 5: บันทึกภาพ – ส่งออกเป็น PNG หรือ JPEG

เมธอด Bitmap.Save จะเขียนภาพลงดิสก์ในรูปแบบที่เลือก เช่น PNG หรือ JPEG หลังจากวาดเสร็จคุณสามารถ **บันทึกบิตแมพเป็น PNG** เพื่อคุณภาพไม่มีการสูญเสียหรือ **ส่งออกภาพเป็น JPEG** เพื่อขนาดไฟล์ที่เล็กลง เลือกรูปแบบที่เหมาะกับสถานการณ์ต่อไปของคุณ:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

ทำซ้ำขั้นตอนเหล่านี้ตามต้องการเพื่อสร้างเส้นทางที่ซับซ้อนและสวยงาม

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **เส้นทางไม่ปรากฏ** | ตรวจสอบให้แน่ใจว่าความสีของ Pen แตกต่างจากพื้นหลังและบิตแมพถูกบันทึกอย่างถูกต้อง. |
| **ขนาดภาพไม่คาดคิด** | ตรวจสอบขนาดบิตแมพและรูปแบบพิกเซลให้ตรงกับความต้องการของคุณ. |
| **ข้อยกเว้นไลเซนส์** | ใช้ไลเซนส์ทดลองสำหรับการทดสอบ; ใส่ไลเซนส์ที่ถูกต้องก่อนนำไปใช้งานจริง. |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.Drawing กับไลบรารี .NET อื่น ๆ ได้หรือไม่?

A1: ได้, Aspose.Drawing ผสานรวมอย่างราบรื่นกับไลบรารี .NET อื่น ๆ ให้ความหลากหลายในการพัฒนาโครงการของคุณ.

### Q2: มีเวอร์ชันทดลองหรือไม่?

A2: มี, คุณสามารถเข้าถึงการทดลองใช้ฟรีได้ [ที่นี่](https://releases.aspose.com/).

### Q3: ฉันจะหาแหล่งสนับสนุนสำหรับ Aspose.Drawing ได้จากที่ไหน?

A3: เยี่ยมชม [ฟอรั่ม](https://forum.aspose.com/c/drawing/44) ของ Aspose.Drawing เพื่อขอความช่วยเหลือและการสนับสนุนจากชุมชน.

### Q4: ฉันจะขอรับไลเซนส์ชั่วคราวได้อย่างไร?

A4: รับไลเซนส์ชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ฉันสามารถซื้อ Aspose.Drawing ได้หรือไม่?

A5: ได้, คุณสามารถซื้อ Aspose.Drawing ได้ [ที่นี่](https://purchase.aspose.com/buy).

**คำถามเพิ่มเติม & คำตอบ**

**ถาม: ฉันสามารถวาด Bezier curve กำหนดเองด้วย GraphicsPath ได้หรือไม่?**  
**ตอบ:** แน่นอน – ใช้ `path.AddBezier(...)` เพื่อกำหนดโค้งที่เรียบ.

**ถาม: ฉันจะล้าง GraphicsPath ก่อนนำกลับมาใช้ใหม่ได้อย่างไร?**  
**ตอบ:** เรียก `path.Reset()` เพื่อลบทุกรูปและเริ่มใหม่.

## สรุป

ขอแสดงความยินดี! คุณได้เรียนรู้ **วิธีใช้ GraphicsPath** เพื่อวาดเส้นทางและจากนั้น **บันทึกบิตแมพเป็น PNG** หรือ **ส่งออกภาพเป็น JPEG** ด้วย Aspose.Drawing สำหรับ .NET บทเรียนนี้ครอบคลุมการสร้างบิตแมพ, การกำหนด Pen, การสร้าง `GraphicsPath`, การเรนเดอร์รูปร่างต่าง ๆ, และการส่งออกภาพสุดท้ายในหลายรูปแบบ ทดลองเปลี่ยนพิกัด, สี, และความกว้างของเส้นเพื่อปลดปล่อยศักยภาพการสร้างสรรค์เต็มที่ของ Aspose.Drawing.

---

**อัปเดตล่าสุด:** 2026-07-22  
**ทดสอบกับ:** Aspose.Drawing 24.12 for .NET  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [บันทึกบิตแมพเป็น PNG & วาดเส้นโค้งปิดด้วย Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [บันทึกบิตแมพ C# – วาด Bezier Spline ด้วย Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [วิธีบันทึกภาพและวาด Cardinal Spline ใน Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}