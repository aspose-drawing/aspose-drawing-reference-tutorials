---
date: 2026-03-02
description: เพิ่มความสวยงามให้กับภาพประกอบในเอกสารของคุณด้วย Aspose.Drawing สำหรับ
  .NET! เรียนรู้ขั้นตอนทีละขั้นตอนว่าต้องเพิ่มคำอธิบายเสริมอย่างไรเพื่อให้ภาพชัดเจนและให้ข้อมูลมากยิ่งขึ้น.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: วิธีเพิ่ม Callouts ด้วย Aspose.Drawing สำหรับ .NET
url: /th/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การสร้าง Callouts ใน Aspose.Drawing

## บทนำ
หากคุณกำลังสงสัย **วิธีการเพิ่ม callouts** ลงในภาพหรือไดอะแกรมของคุณโดยใช้ Aspose.Drawing สำหรับ .NET คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะอธิบายขั้นตอนทั้งหมด—from การโหลดภาพจนถึงการวาด callouts ที่มีสไตล์สวยงาม—เพื่อให้ภาพประกอบของคุณชัดเจนและให้ข้อมูลมากขึ้น.

## คำตอบอย่างรวดเร็ว
- **ต้องการไลบรารีอะไร?** Aspose.Drawing for .NET (downloadable from the official site).  
- **รองรับเวอร์ชัน .NET ใด?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **ต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีทำงานสำหรับการพัฒนา; ไลเซนส์เชิงพาณิชย์จำเป็นสำหรับการผลิต.  
- **ใช้เวลานานเท่าไหร่ในการทำงาน?** ปกติใช้เวลาน้อยกว่า 10 นาทีสำหรับ callout พื้นฐาน.  
- **สามารถปรับแต่งสีและฟอนต์ได้หรือไม่?** ใช่—ทุกอย่างถูกควบคุมโดยออบเจ็กต์มาตรฐานของ GDI+ (Pen, Font, Brush).

## วิธีการเพิ่ม Callouts ใน Aspose.Drawing
ด้านล่างเป็นคู่มือสั้น ๆ ทีละขั้นตอนที่แสดงอย่างชัดเจน **วิธีการเพิ่ม callouts** ลงในภาพ คุณสามารถคัดลอกโค้ด ทดลองตำแหน่งต่าง ๆ และปรับสไตล์ให้ตรงกับแบรนด์ของคุณได้ตามต้องการ.

## ข้อกำหนดเบื้องต้น
- ความรู้พื้นฐานของภาษาโปรแกรม C#.
- ไลบรารี Aspose.Drawing ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [here](https://releases.aspose.com/drawing/net/).
- เอกสารหรือภาพที่คุณต้องการเพิ่ม callouts.

## นำเข้า Namespaces
ตรวจสอบว่าคุณได้รวม namespaces ที่จำเป็นในโปรเจกต์ของคุณแล้ว:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## ขั้นตอนที่ 1: โหลดภาพ
เริ่มต้นด้วยการโหลดภาพที่คุณต้องการเพิ่ม callouts แทนที่ `"Your Document Directory"` และ `"gears.png"` ด้วยไดเรกทอรีและชื่อไฟล์ภาพของคุณจริง

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## ขั้นตอนที่ 2: สร้าง Graphics Object
สร้างออบเจ็กต์ `Graphics` จากภาพเพื่อทำการวาด.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## ขั้นตอนที่ 3: กำหนดตำแหน่ง Callout
กำหนดจุดเริ่มต้นและจุดสิ้นสุดสำหรับแต่ละ callout พร้อมกับค่าและหน่วยของ callout.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## ขั้นตอนที่ 4: วาด Callouts
ทำการ implement เมธอด `DrawCallOut` เพื่อวาด callouts บนภาพ.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## ขั้นตอนที่ 5: บันทึกภาพ
บันทึกภาพที่มี callouts ไปยังไดเรกทอรีที่คุณต้องการ.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## โค้ดต้นฉบับของ Draw Callout
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## ปัญหาและเคล็ดลับทั่วไป
- **พิกัด anchor ไม่ถูกต้อง** – ตรวจสอบให้แน่ใจว่าจุดเริ่มและจุดสิ้นสุดอยู่ภายในขอบเขตของภาพ; หากไม่เช่นนั้น callout อาจถูกตัด.  
- **ข้อความทับซ้อน** – ปรับ `spaceSize` หรือขนาดฟอนต์หากป้ายทับกับกราฟิกอื่น.  
- **ประสิทธิภาพ** – สำหรับภาพขนาดใหญ่มาก, พิจารณาเรียก dispose ออบเจ็กต์ `Pen`, `Font`, และ `Brush` หลังการใช้เพื่อคืนทรัพยากร.

## สรุป
ยินดีด้วย! ตอนนี้คุณรู้ **วิธีการเพิ่ม callouts** ลงในภาพโดยใช้ Aspose.Drawing สำหรับ .NET แล้ว คุณสามารถทดลองตำแหน่ง สี และฟอนต์ต่าง ๆ เพื่อให้ตรงกับสไตล์ภาพของคุณได้ตามต้องการ.

## คำถามที่พบบ่อย

### ฉันสามารถใช้ Aspose.Drawing สำหรับภาพประกอบประเภทอื่นได้หรือไม่?
ใช่, Aspose.Drawing รองรับการดำเนินการวาดที่หลากหลายสำหรับภาพประกอบประเภทต่าง ๆ.

### Aspose.Drawing รองรับรูปแบบภาพต่าง ๆ หรือไม่?
แน่นอน! Aspose.Drawing รองรับรูปแบบภาพที่นิยมเช่น PNG, JPEG, GIF, และอื่น ๆ.

### ฉันจะหา ตัวอย่างและเอกสารเพิ่มเติมได้จากที่ไหน?
สำรวจเอกสารที่ครอบคลุม [here](https://reference.aspose.com/drawing/net/).

### ฉันจะรับการสนับสนุนเมื่อพบปัญหาได้อย่างไร?
เยี่ยมชม [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) เพื่อรับการสนับสนุนจากชุมชน.

### ฉันสามารถทดลองใช้ Aspose.Drawing ก่อนซื้อได้หรือไม่?
แน่นอน! เริ่มต้นด้วยการทดลองใช้ฟรี [here](https://releases.aspose.com/).

**Q: ฉันสามารถเปลี่ยนสไตล์เส้น callout (dashed, dotted) ได้หรือไม่?**  
A: ใช่—เพียงกำหนดคุณสมบัติ `Pen.DashStyle` ก่อนวาดเส้น.

**Q: สามารถเพิ่มสีพื้นหลังให้กับป้าย callout ได้หรือไม่?**  
A: แน่นอน. สร้าง `SolidBrush` ด้วยสีที่ต้องการและเติมสี่เหลี่ยมผืนผ้าด้านหลังข้อความก่อนเรียก `DrawString`.

**Q: ฉันจะทำให้ callout แสดงผลเหมือนกันบนหน้าจอ high‑DPI ได้อย่างไร?**  
A: ตั้งค่า `graphics.PageUnit = GraphicsUnit.Pixel` (ตามที่แสดง) และใช้การวัดแบบเวกเตอร์เพื่อให้การสเกลคงที่.

---

**อัปเดตล่าสุด:** 2026-03-02  
**ทดสอบกับ:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}