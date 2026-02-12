---
date: 2026-02-12
description: เรียนรู้วิธีบันทึกรูปภาพและวาดเส้น spline แบบ cardinal ใน .NET ด้วย Aspose.Drawing
  บันทึกเส้นโค้งเป็น PNG และสร้างกราฟิกที่เรียบเนียนอย่างง่ายดาย.
linktitle: Drawing Cardinal Splines in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: วิธีบันทึกรูปภาพและวาด Cardinal Splines ใน Aspose.Drawing
url: /th/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีบันทึกภาพและวาด Cardinal Splines ใน Aspose.Drawing

## คำแนะนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีบันทึกภาพ** ขณะวาด cardinal splines ที่เรียบเนียนโดยใช้ Aspose.Drawing สำหรับ .NET ไม่ว่าคุณจะกำลังสร้างคอมโพเนนต์แผนภูมิ, ตัวแก้ไขไดอะแกรม, หรือเพียงต้องการส่งออกเส้นโค้งที่กำหนดเองเป็น PNG ขั้นตอนต่อไปนี้จะแสดงให้คุณเห็นอย่างชัดเจนว่าการวาดเส้นโค้งด้วยปากกา, ปรับแต่ง spline, และบันทึกผลลัพธ์ลงดิสก์ทำอย่างไร

## คำตอบสั้น
- **เมธอดหลักทำอะไร?** `Graphics.DrawCurve` ทำการอินเตอร์โพเลตชุดจุดให้เป็น cardinal spline ที่เรียบเนียน.  
- **รูปแบบใดที่ใช้บันทึกภาพ?** PNG ผ่าน `Bitmap.Save`.  
- **ต้องมีลิขสิทธิ์เพื่อบันทึกภาพหรือไม่?** เวอร์ชันทดลองใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **สามารถเปลี่ยนความตึงของเส้นโค้งได้หรือไม่?** ได้, มี overload ของ `DrawCurve` ที่ให้คุณระบุ tension.  
- **Aspose.Drawing รองรับ .NET 6+ หรือไม่?** แน่นอน – รองรับ .NET Framework และ .NET Core/5/6.

## “วิธีบันทึกภาพ” หมายถึงอะไรในบริบทของ Aspose.Drawing?

การบันทึกภาพหมายถึงการแปลง bitmap ที่อยู่ในหน่วยความจำซึ่งคุณวาดอยู่ให้เป็นไฟล์จริง เช่น PNG, JPEG หรือ BMP Aspose.Drawing มีเมธอด `Bitmap.Save` ที่ง่ายต่อการใช้งานซึ่งจัดการการเข้ารหัสให้คุณ

## ทำไมต้องวาด cardinal spline ด้วย Aspose.Drawing?

Cardinal spline ให้เส้นโค้งที่เรียบและไหลลื่นซึ่งผ่านใกล้กับชุดจุดควบคุม เหมาะสำหรับการแสดงข้อมูล, กราฟิก UI, และรูปร่างที่กำหนดเอง การใช้ Aspose.Drawing จะช่วยหลีกเลี่ยงข้อจำกัดของ `System.Drawing.Common` และทำให้ได้ความสอดคล้องข้ามแพลตฟอร์ม

## ข้อกำหนดเบื้องต้น

- Visual Studio (เวอร์ชันล่าสุดใดก็ได้) ติดตั้งแล้ว.  
- ไลบรารี Aspose.Drawing สำหรับ .NET คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/drawing/net/).  
- ความรู้พื้นฐานการเขียนโปรแกรม C#.

## นำเข้า Namespaces

ในไฟล์ C# ของคุณ ให้เริ่มต้นด้วยการนำเข้า namespace ที่จำเป็น:

```csharp
using System.Drawing;
```

## ขั้นตอนที่ 1: สร้าง Bitmap (Canvas)

แรกเริ่มให้สร้าง bitmap ที่จะทำหน้าที่เป็น canvas สำหรับการวาดของคุณ Bitmap นี้คือที่ที่ spline จะถูกเรนเดอร์ก่อนที่คุณจะ **บันทึกภาพ**.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## ขั้นตอนที่ 2: สร้าง Graphics Object

ต่อไปให้รับ `Graphics` object จาก bitmap ซึ่งออบเจ็กต์นี้ให้พื้นผิวสำหรับการวาด.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## ขั้นตอนที่ 3: กำหนด Pen และวาดเส้นโค้ง

กำหนด `Pen` ด้วยสีและความกว้างที่ต้องการ จากนั้นวาด cardinal spline ด้วย `DrawCurve` ซึ่งเป็นการสาธิตเทคนิค **draw curve with pen** และทำหน้าที่เป็น **ตัวอย่าง cardinal spline**.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## ขั้นตอนที่ 4: บันทึกภาพ (บันทึกเส้นโค้งเป็น PNG)

