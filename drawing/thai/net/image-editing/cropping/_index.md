---
date: 2026-10-13
description: เรียนรู้วิธีการตัดภาพเป็นชุดเป็น PNG ด้วย Aspose.Drawing API ซึ่งเป็นทางเลือกแบบข้ามแพลตฟอร์มของ
  System.Drawing สำหรับนักพัฒนา .NET
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: บทเรียนการตัดภาพ – Aspose.Drawing
og_description: เรียนรู้วิธีการตัดภาพเป็นชุดเป็น PNG อย่างรวดเร็วด้วย Aspose.Drawing
  ซึ่งเป็นทางเลือกแบบข้ามแพลตฟอร์มของ System.Drawing สำหรับนักพัฒนา .NET ทำตามคำแนะนำขั้นตอนต่อขั้นตอนเพื่อประมวลผลหลายไฟล์อย่างมีประสิทธิภาพ
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: วิธีการตัดภาพเป็นชุดเป็น PNG ด้วย Aspose.Drawing สำหรับ .NET
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: วิธีการตัดภาพเป็นชุดเป็น PNG ด้วย Aspose.Drawing สำหรับ .NET
url: /th/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีตัดภาพเป็น PNG เป็นชุดโดยใช้ Aspose.Drawing สำหรับ .NET

ถ้าคุณต้องการ **crop image to PNG** อย่างรวดเร็ว เชื่อถือได้ และในปริมาณมากในสภาพแวดล้อม .NET คุณอยู่ในที่ถูกต้อง ในบทแนะนำนี้เราจะอธิบายขั้นตอนที่แน่นอนในการโหลดภาพ กำหนดพื้นที่การตัด และบันทึกผลลัพธ์เป็นไฟล์ PNG — ทั้งหมดโดยใช้ Aspose.Drawing ซึ่งเป็น **alternative to System.Drawing** สมัยใหม่ที่ทำงานข้ามแพลตฟอร์ม คุณยังจะได้เห็นวิธีขยายกระบวนการภาพเดียวให้เป็น **batch crop** pipeline เต็มรูปแบบ

## คำตอบอย่างรวดเร็ว
- **ควรใช้ไลบรารีอะไร?** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **การตัดพื้นฐานใช้เวลานานเท่าไหร่?** Usually under a second for a single image on a modern CPU  
- **ฉันสามารถตัดเป็น PNG ได้หรือไม่?** Yes – save the cropped bitmap as a PNG file (see Step 6)  
- **ฉันต้องการไลเซนส์หรือไม่?** A free trial works for development; a commercial license is required for production  
- **การประมวลผลเป็นชุดทำได้หรือไม่?** Absolutely – wrap the same steps in a loop to process multiple files in seconds  

## วิธีตัดภาพเป็น PNG เป็นชุด?

โหลดไฟล์ต้นทางแต่ละไฟล์ด้วย `new Bitmap(path)` สร้าง `Bitmap` ว่างที่ตรงกันสำหรับพื้นที่การตัด วาดสี่เหลี่ยมที่เลือกโดยใช้ `Graphics.DrawImage` และสุดท้ายเรียก `Save("output.png", ImageFormat.Png)` ใส่บรรทัดทั้งหกนี้ไว้ในลูป `foreach` ที่วนผ่านไดเรกทอรี แล้วคุณจะได้โซลูชัน batch‑crop ที่สมบูรณ์ซึ่งประมวลผลหลายสิบภาพในไม่กี่วินาที

## ทำไมต้องใช้ Aspose.Drawing สำหรับการตัดภาพเป็นชุด?

Aspose.Drawing ทำงานบน **Windows, Linux, and macOS**, ประมวลผล **500‑plus‑pixel images in under 0.5 seconds** บน CPU ระดับเซิร์ฟเวอร์ทั่วไป และรองรับ **50+ image formats** พร้อมการรักษา alpha‑channel อย่างเต็มรูปแบบ เนื่องจากมันขจัดการพึ่งพา GDI+ แบบเนทีฟ คุณสามารถปรับใช้โค้ดเดียวกันไปยังคอนเทนเนอร์, Azure App Service หรือ AWS Lambda โดยไม่ต้องใช้ไลบรารีเพิ่มเติม ทำให้เหมาะสำหรับ pipeline ภาพขนาดใหญ่

