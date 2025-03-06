---
title: การวาดข้อความใน Aspose. Drawing
linktitle: การวาดข้อความใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: ปรับปรุงแอปพลิเคชัน .NET ของคุณด้วยข้อความแบบไดนามิกโดยใช้ Aspose. Drawing สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อวาดข้อความ ปรับแต่งแบบอักษร และสร้างรูปภาพที่ดึงดูดสายตา
weight: 10
url: /th/net/text-and-fonts/draw-text/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การวาดข้อความใน Aspose. Drawing

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนในการวาดข้อความโดยใช้ Aspose. Drawing สำหรับ .NET! หากคุณต้องการปรับปรุงแอปพลิเคชัน .NET ของคุณด้วยข้อความที่สมบูรณ์และสวยงาม คุณมาถูกที่แล้ว ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการสร้างข้อความแบบไดนามิกในรูปภาพโดยใช้ Aspose. Drawing

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose. Drawing สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถดาวน์โหลดได้จาก[Aspose.เอกสารการเขียนแบบ](https://reference.aspose.com/drawing/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET เช่น Visual Studio บนเครื่องของคุณ

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นในโครงการของคุณ:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## ขั้นตอนที่ 1: สร้างวัตถุบิตแมปและกราฟิก

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

ในขั้นตอนนี้ เราสร้างวัตถุบิตแมปที่มีความกว้างและความสูงที่ระบุ ออบเจ็กต์กราฟิกจะเริ่มต้นได้ โดยตั้งค่าการป้องกันนามแฝงเพื่อการแสดงข้อความที่ราบรื่น

## ขั้นตอนที่ 2: ตั้งค่าแปรง ปากกา และแบบอักษร

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

ที่นี่ เรากำหนด SolidBrush สำหรับสีข้อความ ปากกาสำหรับวาดรูปสี่เหลี่ยมผืนผ้ารอบๆ ข้อความ และวัตถุแบบอักษรที่มีรูปแบบแบบอักษรที่ต้องการ

## ขั้นตอนที่ 3: กำหนดข้อความและสี่เหลี่ยมผืนผ้า

```csharp
string text = "Lorem ipsum..."; // (ข้อความที่คุณต้องการ)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

ระบุเนื้อหาข้อความและขนาดสี่เหลี่ยมที่จะวาดข้อความ

## ขั้นตอนที่ 4: วาดรูปสี่เหลี่ยมผืนผ้าและข้อความ

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

ขั้นตอนนี้เกี่ยวข้องกับการวาดรูปสี่เหลี่ยมผืนผ้าโดยใช้ปากกาที่กำหนดไว้ จากนั้นวางข้อความภายในสี่เหลี่ยมผืนผ้าโดยใช้แบบอักษรและแปรงที่ระบุ

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

บันทึกภาพที่ได้ลงในไดเร็กทอรีที่คุณต้องการ แทนที่ "Your Document Directory" ด้วยเส้นทางที่คุณต้องการบันทึกรูปภาพ

ตอนนี้คุณได้สร้างรูปภาพพร้อมข้อความไดนามิกโดยใช้ Aspose. Drawing สำหรับ .NET สำเร็จแล้ว! ทดลองใช้แบบอักษร สี และขนาดต่างๆ เพื่อปรับแต่งข้อความของคุณ

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการวาดข้อความใน Aspose. Drawing สำหรับ .NET ด้วยการใช้ประโยชน์จากคุณสมบัติอันทรงพลังของไลบรารี คุณสามารถรวมข้อความไดนามิกเข้ากับแอปพลิเคชัน .NET ของคุณได้อย่างง่ายดาย ช่วยเพิ่มรูปลักษณ์ที่น่าดึงดูดและประสบการณ์ผู้ใช้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้แบบอักษรแบบกำหนดเองกับ Aspose. Drawing สำหรับ .NET ได้หรือไม่

A1: ได้ คุณสามารถระบุแบบอักษรแบบกำหนดเองได้เมื่อสร้างวัตถุแบบอักษรในโค้ดของคุณ

### คำถามที่ 2: ฉันจะเพิ่มเอฟเฟกต์ข้อความ เช่น ตัวหนาหรือตัวเอียงได้อย่างไร

 A2: ปรับคุณสมบัติ FontStyle ของวัตถุ Font ตัวอย่างเช่น ใช้`FontStyle.Bold` สำหรับข้อความตัวหนา

### คำถามที่ 3: Aspose. Drawing เข้ากันได้กับ .NET Core หรือไม่

A3: ใช่ Aspose. Drawing รองรับ .NET Core ช่วยให้คุณสามารถใช้ในแอปพลิเคชันข้ามแพลตฟอร์มได้

### คำถามที่ 4: ฉันสามารถวาดข้อความบนรูปภาพที่มีอยู่ได้หรือไม่

 A4: แน่นอน! โหลดภาพที่มีอยู่โดยใช้`Bitmap.FromFile()`จากนั้นดำเนินการตามขั้นตอนการวาดข้อความ

### คำถามที่ 5: มีฟอรัมชุมชนสำหรับการสนับสนุน Aspose. Drawing หรือไม่

 A5: ใช่ คุณสามารถค้นหาการสนับสนุนและหารือเกี่ยวกับปัญหาได้ที่[Aspose.กระดานสนทนาการวาดภาพ](https://forum.aspose.com/c/diagram/17).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