สุดท้ายให้บันทึก bitmap เป็นไฟล์ PNG นี่คือหัวใจของ **วิธีบันทึกภาพ** ในบทแนะนำนี้.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **เคล็ดลับ:** ใช้ `Path.Combine` เพื่อสร้างเส้นทางไฟล์อย่างปลอดภัยข้ามแพลตฟอร์ม.

ยินดีด้วย! คุณได้วาด cardinal spline และบันทึกผลลัพธ์เป็นภาพ PNG ด้วย Aspose.Drawing สำหรับ .NET อย่างสำเร็จ คุณสามารถทดลองกับอาร์เรย์จุดต่าง ๆ, สีของ pen, หรือความกว้างของเส้นเพื่อปรับแต่งเส้นโค้งของคุณได้ตามต้องการ.

## กรณีการใช้งานทั่วไป

- **การแสดงข้อมูล** – แผนภูมิเส้นที่เรียบที่ต้องการจุดควบคุมที่แม่นยำ.  
- **คอมโพเนนต์ UI ที่กำหนดเอง** – วาด knob, slider, หรือขอบตกแต่ง.  
- **กราฟิกที่สามารถส่งออกได้** – สร้าง assets PNG แบบเรียลไทม์สำหรับรายงานหรือเนื้อหาเว็บ.

## การแก้ไขปัญหาและเคล็ดลับ

- **ภาพเป็นสีขาวเปล่า?** ตรวจสอบว่า bitmap มี pixel format ที่รองรับ alpha (`Format32bppPArgb`) และเรียก `graphics.Clear(Color.Transparent)` หากจำเป็น.  
- **รูปทรงเส้นโค้งไม่คาดคิด?** ปรับพารามิเตอร์ tension โดยใช้ overload `DrawCurve(pen, points, tension)`.  
- **ข้อผิดพลาดการเข้าถึงไฟล์?** ตรวจสอบว่าไดเรกทอรีเป้าหมายมีอยู่และแอปพลิเคชันของคุณมีสิทธิ์เขียน.

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.Drawing สำหรับโครงการเชิงพาณิชย์ได้หรือไม่?
A1: ใช่, Aspose.Drawing เหมาะสำหรับโครงการส่วนบุคคลและเชิงพาณิชย์ ตรวจสอบรายละเอียดลิขสิทธิ์ได้ที่ [หน้า purchase](https://purchase.aspose.com/buy).

### Q2: ฉันจะขอรับลิขสิทธิ์ชั่วคราวสำหรับการทดสอบได้อย่างไร?
A2: รับลิขสิทธิ์ชั่วคราวสำหรับการทดสอบได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q3: ฉันจะหาแหล่งสนับสนุนเพิ่มเติมได้จากที่ไหน?
A3: เยี่ยมชม [ฟอรั่ม Aspose.Drawing](https://forum.aspose.com/c/drawing/44) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

### Q4: มีการทดลองใช้ฟรีหรือไม่?
A4: มี, คุณสามารถสำรวจคุณลักษณะด้วยเวอร์ชัน [ทดลองฟรี](https://releases.aspose.com/) ก่อนทำการซื้อ.

### Q5: ฉันจะเข้าถึงเอกสารได้อย่างไร?
A5: ดูที่ [เอกสาร](https://reference.aspose.com/drawing/net/) อย่างครบถ้วนสำหรับข้อมูลและตัวอย่างโดยละเอียด.

### Q6: ฉันสามารถเปลี่ยนรูปแบบเอาต์พุตเป็น JPEG ได้หรือไม่?
A6: แน่นอน. แทนที่ส่วนขยาย `.png` ด้วย `.jpg` และระบุ `ImageFormat.Jpeg` ในเมธอด `Save`.

### Q7: สามารถวาดหลาย spline บน bitmap เดียวกันได้หรือไม่?
A7: ได้, เพียงเรียก `graphics.DrawCurve` หลายครั้งโดยใช้อาร์เรย์จุดและ pen ที่แตกต่างกัน.

## สรุป

ในคู่มือนี้เราได้อธิบาย **วิธีบันทึกภาพ** หลังจากวาด cardinal spline, แสดงตัวอย่างการ **draw curve ด้วย C#** อย่างเป็นรูปธรรม, และเน้นสถานการณ์ทั่วไปที่เทคนิคนี้โดดเด่น คุณมีพื้นฐานที่มั่นคงเพื่อรวมกราฟิก spline ที่เรียบเข้าสู่แอปพลิเคชัน .NET ใด ๆ

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}