## อะไรคือ “crop image to PNG”?

การทำงาน `crop image to PNG` จะดึงส่วนสี่เหลี่ยมจาก bitmap ต้นทางและเขียนส่วนนั้นลงในไฟล์ PNG PNG จะรักษา alpha channel ใด ๆ ไว้ ส่งผลให้ได้การบีบอัดแบบ lossless ซึ่งทำให้ภาพที่ได้เหมาะสำหรับ thumbnail, ไอคอน, สินทรัพย์ UI หรือสถานการณ์ใด ๆ ที่ต้องการคุณภาพและความโปร่งใส

## ทำไม Aspose.Drawing จึงเป็นทางเลือกแทน System.Drawing?

Aspose.Drawing ทำหน้าที่เป็นการแทนที่แบบ drop‑in สำหรับ System.Drawing โดยให้ความเข้ากันได้ข้ามแพลตฟอร์มเต็มรูปแบบและขจัดความจำเป็นของไลบรารี GDI+ แบบเนทีฟ มันรองรับรูปแบบพิกเซลหลากหลาย ให้การจัดการภาพที่มีประสิทธิภาพสูง และรวมคุณลักษณะขั้นสูงเช่นการจัดการ alpha‑channel และการสนับสนุนรูปแบบอย่างกว้างขวาง ทำให้เหมาะสำหรับการแก้ไขง่าย ๆ และการประมวลผลเป็นชุดขนาดใหญ่

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ให้แน่ใจว่าคุณมี:

- **Aspose.Drawing library** ที่รวมไว้ในโครงการ .NET ของคุณ คุณสามารถดาวน์โหลดได้จาก [Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)  
- โฟลเดอร์ที่บรรจุภาพต้นทางที่คุณต้องการตัด แทนที่ `"Your Document Directory"` ในโค้ดสแนปด้วยพาธจริงบนเครื่องของคุณ

## นำเข้า namespace

Namespace `System.Drawing` ให้เราเข้าถึง `Bitmap`, `Graphics` และประเภทที่เกี่ยวข้องซึ่ง Aspose.Drawing ขยายเพิ่ม

```csharp
using System.Drawing;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: สร้างแคนวาส bitmap

`Bitmap` คือการแสดงภาพในหน่วยความจำของ Aspose.Drawing ให้การเข้าถึงระดับพิกเซลและการควบคุมรูปแบบ

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

เราเริ่มด้วยแคนวาสว่างที่มีขนาดพอที่จะบรรจุผลลัพธ์ที่ตัดแล้ว ปรับความกว้างและความสูงให้ตรงกับมิติของพื้นที่ที่คุณต้องการดึงออก

### ขั้นตอนที่ 2: สร้างอ็อบเจ็กต์ graphics

`Graphics` คือพื้นผิวการวาดที่ให้คุณเรนเดอร์รูปทรง, ข้อความ หรือภาพอื่น ๆ ลงบน Bitmap

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

อ็อบเจ็กต์ `Graphics` ทำให้เราสามารถวาดบนแคนวาสได้ `InterpolationMode` ควบคุมวิธีการคำนวณค่าพิกเซลระหว่างการสเกลหรือการแปลง — `NearestNeighbor` ทำงานได้ดีสำหรับขอบที่คมชัด

### ขั้นตอนที่ 3: โหลดภาพเพื่อทำการตัด

`Image` (หรือ `Bitmap`) โหลดไฟล์ต้นทางเข้าสู่หน่วยความจำ พร้อมสำหรับการจัดการ

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

โหลดภาพต้นทาง ตรวจสอบให้แน่ใจว่าพาธชี้ไปยังไฟล์ที่มีอยู่ มิฉะนั้นจะเกิดข้อยกเว้น

### ขั้นตอนที่ 4: กำหนดสี่เหลี่ยมต้นทางและปลายทาง

อ็อบเจ็กต์ `Rectangle` บรรยายพื้นที่ของภาพต้นทางที่ต้องการเก็บและตำแหน่งที่ควรวางบนแคนวาสปลายทาง

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` บอก API ว่าส่วนใดของภาพต้นฉบับที่จะเก็บ ที่นี่เราเลือกพื้นที่ 50 × 40 พิกเซลที่มุมบนซ้าย โดยการกำหนดสี่เหลี่ยมเดียวกันให้กับ `destinationRectangle` เราจะเก็บส่วนที่ตัดไว้ในขนาดเดิม

