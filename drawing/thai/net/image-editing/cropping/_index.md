---
date: 2026-05-19
description: บทแนะนำแบบขั้นตอนต่อขั้นตอนเกี่ยวกับวิธีการตัดภาพหลายภาพเป็น PNG ด้วย
  Aspose.Drawing ซึ่งเป็นทางเลือกของ System.Drawing สำหรับนักพัฒนา .NET
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: บทแนะนำการตัดภาพ – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
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
title: วิธีการตัดภาพหลายภาพเป็น PNG ด้วย Aspose.Drawing สำหรับ .NET
url: /th/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการตัดภาพเป็น PNG เป็นชุดโดยใช้ Aspose.Drawing สำหรับ .NET

หากคุณต้องการ **crop image to PNG** อย่างรวดเร็ว เชื่อถือได้ และในปริมาณมากในสภาพแวดล้อม .NET คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายขั้นตอนที่แน่นอนเพื่อโหลดภาพ กำหนดพื้นที่ตัด และบันทึกผลเป็นไฟล์ PNG — ทั้งหมดโดยใช้ Aspose.Drawing ซึ่งเป็น **alternative to System.Drawing** สมัยใหม่ที่ทำงานข้ามแพลตฟอร์ม คุณยังจะได้เห็นวิธีขยายกระบวนการภาพเดี่ยวให้เป็น **batch crop** เต็มรูปแบบ

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่ควรใช้คืออะไร?** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **การตัดพื้นฐานใช้เวลานานเท่าไหร่?** Usually under a second for a single image on a modern CPU  
- **ฉันสามารถตัดเป็น PNG ได้หรือไม่?** Yes – save the cropped bitmap as a PNG file (see Step 6)  
- **ฉันต้องการไลเซนส์หรือไม่?** A free trial works for development; a commercial license is required for production  
- **การประมวลผลเป็นชุดเป็นไปได้หรือไม่?** Absolutely – wrap the same steps in a loop to process multiple files  

## วิธีการตัดภาพเป็น PNG เป็นชุด

โหลดไฟล์ต้นทางแต่ละไฟล์ด้วย `new Bitmap(path)` สร้าง `Bitmap` ว่างที่ตรงกันสำหรับพื้นที่ตัด วาดสี่เหลี่ยมที่เลือกโดยใช้ `Graphics.DrawImage` และสุดท้ายเรียก `Save("output.png", ImageFormat.Png)` ห่อหกบรรทัดเหล่านี้ไว้ในลูป `foreach` ที่วนผ่านไดเรกทอรีและคุณจะได้โซลูชันการตัดเป็นชุดที่สมบูรณ์ซึ่งประมวลผลหลายสิบภาพในไม่กี่วินาที

## ทำไมต้องใช้ Aspose.Drawing สำหรับการตัดเป็นชุด?

Aspose.Drawing รองรับ **3 major operating systems** (Windows, Linux, macOS) และสามารถจัดการ **500‑plus‑pixel images** ได้ภายในเวลาไม่ถึง 0.5 วินาทีบน CPU ระดับเซิร์ฟเวอร์ทั่วไป API ของมันหลีกเลี่ยงการพึ่งพา GDI+ แบบเนทีฟ หมายความว่าคุณสามารถปรับใช้โค้ดเดียวกันไปยังคอนเทนเนอร์, Azure App Service หรือ AWS Lambda โดยไม่ต้องใช้ไลบรารีเพิ่มเติม ไลบรารีนี้ยังมี **50+ image formats** และ **full alpha‑channel preservation** ทำให้เหมาะสำหรับการตัด PNG ที่โปร่งใสในปริมาณมาก

## “crop image to PNG” คืออะไร?

การดำเนินการ `crop image to PNG` จะสกัดส่วนสี่เหลี่ยมจาก bitmap ต้นฉบับและเขียนส่วนนั้นลงในไฟล์ PNG PNG จะคงไว้ซึ่งช่อง alpha ใด ๆ ให้การบีบอัดแบบ lossless ซึ่งทำให้ภาพที่ได้เหมาะสำหรับรูปย่อ, ไอคอน, สินทรัพย์ UI หรือสถานการณ์ใด ๆ ที่ต้องการคุณภาพและความโปร่งใส

