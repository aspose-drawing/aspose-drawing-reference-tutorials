---
date: 2025-12-06
description: เรียนรู้วิธีบันทึกไฟล์ภาพ PNG พร้อมการแสดงรายการฟอนต์ที่ติดตั้ง, แสดงตระกูลฟอนต์,
  สร้างกราฟิกจากบิตแมป, และวาดข้อความด้วยฟอนต์โดยใช้ Aspose.Drawing สำหรับ .NET.
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: บันทึกภาพ PNG และทำงานกับฟอนต์ที่ติดตั้งใน Aspose.Drawing
url: /th/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึกภาพ PNG และทำงานกับฟอนต์ที่ติดตั้งใน Aspose.Drawing

## บทนำ

หากคุณต้องการ **save PNG image** ที่แสดงข้อมูลเกี่ยวกับฟอนต์ที่ติดตั้งบนเครื่อง, Aspose.Drawing for .NET จะมอบวิธีที่สะอาดและข้ามแพลตฟอร์มให้คุณทำได้ ในบทเรียนนี้เราจะอธิบายการแสดงรายการฟอนต์ที่ติดตั้ง, การแสดงฟอนต์แฟมิลี่, การสร้างกราฟิกจาก bitmap, และการวาดข้อความด้วยฟอนต์ — ทั้งหมดนี้จบด้วยการบันทึกผลลัพธ์เป็นไฟล์ PNG เมื่อเสร็จคุณจะได้โค้ดสั้น ๆ ที่สามารถนำไปใช้ในโปรเจกต์ .NET ใดก็ได้

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้สร้างอะไร?** A PNG image that lists installed font families.  
- **ไลบรารีที่ต้องการคืออะไร?** Aspose.Drawing for .NET (no System.Drawing.Common needed).  
- **ฉันสามารถใช้ฟอนต์ที่กำหนดเองได้หรือไม่?** Yes – just load them into `InstalledFontCollection`.  
- **ความละเอียดของผลลัพธ์สามารถปรับได้หรือไม่?** Absolutely – change the bitmap size or pixel format.  
- **ฉันต้องมีลิขสิทธิ์เพื่อรันโค้ดหรือไม่?** A temporary license works for evaluation; a full license is required for production.

## “save PNG image” คืออะไรในบริบทของ Aspose.Drawing?
การบันทึกภาพ PNG หมายถึงการเรนเดอร์พื้นผิวการวาดของคุณ (เช่น `Bitmap`) ไปยังไฟล์ที่มีนามสกุล `.png` Aspose.Drawing จะจัดการการเข้ารหัสให้คุณเอง, ดังนั้นคุณเพียงแค่เรียก `bitmap.Save(...)` พร้อมระบุเส้นทางที่ต้องการ

## ทำไมต้องแสดงรายการฟอนต์ที่ติดตั้งและแสดงฟอนต์แฟมิลี่?
การรู้ว่าฟอนต์ใดบ้างที่พร้อมใช้งานทำให้คุณสร้างกราฟิกแบบไดนามิกที่ปรับให้เข้ากับสภาพแวดล้อมของผู้ใช้ปลายสุดได้ง่าย มันมีประโยชน์อย่างยิ่งสำหรับการสร้างรายงาน, ใบรับรอง, หรือเนื้อหาภาพใด ๆ ที่ต้องสอดคล้องกับแบรนด์ขององค์กรโดยไม่ต้องจัดส่งไฟล์ฟอนต์ไปด้วย

## ข้อกำหนดเบื้องต้น

