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

## การแนะนำ

**ตั้งค่าการจัดตำแหน่งข้อความ** และดูรูปแบบข้อความในแอปพลิเคชัน .NET ของคุณ Aspose. การวาดภาพเป็นไลบรารีที่ต้องใช้ระบบควบคุมประสิทธิภาพและ API การรับรู้สร้างเครื่องมือรายงานบุคคลสร้างแบจไดนามิกหรือส่วนประกอบที่เน้นกราฟิก การควบคุมวิธีการจัดตำแหน่งข้อความภายในรูปร่างทำให้ผลลัพธ์ดูเรียบหรูและห้องนั่งเล่นในบทแนะนำนี้เราจะค้นคว้าทั้งหมด— ตั้งแต่การเริ่มต้นแคนวาสแมพจนถึงเต็มรูปแบบพร้อมข้อความที่ล้นหลามและสุดท้ายวิจัยภาพ

## คำตอบด่วน
- **“ตั้งค่าการจัดตำแหน่งข้อความ” ส่วนใหญ่อะไร?** มันกำหนดว่าข้อความถูกจัดวางตำแหน่งและส่วนการควบคุมภายในวาดอย่างไร
- ** คลาสใดที่ควบคุมแนวแนวได้เหมือนกัน?** `StringFormat` ให้คุณตั้งค่า `Alignment` และ `LineAlignment`.
- **เริ่มต้นเขียนและดูและติดตามได้ตลอดเวลา?** สามารถตรวจสอบ—ใช้ `Graphics.DrawRectangle` จากนั้นจึงค้นหา `Graphics.DrawString`
- ** ฉันจะป้องกันข้อความล้นได้อย่างไร?** ในตอนกลางคืนหรือแยกข้อความเป็นหลายบรรทัดอื่นๆ
- ** บางครั้งจำเป็นต้องมีจริงหรือไม่?** จำเป็นต้องมีการกำหนดรูปแบบการวาดภาพเพื่อตรวจสอบคุณสมบัติของมัน

## **ตั้งค่าการจัดตำแหน่งข้อความ** ใน Aspose. Drawing คืออะไร

`set textการจัดตำแหน่ง`ส่วนใหญ่มักจะเป็นที่ที่เห็นได้ชัด (`StringAlignment`) และ (`LineAlignment`) ของข้อความภายใน `Rectangle` หรือพื้นที่ใดๆ วาดลงไปที่จุดนั้นต้องใช้ตัวควบคุมว่าข้อความที่เป็นการจัดด้านซ้าย, จัดกึ่งกลาง, จัดชิดขวา, จัดบน, จัดกลาง, หรือจัดด้านล่าง

## เหตุใดจึงต้องใช้ Aspose. Drawing เพื่อจัดตำแหน่งข้อความ

- **ความเข้ากันได้ของ .NET เต็มรูปแบบ** – รองรับ .NET Framework, .NET Core, และ .NET 5/6+.
- **การเรนเดอร์พิกเซลที่สมบูรณ์แบบ** – รองรับการแอนตี้เอเลียสและ DPI ของซอฟท์แวร์
- **ไม่มีข้อจำกัด GDI+** – แตกต่างจาก `System.Painting.Common` Aspose. Drawing สามารถทำงานบน Linux ได้โดยไม่มีการวิจารณ์เนทีฟ.
- **Rich styling** – สำหรับฟอนต์, เมนบอร์ด, ปากกา, และอ็อบเจกต์ `StringFormat` ประสิทธิภาพของซอฟท์แวร์มาเลเซีย.

## ข้อกำหนดเบื้องต้น

1. **Aspose. Drawing Library** – ดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/drawing/net/)
2. **สภาพแวดล้อมการพัฒนา** – Visual Studio 2022 (หรือ IDE C# บาหลี)
3. **ความรู้พื้นฐาน .NET** – ส่วนโปรเจกต์ C# และแพ็กเกจ NuGet.

## นำเข้าเนมสเปซ

เพื่อเริ่มต้น ให้นำเนมสเปซที่จำเป็นเข้ามาในสโคป ซึ่งจะทำให้คุณเข้าถึงกราฟิก การเรนเดอร์ข้อความ และออบเจกต์พื้นฐานสำหรับการวาด.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## ขั้นตอนที่ 1: สร้างภาพบิตแมปและวัตถุกราฟิก 

การสร้าง bitmap จะให้แคนวาสที่คุณสามารถวาดบนมันได้ อ็อบเจกต์ `Graphics` คือพื้นผิวการวาด และเราจะเปิดใช้งานการเรนเดอร์ข้อความคุณภาพสูงด้วย `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## ขั้นตอนที่ 2: กำหนด **รูปแบบข้อความ** และสไตล์ 

ที่นี่เราจะ **set text alignment** โดยกำหนดค่าอ็อบเจกต์ `StringFormat` นอกจากนี้เรายังเตรียมแปรง, ปากกา, และฟอนต์ที่จะใช้เมื่อวาดสตริง.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## ขั้นตอนที่ 3: สร้างและจัดรูปแบบข้อความ – **วิธีการวาดข้อความ** และ **การวาดสี่เหลี่ยมที่มีข้อความ**

เราจะประกอบข้อความ, กำหนดสี่เหลี่ยมที่จะบรรจุข้อความ, แล้ววาดทั้งเส้นขอบสี่เหลี่ยมและสตริงเอง.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### วิธีการจัดการข้อความที่ล้นออกมา

หาก `text` ที่ให้มามากเกินขอบเขตของสี่เหลี่ยม คุณมีสองตัวเลือกทั่วไป:

1. **Resize the rectangle** – เพิ่มค่า `rectangle.Width` หรือ `rectangle.Height`.  
2. **Split the text** – แยกสตริงเป็นบรรทัดที่พอดี แล้วเรียก `DrawString` สำหรับแต่ละบรรทัดพร้อมปรับค่า Y‑coordinates.

## ขั้นตอนที่ 4: บันทึกผลลัพธ์ – **การเพิ่มข้อความลงในภาพ**

สุดท้าย เขียน bitmap ลงดิสก์ ขั้นตอนนี้แสดงการ **add text to image** ในหนึ่งคำสั่ง.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## ปัญหาทั่วไปและแนวทางแก้ไข

| ปัญหา | โซลูชั่น |
|-------|----------|
| **ข้อความเบลอ** | การตั้งค่าได้ `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` แล้ว |
| **ข้อความนี้** | ขนาดที่ต่อเนื่องหรือเพื่อให้สามารถตัดคำโดยวัดขนาดได้ (`Graphics.MeasureString`) |
| **ไม่พบแบบอักษร** | ฟอนต์ฟอนต์ได้ติดตั้งบนเครื่องหรือฝังฟอนต์ส่วนตัวด้วย `PrivateFontCollection`. |
| **สีที่ Intel** | การควบคุมแปรงและปากกาอีกครั้ง; หลักการ `Color.FromKnownColor` ใช้สีที่กำหนดโดยระบบ |

## คำถามที่พบบ่อย

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

**คำถามและคำตอบเพิ่มเติม**

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