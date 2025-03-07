---
title: การเปลี่ยนแปลงโลกใน Aspose. Drawing
linktitle: การเปลี่ยนแปลงโลกใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: สำรวจการเปลี่ยนแปลงของโลกใน Aspose. Drawing สำหรับ .NET ยกระดับกราฟิกของคุณด้วยขั้นตอนที่ปฏิบัติตามได้ง่าย
weight: 15
url: /th/net/coordinate-transformations/world-transformation/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเปลี่ยนแปลงโลกใน Aspose. Drawing

## การแนะนำ

ยินดีต้อนรับสู่โลกของ Aspose. Drawing สำหรับ .NET! ในบทช่วยสอนนี้ เราจะสำรวจขอบเขตอันน่าทึ่งของการเปลี่ยนแปลงของโลกโดยใช้ Aspose. Drawing หากคุณกระตือรือร้นที่จะปรับปรุงความสามารถด้านกราฟิกและภาพของคุณในแอปพลิเคชัน .NET แสดงว่าคุณมาถูกที่แล้ว

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะดำดิ่งสู่โลกแห่งการเปลี่ยนแปลง ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  ไลบรารี Aspose. Drawing: ตรวจสอบให้แน่ใจว่าคุณได้รวมไลบรารี Aspose. Drawing เข้ากับโปรเจ็กต์ .NET ของคุณแล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/drawing/net/).

- ไดเร็กทอรีเอกสาร: สร้างไดเร็กทอรีที่กำหนดสำหรับเอกสารของคุณ

- ความรู้พื้นฐาน C#: ทำความคุ้นเคยกับพื้นฐานการเขียนโปรแกรม C#

เอาล่ะ มาเริ่มกันที่เวทย์มนตร์แห่งการเปลี่ยนแปลงกันดีกว่า!

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System.Drawing;
using Aspose.Drawing;
```

## ขั้นตอนที่ 1: สร้างบิตแมป

```csharp
//ExStart: การเปลี่ยนแปลงโลก
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

ที่นี่ เราเริ่มต้นบิตแมปใหม่ด้วยขนาดเฉพาะและกำหนดรูปแบบพิกเซล

## ขั้นตอนที่ 2: ตั้งค่าการเปลี่ยนแปลง

```csharp
// ตั้งค่าการแปลงที่แมปพิกัดโลกกับพิกัดหน้า:
graphics.TranslateTransform(500, 400);
```

 ขั้นตอนนี้เกี่ยวข้องกับการกำหนดการเปลี่ยนแปลงที่แมปพิกัดโลกกับพิกัดเพจ ที่`TranslateTransform` ใช้วิธีการเลื่อนระบบพิกัด

## ขั้นตอนที่ 3: วาดรูปสี่เหลี่ยมผืนผ้า

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

ตอนนี้เราใช้ระบบพิกัดที่ถูกแปลงเพื่อวาดรูปสี่เหลี่ยมผืนผ้าบนบิตแมป

## ขั้นตอนที่ 4: บันทึกผลลัพธ์

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: การเปลี่ยนแปลงโลก
```

สุดท้าย ให้บันทึกรูปภาพที่แปลงแล้วไปยังไดเร็กทอรีเอกสารที่คุณกำหนด

ทำซ้ำขั้นตอนเหล่านี้เพื่อการแปลงเพิ่มเติมหรือปรับแต่งพารามิเตอร์เพื่อดูความมหัศจรรย์ทางภาพของ Aspose. Drawing!

## บทสรุป

ยินดีด้วย! คุณได้ปลดล็อกพลังของการเปลี่ยนแปลงโลกโดยใช้ Aspose. Drawing สำหรับ .NET ทดลอง สำรวจ และยกระดับความพยายามด้านกราฟิกของคุณด้วยไลบรารีอันทรงพลังนี้

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose. Drawing เข้ากันได้กับกรอบงาน .NET ทั้งหมดหรือไม่

ตอบ 1: ใช่ Aspose. Drawing รองรับเฟรมเวิร์ก .NET ที่หลากหลาย ทำให้มั่นใจได้ถึงความเข้ากันได้กับแอปพลิเคชันที่หลากหลาย

### 2: ฉันสามารถใช้การแปลงหลายรายการตามลำดับได้หรือไม่

A2: แน่นอน! อย่าลังเลที่จะเชื่อมโยงการเปลี่ยนแปลงหลายรายการเพื่อให้ได้เอฟเฟกต์กราฟิกที่ซับซ้อน

### คำถามที่ 3: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose. Drawing ได้ที่ไหน

 A3: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/drawing/net/) สำหรับข้อมูลเชิงลึกและตัวอย่างที่ครอบคลุม

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ใช่ สำรวจคุณสมบัติต่างๆ ด้วย[ทดลองฟรี](https://releases.aspose.com/) ก่อนตัดสินใจซื้อ

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือเชื่อมต่อกับชุมชนได้อย่างไร

 A5: เข้าร่วมการสนทนาและขอความช่วยเหลือเกี่ยวกับ[Aspose.กระดานสนทนาการวาดภาพ](https://forum.aspose.com/c/diagram/17).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
