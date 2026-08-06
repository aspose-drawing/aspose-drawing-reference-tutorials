---
date: 2026-05-29
description: เรียนรู้วิธีบันทึก PNG และวาด cardinal splines ใน .NET ด้วย Aspose.Drawing.
  บันทึกเส้นโค้งเป็น PNG, สร้างกราฟิกที่เรียบเนียน, และสร้าง bitmap ไปยังไฟล์อย่างง่ายดาย.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: การวาด Cardinal Splines ใน Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: วิธีบันทึก PNG และวาด Cardinal Splines ด้วย Aspose.Drawing
url: /th/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีบันทึก PNG และวาด Cardinal Splines ด้วย Aspose.Drawing

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีบันทึก PNG** ขณะวาด Cardinal spline ที่เรียบเนียนโดยใช้ Aspose.Drawing สำหรับ .NET ไม่ว่าคุณจะกำลังสร้างคอมโพเนนต์แผนภูมิ, ตัวแก้ไขไดอะแกรม, หรือเพียงต้องการส่งออกโค้งแบบกำหนดเองเป็น PNG ขั้นตอนต่อไปนี้จะพาคุณผ่านการสร้าง bitmap canvas, การวาด spline ด้วยปากกา, และการบันทึกผลลัพธ์ลงดิสก์ คุณยังจะเห็นว่าทำไม Aspose.Drawing จึงเป็นทางเลือกข้ามแพลตฟอร์มที่เชื่อถือได้แทน System.Drawing.Common

## คำตอบสั้น
- **วิธีการหลักทำอะไร?** `Graphics.DrawCurve` interpolates a series of points into a smooth cardinal spline.  
- **รูปแบบใดที่ใช้บันทึกรูปภาพ?** PNG via `Bitmap.Save`.  
- **ฉันต้องมีลิขสิทธิ์เพื่อบันทึกรูปภาพหรือไม่?** A trial works for development; a commercial license is required for production.  
- **ฉันสามารถเปลี่ยนความตึงของเส้นโค้งได้หรือไม่?** Yes, overloads of `DrawCurve` let you specify tension.  
- **Aspose.Drawing รองรับ .NET 6+ หรือไม่?** Absolutely – it supports .NET Framework and .NET Core/5/6.

## “วิธีบันทึก PNG” คืออะไรในบริบทของ Aspose.Drawing?

การบันทึก PNG หมายถึงการแปลง bitmap ที่อยู่ในหน่วยความจำซึ่งคุณวาดอยู่ให้เป็นไฟล์ PNG จริงบนดิสก์ กระบวนการจะเขียนข้อมูลพิกเซลโดยใช้การบีบอัดแบบไม่มีการสูญเสีย, รักษาสีที่แม่นยำและข้อมูลช่องสีอัลฟ่าใด ๆ วิธี `Bitmap.Save` ของ Aspose.Drawing จะจัดการการเข้ารหัส PNG โดยอัตโนมัติ, ดังนั้นคุณไม่จำเป็นต้องจัดการรายละเอียดรูปแบบด้วยตนเอง.

## ทำไมต้องวาด cardinal spline ด้วย Aspose.Drawing?

Cardinal spline สร้างเส้นโค้งที่เรียบและไหลลื่นซึ่งตามจุดควบคุมอย่างใกล้ชิด ทำให้เหมาะอย่างยิ่งสำหรับการแสดงผลข้อมูล, กราฟิก UI, และรูปร่างที่กำหนดเอง Aspose.Drawing รองรับ **30+ รูปแบบภาพ** และสามารถเรนเดอร์กราฟิกหลายร้อยหน้าโดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ, ให้คุณได้ทั้งความเร็วและความยืดหยุ่น.

## ข้อกำหนดเบื้องต้น

