---
date: 2026-02-25
description: เรียนรู้วิธีวาดข้อความและสร้างภาพข้อความแบบไดนามิกด้วย Aspose.Drawing
  สำหรับ .NET คู่มือแบบทีละขั้นตอนนี้จะแสดงวิธีเพิ่มข้อความลงในบิตแมพ, วาดสตริงบนภาพ,
  และบันทึกบิตแมพเป็น PNG.
linktitle: How to Draw Text with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: วิธีวาดข้อความด้วย Aspose.Drawing สำหรับ .NET
url: /th/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีวาดข้อความด้วย Aspise.Drawing สำหรับ .NET

## บทนำ

ในคู่มือแบบขั้นตอนนี้คุณจะได้เรียนรู้ **วิธีวาดข้อความ** บนภาพโดยใช้ Aspose.Drawing สำหรับ .NET ไม่ว่าคุณต้องการสร้าง *ภาพข้อความแบบไดนามิก* เพิ่มข้อความลงในบิตแมปที่มีอยู่แล้ว หรือสร้างกราฟิกพร้อมฟอนต์ที่กำหนดเอง คู่มือนี้จะพาคุณผ่านทุกขั้นตอนเพื่อให้คุณเริ่มวาดข้อความได้ในไม่กี่นาที

## คำตอบอย่างรวดเร็ว
- **ไลบรารีที่ใช้คืออะไร?** Aspose.Drawing สำหรับ .NET  
- **งานหลักคืออะไร?** วาดข้อความบนภาพ (สร้างภาพพร้อมข้อความ)  
- **เมธอดสำคัญคืออะไร?** `Graphics.DrawString` (วาดสตริงบนภาพ)  
- **รูปแบบผลลัพธ์คืออะไร?** PNG (บันทึกบิตแมปเป็น PNG)  
- **ข้อกำหนดเบื้องต้นคืออะไร?** สภาพแวดล้อมการพัฒนา .NET และไลบรารี Aspose.Drawing  

## การวาดข้อความด้วย Aspose.Drawing คืออะไร?
Aspose.Drawing ให้ API ที่จัดการเต็มรูปแบบซึ่งจำลองโมเดล GDI+ แบบคลาสสิกพร้อมเพิ่มการสนับสนุนข้ามแพลตฟอร์ม มันช่วยให้คุณเรนเดอร์ข้อความ รูปร่าง และภาพคุณภาพสูงโดยไม่ต้องพึ่งพา System.Drawing.Common

## ทำไมต้องใช้ Aspose.Drawing เพื่อเพิ่มข้อความลงในภาพ?
- **ความน่าเชื่อถือข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux และ macOS  
- **การเรนเดอร์ขั้นสูง** – การทำแอนติอาลิอาสและการทำให้ข้อความเรียบเนียนระดับพิกเซลย่อยสำหรับผลลัพธ์คมชัด  
- **ไม่มีการพึ่งพาภายนอก** – ไลบรารีบรรจุทุกอย่างที่คุณต้องการเพื่อ *สร้างภาพพร้อมข้อความ*  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมี:

