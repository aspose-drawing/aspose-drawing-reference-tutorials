---
title: การวาดเส้นทางใน Aspose. Drawing
linktitle: การวาดเส้นทางใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: เรียนรู้การวาดเส้นทางใน Aspose. Drawing สำหรับ .NET พร้อมคำแนะนำทีละขั้นตอนนี้ สร้างกราฟิกที่น่าทึ่งได้อย่างง่ายดาย
weight: 17
url: /th/net/lines-curves-and-shapes/draw-path/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การวาดเส้นทางใน Aspose. Drawing

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำที่ครอบคลุมของเราเกี่ยวกับการวาดเส้นทางใน Aspose. Drawing สำหรับ .NET ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเป็นมือใหม่ในการเขียนโปรแกรมกราฟิก บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการสร้างเส้นทางที่ซับซ้อนโดยใช้ Aspose. Drawing Aspose. Drawing เป็นไลบรารีอันทรงพลังที่ทำให้การทำงานกราฟิกในแอปพลิเคชัน .NET ง่ายขึ้น โดยมีฟังก์ชันการทำงานที่หลากหลายสำหรับการสร้าง แก้ไข และจัดการรูปภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose. Drawing: ดาวน์โหลดและติดตั้งไลบรารี Aspose. Drawing คุณสามารถค้นหาห้องสมุด[ที่นี่](https://releases.aspose.com/drawing/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ของคุณด้วยเครื่องมือที่จำเป็น

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นในโปรเจ็กต์ของคุณ:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## ขั้นตอนที่ 1: สร้างบิตแมปและกราฟิก

เริ่มต้นด้วยการสร้างบิตแมปและออบเจ็กต์กราฟิกเพื่อใช้งาน:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## ขั้นตอนที่ 2: กำหนดปากกาและ GraphicsPath

ถัดไป กำหนดปากกาเพื่อระบุคุณลักษณะการวาดและ GraphicsPath เพื่อแสดงเส้นทาง:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## ขั้นตอนที่ 3: เพิ่มเส้นและรูปร่าง

เพิ่มเส้น สี่เหลี่ยม และวงรีให้กับ GraphicsPath เพื่อสร้างเส้นทางที่ซับซ้อน:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## ขั้นตอนที่ 4: วาดเส้นทาง

วาดเส้นทางไปยังวัตถุกราฟิกโดยใช้ปากกาที่ระบุ:

```csharp
graphics.DrawPath(pen, path);
```

## ขั้นตอนที่ 5: บันทึกรูปภาพ

สุดท้าย บันทึกรูปภาพที่สร้างขึ้นไปยังไดเร็กทอรีที่คุณต้องการ:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

ทำซ้ำขั้นตอนเหล่านี้ตามความจำเป็นเพื่อสร้างเส้นทางที่ซับซ้อนและดึงดูดสายตา

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีการวาดเส้นทางโดยใช้ Aspose. Drawing สำหรับ .NET เรียบร้อยแล้ว บทช่วยสอนนี้ครอบคลุมพื้นฐานของการสร้างบิตแมป การกำหนดปากกา การสร้าง GraphicsPath และการวาดรูปทรงต่างๆ ทดลองใช้พารามิเตอร์และรูปร่างต่างๆ เพื่อปลดปล่อยศักยภาพสูงสุดของ Aspose. Drawing

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose. Drawing กับไลบรารี .NET อื่นได้หรือไม่

คำตอบ 1: ใช่ Aspose. Drawing ผสานรวมกับไลบรารี .NET อื่นๆ ได้อย่างราบรื่น ให้ความคล่องตัวในโครงการพัฒนาของคุณ

### คำถามที่ 2: มีเวอร์ชันทดลองใช้งานหรือไม่

 A2: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose. Drawing ได้ที่ไหน

 A3: เยี่ยมชม Aspose. Drawing[ฟอรั่ม](https://forum.aspose.com/c/drawing/44) เพื่อช่วยเหลือและสนับสนุนชุมชน

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A4: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันสามารถซื้อ Aspose. Drawing ได้หรือไม่

 A5: ใช่ คุณสามารถซื้อ Aspose. Drawing ได้[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
