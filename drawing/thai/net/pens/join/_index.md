---
title: การรวมเส้นทางด้วยปากกาใน Aspose. Drawing
linktitle: การรวมเส้นทางด้วยปากกาใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: สำรวจศิลปะแห่งการเชื่อมโยงเส้นทางด้วยปากกาใน Aspose. Drawing สำหรับ .NET สร้างกราฟิกที่น่าทึ่งด้วยตัวเลือก LineJoin
weight: 11
url: /th/net/pens/join/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การรวมเส้นทางด้วยปากกาใน Aspose. Drawing

## การแนะนำ

ยินดีต้อนรับสู่โลกของ Aspose. Drawing สำหรับ .NET! ในบทช่วยสอนนี้ เราจะเจาะลึกศิลปะแห่งการเชื่อมโยงเส้นทางด้วยปากกาโดยใช้ Aspose. Drawing ซึ่งเป็นไลบรารีอันทรงพลังที่มีฟังก์ชันการทำงานมากมายสำหรับการทำงานกับกราฟิกและรูปภาพในแอปพลิเคชัน .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะดำดิ่งสู่โลกแห่งการเข้าร่วมเส้นทางที่น่าตื่นเต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1.  ไลบรารี Aspose. Drawing: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose. Drawing สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/drawing/net/).

2. สภาพแวดล้อมการพัฒนา .NET: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้บนเครื่องของคุณ

ตอนนี้เราพร้อมแล้ว มาดูขั้นตอนเพื่อรวมเส้นทางโดยใช้ปากกาใน Aspose. Drawing กัน

## นำเข้าเนมสเปซ

ก่อนที่คุณจะเริ่มเขียนโค้ด ตรวจสอบให้แน่ใจว่าได้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงคลาสและวิธีการที่จำเป็น เพิ่มเนมสเปซต่อไปนี้ที่จุดเริ่มต้นของโค้ดของคุณ:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## ขั้นตอนที่ 1: สร้างวัตถุบิตแมปและกราฟิก

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

 ที่นี่เราเริ่มต้นใหม่`Bitmap` วัตถุที่มีขนาดที่ระบุและสร้าง`Graphics` วัตถุจากบิตแมปนั้น

## ขั้นตอนที่ 2: กำหนดวิธี DrawPath

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

 ในขั้นตอนนี้ เราจะกำหนดวิธีการที่เรียกว่า`DrawPath` นั่นต้องใช้เวลา`Graphics` วัตถุ ก`LineJoin`การแจงนับและตำแหน่งแนวตั้ง (`y` ) เป็นพารามิเตอร์ ภายในวิธีการ เราสร้างไฟล์`Pen` วัตถุที่มีสีและความกว้างที่ระบุ`GraphicsPath` วัตถุและเพิ่มบรรทัดลงไป

## ขั้นตอนที่ 3: เข้าร่วมเส้นทางกับ Bevel LineJoin

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

 โทรหา`DrawPath` วิธีการด้วย`LineJoin.Bevel` เพื่อรวมเส้นทางด้วยการรวมเส้นเอียง

## ขั้นตอนที่ 4: เข้าร่วมเส้นทางด้วย Round LineJoin

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

 ตอนนี้โทรไปที่`DrawPath` วิธีการด้วย`LineJoin.Round` เพื่อเข้าร่วมเส้นทางด้วยการเข้าร่วมเส้นกลม

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

บันทึกภาพที่ได้ลงในไดเร็กทอรีที่คุณต้องการ

ตอนนี้คุณได้สร้างเส้นทางเข้าร่วมโดยใช้ปากกาใน Aspose. Drawing สำเร็จแล้ว! ทดลองใช้รูปแบบการรวมเส้นที่แตกต่างกันและรวมเข้ากับกราฟิกของคุณ

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการรวมเส้นทางด้วยปากกาใน Aspose. Drawing สำหรับ .NET เพียงไม่กี่ขั้นตอน คุณสามารถปรับปรุงกราฟิกของคุณและสร้างการออกแบบที่ดึงดูดสายตาได้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose. Drawing ได้ฟรีหรือไม่

 คำตอบ 1: Aspose. Drawing เป็นผลิตภัณฑ์เชิงพาณิชย์ แต่คุณสามารถสำรวจความสามารถของมันได้ด้วย[ทดลองฟรี](https://releases.aspose.com/).

### คำถามที่ 2: ฉันจะหาเอกสารประกอบ Aspose. Drawing ได้ที่ไหน

 A2: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/drawing/net/) เพื่อรับคำแนะนำอย่างครอบคลุม

### คำถามที่ 3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose. Drawing ได้อย่างไร

 A3: เยี่ยมชม[Aspose.กระดานสนทนาการวาดภาพ](https://forum.aspose.com/c/diagram/17) เพื่อชุมชนและการสนับสนุน

### คำถามที่ 4: Aspose. Drawing มีใบอนุญาตชั่วคราวหรือไม่

 A4: ใช่ คุณสามารถขอรับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) สำหรับการใช้งานระยะสั้น

### คำถามที่ 5: Aspose. Drawing หาซื้อได้ที่ไหน

 A5: ซื้อ Aspose. Drawing[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
