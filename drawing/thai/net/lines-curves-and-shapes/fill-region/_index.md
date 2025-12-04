---
title: การเติมขอบเขตใน Aspose. Drawing
linktitle: การเติมขอบเขตใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: เรียนรู้วิธีเติมขอบเขตใน Aspose. Drawing สำหรับ .NET ด้วยบทช่วยสอนทีละขั้นตอนนี้ เสริมทักษะการออกแบบกราฟิกของคุณได้อย่างง่ายดาย
weight: 20
url: /th/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเติมขอบเขตใน Aspose. Drawing

## การแนะนำ

การสร้างกราฟิกที่ดึงดูดสายตามักจะเกี่ยวข้องกับการเติมสี ลวดลาย หรือการไล่ระดับสีให้กับบริเวณต่างๆ Aspose. Drawing สำหรับ .NET มอบเครื่องมืออันทรงพลังเพื่อให้บรรลุเป้าหมายนี้อย่างมีประสิทธิภาพ ในบทช่วยสอนนี้ เราจะเจาะลึกกระบวนการเติมขอบเขตโดยใช้ Aspose. Drawing ซึ่งเป็นไลบรารีอเนกประสงค์ที่ช่วยลดความยุ่งยากในการใช้งานกราฟิกในแอปพลิเคชัน .NET

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  ไลบรารี Aspose. Drawing: ดาวน์โหลดและติดตั้งไลบรารี Aspose. Drawing คุณสามารถค้นหาห้องสมุดและเอกสารประกอบของห้องสมุดได้[ที่นี่](https://reference.aspose.com/drawing/net/).

2. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET เช่น Visual Studio เพื่อรวม Aspose. Drawing เข้ากับโครงการของคุณ

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณ เนมสเปซเหล่านี้ให้การเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับการทำงานกับ Aspose. Drawing

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


ตอนนี้ เรามาแบ่งโค้ดตัวอย่างออกเป็นหลายขั้นตอนเพื่อความเข้าใจที่ชัดเจนและครอบคลุม

## ขั้นตอนที่ 1: สร้างวัตถุบิตแมปและกราฟิก

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

ในขั้นตอนนี้ เราจะเตรียมใช้งานบิตแมปใหม่และออบเจ็กต์กราฟิกเพื่อวาดลงไป

## ขั้นตอนที่ 2: กำหนด GraphicsPath และสร้างภูมิภาค

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

กำหนดเส้นทางกราฟิกโดยการระบุรูปหลายเหลี่ยมด้วยชุดจุด สร้างภูมิภาคโดยใช้เส้นทางนี้

## ขั้นตอนที่ 3: ยกเว้นภูมิภาคด้านใน

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

สร้างเส้นทางกราฟิกอื่นที่แสดงถึงสี่เหลี่ยมด้านใน และแยกออกจากขอบเขตหลัก

## ขั้นตอนที่ 4: เลือกแปรงและเติมพื้นที่

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

เลือกแปรง (ในกรณีนี้คือสีน้ำเงินทึบ) และเติมพื้นที่ที่กำหนดไว้ก่อนหน้าด้วยแปรงที่เลือก

## ขั้นตอนที่ 5: บันทึกภาพที่ได้

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

บันทึกภาพสุดท้ายลงในไดเร็กทอรีที่คุณต้องการ

## บทสรุป

การเติมขอบเขตใน Aspose. Drawing สำหรับ .NET เป็นกระบวนการที่ไม่ซับซ้อน ซึ่งให้ความยืดหยุ่นแก่คุณในการสร้างกราฟิกที่ซับซ้อนและดึงดูดสายตา ทดลองใช้รูปทรง สี และลวดลายต่างๆ เพื่อปลดปล่อยความคิดสร้างสรรค์ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose. Drawing สำหรับโครงการเชิงพาณิชย์ได้หรือไม่

 A1: ได้ Aspose. Drawing สามารถใช้กับทั้งโครงการส่วนตัวและเชิงพาณิชย์ สำหรับรายละเอียดใบอนุญาต โปรดไปที่[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 2: มีการทดลองใช้ฟรีหรือไม่?

 A2: ได้ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะได้รับการสนับสนุนสำหรับ Aspose. Drawing ได้อย่างไร

 A3: เยี่ยมชม[Aspose.กระดานสนทนาการวาดภาพ](https://forum.aspose.com/c/drawing/44) เพื่อรับความช่วยเหลือจากชุมชนและผู้เชี่ยวชาญ

### คำถามที่ 4: ฉันสามารถสร้างภาพไดนามิกโดยใช้ Aspose. Drawing ได้หรือไม่

A4: แน่นอน. Aspose. Drawing ช่วยให้คุณสามารถสร้างและจัดการรูปภาพในแอปพลิเคชัน .NET ของคุณได้แบบไดนามิก

### คำถามที่ 5: มีใบอนุญาตชั่วคราวหรือไม่

 A5: ได้ สามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
