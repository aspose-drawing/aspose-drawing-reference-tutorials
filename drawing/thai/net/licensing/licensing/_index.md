---
title: การออกใบอนุญาตใน Aspose. Drawing
linktitle: การออกใบอนุญาตใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: ปลดล็อกศักยภาพเต็มรูปแบบของ Aspose. Drawing ใน .NET ใบอนุญาตหลักเพื่อการบูรณาการที่ราบรื่น ดาวน์โหลดตอนนี้และยกระดับการจัดการกราฟิกและรูปภาพของคุณ
weight: 10
url: /th/net/licensing/licensing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การออกใบอนุญาตใน Aspose. Drawing

## การแนะนำ

ในขอบเขตของการพัฒนา .NET นั้น Aspose. Drawing โดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับการจัดการกราฟิกและรูปภาพ เพื่อปลดล็อกศักยภาพสูงสุดของ Aspose.Drawing การทำความเข้าใจเรื่องลิขสิทธิ์เป็นสิ่งสำคัญยิ่ง บทช่วยสอนนี้จะแนะนำคุณตลอดวิธีการออกใบอนุญาตต่างๆ เพื่อให้มั่นใจว่าคุณจะผสานรวม Aspose. Drawing เข้ากับโปรเจ็กต์ .NET ของคุณได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่จะดำดิ่งลงสู่การอนุญาตให้ใช้สิทธิกับ Aspose. Drawing ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose. Drawing Library: ดาวน์โหลดไลบรารี่จาก[ที่นี่](https://releases.aspose.com/drawing/net/).
-  ไฟล์ลิขสิทธิ์: รับไฟล์ลิขสิทธิ์ที่ถูกต้องจาก[กำหนด](https://purchase.aspose.com/buy).
- สภาพแวดล้อม .NET: ตรวจสอบให้แน่ใจว่าคุณมีสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้

## นำเข้าเนมสเปซ

ก่อนที่เราจะดำเนินการต่อ จำเป็นต้องนำเข้าเนมสเปซที่จำเป็นในโครงการของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## กำลังโหลดใบอนุญาตจากไฟล์

เริ่มจากพื้นฐานกันก่อน การโหลดใบอนุญาตจากไฟล์ถือเป็นแนวทางปฏิบัติทั่วไป ทำตามขั้นตอนเหล่านี้:

### ขั้นตอนที่ 1: เริ่มต้นวัตถุลิขสิทธิ์

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### ขั้นตอนที่ 2: ตั้งค่าใบอนุญาตจากไฟล์

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### ขั้นตอนที่ 3: แสดงข้อความแสดงความสำเร็จ

```csharp
Console.WriteLine("License set successfully.");
```

## กำลังโหลดใบอนุญาตจากสตรีม

การโหลดใบอนุญาตจากสตรีมให้ความยืดหยุ่น ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

### ขั้นตอนที่ 1: เริ่มต้นวัตถุลิขสิทธิ์

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### ขั้นตอนที่ 2: โหลดใบอนุญาตจาก FileStream

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### ขั้นตอนที่ 3: แสดงข้อความแสดงความสำเร็จ

```csharp
Console.WriteLine("License set successfully.");
```

## การใช้ใบอนุญาตแบบมิเตอร์

การให้สิทธิ์การใช้งานแบบคิดค่าบริการตามปริมาณการใช้งานมีรูปแบบตามการใช้งาน ต่อไปนี้เป็นวิธีการตั้งค่า:

### ขั้นตอนที่ 1: เริ่มต้นวัตถุที่วัดแสง

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### ขั้นตอนที่ 2: ตั้งค่าคีย์สาธารณะและคีย์ส่วนตัวแบบมิเตอร์

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### ขั้นตอนที่ 3: ดำเนินการประมวลผล

```csharp
// ตรรกะการประมวลผลภาพของคุณที่นี่
```

### ขั้นตอนที่ 4: รับข้อมูลการบริโภค

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### ขั้นตอนที่ 5: แสดงข้อมูล

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

## บทสรุป

การเรียนรู้ใบอนุญาตใน Aspose. Drawing เป็นสิ่งสำคัญสำหรับการปลดปล่อยศักยภาพสูงสุดของไลบรารี .NET อันทรงพลังนี้ ไม่ว่าจะโหลดจากไฟล์ สตรีม หรือใช้สิทธิ์การใช้งานแบบคิดค่าบริการตามปริมาณข้อมูล ขั้นตอนเหล่านี้รับประกันว่าจะมีการผสานรวมเข้ากับโปรเจ็กต์ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose. Drawing โดยไม่มีใบอนุญาตได้หรือไม่

ตอบ 1: แม้ว่าคุณจะสามารถใช้งานได้โดยไม่ต้องมีใบอนุญาต แต่ใบอนุญาตที่ถูกต้องจะปลดล็อกคุณสมบัติเพิ่มเติมและลบลายน้ำออก

### คำถามที่ 2: ฉันต้องต่ออายุใบอนุญาต Aspose.ถอนเงินบ่อยแค่ไหน?

ตอบ 2: โดยทั่วไปแล้วสิทธิ์การใช้งานจะมีผลถาวร ทำให้คุณสามารถใช้เวอร์ชันที่คุณซื้อได้อย่างไม่มีกำหนด อย่างไรก็ตาม การอัปเดตและการสนับสนุนอาจจำเป็นต้องต่ออายุ

### คำถามที่ 3: สิทธิ์การใช้งานแบบคิดค่าบริการตามปริมาณข้อมูลคืออะไร และฉันควรใช้เมื่อใด

A3: สิทธิ์ใช้งานแบบมิเตอร์จะขึ้นอยู่กับการใช้งาน เหมาะสำหรับสถานการณ์ที่คุณต้องการชำระเงินตามจำนวนการดำเนินงานหรือข้อมูลที่ประมวลผล

### คำถามที่ 4: ฉันสามารถใช้ Aspose. Drawing ในโครงการเชิงพาณิชย์ได้หรือไม่

A4: ได้ คุณสามารถใช้ Aspose. Drawing ได้ทั้งในโครงการเชิงพาณิชย์และไม่ใช่เชิงพาณิชย์พร้อมใบอนุญาตที่เหมาะสม

### คำถามที่ 5: ฉันจะรับการสนับสนุนจากชุมชนสำหรับ Aspose. Drawing ได้ที่ไหน

 A5: เยี่ยมชม[Aspose. ฟอรั่มการวาดภาพ](https://forum.aspose.com/c/drawing/44) สำหรับการสนับสนุนและการอภิปรายของชุมชน
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