## ทำไม Aspose.Drawing จึงเป็น Alternative to System.Drawing?

Aspose.Drawing ทำหน้าที่เป็นการแทนที่แบบ drop‑in สำหรับ System.Drawing โดยให้ความเข้ากันได้ข้ามแพลตฟอร์มเต็มรูปแบบ ลดความจำเป็นของไลบรารี GDI+ แบบเนทีฟ รองรับรูปแบบพิกเซลหลากหลาย ให้การจัดการภาพที่มีประสิทธิภาพสูง และรวมคุณสมบัติขั้นสูงเช่นการจัดการช่อง alpha และการสนับสนุนรูปแบบที่กว้าง ทำให้เหมาะสำหรับการแก้ไขง่าย ๆ และการประมวลผลเป็นชุดขนาดใหญ่

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม ให้แน่ใจว่าคุณมี:

- **Aspose.Drawing library** ที่รวมเข้าในโครงการ .NET ของคุณ คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/drawing/net/).  
- โฟลเดอร์ที่มีภาพต้นฉบับที่คุณต้องการตัด แทนที่ `"Your Document Directory"` ในโค้ดสแนปด้วยพาธจริงบนเครื่องของคุณ.

## นำเข้า Namespaces

`System.Drawing` namespace ให้เราเข้าถึง `Bitmap`, `Graphics` และประเภทที่เกี่ยวข้องที่ Aspose.Drawing ขยาย.

```csharp
using System.Drawing;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอน 1: สร้าง Bitmap Canvas

`Bitmap` คือการแสดงผลภาพในหน่วยความจำของ Aspose.Drawing ให้การเข้าถึงระดับพิกเซลและการควบคุมรูปแบบ  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

เราเริ่มด้วย canvas ว่างที่มีขนาดพอสำหรับผลลัพธ์ที่ตัด ปรับความกว้างและความสูงให้ตรงกับมิติของพื้นที่ที่คุณต้องการสกัด

### ขั้นตอน 2: สร้าง Graphics Object

`Graphics` คือพื้นผิวการวาดที่ให้คุณเรนเดอร์รูปทรง, ข้อความ หรือภาพอื่น ๆ ลงบน Bitmap  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` object ทำให้เราวาดลงบน canvas ได้ `InterpolationMode` ควบคุมวิธีการคำนวณค่าพิกเซลระหว่างการสเกลหรือการแปลง—`NearestNeighbor` ทำงานได้ดีสำหรับขอบที่คมชัด

### ขั้นตอน 3: โหลดภาพเพื่อทำการตัด

`Image` (หรือ `Bitmap`) โหลดไฟล์ต้นฉบับเข้าสู่หน่วยความจำ พร้อมสำหรับการจัดการ  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

โหลดภาพต้นฉบับ ตรวจสอบให้แน่ใจว่าพาธชี้ไปยังไฟล์ที่มีอยู่; มิฉะนั้นจะเกิดข้อยกเว้น

### ขั้นตอน 4: กำหนด Rectangle ของต้นฉบับและปลายทาง

`Rectangle` อธิบายส่วนของภาพต้นฉบับที่ต้องการเก็บและตำแหน่งที่ควรวางบน canvas ปลายทาง  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` บอก API ว่าส่วนใดของภาพต้นฉบับที่จะเก็บ ที่นี่เราเลือกพื้นที่ 50 × 40 พิกเซลที่มุมซ้ายบน โดยการกำหนด rectangle เดียวกันให้กับ `destinationRectangle` เราจะเก็บส่วนที่ตัดไว้ที่ขนาดเดิม

### ขั้นตอน 5: ดำเนินการตัด

`Graphics.DrawImage` คัดลอกส่วนที่กำหนดของ `image` ไปยัง `bitmap` ว่างของเรา  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` คัดลอกส่วนที่กำหนดของ `image` ไปยัง `bitmap` ว่างของเรา นี่คือการดำเนินการ **crop image to PNG** หลัก

