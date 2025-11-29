---
date: 2025-11-29
description: เรียนรู้วิธีสร้างบิตแมปด้วย Aspose.Drawing, ใช้การแปลงโลก, และแปลงกราฟิกเป็น
  PNG. คู่มือขั้นตอนโดยละเอียดสำหรับนักพัฒนา .NET.
language: th
linktitle: World Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: สร้างบิตแมพด้วย Aspose.Drawing – คู่มือการแปลงโลก
url: /net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง Bitmap ด้วย Aspose.Drawing – การแปลง World

## Introduction

ยินดีต้อนรับ! ในบทเรียนนี้คุณจะ **สร้าง bitmap ด้วย Aspose.Drawing** และสำรวจการแปลง world ที่ช่วยให้คุณย้าย, หมุน, หรือปรับขนาดกราฟิกได้อย่างง่ายดาย ไม่ว่าคุณจะต้องการ **ตัวอย่างการแปลงกราฟิก**, ต้องการ **แปลงกราฟิกเป็น PNG**, หรือกำลังวางแผน **การแปลงกราฟิกหลายขั้นตอน**, คู่มือนี้จะพาคุณผ่านทุกขั้นตอนด้วยสไตล์ที่ชัดเจนและเป็นกันเอง

## Quick Answers
- **“world transformation” หมายถึงอะไร?** มันทำการแมปพิกัดเชิงตรรกะ (world) ของการวาดของคุณไปยังพิกัดของหน้า (device)  
- **ฉันสามารถส่งออกผลลัพธ์เป็น PNG ได้หรือไม่?** ได้ – หลังจากวาดเสร็จคุณเพียงเรียก `bitmap.Save(...)` พร้อมส่วนขยาย `.png`  
- **ต้องใช้ลิขสิทธิ์สำหรับ Aspose.Drawing หรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รองรับ .NET 6/7 หรือไม่?** แน่นอน – Aspose.Drawing รองรับ .NET Framework 4.5+ และ .NET Core/5/6/7  
- **สามารถเชื่อมต่อการแปลงได้กี่ขั้นตอน?** คุณสามารถใช้ **multiple graphics transformations** ต่อเนื่อง (translate, rotate, scale ฯลฯ)

## What is a World Transformation in Aspose.Drawing?

การแปลง world จะเปลี่ยนระบบพิกัดที่คำสั่งการวาดของคุณใช้ โดยค่าเริ่มต้น (0,0) อยู่ที่มุมซ้ายบนของ bitmap ด้วย `TranslateTransform`, `RotateTransform` หรือ `ScaleTransform` คุณสามารถย้ายจุดกำเนิด, หมุนรูปทรง, หรือปรับขนาดโดยไม่ต้องแก้ไขเรขาคณิตเดิม

## Why Use a Graphics Translate Example?

- **ทำให้การวางตำแหน่งง่ายขึ้น** – ย้ายวัตถุโดยไม่ต้องคำนวณจุดแต่ละจุดใหม่  
- **ทำให้โค้ดสะอาด** – คำสั่งแปลงเดียวแทนการปรับพิกัดหลายครั้งด้วยตนเอง  
- **เพิ่มประสิทธิภาพ** – เngine กราฟิกจะคำนวณคณิตศาสตร์ภายในให้เอง  

## Prerequisites

ก่อนเริ่มทำตามขั้นตอนนี้ ให้ตรวจสอบว่าคุณมี:

- **Aspose.Drawing library** ที่รวมไว้ในโปรเจกต์ .NET ของคุณ (ดาวน์โหลดจากหน้า [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/))  
- **document directory** ที่จะบันทึกไฟล์ภาพผลลัพธ์  
- ความคุ้นเคยพื้นฐานกับไวยากรณ์ **C#** และ Visual Studio หรือ IDE ที่คุณชื่นชอบ  

ตอนนี้มาดูโค้ดกันเลย!

## Import Namespaces

First, bring in the required namespaces:

```csharp
using System.Drawing;
using Aspose.Drawing;
```

These give you access to `Bitmap`, `Graphics`, and the Aspose drawing utilities.

## Step‑by‑Step Guide

### Step 1: Create a Bitmap

