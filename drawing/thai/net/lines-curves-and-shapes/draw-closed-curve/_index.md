---
title: การวาดเส้นโค้งปิดใน Aspose. Drawing
linktitle: การวาดเส้นโค้งปิดใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: สำรวจศิลปะของการวาดเส้นโค้งแบบปิดในแอปพลิเคชัน .NET ด้วย Aspose. Drawing ยกระดับภาพของคุณได้อย่างง่ายดาย
weight: 14
url: /th/net/lines-curves-and-shapes/draw-closed-curve/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การวาดเส้นโค้งปิดใน Aspose. Drawing

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำที่ครอบคลุมของเราเกี่ยวกับการวาดเส้นโค้งแบบปิดใน Aspose. Drawing สำหรับ .NET! หากคุณกำลังมองหาการปรับปรุงแอปพลิเคชัน .NET ของคุณด้วยเส้นโค้งปิดที่ชัดเจนและแม่นยำ คุณมาถูกที่แล้ว ในบทช่วยสอนนี้ เราจะสำรวจกระบวนการทีละขั้นตอน เพื่อให้แน่ใจว่าคุณมีความเข้าใจที่ชัดเจนเกี่ยวกับไลบรารี Aspose. Drawing และความสามารถของไลบรารี

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะดำดิ่งสู่โลกที่น่าตื่นเต้นของการวาดเส้นโค้งปิด ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  ไลบรารี Aspose. Drawing: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose. Drawing สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/drawing/net/).

2. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้บนเครื่องของคุณ

ตอนนี้เรามีข้อมูลสำคัญที่ครอบคลุมแล้ว เรามาเริ่มใช้งานจริงกันดีกว่า

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณ เนมสเปซเหล่านี้ให้การเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับการวาดเส้นโค้งแบบปิด

```csharp
using System.Drawing;
```

## ขั้นตอนที่ 1: สร้างวัตถุบิตแมปและกราฟิก

 ขั้นตอนแรกคือการสร้าง`Bitmap` วัตถุซึ่งเป็นตัวแทนของพื้นผิวการวาดภาพและ`Graphics` วัตถุช่วยให้คุณสามารถวาดบนบิตแมป

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## ขั้นตอนที่ 2: กำหนดปากกาและวาดเส้นโค้งปิด

 ต่อไป ให้นิยาม ก`Pen` วัตถุที่มีสีและความหนาที่คุณต้องการ จากนั้นใช้`DrawClosedCurve` วิธีการวาดเส้นโค้งปิดบนบิตแมป

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawClosedCurve(pen, new Point[] { new Point(100, 700), new Point(350, 600), new Point(500, 500), new Point(650, 600), new Point(900, 700) });
```

## ขั้นตอนที่ 3: บันทึกภาพที่ส่งออก

หลังจากวาดเส้นโค้งปิดแล้ว ให้บันทึกภาพที่ได้ลงในไดเร็กทอรีที่คุณต้องการ

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawClosedCurve_out.png");
```

ยินดีด้วย! คุณวาดเส้นโค้งปิดได้สำเร็จโดยใช้ Aspose. Drawing สำหรับ .NET

## บทสรุป

ในบทช่วยสอนนี้ เราได้อธิบายขั้นตอนการวาดเส้นโค้งแบบปิดใน Aspose. Drawing สำหรับ .NET แล้ว ด้วยขั้นตอนง่ายๆ เพียงไม่กี่ขั้นตอน คุณก็สามารถยกระดับรูปลักษณ์ที่ดึงดูดใจให้กับแอปพลิเคชัน .NET ของคุณได้

 หากคุณมีคำถามหรือพบปัญหา คุณสามารถขอความช่วยเหลือได้ที่[Aspose. ฟอรั่มการวาดภาพ](https://forum.aspose.com/c/diagram/17).

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose. Drawing สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

 A1: ใช่ Aspose. Drawing เหมาะสำหรับการใช้งานส่วนตัวและเชิงพาณิชย์ ตรวจสอบ[หน้าซื้อ](https://purchase.aspose.com/buy) สำหรับรายละเอียดใบอนุญาต

### คำถามที่ 2: มีการทดลองใช้ฟรีหรือไม่?

 A2: แน่นอน! คุณสามารถสำรวจ Aspose การวาดภาพพร้อมทดลองใช้ฟรีโดยไปที่[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A3: สำหรับใบอนุญาตชั่วคราว โปรดไปที่[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).

### Q4: ฉันจะหาเอกสารโดยละเอียดได้จากที่ไหน?

 A4: มีเอกสารประกอบที่ครอบคลุม[ที่นี่](https://reference.aspose.com/drawing/net/).

### คำถามที่ 5: มีตัวเลือกการสนับสนุนอะไรบ้าง?

 A5: หากคุณต้องการความช่วยเหลือหรือมีคำถาม โปรดไปที่[Aspose. ฟอรั่มการวาดภาพ](https://forum.aspose.com/c/diagram/17).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
