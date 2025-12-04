---
title: หน่วยวัดใน Aspose. Drawing สำหรับ .NET
linktitle: หน่วยวัดใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: สำรวจความเก่งกาจของ Aspose. Drawing สำหรับ .NET ในบทช่วยสอนเชิงลึกนี้ ซึ่งเป็นการเรียนรู้หน่วยวัดสำหรับกราฟิกที่มีความแม่นยำ
weight: 14
url: /th/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# หน่วยวัดใน Aspose. Drawing สำหรับ .NET

## การแนะนำ

ยินดีต้อนรับสู่โลกของ Aspose. Drawing สำหรับ .NET ที่ซึ่งความแม่นยำและความยืดหยุ่นมาบรรจบกันในการจัดการกราฟิก ในบทช่วยสอนนี้ เราจะเจาะลึกความซับซ้อนของหน่วยวัดภายใน Aspose. Drawing โดยให้คำแนะนำทีละขั้นตอนเพื่อควบคุมพลังของไลบรารีที่น่าทึ่งนี้

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose. Drawing สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/drawing/net/).

- ไดเร็กทอรีเอกสาร: มีไดเร็กทอรีที่กำหนดซึ่งคุณต้องการบันทึกเอกสารที่คุณสร้างขึ้น

- ความรู้พื้นฐาน C#: แนะนำให้มีความเข้าใจพื้นฐานเกี่ยวกับ C# เพื่อใช้ประโยชน์สูงสุดจากคู่มือนี้

## นำเข้าเนมสเปซ

ก่อนที่เราจะเริ่ม เรามานำเข้าเนมสเปซที่จำเป็นเพื่อใช้ Aspose. Drawing อย่างมีประสิทธิภาพก่อน:

```csharp
using System.Drawing;
```

ตอนนี้ เราจะแบ่งแต่ละตัวอย่างออกเป็นหลายขั้นตอน:

## แต้มเป็นหน่วยวัด

1. สร้างบิตแมป: เริ่มต้นบิตแมปด้วยความกว้างและความสูงที่ระบุ

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. สร้างกราฟิก: สร้างวัตถุกราฟิกจากบิตแมปเพื่อวาดลงไป

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. ตั้งค่าหน่วยของหน้าเป็นจุด: กำหนดจุดเป็นหน่วยวัด (1 จุด = 1/72 นิ้ว)

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. วาดสี่เหลี่ยมผืนผ้า: วาดรูปสี่เหลี่ยมผืนผ้าโดยใช้จุดเป็นหน่วย

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## มิลลิเมตรเป็นหน่วยวัด

1. ตั้งค่าหน่วยของหน้าเป็นมิลลิเมตร: เปลี่ยนหน่วยวัดเป็นมิลลิเมตร (1 มม. = 1/25.4 นิ้ว)

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. วาดรูปสี่เหลี่ยมผืนผ้าเป็นมิลลิเมตร: วาดรูปสี่เหลี่ยมผืนผ้าอื่นโดยใช้หน่วยมิลลิเมตรเป็นหน่วย

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## นิ้วเป็นหน่วยวัด

1. ตั้งค่าหน่วยของหน้าเป็นนิ้ว: สลับหน่วยวัดเป็นนิ้ว

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. วาดรูปสี่เหลี่ยมผืนผ้าเป็นนิ้ว: วาดรูปสี่เหลี่ยมผืนผ้าโดยใช้นิ้วเป็นหน่วย

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## บันทึกผลลัพธ์

หลังจากเสร็จสิ้นตัวอย่างแล้ว ให้บันทึกรูปภาพผลลัพธ์ลงในไดเร็กทอรีเอกสารของคุณ:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

ตอนนี้ คุณได้สำรวจหน่วยวัดต่างๆ ใน Aspose. Drawing สำหรับ .NET สำเร็จแล้ว โดยสร้างการแสดงรูปสี่เหลี่ยมผืนผ้าโดยใช้จุด มิลลิเมตร และนิ้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจว่า Aspose. Drawing สำหรับ .NET จัดการกับหน่วยวัดต่างๆ อย่างไร ด้วยการปรับเปลี่ยนจุด มิลลิเมตร และนิ้ว คุณจะได้รับความแม่นยำและความสามารถในการปรับเปลี่ยนในการสร้างสรรค์กราฟิกของคุณ ทดลองใช้แนวคิดเหล่านี้เพื่อปลดล็อกศักยภาพสูงสุดของ Aspose. Drawing

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose. Drawing สำหรับ .NET กับเฟรมเวิร์ก .NET อื่นๆ ได้หรือไม่

ตอบ 1: ใช่ Aspose. Drawing เข้ากันได้กับเฟรมเวิร์ก .NET ต่างๆ ซึ่งให้ความยืดหยุ่นในสภาพแวดล้อมการพัฒนาของคุณ

### คำถามที่ 2: มีการทดลองใช้ฟรีหรือไม่?

 A2: ได้ คุณสามารถสำรวจ Aspose ได้ วาดภาพพร้อมทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose. Drawing สำหรับ .NET ได้อย่างไร

 A3: เยี่ยมชม[Aspose. ฟอรั่มการวาดภาพ](https://forum.aspose.com/c/drawing/44) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 4: ฉันสามารถซื้อใบอนุญาตชั่วคราวสำหรับโครงการระยะสั้นได้หรือไม่

 A4: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose. Drawing ได้ที่ไหน

 A5: มีเอกสารประกอบที่ครอบคลุม[ที่นี่](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