We start by creating a blank canvas that will hold our drawing.

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

- **Why 32bppPArgb?** รูปแบบพิกเซลนี้รองรับความโปร่งใสแบบอัลฟาและการเรนเดอร์สีคุณภาพสูง เหมาะสำหรับการส่งออกเป็น PNG  
- **Pro tip:** ปรับความกว้าง/สูงให้ตรงกับขนาดภาพเป้าหมายของคุณ  

### Step 2: Set the World Transformation (Graphics Translate Example)

Here we shift the origin to the center of the bitmap so that drawing commands are relative to that point.

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

- การทำเช่นนี้จะย้ายจุด (0,0) ไปที่ (500, 400) – จุดกึ่งกลางของแคนวาสขนาด 1000 × 800  
- คุณสามารถเชื่อมต่อการแปลงเพิ่มเติม (เช่น `RotateTransform`, `ScaleTransform`) เพื่อทำ **multiple graphics transformations**  

### Step 3: Draw a Rectangle Using the Transformed Coordinates

Now any shape we draw will be positioned relative to the new origin.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

- มุมซ้ายบนของสี่เหลี่ยมจะเริ่มจากจุดกำเนิดที่แปลงแล้ว (กึ่งกลางของภาพ)  
- อย่าลังเลที่จะทดลองกับรูปทรงอื่น ๆ – วงรี, เส้น, หรือพาธที่กำหนดเอง  

### Step 4: Save the Result – Convert Graphics to PNG

Finally, persist the bitmap as a PNG file.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

- PNG จะคงสีและความโปร่งใสที่ตั้งค่าไว้ก่อนหน้าอย่างแม่นยำ  
- แทนที่ `"Your Document Directory"` ด้วยพาธจริงบนเครื่องของคุณ  

## Common Issues and Solutions

| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **File not found error** when saving | โฟลเดอร์เป้าหมายไม่มีอยู่ | สร้างโฟลเดอร์โดยโปรแกรม (`Directory.CreateDirectory`) ก่อนเรียก `Save` |
| **Blank image** after transformation | `TranslateTransform` ถูกเรียกหลังการวาด | ตรวจสอบให้แน่ใจว่าการแปลงถูกตั้งค่า **ก่อน** คำสั่งวาดใด ๆ |
| **Distorted colors** | ใช้รูปแบบพิกเซลที่ไม่เข้ากัน | ใช้ `Format32bppPArgb` สำหรับการส่งออกเป็น PNG |

## Frequently Asked Questions

**Q: Can I apply more than one transformation?**  
A: ใช่ – คุณสามารถเชื่อมต่อ `TranslateTransform`, `RotateTransform`, และ `ScaleTransform` เพื่อสร้างเอฟเฟกต์ที่ซับซ้อนได้  

**Q: Is Aspose.Drawing free for commercial projects?**  
A: มีเวอร์ชันทดลองฟรีสำหรับการประเมินค่า, แต่ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  

**Q: Does this work with .NET Core and .NET 5/6/7?**  
A: แน่นอน Aspose.Drawing รองรับรันไทม์ .NET สมัยใหม่ทั้งหมด  

**Q: Where can I find the full API reference?**  
A: เอกสารฉบับเต็มสามารถเข้าถึงได้ที่ [here](https://reference.aspose.com/drawing/net/)  

**Q: How do I troubleshoot a missing output file?**  
A: ตรวจสอบสตริงพาธ, ยืนยันว่ามีสิทธิ์เขียน, และตรวจสอบว่าไดเรกทอรีมีอยู่ก่อนเรียก `Save`  

## Conclusion

คุณได้เรียนรู้วิธี **สร้าง bitmap ด้วย Aspose.Drawing**, ใช้ **world transformation**, และ **แปลงกราฟิกเป็น PNG** แล้ว การเข้าใจพื้นฐานเหล่านี้จะช่วยให้คุณสร้างกราฟิกที่หลากหลาย, สร้างภาพไดนามิก, และผสานเอฟเฟกต์ภาพขั้นสูงเข้าไปในแอปพลิเคชัน .NET ใด ๆ

---

**Last Updated:** 2025-11-29  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  
**Related Resources:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}