- Visual Studio (เวอร์ชันล่าสุดใดก็ได้) ติดตั้งแล้ว.  
- Aspose.Drawing for .NET library. คุณสามารถดาวน์โหลดได้ [here](https://releases.aspose.com/drawing/net/).  
- ความรู้พื้นฐานการเขียนโปรแกรม C#.

## นำเข้า Namespace

ในไฟล์ C# ของคุณ, เริ่มต้นโดยนำเข้า namespace ที่จำเป็น:

Namespace `Aspose.Drawing` มีประเภทหลักทั้งหมดเช่น `Bitmap`, `Graphics`, และ `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## ขั้นตอนที่ 1: สร้าง Bitmap (Canvas)

ขั้นแรก, สร้าง bitmap ที่จะทำหน้าที่เป็น canvas สำหรับการวาดของคุณ Bitmap นี้คือที่ที่ spline จะถูกเรนเดอร์ก่อนที่คุณจะ **บันทึกรูปภาพ**.

Bitmap แสดงถึงภาพในหน่วยความจำที่มีรูปแบบพิกเซลและขนาดที่กำหนด.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## ขั้นตอนที่ 2: สร้าง Graphics Object

ต่อไป, รับอ็อบเจ็กต์ `Graphics` จาก bitmap. อ็อบเจ็กต์นี้ให้พื้นผิวสำหรับการวาด.

Graphics ให้พื้นผิวการวาดสำหรับการเรนเดอร์รูปทรง, ข้อความ, และภาพลงบน bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## ขั้นตอนที่ 3: กำหนด Pen และวาด Curve

กำหนด `Pen` ด้วยสีและความกว้างที่ต้องการ, แล้ววาด cardinal spline โดยใช้ `DrawCurve`. นี้เป็นการสาธิตเทคนิค **draw curve with pen** และทำหน้าที่เป็น **cardinal spline example**.

Pen รวมสี, ความกว้าง, และสไตล์เส้นที่ใช้สำหรับการวาดเส้นและโค้ง.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## ขั้นตอนที่ 4: บันทึกรูปภาพ (บันทึก Curve เป็น PNG)

สุดท้าย, บันทึก bitmap ลงไฟล์ PNG. นี้คือหัวใจของ **วิธีบันทึก PNG** ในบทแนะนำนี้.

`Bitmap.Save` เขียนภาพลงไฟล์ในรูปแบบที่ระบุ, เช่น PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **เคล็ดลับ:** ใช้ `Path.Combine` เพื่อสร้างเส้นทางไฟล์อย่างปลอดภัยบนหลายแพลตฟอร์ม.

ยินดีด้วย! คุณได้วาด cardinal spline สำเร็จและบันทึกผลลัพธ์เป็นภาพ PNG ด้วย Aspose.Drawing สำหรับ .NET เรียบร้อยแล้ว คุณสามารถทดลองเปลี่ยนแปลงอาร์เรย์จุด, สีของ pen, หรือความกว้างของเส้นเพื่อปรับแต่งโค้งของคุณได้ตามต้องการ.

## กรณีการใช้งานทั่วไป

- **การแสดงผลข้อมูล** – แผนภูมิเส้นเรียบที่ต้องการจุดควบคุมที่แม่นยำ.  
- **คอมโพเนนต์ UI ที่กำหนดเอง** – วาดปุ่มหมุน, สไลเดอร์, หรือกรอบตกแต่ง.  
- **กราฟิกที่สามารถส่งออกได้** – สร้างทรัพยากร PNG แบบเรียลไทม์สำหรับรายงานหรือเนื้อหาเว็บ.

## การแก้ไขปัญหาและเคล็ดลับ

- **รูปภาพเป็นสีขาว?** ตรวจสอบว่า bitmap มีรูปแบบพิกเซลที่รองรับอัลฟ่า (`Format32bppPArgb`) และเรียก `graphics.Clear(Color.Transparent)` หากจำเป็น.  
- **รูปทรงโค้งไม่คาดคิด?** ปรับพารามิเตอร์ความตึงโดยใช้ overload `DrawCurve(pen, points, tension)`.  
- **ข้อผิดพลาดการเข้าถึงไฟล์?** ตรวจสอบว่าไดเรกทอรีเป้าหมายมีอยู่และแอปพลิเคชันของคุณมีสิทธิ์เขียน.

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้ Aspose.Drawing สำหรับโครงการเชิงพาณิชย์ได้หรือไม่?**  
A1: ใช่, Aspose.Drawing เหมาะสำหรับโครงการส่วนบุคคลและเชิงพาณิชย์ ตรวจสอบรายละเอียดลิขสิทธิ์ได้ที่ [purchase page](https://purchase.aspose.com/buy).

**Q2: ฉันจะได้รับลิขสิทธิ์ชั่วคราวสำหรับการทดสอบได้อย่างไร?**  
A2: รับลิขสิทธิ์ชั่วคราวสำหรับการทดสอบได้จาก [here](https://purchase.aspose.com/temporary-license/).

**Q3: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมได้จากที่ไหน?**  
A3: เยี่ยมชม [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

**Q4: มีรุ่นทดลองฟรีหรือไม่?**  
A4: มี, ลองสำรวจคุณสมบัติต่าง ๆ ด้วยเวอร์ชัน [free trial](https://releases.aspose.com/) ก่อนทำการซื้อ.

**Q5: ฉันจะเข้าถึงเอกสารได้อย่างไร?**  
A5: ดูที่ [documentation](https://reference.aspose.com/drawing/net/) อย่างครบถ้วนสำหรับข้อมูลและตัวอย่างโดยละเอียด.

---

**อัปเดตล่าสุด:** 2026-05-29  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