### ขั้นตอนที่ 5: ทำการตัดภาพ

`Graphics.DrawImage` คัดลอกส่วนที่กำหนดของ `image` ไปยัง `bitmap` ว่างของเรา

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

นี่คือการทำงานหลักของ **crop image to PNG** วิธีนี้เคารพสี่เหลี่ยมต้นทางและเขียนเฉพาะพิกเซลที่เลือกไปยัง bitmap ปลายทาง

### ขั้นตอนที่ 6: บันทึกภาพที่ตัดแล้ว (crop image to PNG)

`Bitmap.Save` เขียน bitmap ในหน่วยความจำลงไฟล์โดยใช้รูปแบบที่ระบุ

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

สุดท้าย เขียนแคนวาสลงดิสก์เป็นไฟล์ PNG PNG จะรักษา alpha channel ใด ๆ และให้คุณภาพ lossless — เหมาะสำหรับสินทรัพย์ UI

## วิธีตัดภาพเป็นชุดในลูป?

วนซ้ำแต่ละพาธไฟล์ด้วย `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` ทำซ้ำขั้นตอน 1‑6 ภายในลูปและเก็บผลลัพธ์แต่ละไฟล์ในโฟลเดอร์เป้าหมาย รูปแบบนี้ขยายได้เชิงเส้น สามารถทำแบบขนานด้วย `Parallel.ForEach` เพื่อเพิ่มอัตราการทำงานและประมวลผลภาพได้อย่างมีประสิทธิภาพและรวดเร็ว

## ข้อผิดพลาดทั่วไป & เคล็ดลับ

- **Pixel format mismatches** – ตรวจสอบให้แน่ใจว่าภาพต้นทางและ bitmap ของแคนวาสใช้รูปแบบพิกเซลที่เข้ากันได้เพื่อหลีกเลี่ยงการเปลี่ยนสี  
- **Disposal of GDI objects** – ห่อ `Bitmap` และ `Graphics` ด้วยคำสั่ง `using` หรือเรียก `Dispose()` ด้วยตนเอง มิฉะนั้นอาจทำให้ทรัพยากรที่ไม่ได้จัดการรั่วไหล  
- **Coordinate errors** – พิกัดของสี่เหลี่ยมเริ่มจากศูนย์ การเลือกสี่เหลี่ยมที่เกินขอบเขตของภาพต้นทางจะทำให้เกิดข้อยกเว้น  

## คำถามที่พบบ่อย

**Q: ฉันสามารถตัดภาพจากฟอร์แมตใดก็ได้โดยใช้ Aspose.Drawing หรือไม่?**  
A: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP, GIF, TIFF, etc.), so you can crop virtually any image type.

**Q: มีตัวเลือกการตัดขั้นสูงหรือไม่?**  
A: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations, or use the `ImageProcessor` class for more complex selections like circular crops.

**Q: ฉันสามารถทำการตัดหลายครั้งต่อภาพเดียวได้หรือไม่?**  
A: Yes. After the first crop, you can reuse the resulting bitmap as the new source and repeat the process to chain multiple crops.

**Q: Aspose.Drawing เหมาะสำหรับการประมวลผลภาพเป็นชุดหรือไม่?**  
A: Indeed. Its lightweight API and lack of native dependencies make it perfect for processing large image collections on servers.

**Q: ฉันจะขอรับการสนับสนุนสำหรับคำถามที่เกี่ยวกับ Aspose.Drawing ได้อย่างไร?**  
A: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) to seek assistance and connect with the community.

**อัปเดตล่าสุด:** 2026-10-13  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [โหลด, แปลง BMP เป็น PNG และรูปแบบอื่น ๆ ด้วย Aspose.Drawing](/drawing/net/image-editing/load-save/)
- [วิธีขอไลเซนส์ Aspose.Drawing สำหรับ .NET – วิธีขอไลเซนส์ aspose.drawing](/drawing/net/licensing/)
- [วิธีวาดสี่เหลี่ยม – การแปลงระบบพิกัด (การแปลงหน้า) ด้วย Aspose.Drawing API สำหรับ .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}