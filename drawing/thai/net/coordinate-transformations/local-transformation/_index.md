---
date: 2026-01-27
description: เรียนรู้วิธีการหมุนวงรีและแปลงกราฟิกเป็น PNG ด้วย Aspose.Drawing สำหรับ
  .NET คู่มือแบบขั้นตอนพร้อมตัวอย่างโค้ด
linktitle: Local Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 'วิธีการหมุนวงรี: การแปลงเชิงท้องถิ่นใน Aspose.Drawing สำหรับ .NET'
url: /th/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการหมุนวงรี: การแปลงแบบท้องถิ่นใน Aspose.Drawing สำหรับ .NET

## บทนำ

หากคุณต้องการ **rotate an ellipse** ในแอปพลิเคชัน .NET, Aspose.Drawing มีวิธีที่ง่ายและเชื่อถือได้สำหรับทำเช่นนั้น ในบทแนะนำนี้คุณจะได้เรียนรู้ **how to rotate ellipse** ด้วยการใช้เมทริกซ์การแปลง, แสดงผลลัพธ์, และสุดท้าย **convert graphics to PNG** เพื่อจัดเก็บหรือประมวลผลต่อไป เมื่อเสร็จสิ้นคุณจะมีรูปแบบที่นำกลับมาใช้ใหม่ได้สำหรับสถานการณ์การแปลงแบบท้องถิ่นใด ๆ

## คำตอบสั้น ๆ
- **การแปลงแบบท้องถิ่นคืออะไร?** เป็นการดำเนินการแบบเมทริกซ์ (rotate, scale, translate, skew) ที่ใช้กับองค์ประกอบการวาดเฉพาะโดยไม่กระทบต่อแคนวาสทั้งหมด  
- **ไลบรารีใดสนับสนุนใน .NET?** Aspose.Drawing for .NET มี API ครบชุดที่ทำงานบน .NET เวอร์ชันทั้งหมดที่รองรับ  
- **ฉันสามารถบันทึกผลลัพธ์เป็น PNG ได้หรือไม่?** ได้ — เพียงเรียก `Bitmap.Save` พร้อมชื่อไฟล์ “.png” แล้ว Aspose.Drawing จะจัดการการแปลงให้  
- **ต้องใช้ลิขสิทธิ์สำหรับการพัฒนาหรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบ; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **ใช้เวลานานเท่าไหร่ในการทำตาม?** ประมาณ 10‑15 นาทีสำหรับตัวอย่างพื้นฐาน

## วิธีการหมุนวงรีด้วย Aspose.Drawing
การหมุนวงรีโดยพื้นฐานคือ **การหมุนรูปทรงโดยใช้เมทริกซ์** คุณจะสร้าง `Matrix`, ตั้งค่ามุมการหมุน, ระบุจุดศูนย์กลางของวงรี, แล้วนำเมทริกซ์นั้นไปใช้กับ `GraphicsPath` ซึ่งทำให้การหมุนจำกัดอยู่ที่วงรีเท่านั้น ส่วนแคนวาสส่วนอื่นคงเดิม

## “การนำการแปลงไปใช้” ในการเขียนโปรแกรมกราฟิกคืออะไร?
การนำการแปลงไปใช้หมายถึงการปรับระบบพิกัดของอ็อบเจ็กต์การวาดโดยใช้ **Matrix** เมทริกซ์กำหนดว่าจุดต่าง ๆ จะถูกหมุน, ยืด, หรือย้ายอย่างไร ทำให้คุณสร้างเอฟเฟกต์ภาพที่ซับซ้อนได้ด้วยโค้ดเพียงเล็กน้อย

## ทำไมต้องใช้ Aspose.Drawing เพื่อ **convert graphics to PNG**?
- **ข้ามแพลตฟอร์ม**: ทำงานบน .NET Framework, .NET Core, และ .NET 5/6+  
- **ไม่มีการพึ่งพา GDI+**: หลีกเลี่ยงข้อจำกัดของ `System.Drawing.Common` บนแพลตฟอร์มที่ไม่ใช่ Windows  
- **การเรนเดอร์คุณภาพสูง**: รองรับ Anti‑aliasing และผลลัพธ์พิกเซลที่สมบูรณ์สำหรับไฟล์ PNG  
- **API ครบถ้วน**: รองรับ Paths, Pens, Brushes, และเมทริกซ์การแปลงอย่างเต็มที่

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอน, ตรวจสอบว่าคุณมี:

