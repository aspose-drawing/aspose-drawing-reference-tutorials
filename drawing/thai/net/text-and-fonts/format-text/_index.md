---
date: 2026-02-25
description: เรียนรู้วิธีตั้งการจัดแนวข้อความใน Aspose.Drawing สำหรับ .NET และเพิ่มข้อความลงในภาพ
  คู่มือแบบขั้นตอนพร้อมตัวอย่าง
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: ตั้งค่าการจัดแนวข้อความด้วย Aspose.Drawing สำหรับ .NET
url: /th/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าการจัดแนวข้อความใน Aspose.Drawing

## Introduction

เมื่อพูดถึง **set text alignment** และการจัดรูปแบบข้อความในแอปพลิเคชัน .NET ของคุณ Aspose.Drawing เป็นไลบรารีที่นักพัฒนาต้องพึ่งพาเพื่อความแม่นยำ ประสิทธิภาพ และ API ที่ครอบคลุม ไม่ว่าคุณจะสร้างเครื่องมือรายงาน ตัวสร้างแบจไดนามิก หรือโซลูชันที่เน้นกราฟิก การควบคุมวิธีการจัดตำแหน่งข้อความภายในรูปร่างทำให้ผลลัพธ์ดูเรียบหรูและเป็นมืออาชีพ ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมด—ตั้งแต่การสร้างแคนวาสบิตแมพจนถึงการวาดสี่เหลี่ยมพร้อมข้อความ การจัดการ overflow และสุดท้ายการบันทึกภาพ

## Quick Answers
- **“set text alignment” หมายถึงอะไร?** มันกำหนดว่าข้อความถูกจัดตำแหน่งแนวนอนและแนวตั้งภายในสี่เหลี่ยมวาดอย่างไร.  
- **คลาสใดที่ควบคุมการจัดแนว?** `StringFormat` ให้คุณตั้งค่า `Alignment` และ `LineAlignment`.  
- **ฉันสามารถวาดสตริงและสี่เหลี่ยมพร้อมกันได้หรือไม่?** ใช่—ใช้ `Graphics.DrawRectangle` แล้วตามด้วย `Graphics.DrawString`.  
- **ฉันจะป้องกันข้อความล้นได้อย่างไร?** ปรับขนาดสี่เหลี่ยมหรือแยกข้อความเป็นหลายบรรทัดด้วยตนเอง.  
- **ฉันต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีใบอนุญาต Aspose.Drawing แบบเชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่การประเมินผล.

## What is **set text alignment** in Aspose.Drawing?

`set text alignment` หมายถึงการกำหนดค่าการจัดตำแหน่งแนวนอน (`StringAlignment`) และแนวตั้ง (`LineAlignment`) ของข้อความภายใน `Rectangle` หรือพื้นที่วาดใด ๆ การปรับแต่งการตั้งค่าเหล่านี้ทำให้คุณควบคุมว่าข้อความจะแสดงเป็นจัดซ้าย, จัดกึ่งกลาง, จัดขวา, จัดบน, จัดกลาง, หรือจัดล่าง.

## Why use Aspose.Drawing for text alignment?

- **Full .NET compatibility** – ทำงานกับ .NET Framework, .NET Core, และ .NET 5/6+.  
- **Pixel‑perfect rendering** – รองรับการแอนตี้เอเลียสและ DPI สูงโดยอัตโนมัติ.  
- **No GDI+ limitations** – แตกต่างจาก `System.Drawing.Common` Aspose.Drawing สามารถทำงานบนคอนเทนเนอร์ Linux โดยไม่มีการพึ่งพาเนทีฟ.  
- **Rich styling** – ผสานฟอนต์, แปรง, ปากกา, และอ็อบเจกต์ `StringFormat` ที่กำหนดเองเพื่อสร้างเลย์เอาต์ที่ซับซ้อน.

## Prerequisites

