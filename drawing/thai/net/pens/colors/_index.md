---
date: 2026-09-18
description: เรียนรู้วิธีตั้งค่าสีปากกาใน Aspose.Drawing สำหรับ .NET, draw colored
  lines, และบันทึก PNG images ด้วยตัวอย่างโค้ดง่ายๆ
keywords:
- set pen color
- save png image
- cross platform drawing
- draw lines with pen
- high quality png
lastmod: 2026-09-18
linktitle: ทำงานกับสีใน Aspose.Drawing
og_description: ตั้งค่าสีปากกาใน Aspose.Drawing สำหรับ .NET และสร้าง PNG images คุณภาพสูง.
  Learn cross‑platform drawing, draw lines with pen, และบันทึก PNG images ภายในไม่กี่นาที.
og_image_alt: Screenshot of code setting pen color and saving a PNG with Aspose.Drawing
og_title: ตั้งค่าสีปากกาใน Aspose.Drawing – คู่มือสำหรับการสร้าง PNG คุณภาพสูง
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored
    lines, and save PNG images with simple code examples.
  headline: How to set pen color in Aspose.Drawing
  type: TechArticle
- description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored
    lines, and save PNG images with simple code examples.
  name: How to set pen color in Aspose.Drawing
  steps:
  - name: '**Aspose.Drawing Library** – download and install from the official site
      **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.'
    text: '**Aspose.Drawing Library** – download and install from the official site
      **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.'
  - name: '**A .NET development environment** – Visual Studio, VS Code, or any IDE
      you prefer.'
    text: '**A .NET development environment** – Visual Studio, VS Code, or any IDE
      you prefer.'
  - name: '**Basic C# knowledge** – familiarity with classes, objects, and namespaces.'
    text: '**Basic C# knowledge** – familiarity with classes, objects, and namespaces.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing integrates smoothly with other .NET libraries, providing
      a versatile environment for graphic manipulation.
    question: Can I use Aspose.Drawing with other .NET libraries?
  - answer: You can get a temporary license **[Aspose temporary license page](https://purchase.aspose.com/temporary-license/)**,
      allowing you to explore the full potential of Aspose.Drawing.
    question: How can I obtain a temporary license for Aspose.Drawing?
  - answer: Yes, Aspose.Drawing supports JPEG, GIF, BMP, TIFF, and more. Refer to
      the documentation for a complete list.
    question: Does Aspose.Drawing support image formats other than PNG?
  - answer: Absolutely! Aspose.Drawing works in both desktop and web applications,
      enabling dynamic graphic generation on servers.
    question: Can I use Aspose.Drawing for web development?
  - answer: Yes, you can explore a free trial **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**,
      letting you evaluate the library before purchasing.
    question: Is there a free trial available for Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- .NET graphics
- pen color
- PNG output
title: วิธีตั้งค่าสีปากกาใน Aspose.Drawing
url: /th/net/pens/colors/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีตั้งค่าสีปากกาใน Aspose.Drawing

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **ตั้งค่าสีปากกา** เมื่อวาดด้วย Aspose.Drawing สำหรับ .NET, สร้างแคนวาสกราฟิก, วาดเส้นสี, และ **บันทึกไฟล์ภาพ PNG** ด้วยคุณภาพสูง ไม่ว่าคุณจะกำลังสร้างยูทิลิตี้เดสก์ท็อป, บริการรายงาน, หรือเว็บ API ที่สร้างแผนภูมิ การควบคุมสีปากกาเป็นสิ่งสำคัญสำหรับกราฟิกที่ดูเป็นมืออาชีพ

## คำตอบสั้น
- **คลาสหลักสำหรับการวาดคืออะไร?** `Graphics` ที่สร้างจาก `Bitmap`
- **จะเปลี่ยนสีของปากกาอย่างไร?** ใช้ `Color.FromKnownColor` หรือ `Color.FromArgb`
- **ฟอร์แมตใดที่แนะนำสำหรับผลลัพธ์แบบไม่มีการสูญเสีย?** PNG (`.png`)
- **ต้องมีลิขสิทธิ์สำหรับการพัฒนาหรือไม่?** มีลิขสิทธิ์ชั่วคราวสำหรับการประเมินผล
- **สามารถใช้กับ ASP.NET Core ได้หรือไม่?** ใช่, Aspose.Drawing ทำงานกับ .NET Core และ .NET 5+

## “ตั้งค่าสีปากกา” ใน Aspose.Drawing คืออะไร?

การตั้งค่าสีปากกาหมายถึงการกำหนดค่า `Color` ให้กับอ็อบเจกต์ `Pen` ก่อนทำการวาดใด ๆ สีที่เลือกจะมีผลต่อเฉดสี, ความทึบ, และความหนาของเส้น, รูปร่าง, และเส้นขอบข้อความที่เรนเดอร์บนแคนวาส, ทำให้คุณควบคุมภาพสุดท้ายได้อย่างแม่นยำ

## ทำไมต้องใช้ Aspose.Drawing สำหรับการจัดการสี?

Aspose.Drawing ให้ **การวาดข้ามแพลตฟอร์ม** ที่ทำงานบน Windows, Linux, และ macOS โดยไม่มีข้อจำกัดของ System.Drawing.Common รองรับ **การส่งออก PNG คุณภาพสูง** (สูงสุด 32‑bit ARGB) และมีชุด API สีที่หลากหลายรวมถึงสีที่รู้จักกว่า 50 สีและการปรับแต่ง ARGB เต็มรูปแบบ ไลบรารีสามารถประมวลผลภาพหลายร้อยหน้าโดยใช้หน่วยความจำต่ำกว่า 50 MB ทำให้เหมาะสำหรับการสร้างบนเซิร์ฟเวอร์

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในโค้ด, โปรดตรวจสอบว่าคุณมี:

1. **Aspose.Drawing Library** – ดาวน์โหลดและติดตั้งจากหน้าเว็บไซต์อย่างเป็นทางการ **[หน้าโหลด Aspose.Drawing](https://releases.aspose.com/drawing/net/)**  
2. **สภาพแวดล้อมการพัฒนา .NET** – Visual Studio, VS Code, หรือ IDE ที่คุณชื่นชอบ  
3. **ความรู้พื้นฐาน C#** – ความคุ้นเคยกับคลาส, อ็อบเจกต์, และเนมสเปซ

## นำเข้าเนมสเปซ

เนมสเปซ `Aspose.Drawing` เป็นไลบรารีหลักที่ให้ประเภทที่เกี่ยวกับการวาดทั้งหมด เช่น `Bitmap`, `Graphics`, `Pen`, และ `Color`, ทำให้ผู้พัฒนาสามารถสร้าง, ปรับแต่ง, และเรนเดอร์ภาพข้ามแพลตฟอร์มโดยไม่ต้องพึ่งพา System.Drawing.Common

```csharp
using System.Drawing;
```

## ขั้นตอนที่ 1: สร้าง bitmap (แคนวาส)

คลาส `Bitmap` แทนบัฟเฟอร์พิกเซลในหน่วยความจำที่สามารถวาดได้; รองรับรูปแบบพิกเซลหลายแบบรวมถึง 32‑bit ARGB ซึ่งรักษาความลึกสีและความโปร่งใสเต็มที่สำหรับการส่งออก PNG คุณภาพสูง

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## ขั้นตอนที่ 2: สร้างอ็อบเจกต์ graphics

อ็อบเจกต์ `Graphics` ทำหน้าที่เป็นพื้นผิวการวาดที่เชื่อมต่อกับ `Bitmap`, มีเมธอดเช่น `DrawLine`, `DrawRectangle`, และ `DrawString` ที่วาดรูปทรง, เส้น, และข้อความลงบนบัฟเฟอร์ภาพพื้นฐาน

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## ขั้นตอนที่ 3: วาดเส้นด้วยปากกาสีฟ้า (เส้นสีแรก)

คลาส `Pen` กำหนดคุณลักษณะของเส้นและขอบ, รวมถึงสี, ความกว้าง, รูปแบบ dash, และการจัดแนว, และใช้โดยเมธอดของ `Graphics` เพื่อวาดรูปร่างและเส้นทางบนแคนวาส

```csharp
Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawLine(bluePen, 100, 100, 900, 100);
```

## ขั้นตอนที่ 4: วาดเส้นด้วยปากกาสีแดงที่กำหนดเอง

ตัวอย่างนี้แสดงวิธี **วาดเส้นสี** ด้วยค่า ARGB ที่กำหนดเอง, ให้คุณควบคุมความทึบและเฉดสีได้อย่างเต็มที่

```csharp
Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
graphics.DrawLine(redPen, 100, 200, 900, 200);
```

## ขั้นตอนที่ 5: บันทึกภาพเป็น PNG

สุดท้ายเราจะ **บันทึกภาพ PNG** ไปยังโฟลเดอร์ที่ต้องการ PNG รักษาความโปร่งใสและความแม่นยำของสี ทำให้เป็นฟอร์แมตที่นิยมสำหรับกราฟิกเว็บและรายงาน

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **ภาพว่างเปล่า** | Graphics ไม่ได้ flush ก่อนบันทึก | เรียก `graphics.Dispose();` หรือใช้ `Graphics` ภายในบล็อก `using` |
| **สีไม่ตรง** | ใช้ `FromKnownColor` กับ enum ที่ผิด | ตรวจสอบค่า enum หรือใช้ `FromArgb` เพื่อควบคุมอย่างแม่นยำ |
| **ข้อผิดพลาดเส้นทางไฟล์** | โฟลเดอร์ไม่ถูกต้องหรือไม่มีสิทธิ์ | ตรวจสอบให้โฟลเดอร์เป้าหมายมีอยู่และแอปมีสิทธิ์เขียน |

## คำถามที่พบบ่อย

**ถาม: สามารถใช้ Aspose.Drawing ร่วมกับไลบรารี .NET อื่นได้หรือไม่?**  
ตอบ: ใช่, Aspose.Drawing สามารถผสานรวมกับไลบรารี .NET อื่นได้อย่างราบรื่น, ให้สภาพแวดล้อมที่หลากหลายสำหรับการจัดการกราฟิก

**ถาม: จะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.Drawing อย่างไร?**  
ตอบ: คุณสามารถรับลิขสิทธิ์ชั่วคราว **[หน้าลิขสิทธิ์ชั่วคราวของ Aspose](https://purchase.aspose.com/temporary-license/)** เพื่อสำรวจศักยภาพเต็มของ Aspose.Drawing

**ถาม: Aspose.Drawing รองรับฟอร์แมตภาพอื่นนอกจาก PNG หรือไม่?**  
ตอบ: ใช่, Aspose.Drawing รองรับ JPEG, GIF, BMP, TIFF, และอื่น ๆ ดูเอกสารสำหรับรายการเต็ม

**ถาม: สามารถใช้ Aspose.Drawing สำหรับการพัฒนาเว็บได้หรือไม่?**  
ตอบ: แน่นอน! Aspose.Drawing ทำงานได้ทั้งในแอปเดสก์ท็อปและเว็บ, ช่วยสร้างกราฟิกแบบไดนามิกบนเซิร์ฟเวอร์

**ถาม: มีการทดลองใช้ฟรีสำหรับ Aspose.Drawing หรือไม่?**  
ตอบ: มี, คุณสามารถทดลองใช้ฟรี **[หน้าโหลด Aspose.Drawing](https://releases.aspose.com/drawing/net/)** เพื่อประเมินไลบรารีก่อนซื้อ

## สรุป

ในคู่มือนี้เราได้ครอบคลุมวิธี **ตั้งค่าสีปากกา**, **วาดเส้นสี**, **สร้างอ็อบเจกต์ graphics**, และ **บันทึกผลลัพธ์เป็น PNG คุณภาพสูง** ด้วย Aspose.Drawing สำหรับ .NET พื้นฐานเหล่านี้เปิดประตูสู่สถานการณ์ขั้นสูงเช่นการวาดรูปทรง, การเรนเดอร์ข้อความ, และการสร้างแผนภูมิแบบไดนามิก หากคุณเจออุปสรรค, **[เอกสาร Aspose.Drawing](https://reference.aspose.com/drawing/net/)** และ **[ฟอรั่มสนับสนุน](https://forum.aspose.com/c/drawing/44)** เป็นแหล่งข้อมูลที่ดีสำหรับหาคำตอบ

---

**อัปเดตล่าสุด:** 2026-09-18  
**ทดสอบกับ:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีบันทึก bitmap เป็น PNG ขณะวาดหลายเส้นด้วย Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [วิธีเชื่อมต่อ Path ด้วย Pen ใน Aspose.Drawing .NET](/drawing/net/pens/)
- [ปรับปรุงคุณภาพภาพด้วย Antialiasing ใน Aspose.Drawing](/drawing/net/rendering/antialiasing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}