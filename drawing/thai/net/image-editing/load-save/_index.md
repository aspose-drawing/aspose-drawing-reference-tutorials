---
date: 2025-12-04
description: เชี่ยวชาญการโหลดภาพ, การแปลงภาพเป็นชุด, และการเปลี่ยนรูปแบบใน .NET ด้วย
  Aspose.Drawing. เรียนรู้การแปลง BMP เป็น PNG และอื่น ๆ อีกมากมาย.
language: th
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: แปลง BMP เป็น PNG และรูปแบบอื่น ๆ ด้วย Aspose.Drawing
url: /net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง BMP เป็น PNG และรูปแบบอื่นด้วย Aspose.Drawing

## บทนำ

ยินดีต้อนรับสู่คู่มือแบบขั้นตอนของเราว่าจะ **แปลง BMP เป็น PNG** (และรูปแบบภาพอื่น ๆ อีกมากมาย) โดยใช้ Aspose.Drawing สำหรับ .NET ไม่ว่าคุณจะต้อง **เปลี่ยนรูปแบบภาพ** สำหรับไฟล์เดียวหรือทำ **การแปลงภาพเป็นชุด** สำหรับหลายสิบรูปภาพ บทเรียนนี้จะแสดงให้คุณเห็นอย่างชัดเจนว่าต้องโหลด แปลง และบันทึกภาพอย่างไรด้วยโค้ดที่สะอาดและดูแลรักษาง่าย

## คำตอบสั้น
- **Aspose.Drawing สามารถแปลง BMP เป็น PNG ได้หรือไม่?** ได้ – เพียงโหลดไฟล์ BMP แล้วเรียก `Save` พร้อมส่วนขยาย .png  
- **รองรับการแปลงเป็นชุดหรือไม่?** แน่นอน; วนลูปไฟล์และใช้เมธอด `LoadAndSave` เดียวกัน  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในโปรดักชันหรือไม่?** จำเป็นต้องมีลิขสิทธิ์สำหรับการใช้งานในโปรดักชัน; มีลิขสิทธิ์ชั่วคราวสำหรับการประเมินผล  
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** ทำงานกับ .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7  
- **สามารถดาวน์โหลดไลบรารีได้จากที่ไหน?** ดาวน์โหลดแพคเกจ Aspose.Drawing ล่าสุดจากหน้าดาวน์โหลดอย่างเป็นทางการ

## การแปลงรูปแบบภาพด้วย C# และ Aspose.Drawing คืออะไร?

Aspose.Drawing เป็นไลบรารี .NET ที่มีประสิทธิภาพสูงและจัดการทั้งหมด ซึ่งแทนที่ `System.Drawing.Common` รุ่นเก่า ให้คุณควบคุม **การโหลดภาพใน ASP.NET** ได้เต็มที่ รองรับรูปแบบภาพกว่า 100 รูปแบบ และขจัดข้อจำกัดเฉพาะแพลตฟอร์ม

## ทำไมต้องใช้ Aspose.Drawing สำหรับการแปลงภาพเป็นชุด?

- **ความน่าเชื่อถือข้ามแพลตฟอร์ม** – ไม่ต้องพึ่งพา GDI+  
- **การสนับสนุนรูปแบบที่หลากหลาย** – BMP, GIF, JPG, PNG, TIFF และอื่น ๆ อีกมาก  
- **API ที่สอดคล้องกัน** – โค้ดเดียวทำงานบน Windows, Linux, และ macOS  
- **ประสิทธิภาพ** – ปรับให้เหมาะกับการประมวลผลภาพขนาดใหญ่ในสายงาน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ให้ตรวจสอบว่าคุณมี:

- **Aspose.Drawing for .NET** – ดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/drawing/net/)  
- สภาพแวดล้อมการพัฒนา **.NET** ที่ทำงานได้ (Visual Studio, VS Code หรือ Rider)

เมื่อพร้อมแล้ว ให้เรานำเข้าเนมสเปซที่จำเป็นและเริ่มเขียนโค้ดกัน

## นำเข้าเนมสเปซ

