---
title: การโหลดและบันทึกรูปภาพใน Aspose. Drawing
linktitle: การโหลดและบันทึกรูปภาพใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: การโหลดและบันทึกรูปภาพหลักใน .NET ด้วย Aspose. Drawing สำรวจรูปแบบ BMP, GIF, JPG, PNG, TIFF ได้อย่างง่ายดาย
weight: 13
url: /th/net/image-editing/load-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การโหลดและบันทึกรูปภาพใน Aspose. Drawing

## การแนะนำ

ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนในการเรียนรู้การโหลดและบันทึกรูปภาพโดยใช้ Aspose. Drawing สำหรับ .NET! หากคุณกำลังมองหาที่จะพัฒนาทักษะในการจัดการกับรูปแบบรูปภาพต่าง ๆ ได้อย่างง่ายดาย คุณมาถูกที่แล้ว Aspose. Drawing for .NET เป็นไลบรารีที่มีประสิทธิภาพซึ่งช่วยให้กระบวนการทำงานกับรูปภาพง่ายขึ้น และในบทช่วยสอนนี้ เราจะเจาะลึกเรื่องการโหลดและบันทึกรูปภาพในรูปแบบต่างๆ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้นการเดินทางแห่งการเรียนรู้นี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose. Drawing สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/drawing/net/).

- สภาพแวดล้อม .NET: บทช่วยสอนนี้ถือว่าคุณมีความรู้เกี่ยวกับการพัฒนา .NET

ตอนนี้เราพร้อมแล้ว เรามาสำรวจเนมสเปซที่จำเป็นและเจาะลึกคำแนะนำทีละขั้นตอนกันดีกว่า

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System.Drawing;
```

เนมสเปซเหล่านี้จัดเตรียมคลาสพื้นฐานและวิธีการที่จำเป็นสำหรับการจัดการรูปภาพ

## ขั้นตอนที่ 1: กำลังโหลดรูปภาพ

เริ่มต้นด้วยการโหลดภาพ ตัวอย่างนี้โหลดรูปภาพในรูปแบบต่างๆ เช่น BMP, GIF, JPG, PNG และ TIFF

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## ขั้นตอนที่ 2: การใช้วิธี LoadAndSave

 ตอนนี้แยกย่อย`LoadAndSave` วิธีการออกเป็นหลายขั้นตอน:

### ขั้นตอนที่ 2.1: โหลดรูปภาพ

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### ขั้นตอนที่ 2.2: บันทึกรูปภาพ

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // บันทึกภาพ
    loadedImage.Save(outputPath);
}
```

ทำซ้ำขั้นตอนเหล่านี้กับรูปแบบภาพแต่ละรูปแบบที่คุณต้องการรองรับ

## บทสรุป

ยินดีด้วย! คุณเชี่ยวชาญศิลปะในการโหลดและบันทึกภาพโดยใช้ Aspose. Drawing สำหรับ .NET แล้ว ทักษะนี้มีค่าอย่างยิ่งสำหรับนักพัฒนาที่ทำงานกับรูปแบบภาพที่หลากหลาย ทดลอง สำรวจ และบูรณาการความรู้นี้ในโครงการของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose. Drawing เข้ากันได้กับทุกรูปแบบภาพหรือไม่

A1: Aspose. Drawing รองรับรูปแบบที่หลากหลาย รวมถึง BMP, GIF, JPG, PNG และ TIFF

### คำถามที่ 2: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose. Drawing ได้ที่ไหน

A2: ตรวจสอบเอกสารอย่างเป็นทางการ[ที่นี่](https://reference.aspose.com/drawing/net/).

### คำถามที่ 3: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose. Drawing ได้อย่างไร

 A3: เยี่ยมเลย[ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับรายละเอียดใบอนุญาตชั่วคราว

### คำถามที่ 4: จะเกิดอะไรขึ้นหากฉันพบปัญหาหรือมีคำถามระหว่างการใช้งาน

 A4: ขอความช่วยเหลือจากชุมชน Aspose. Drawing ได้ที่[ตั้งฟอรั่ม](https://forum.aspose.com/c/diagram/17).

### คำถามที่ 5: ฉันจะซื้อไลบรารี Aspose. Drawing ได้ที่ไหน

 A5: คุณสามารถซื้อได้[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