### ขั้นตอน 6: บันทึกภาพที่ตัดแล้ว (Crop Image to PNG)

`Bitmap.Save` เขียน bitmap ในหน่วยความจำลงไฟล์โดยใช้รูปแบบที่ระบุ  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

สุดท้าย เขียน canvas ลงดิสก์เป็นไฟล์ PNG PNG จะคงช่อง alpha ใด ๆ และให้คุณภาพ lossless — เหมาะสำหรับสินทรัพย์ UI

## วิธีการตัดภาพเป็นชุดในลูป?

วนซ้ำแต่ละพาธไฟล์ด้วย `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))` ทำซ้ำขั้นตอน 1‑6 ภายในลูปและเก็บผลลัพธ์แต่ละไฟล์ในโฟลเดอร์เป้าหมาย รูปแบบนี้ขยายได้เชิงเส้น สามารถทำแบบขนานด้วย `Parallel.ForEach` เพื่อเพิ่มอัตราการทำงานและประมวลผลภาพได้อย่างมีประสิทธิภาพและรวดเร็ว

## ข้อผิดพลาดทั่วไป & เคล็ดลับ

- **Pixel format mismatches** – ตรวจสอบให้แน่ใจว่าภาพต้นฉบับและ bitmap ของ canvas มีรูปแบบพิกเซลที่เข้ากันได้เพื่อหลีกเลี่ยงการเปลี่ยนสี.  
- **Disposal of GDI objects** – ห่อ `Bitmap` และ `Graphics` ด้วยคำสั่ง `using` หรือเรียก `Dispose()` ด้วยตนเอง; มิฉะนั้นอาจทำให้รั่วของทรัพยากรที่ไม่ได้จัดการ.  
- **Coordinate errors** – พิกัดของ rectangle เริ่มจากศูนย์ การเลือก rectangle ที่เกินขอบของภาพต้นฉบับจะทำให้เกิดข้อยกเว้น.  

## คำถามที่พบบ่อย

**Q: ฉันสามารถตัดภาพของรูปแบบใดก็ได้โดยใช้ Aspose.Drawing?**  
A: ใช่, Aspose.Drawing รองรับรูปแบบหลากหลาย (PNG, JPEG, BMP, GIF, TIFF, ฯลฯ) ดังนั้นคุณสามารถตัดภาพเกือบทุกประเภทได้.

**Q: มีตัวเลือกการตัดขั้นสูงหรือไม่?**  
A: แน่นอน. คุณสามารถรวม `GraphicsPath`, `Matrix` transformations, หรือใช้คลาส `ImageProcessor` สำหรับการเลือกที่ซับซ้อนเช่นการตัดเป็นวงกลม.

**Q: ฉันสามารถทำการตัดหลายครั้งบนภาพเดียวได้หรือไม่?**  
A: ใช่. หลังจากการตัดครั้งแรก คุณสามารถใช้ bitmap ที่ได้เป็นแหล่งใหม่และทำซ้ำกระบวนการเพื่อเชื่อมต่อการตัดหลายครั้ง.

**Q: Aspose.Drawing เหมาะกับการประมวลผลภาพเป็นชุดหรือไม่?**  
A: แน่นอน. API ที่เบาและไม่มีการพึ่งพาเนทีฟทำให้เหมาะสำหรับการประมวลผลคอลเลกชันภาพขนาดใหญ่บนเซิร์ฟเวอร์.

**Q: ฉันจะขอรับการสนับสนุนสำหรับคำถามที่เกี่ยวกับ Aspose.Drawing ได้อย่างไร?**  
A: ไปที่ [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) เพื่อขอความช่วยเหลือและเชื่อมต่อกับชุมชน.

---

**อัปเดตล่าสุด:** 2026-05-19  
**ทดสอบกับ:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
