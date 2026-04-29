---
date: 2026-02-07
description: บทเรียนแบบขั้นตอนต่อขั้นตอนในการตัดภาพเป็น PNG ด้วย Aspose.Drawing ซึ่งเป็นทางเลือกของ
  System.Drawing สำหรับนักพัฒนา .NET รวมถึงการตัดภาพเป็นชุดและเทคนิคสำคัญ
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: วิธีตัดภาพเป็น PNG ด้วย Aspose.Drawing สำหรับ .NET
url: /th/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีครอปรูปภาพเป็น PNG ด้วย Aspose.Drawing สำหรับ .NET

หากคุณต้องการ **crop image to PNG** อย่างรวดเร็วและเชื่อถือได้ในสภาพแวดล้อม .NET คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายขั้นตอนที่แน่นอนในการโหลดรูปภาพ, กำหนดพื้นที่ครอป, และบันทึกผลลัพธ์เป็นไฟล์ PNG — ทั้งหมดโดยใช้ Aspose.Drawing ซึ่งเป็น **alternative to System.Drawing** สมัยใหม่ที่ทำงานข้ามแพลตฟอร์ม

## คำตอบด่วน
- **ควรใช้ไลบรารีอะไร?** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **ใช้เวลาครอปพื้นฐานเท่าไหร่?** Usually under a second for a single image on a modern CPU  
- **ฉันสามารถครอปเป็น PNG ได้หรือไม่?** Yes – save the cropped bitmap as a PNG file (see Step 6)  
- **ฉันต้องการไลเซนส์หรือไม่?** A free trial works for development; a commercial license is required for production  
- **สามารถทำการประมวลผลแบบแบตช์ได้หรือไม่?** Absolutely – wrap the same steps in a loop to process multiple files  

## “crop image to PNG” คืออะไร?

การครอปรูปภาพหมายถึงการดึงส่วนสี่เหลี่ยมออกจากบิตแมพต้นฉบับ เมื่อคุณบันทึกส่วนนั้นเป็น PNG คุณจะรักษาความโปร่งใสและได้การบีบอัดแบบ lossless — เหมาะอย่างยิ่งสำหรับรูปย่อ, ไอคอน, หรือทรัพยากร UI ใด ๆ

## ทำไม Aspose.Drawing จึงเป็น Alternative to System.Drawing?

- **Cross‑platform support** – ทำงานบน Windows, Linux, และ macOS โดยไม่ต้องพึ่งพา native GDI+ dependencies.  
- **Rich pixel‑format handling** – 32‑bit, 24‑bit, indexed, and more.  
- **Performance‑focused API** – ideal for both single‑image edits and large‑scale batch jobs.  

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่ม, โปรดตรวจสอบว่าคุณมี:

