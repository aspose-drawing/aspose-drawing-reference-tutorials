---
title: การแปลงหน้าใน Aspose. Drawing สำหรับ .NET
linktitle: การแปลงหน้าใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: เรียนรู้การแปลงหน้าทีละขั้นตอนใน .NET โดยใช้ Aspose. Drawing เสริมทักษะด้านกราฟิกของคุณด้วยบทช่วยสอนที่ครอบคลุมนี้
weight: 13
url: /th/net/coordinate-transformations/page-transformation/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแปลงหน้าใน Aspose. Drawing สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการแปลงหน้าโดยใช้ Aspose. Drawing สำหรับ .NET หากคุณกำลังมองหาเพื่อเพิ่มทักษะในการทำงานกับการแปลงกราฟิกและบิตแมป คุณมาถูกที่แล้ว ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงหน้าโดยใช้ Aspose. Drawing เพื่อให้มั่นใจว่าคุณจะเข้าใจแต่ละขั้นตอนได้ชัดเจน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose. Drawing: ดาวน์โหลดและติดตั้งไลบรารี Aspose. Drawing คุณสามารถค้นหาเวอร์ชันล่าสุดได้[ที่นี่](https://releases.aspose.com/drawing/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาของคุณด้วย Visual Studio หรือเครื่องมือพัฒนา .NET ที่ต้องการอื่นๆ

- ไดเรกทอรีเอกสารของคุณ: แทนที่ "ไดเรกทอรีเอกสารของคุณ" ในโค้ดด้วยไดเรกทอรีจริงที่คุณต้องการบันทึกภาพที่แปลงแล้ว

ตอนนี้เรามีข้อกำหนดเบื้องต้นตามลำดับแล้ว เรามาดำเนินการตามคำแนะนำทีละขั้นตอนกันดีกว่า

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System.Drawing;
```

## ขั้นตอนที่ 1: สร้างบิตแมป

เริ่มต้นด้วยการสร้างบิตแมปใหม่ด้วยขนาดและรูปแบบพิกเซลเฉพาะ:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

นี่เป็นการเริ่มต้นผืนผ้าใบเปล่าสำหรับการแปลงของคุณ

## ขั้นตอนที่ 2: สร้างวัตถุกราฟิก

สร้างวัตถุกราฟิกจากบิตแมปเพื่อวาด:

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## ขั้นตอนที่ 3: ล้างผ้าใบ

ล้างผ้าใบโดยเติมสีเฉพาะ (ในกรณีนี้คือสีเทา):

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## ขั้นตอนที่ 4: ตั้งค่าการเปลี่ยนแปลง

ตั้งค่าการแปลงที่แมปพิกัดหน้ากับพิกัดอุปกรณ์ ในตัวอย่างนี้ เราใช้นิ้ว:

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

## ขั้นตอนที่ 5: วาดรูปสี่เหลี่ยมผืนผ้า

ใช้วัตถุกราฟิกเพื่อวาดรูปสี่เหลี่ยมผืนผ้าด้วยปากกาที่ระบุ:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

## ขั้นตอนที่ 6: บันทึกรูปภาพ

บันทึกภาพที่แปลงแล้วไปยังไดเร็กทอรีที่คุณระบุ:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

ยินดีด้วย! คุณได้แปลงหน้าโดยใช้ Aspose. Drawing สำหรับ .NET สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงขั้นตอนพื้นฐานในการแปลงหน้าโดยใช้ Aspose. Drawing ด้วยการทำตามขั้นตอนเหล่านี้ คุณสามารถรวมการแปลงเหล่านี้เข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose. Drawing ได้ฟรีหรือไม่

 A1: Aspose. Drawing เสนอการทดลองใช้ฟรีที่คุณสามารถเข้าถึงได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 2: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose. Drawing ได้ที่ไหน

 A2: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/drawing/net/).

### คำถามที่ 3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose. Drawing ได้อย่างไร

 A3: สำหรับการสนับสนุน โปรดไปที่[Aspose. ฟอรั่มการวาดภาพ](https://forum.aspose.com/c/diagram/17).

### คำถามที่ 4: Aspose. Drawing มีใบอนุญาตชั่วคราวหรือไม่

 A4: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: Aspose. Drawing หาซื้อได้ที่ไหน

 A5: คุณสามารถซื้อ Aspose. Drawing ได้[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