ในโปรเจกต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System.Drawing;
```

คลาสเหล่านี้ให้ฟังก์ชันหลักสำหรับการโหลดและบันทึกภาพ

## ขั้นตอนที่ 1: การโหลดภาพ

ขั้นตอนแรกคือการโหลดไฟล์ภาพ ตัวอย่างด้านล่างแสดงการโหลดภาพหลายรูปแบบรวมถึง BMP ซึ่งเราจะเปลี่ยนเป็น PNG ต่อไป

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

## วิธีแปลง BMP เป็น PNG ด้วย Aspose.Drawing

เมธอด `LoadAndSave` จัดการทั้งการโหลดไฟล์ต้นฉบับและการบันทึกในรูปแบบที่ต้องการ โดยการส่งค่า `"bmp"` เป็นอาร์กิวเมนต์ เมธอดจะสร้างไฟล์ PNG อัตโนมัติเมื่อคุณเปลี่ยนส่วนขยายใน `outputPath`

### ขั้นตอน 2.1: โหลดภาพ

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### ขั้นตอน 2.2: บันทึกภาพ (เปลี่ยนรูปแบบภาพ)

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

ทำการเรียก `LoadAndSave` ซ้ำสำหรับแต่ละรูปแบบภาพที่ต้องการประมวลผล โดยปรับส่วนขยายของ `outputPath` คุณสามารถ **แปลง BMP เป็น PNG**, **เปลี่ยนรูปแบบภาพ** เป็น GIF, JPG ฯลฯ ได้ทั้งหมดด้วยเมธอดเดียวกัน

## ข้อผิดพลาดทั่วไป & เคล็ดลับ

- **ตัวคั่นเส้นทางไฟล์** – ใช้ `Path.Combine` เพื่อความปลอดภัยข้ามแพลตฟอร์มแทนการต่อสตริงด้วยตนเอง  
- **การปล่อย Bitmap** – ห่อ `Bitmap` ด้วยบล็อก `using` เพื่อให้ทรัพยากรเนทีฟถูกปล่อยโดยเร็ว  
- **การตั้งค่าคุณภาพ** – เมื่อบันทึก JPEG ให้พิจารณากำหนดอ็อบเจ็กต์ `EncoderParameters` เพื่อควบคุมคุณภาพการบีบอัด  
- **การประมวลผลเป็นชุด** – วางไฟล์ภาพไว้ในโฟลเดอร์แล้วใช้ `Directory.GetFiles` เพื่อทำการแปลงจำนวนมากโดยอัตโนมัติ

## คำถามที่พบบ่อย

### Q1: Aspose.Drawing รองรับรูปแบบภาพทั้งหมดหรือไม่?

A1: Aspose.Drawing รองรับรูปแบบหลากหลายรวมถึง BMP, GIF, JPG, PNG, และ TIFF

### Q2: จะหาเอกสารรายละเอียดของ Aspose.Drawing ได้จากที่ไหน?

A2: ดูเอกสารอย่างเป็นทางการ [ที่นี่](https://reference.aspose.com/drawing/net/)

### Q3: จะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.Drawing ได้อย่างไร?

A3: เยี่ยมชม [ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับรายละเอียดลิขสิทธิ์ชั่วคราว

### Q4: หากพบปัญหาหรือมีคำถามระหว่างการใช้งานควรทำอย่างไร?

A4: ขอความช่วยเหลือจากชุมชน Aspose.Drawing ที่ [Aspose Forum](https://forum.aspose.com/c/drawing/44)

### Q5: จะซื้อไลบรารี Aspose.Drawing ได้จากที่ไหน?

A5: คุณสามารถซื้อได้ [ที่นี่](https://purchase.aspose.com/buy)

**คำถามเพิ่มเติม**

**Q: สามารถใช้โค้ดนี้ในแอปพลิเคชันเว็บ ASP.NET ได้หรือไม่?**  
A: ได้ – ลอจิก `LoadAndSave` เดียวกันทำงานใน ASP.NET, MVC หรือ Razor Pages; เพียงตรวจสอบให้แน่ใจว่าเส้นทางไฟล์เข้าถึงได้จากกระบวนการเว็บ

**Q: สามารถประมวลผลภาพแบบขนานเพื่อเร่งการแปลงเป็นชุดได้หรือไม่?**  
A: แน่นอน. ห่อการเรียก `LoadAndSave` ด้วยลูป `Parallel.ForEach` แต่ต้องจัดการการปล่อย `Bitmap` อย่างปลอดภัยต่อเธรด

## สรุป

คุณได้เรียนรู้วิธี **แปลง BMP เป็น PNG**, ทำ **การแปลงภาพเป็นชุด**, และ **เปลี่ยนรูปแบบภาพ** ด้วย Aspose.Drawing สำหรับ .NET แล้ว นำรูปแบบเหล่านี้ไปใช้ในการอัตโนมัติสายงานภาพ, สร้างภาพย่อ, หรือเตรียมทรัพยากรสำหรับการส่งบนเว็บ ทดลองกับรูปแบบต่าง ๆ รวมโค้ดเข้ากับบริการของคุณและเพลิดเพลินกับความน่าเชื่อถือของไลบรารีการวาดแบบจัดการเต็มรูปแบบ

---

**อัปเดตล่าสุด:** 2025-12-04  
**ทดสอบกับ:** Aspose.Drawing 24.12 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}