- **Aspose.Drawing library** integrated into your .NET project. You can download it [here](https://releases.aspose.com/drawing/net/).  
- โฟลเดอร์ที่มีรูปภาพต้นฉบับที่คุณต้องการครอป แทนที่ `"Your Document Directory"` ในโค้ดด้วยเส้นทางจริงบนเครื่องของคุณ.

## นำเข้า Namespaces

```csharp
using System.Drawing;
```

Namespace `System.Drawing` ให้เราเข้าถึง `Bitmap`, `Graphics` และประเภทที่เกี่ยวข้องที่ Aspose.Drawing ขยายเพิ่ม.

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: สร้าง Bitmap Canvas

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

เราเริ่มด้วยแคนวาสเปล่า ที่มีขนาดพอสำหรับผลลัพธ์ที่ครอป ปรับความกว้างและความสูงให้ตรงกับมิติของพื้นที่ที่คุณต้องการดึงออก.

### ขั้นตอนที่ 2: สร้าง Graphics Object

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

`Graphics` object ช่วยให้เราวาดบนแคนวาสได้ `InterpolationMode` ควบคุมวิธีการคำนวณค่าพิกเซลระหว่างการสเกลหรือการแปลง — `NearestNeighbor` ทำงานได้ดีสำหรับขอบที่คมชัด.

### ขั้นตอนที่ 3: โหลดรูปภาพที่ต้องการครอป

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

โหลดรูปภาพต้นฉบับ ตรวจสอบให้แน่ใจว่าเส้นทางชี้ไปยังไฟล์ที่มีอยู่ มิฉะนั้นจะเกิดข้อยกเว้น.

### ขั้นตอนที่ 4: กำหนด Source และ Destination Rectangles

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` บอก API ว่าส่วนใดของรูปต้นฉบับที่จะเก็บ ที่นี่เราเลือกพื้นที่บนซ้ายขนาด 50 × 40 พิกเซล โดยการกำหนด rectangle เดียวกันให้กับ `destinationRectangle` เราจะคงขนาดเดิมของส่วนที่ครอป.

### ขั้นตอนที่ 5: ดำเนินการครอป

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` คัดลอกส่วนที่กำหนดของ `image` ไปยัง `bitmap` เปล่าของเรา นี่คือการดำเนินการ **crop image to PNG** หลัก.

### ขั้นตอนที่ 6: บันทึกรูปภาพที่ครอป (Crop Image to PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

สุดท้าย, เขียนแคนวาสลงดิสก์เป็นไฟล์ PNG PNG จะรักษาแชนแนลอัลฟาและให้คุณภาพ lossless — เหมาะสำหรับทรัพยากร UI.

## วิธีครอปรูปภาพในสถานการณ์แบตช์

เมื่อคุณมีรูปภาพหลายสิบหรือหลายร้อยรูป เพียงใส่โค้ดทั้งหมดภายในลูป `foreach` ที่วนผ่านคอลเลกชันของเส้นทางไฟล์เดียวกัน ตรรกะ `Graphics.DrawImage` เดียวกันจะใช้ได้ ทำให้ **batch image cropping** เป็นการขยายที่ง่ายดายของบทแนะนำนี้.

## ข้อผิดพลาดทั่วไปและเคล็ดลับ

- **Pixel format mismatches** – ตรวจสอบให้แน่ใจว่ารูปภาพต้นฉบับและ bitmap ของแคนวาสใช้ pixel format ที่เข้ากันเพื่อหลีกเลี่ยงการเปลี่ยนสี.  
- **Disposal of GDI objects** – ห่อ `Bitmap` และ `Graphics` ด้วย `using` หรือเรียก `Dispose()` ด้วยตนเอง; มิฉะนั้นอาจทำให้ทรัพยากรที่ไม่ได้จัดการรั่ว.  
- **Coordinate errors** – พิกัดของ rectangle เริ่มจากศูนย์ การเลือก rectangle ที่เกินขอบของรูปต้นฉบับจะทำให้เกิดข้อยกเว้น.  

## คำถามที่พบบ่อย

**Q: ฉันสามารถครอปรูปภาพทุกฟอร์แมตด้วย Aspose.Drawing ได้หรือไม่?**  
A: ใช่, Aspose.Drawing รองรับฟอร์แมตหลากหลาย (PNG, JPEG, BMP, GIF, TIFF, ฯลฯ) ดังนั้นคุณสามารถครอปรูปภาพเกือบทุกประเภทได้.

**Q: มีตัวเลือกการครอปขั้นสูงหรือไม่?**  
A: แน่นอน คุณสามารถรวม `GraphicsPath`, การแปลง `Matrix`, หรือใช้คลาส `ImageProcessor` สำหรับการเลือกที่ซับซ้อนเช่นการครอปเป็นวงกลม.

**Q: ฉันสามารถทำการครอปหลายครั้งบนรูปเดียวได้หรือไม่?**  
A: ได้ หลังจากการครอปครั้งแรก คุณสามารถใช้ bitmap ที่ได้เป็นแหล่งใหม่และทำซ้ำกระบวนการเพื่อเชื่อมต่อการครอปหลายครั้ง.

**Q: Aspose.Drawing เหมาะสำหรับการประมวลผลรูปภาพแบบแบตช์หรือไม่?**  
A: แน่นอน API ที่เบาและไม่มีการพึ่งพา native ทำให้เหมาะกับการประมวลผลคอลเลกชันรูปภาพขนาดใหญ่บนเซิร์ฟเวอร์.

**Q: ฉันจะขอรับการสนับสนุนสำหรับคำถามที่เกี่ยวกับ Aspose.Drawing ได้อย่างไร?**  
A: ไปที่ [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) เพื่อขอความช่วยเหลือและเชื่อมต่อกับชุมชน.

---

**อัปเดตล่าสุด:** 2026-02-07  
**ทดสอบกับ:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}