- **Aspose.Drawing สำหรับ .NET** – ดาวน์โหลดจาก [เอกสาร Aspose.Drawing](https://reference.aspose.com/drawing/net/)  
- **IDE ของ .NET** เช่น Visual Studio หรือ VS Code  

## นำเข้า Namespaces

เริ่มต้นโดยนำเข้า Namespaces ที่จำเป็น:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## ขั้นตอนที่ 1: สร้างอ็อบเจ็กต์ Bitmap และ Graphics

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

ที่นี่เราจะสร้าง `Bitmap` ที่จะเก็บภาพสุดท้ายและอ็อบเจ็กต์ `Graphics` ที่ให้เราวาดบนมัน การตั้งค่า anti‑aliasing จะทำให้ข้อความดูเรียบเนียน

## ขั้นตอนที่ 2: ตั้งค่า Brush, Pen, และ Font

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** กำหนดสีของข้อความ  
- **Pen** ใช้ในภายหลังเพื่อวาดสี่เหลี่ยมรอบข้อความ (ไม่บังคับ)  
- **Font** ระบุแบบอักษร, ขนาด, และสไตล์สำหรับการ *วาดสตริงบนภาพ*  

## ขั้นตอนที่ 3: กำหนดข้อความและ Rectangle

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` จะกำหนดตำแหน่งที่ข้อความจะถูกวาง ปรับค่าพิกัดและขนาดให้เหมาะกับการจัดวางของคุณ

## ขั้นตอนที่ 4: วาด Rectangle และข้อความ

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

ก่อนอื่นเราจะร่างพื้นที่ด้วยสี่เหลี่ยมสีน้ำเงิน แล้วเราจะ **เพิ่มข้อความลงในบิตแมป** โดยเรียก `DrawString` นี่คือหัวใจของ *การวาดข้อความ* บนภาพ

## ขั้นตอนที่ 5: บันทึกผลลัพธ์

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

ภาพจะถูกบันทึกเป็นไฟล์ PNG ซึ่งสอดคล้องกับความต้องการ *บันทึกบิตแมปเป็น PNG* แทนที่พาธตัวอย่างด้วยโฟลเดอร์จริงที่คุณต้องการเก็บไฟล์

## กรณีการใช้งานทั่วไป

- **สร้างใบรับรอง** พร้อมชื่อส่วนบุคคล  
- **สร้างภาพย่อที่มีลายน้ำ** สำหรับแกลเลอรีเว็บ  
- **สร้างแผนภูมิดินามิก** ที่รวมป้ายหรือคำอธิบาย  

## การแก้ไขปัญหาและเคล็ดลับ

- **ไม่พบฟอนต์?** ตรวจสอบว่าฟอนต์ได้ติดตั้งบนเครื่องโฮสต์หรือใช้คอลเลกชันฟอนต์ส่วนตัว  
- **ข้อความถูกตัด?** เพิ่มขนาดของ Rectangle หรือทำให้ขนาดฟอนต์เล็กลง  
- **กังวลเรื่องประสิทธิภาพ?** ใช้อ็อบเจ็กต์ `Graphics` เดียวกันสำหรับการวาดหลายครั้งเมื่อเป็นไปได้  

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ฟอนต์ที่กำหนดเองกับ Aspose.Drawing สำหรับ .NET ได้หรือไม่?

A1: ได้, คุณสามารถระบุฟอนต์ที่กำหนดเองเมื่อสร้างอ็อบเจ็กต์ `Font` ในโค้ดของคุณ

### Q2: ฉันจะเพิ่มเอฟเฟกต์ข้อความเช่น ตัวหนา หรือ ตัวเอียงได้อย่างไร?

A2: ปรับคุณสมบัติ `FontStyle` ของอ็อบเจ็กต์ `Font` ตัวอย่างเช่น ใช้ `FontStyle.Bold` สำหรับข้อความตัวหนา

### Q3: Aspose.Drawing รองรับ .NET Core หรือไม่?

A3: ใช่, Aspose.Drawing รองรับ .NET Core ทำให้คุณสามารถใช้ในแอปพลิเคชันข้ามแพลตฟอร์มได้

### Q4: ฉันสามารถวาดข้อความบนภาพที่มีอยู่แล้วได้หรือไม่?

A4: แน่นอน! โหลดภาพที่มีอยู่โดยใช้ `Bitmap.FromFile()` แล้วดำเนินการตามขั้นตอนการวาดข้อความต่อ

### Q5: มีฟอรั่มชุมชนสำหรับการสนับสนุน Aspose.Drawing หรือไม่?

A5: มี, คุณสามารถหาแหล่งสนับสนุนและอภิปรายปัญหาได้ที่ [ฟอรั่ม Aspose.Drawing](https://forum.aspose.com/c/drawing/44)

## คำถามที่พบบ่อย

**Q: ฉันจะเปลี่ยนรูปแบบผลลัพธ์เป็น JPEG ได้อย่างไร?**  
A: แทนที่ส่วนขยาย `.png` ด้วย `.jpg` ในเมธอด `Save` และอาจระบุ `ImageCodecInfo` สำหรับคุณภาพ JPEG

**Q: ฉันสามารถวาดข้อความหลายบรรทัดได้หรือไม่?**  
A: ได้, ใส่ตัวอักษรขึ้นบรรทัดใหม่ (`\n`) ในสตริงหรือใช้ `StringFormat` พร้อม `FormatFlags.LineLimit`

**Q: มีวิธีวัดขนาดข้อความก่อนวาดหรือไม่?**  
A: ใช้ `Graphics.MeasureString` เพื่อรับขนาดที่แม่นยำของข้อความที่เรนเดอร์

**Q: Aspose.Drawing รองรับอักขระ Unicode หรือไม่?**  
A: แน่นอน. ให้ใช้ฟอนต์ที่มี glyph ที่ต้องการและไลบรารีจะเรนเดอร์ได้อย่างถูกต้อง

**Q: เวอร์ชันของ Aspose.Drawing ที่ใช้ในการทดสอบคืออะไร?**  
A: ตัวอย่างถูกทดสอบด้วย Aspose.Drawing 24.11 สำหรับ .NET

---

**อัปเดตล่าสุด:** 2026-02-25  
**ทดสอบด้วย:** Aspose.Drawing 24.11 สำหรับ .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}