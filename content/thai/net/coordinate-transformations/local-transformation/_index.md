---
title: การเปลี่ยนแปลงท้องถิ่นใน Aspose. Drawing สำหรับ .NET
linktitle: การเปลี่ยนแปลงท้องถิ่นใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: สำรวจการเปลี่ยนแปลงเฉพาะที่ใน Aspose. Drawing สำหรับ .NET ยกระดับกราฟิกด้วยขั้นตอนที่ปฏิบัติตามได้ง่าย
type: docs
weight: 11
url: /th/net/coordinate-transformations/local-transformation/
---
## การแนะนำ

คุณกำลังมองหาการยกระดับกราฟิกของแอปพลิเคชัน .NET ของคุณด้วยการแปลงภายในขั้นสูงหรือไม่? Aspose. Drawing for .NET ช่วยให้นักพัฒนาสามารถสร้างภาพที่น่าทึ่งด้วยการผสมผสานการเปลี่ยนแปลงในท้องถิ่นได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะเจาะลึกเข้าไปในโลกแห่งการเปลี่ยนแปลงในท้องถิ่นโดยใช้ Aspose. Drawing ซึ่งจะแนะนำคุณผ่านแต่ละขั้นตอนเพื่อปลดล็อกศักยภาพสูงสุดของไลบรารีอันทรงพลังนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose. Drawing สำหรับ .NET: ดาวน์โหลดและติดตั้งไลบรารีจาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/drawing/net/).

2. ไดเร็กทอรีเอกสาร: เลือกไดเร็กทอรีที่เหมาะสมบนเครื่องของคุณที่จะบันทึกภาพที่แปลงแล้ว

3. ความเข้าใจพื้นฐานของการเขียนโปรแกรม .NET: ความคุ้นเคยกับแนวคิดการเขียนโปรแกรม C# และกราฟิกจะเป็นประโยชน์

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## ขั้นตอนที่ 1: สร้างบิตแมป

เริ่มต้นบิตแมปด้วยขนาดเฉพาะและรูปแบบพิกเซล:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## ขั้นตอนที่ 2: สร้างวัตถุกราฟิก

สร้างวัตถุกราฟิกจากบิตแมปเพื่อดำเนินการวาดภาพ:

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## ขั้นตอนที่ 3: สร้าง GraphicsPath

สร้างเส้นทางกราฟิกในตัวอย่างนี้ วงรี และระบุตำแหน่งและขนาด:

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

## ขั้นตอนที่ 4: ใช้การเปลี่ยนแปลงในท้องถิ่น

ตั้งค่าเมทริกซ์การแปลงและใช้การแปลงการหมุนกับเส้นทางที่ระบุ:

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

## ขั้นตอนที่ 5: วาดเส้นทางที่เปลี่ยนไป

กำหนดปากกาและวาดเส้นทางที่แปลงแล้วบนวัตถุกราฟิก:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

## ขั้นตอนที่ 6: บันทึกภาพที่แปลงแล้ว

บันทึกภาพที่แปลงแล้วลงในไดเร็กทอรีเอกสารของคุณ:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับการแปลงต่างๆ และปลดปล่อยศักยภาพของ Aspose. Drawing ในแอปพลิเคชัน .NET ของคุณ

## บทสรุป

การผสมผสานการแปลงท้องถิ่นเข้ากับ Aspose. Drawing สำหรับ .NET จะเปิดขอบเขตความเป็นไปได้ในการปรับปรุงกราฟิกของคุณ ด้วยการทำตามคำแนะนำทีละขั้นตอนนี้ คุณจะได้เรียนรู้วิธีใช้การเปลี่ยนแปลงเฉพาะที่ได้อย่างง่ายดาย โดยนำมิติใหม่มาสู่การแสดงภาพของคุณ


## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้การแปลงหลายรายการตามลำดับได้หรือไม่*

A1: ได้ คุณสามารถโยงการแปลงหลายรายการเข้าด้วยกันได้โดยใช้การแปลงเมทริกซ์อย่างต่อเนื่อง

### คำถามที่ 2: Aspose. Drawing เหมาะสำหรับการใช้งานกราฟิกที่ซับซ้อนหรือไม่*

A2: แน่นอน! Aspose. Drawing ได้รับการออกแบบมาเพื่อรองรับการใช้งานกราฟิกที่หลากหลาย ทำให้เหมาะสำหรับการใช้งานที่ซับซ้อน

### คำถามที่ 3: รองรับการแปลงประเภทอื่นๆ หรือไม่*

A3: นอกจากการหมุนแล้ว Aspose. Drawing ยังรองรับการแปล การปรับขนาด และการเอียงเพื่อความสามารถในการแปลงที่ครอบคลุม

### คำถามที่ 4: ฉันจะจัดการกับข้อยกเว้นในระหว่างกระบวนการเปลี่ยนแปลงได้อย่างไร*

 A4: ตรวจสอบให้แน่ใจว่ามีการจัดการข้อผิดพลาดที่เหมาะสมในโค้ดของคุณและอ้างอิงถึง[Aspose.เอกสารการเขียนแบบ](https://reference.aspose.com/drawing/net/) สำหรับการแก้ไขปัญหา

### คำถามที่ 5: ฉันสามารถลองใช้ Aspose. Drawing ก่อนซื้อได้หรือไม่*

 A5: ใช่ คุณสามารถสำรวจห้องสมุดได้ด้วย[ทดลองฟรี](https://releases.aspose.com/).