1. **Aspose.Drawing for .NET** – ดาวน์โหลดและติดตั้งจาก [download link](https://releases.aspose.com/drawing/net/)  
2. โฟลเดอร์บนเครื่องของคุณที่ใช้เก็บภาพผลลัพธ์ (เช่น `C:\MyImages\`)  
3. ความคุ้นเคยพื้นฐานกับ C# และการตั้งค่าโปรเจกต์ .NET  

## นำเข้า Namespaces

แรกสุดให้เพิ่ม Namespaces ที่จำเป็นลงในไฟล์ C# ของคุณ:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Namespaces เหล่านี้ทำให้คุณเข้าถึงคลาส `Bitmap`, `Graphics`, `GraphicsPath`, และ `Matrix` ที่จำเป็นสำหรับกระบวนการแปลง

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: สร้าง Bitmap

เราเริ่มด้วยแคนวาสเปล่า ขนาดและรูปแบบพิกเซลถูกเลือกเพื่อให้ได้ภาพคุณภาพสูง 32‑bit ที่รองรับการโปร่งใส (alpha)

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **เคล็ดลับ:** การใช้ `Format32bppPArgb` ทำให้ภาพคงค่า premultiplied alpha ซึ่งเหมาะสำหรับการส่งออกเป็น PNG

### ขั้นตอนที่ 2: สร้าง Graphics Object

อ็อบเจ็กต์ `Graphics` ให้เมธอดการวาดที่ทำงานบน bitmap เราจะล้างพื้นหลังเป็นสีเทากลางเพื่อให้รูปทรงที่แปลงโดดเด่น

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### ขั้นตอนที่ 3: สร้าง GraphicsPath

`GraphicsPath` ช่วยให้คุณกำหนดรูปทรงซับซ้อนได้ ที่นี่เราจะเพิ่มวงรีที่ตำแหน่ง (300, 300) มีความกว้าง 400 และความสูง 200

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### ขั้นตอนที่ 4: นำการแปลงแบบท้องถิ่นไปใช้ (rotate shape using matrix)

ตอนนี้เราตอบคำถามหลัก: **how to rotate ellipse** เราจะสร้าง `Matrix`, หมุน 45° รอบศูนย์กลางของวงรี (500, 400) แล้วนำเมทริกซ์ไปใช้กับ path

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **ทำไมต้องหมุนที่จุดศูนย์กลาง?** การหมุนรอบศูนย์กลางของรูปทรงจะป้องกันไม่ให้รูปทรงโคจรรอบจุดกำเนิด ทำให้ดูเป็นธรรมชาติ

### ขั้นตอนที่ 5: วาด Path ที่แปลงแล้ว

เมื่อมีการแปลงอยู่แล้ว เราจะเรนเดอร์ path ด้วยปากกาสีฟ้า ความหนา 2

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### ขั้นตอนที่ 6: บันทึกภาพที่แปลงแล้ว (convert graphics to PNG)

สุดท้ายเราจะบันทึก bitmap เป็นไฟล์ PNG เส้นทางจะรวมไดเรกทอรีที่คุณเลือกกับโฟลเดอร์ย่อยสำหรับตัวอย่างการแปลง

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **หมายเหตุ:** บรรทัดนี้ยังแสดงวิธี **save bitmap as PNG** อีกด้วย ส่วนขยาย `.png` จะเรียกใช้ตัวเข้ารหัส PNG ของ Aspose.Drawing โดยอัตโนมัติ ตอบสนองความต้องการ **convert graphics to PNG** ของคุณ

## ปัญหาที่พบบ่อยและวิธีแก้

| Issue | Cause | Fix |
|-------|-------|-----|
| **Blank output image** | Graphics not cleared or pen color matches background | Call `graphics.Clear` with a contrasting color and ensure the pen color is visible. |
| **Distorted rotation** | Using `Rotate` instead of `RotateAt` | Use `RotateAt` and specify the centre point of the shape. |
| **File not saved** | Invalid directory path or missing write permissions | Verify the directory exists and the application has write access. |
| **PNG appears fuzzy** | Low DPI setting on the bitmap | Create the bitmap with a higher resolution or set `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## คำถามที่พบบ่อย

**Q:** ฉันสามารถเชื่อมต่อการแปลงหลายอย่าง (เช่น scale แล้ว rotate) ได้หรือไม่?  
**A:** ได้. สร้าง `Matrix` เดียวแล้วเรียกเมธอดเช่น `Scale`, `RotateAt`, และ `Translate` ตามลำดับที่ต้องการ, จากนั้นใช้ `path.Transform(matrix);`.

**Q:** Aspose.Drawing เหมาะกับการเรนเดอร์ประสิทธิภาพสูงหรือไม่?  
**A:** แน่นอน. ไลบรารีนี้ถูกปรับให้ทำงานเร็วและคุณภาพสูง, และหลีกเลี่ยงข้อจำกัดของ GDI+ บนแพลตฟอร์มที่ไม่ใช่ Windows.

**Q:** มีประเภทการแปลงอื่น ๆ ที่รองรับบ้าง?  
**A:** นอกจากการหมุนแล้ว คุณยังสามารถทำ translation, scaling, และ skewing ได้ด้วยคลาส `Matrix` เดียวกัน.

**Q:** ฉันควรจัดการกับข้อยกเว้นระหว่างกระบวนการแปลงอย่างไร?  
**A:** ห่อโค้ดการวาดด้วยบล็อก `try‑catch` แล้วตรวจสอบข้อยกเว้นจาก `System.Drawing.Drawing2D`. ดูรายละเอียดเพิ่มเติมใน [Aspose.Drawing documentation](https://reference.aspose.com/drawing/net/) สำหรับแนวทางการจัดการข้อผิดพลาด

**Q:** สามารถทดลองใช้ Aspose.Drawing ก่อนซื้อได้หรือไม่?  
**A:** ได้, มีรุ่นทดลองเต็มรูปแบบให้ดาวน์โหลดผ่านลิงก์ [free trial](https://releases.aspose.com/)

## สรุป

โดยทำตามคู่มือนี้ คุณจะรู้ **how to rotate ellipse** ด้วย Aspose.Drawing สำหรับ .NET และวิธี **convert graphics to PNG** เพื่อจัดเก็บอย่างถาวร รูปแบบเดียวกันนี้สามารถนำไปใช้กับการสเกล, การแปล, หรือการบิดเบือนรูปทรงใด ๆ ได้, ช่วยให้คุณสร้างคอมโพเนนต์ภาพที่อินเทอร์แอคทีฟและสวยงามในแอปพลิเคชันของคุณ

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-27  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

---