1. **Aspose.Drawing Library** – ดาวน์โหลดได้จาก [here](https://releases.aspose.com/drawing/net/).  
2. **Development Environment** – Visual Studio 2022 (หรือ IDE C# ใดก็ได้).  
3. **Basic .NET knowledge** – คุณควรคุ้นเคยกับโปรเจกต์ C# และแพ็กเกจ NuGet.

## Import Namespaces

เพื่อเริ่มต้น ให้นำเนมสเปซที่จำเป็นเข้ามาในสโคป ซึ่งจะทำให้คุณเข้าถึงกราฟิก การเรนเดอร์ข้อความ และออบเจกต์พื้นฐานสำหรับการวาด.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step 1: Create Bitmap and Graphics Objects  

การสร้าง bitmap จะให้แคนวาสที่คุณสามารถวาดบนมันได้ อ็อบเจกต์ `Graphics` คือพื้นผิวการวาด และเราจะเปิดใช้งานการเรนเดอร์ข้อความคุณภาพสูงด้วย `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Step 2: Define **StringFormat** and Styling  

ที่นี่เราจะ **set text alignment** โดยกำหนดค่าอ็อบเจกต์ `StringFormat` นอกจากนี้เรายังเตรียมแปรง, ปากกา, และฟอนต์ที่จะใช้เมื่อวาดสตริง.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Step 3: Create and Format Text – **how to draw string** and **draw rectangle with text**

เราจะประกอบข้อความ, กำหนดสี่เหลี่ยมที่จะบรรจุข้อความ, แล้ววาดทั้งเส้นขอบสี่เหลี่ยมและสตริงเอง.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### How to handle text overflow

หาก `text` ที่ให้มามากเกินขอบเขตของสี่เหลี่ยม คุณมีสองตัวเลือกทั่วไป:

1. **Resize the rectangle** – เพิ่มค่า `rectangle.Width` หรือ `rectangle.Height`.  
2. **Split the text** – แยกสตริงเป็นบรรทัดที่พอดี แล้วเรียก `DrawString` สำหรับแต่ละบรรทัดพร้อมปรับค่า Y‑coordinates.

## Step 4: Save the Output – **add text to image**

สุดท้าย เขียน bitmap ลงดิสก์ ขั้นตอนนี้แสดงการ **add text to image** ในหนึ่งคำสั่ง.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **ข้อความเบลอ** | ตรวจสอบว่าได้ตั้งค่า `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` แล้ว. |
| **ข้อความถูกตัด** | เพิ่มขนาดสี่เหลี่ยมหรือเปิดใช้งานการตัดคำโดยวัดขนาดสตริง (`Graphics.MeasureString`). |
| **ไม่พบฟอนต์** | ตรวจสอบว่าฟอนต์ได้ติดตั้งบนเครื่องหรือฝังฟอนต์ส่วนตัวด้วย `PrivateFontCollection`. |
| **สีที่ไม่คาดคิด** | ตรวจสอบสีของแปรงและปากกาอีกครั้ง; จำไว้ว่า `Color.FromKnownColor` ใช้สีที่กำหนดโดยระบบ. |

## Frequently Asked Questions

### Q1: Aspose.Drawing รองรับทุกเวอร์ชันของ .NET หรือไม่?

A1: ใช่, Aspose.Drawing ถูกออกแบบให้เข้ากันได้กับหลายเวอร์ชันของ .NET เพื่อให้ความยืดหยุ่นกับนักพัฒนา.

### Q2: ฉันสามารถปรับแต่งสไตล์ฟอนต์เพิ่มเติมได้หรือไม่?

A2: แน่นอน! ปรับพารามิเตอร์ของอ็อบเจกต์ `Font` เพื่อให้ได้ขนาด, สไตล์, และตระกูลฟอนต์ที่ต้องการ.

### Q3: ฉันจะจัดการกับข้อความล้นภายในสี่เหลี่ยมที่กำหนดได้อย่างไร?

A3: คุณสามารถจัดการข้อความล้นได้โดยปรับขนาดสี่เหลี่ยมหรือใช้ตรรกะแบบกำหนดเองเพื่อจัดการข้อความยาว.

### Q4: มีตัวเลือกการจัดรูปแบบอื่น ๆ ใน Aspose.Drawing หรือไม่?

A4: มี, Aspose.Drawing มีชุดเครื่องมือที่ครอบคลุมสำหรับการจัดการกราฟิก รวมถึงตัวเลือกการจัดรูปแบบต่าง ๆ สำหรับข้อความ, รูปร่าง, และอื่น ๆ.

### Q5: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมสำหรับ Aspose.Drawing ได้จากที่ไหน?

A5: สำรวจฟอรั่ม Aspose.Drawing ที่ [here](https://forum.aspose.com/c/drawing/44) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

**Additional Q&A**

**Q: ฉันจะวาดสตริงโดยไม่มีสี่เหลี่ยมล้อมรอบได้อย่างไร?**  
A: ละเว้นการเรียก `DrawRectangle` และส่งตำแหน่ง `PointF` ที่ต้องการให้กับ `Graphics.DrawString`.

**Q: ฉันสามารถหมุนข้อความพร้อมคงการจัดแนวได้หรือไม่?**  
A: ใช่—ใช้การแปลง `Matrix` กับอ็อบเจกต์ `Graphics` ก่อนวาด แล้วรีเซ็ตหลังจากนั้น.

**Q: สามารถส่งออกภาพเป็น JPEG แทน PNG ได้หรือไม่?**  
A: เพียงเปลี่ยนส่วนขยายไฟล์ใน `bitmap.Save` และอาจระบุ `ImageFormat.Jpeg` เพิ่มเติม.

---

**อัปเดตล่าสุด:** 2026-02-25  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}