- **Aspose.Drawing Library** – download the latest version from the [Aspose Drawing download page](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider, or any .NET‑compatible editor.  
- **ความรู้พื้นฐานของ C#** – you should be comfortable with classes, objects, and simple loops.

## นำเข้า Namespaces
เพื่อทำงานกับฟอนต์และกราฟิก, ให้นำเข้า namespaces เหล่านี้ที่ส่วนหัวของไฟล์ C# ของคุณ:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: สร้าง bitmap (ผ้าใบ)
ก่อนอื่นเราจะสร้าง bitmap ที่จะเก็บภาพสุดท้าย ขนาดและ pixel format ของ bitmap จะกำหนดคุณภาพของ PNG ที่บันทึก

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### ขั้นตอนที่ 2: สร้าง graphics จาก bitmap
ต่อไปเราจะรับอ็อบเจ็กต์ `Graphics` จาก bitmap อ็อบเจ็กต์นี้ช่วยให้เราวาดรูปทรง, ข้อความ, และภาพลงบนผ้าใบได้

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### ขั้นตอนที่ 3: ตั้งค่า brush และ font (วาดข้อความด้วยฟอนต์)
เราต้องการ brush สำหรับสีข้อความและอ็อบเจ็กต์ `Font` ที่กำหนดแบบอักษร, ขนาด, และสไตล์

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### ขั้นตอนที่ 4: แสดงรายการฟอนต์ที่ติดตั้งและแสดงฟอนต์แฟมิลี่
ตอนนี้เราจะแสดงจำนวนฟอนต์แฟมิลี่และชื่อบางส่วนโดยตรงบน bitmap ซึ่งเป็นการสาธิตความสามารถ **list installed fonts** และ **show font families**

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### ขั้นตอนที่ 5: บันทึก PNG image
สุดท้ายเราจะเขียน bitmap ลงดิสก์เป็นไฟล์ PNG ซึ่งเป็นการดำเนินการ **save png image** หลัก

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **เคล็ดลับ:** ใช้ `Path.Combine` เพื่อสร้างเส้นทางไฟล์เพื่อหลีกเลี่ยงปัญหาตัวคั่นโฟลเดอร์บนระบบปฏิบัติการต่าง ๆ.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **ไม่มีฟอนต์แสดงผล** | `InstalledFontCollection` ไม่ได้ถูกเติม (เช่น รันบนเซิร์ฟเวอร์ headless ที่ไม่มีฟอนต์). | Install the required fonts on the server or embed custom fonts in your application. |
| **ไฟล์ที่บันทึกเสียหาย** | Incorrect pixel format or missing write permissions. | Ensure the target folder exists and the app has write access; keep `Format32bppPArgb`. |
| **ข้อความดูเบลอ** | Low DPI settings. | Increase bitmap dimensions or set `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ฟอนต์ที่กำหนดเองที่ไม่ได้ติดตั้งบนเครื่องได้หรือไม่?**  
A: Yes. Load the font file into a `PrivateFontCollection` and create a `Font` from that collection.

**Q: ฉันจะจัดการกับข้อยกเว้นที่เกี่ยวกับฟอนต์อย่างไร?**  
A: Wrap font creation in a `try/catch` block and inspect `ArgumentException` for missing families.

**Q: Aspose.Drawing เหมาะกับแอปพลิเคชันเว็บหรือไม่?**  
A: Absolutely. The library works in ASP.NET Core, Azure Functions, and other server‑side environments.

**Q: ฉันสามารถเปลี่ยนสีหรือสไตล์ของข้อความได้หรือไม่?**  
A: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify the `FontStyle` enum.

**: จะหาลิขสิทธิ์ชั่วคราวสำหรับการทดสอบได้จากที่ไหน?**  
A: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).

## สรุป

โดยทำตามขั้นตอนเหล่านี้คุณได้เรียนรู้วิธี **save PNG image** ที่แสดง **list installed fonts**, **show font families**, **create graphics from bitmap**, และ **draw text with fonts** ด้วย Aspose.Drawing for .NET อย่าลังเลที่จะทดลองฟอนต์, สี, และขนาด bitmap อื่น ๆ เพื่อให้ตรงกับความต้องการด้านภาพของโปรเจกต์ของคุณ

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2025-12-06  
**ทดสอบกับ:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose