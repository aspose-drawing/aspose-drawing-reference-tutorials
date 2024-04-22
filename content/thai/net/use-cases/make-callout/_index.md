---
title: การสร้างคำบรรยายภาพใน Aspose. Drawing
linktitle: การสร้างคำบรรยายภาพใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: ปรับปรุงภาพประกอบเอกสารของคุณโดยใช้ Aspose. Drawing สำหรับ .NET! เรียนรู้วิธีเพิ่มคำบรรยายภาพทีละขั้นตอนเพื่อให้ได้ภาพที่ชัดเจนและให้ข้อมูลมากขึ้น
type: docs
weight: 10
url: /th/net/use-cases/make-callout/
---
## การแนะนำ
ยินดีต้อนรับสู่คำแนะนำทีละขั้นตอนของเราเกี่ยวกับการสร้างคำบรรยายภาพใน Aspose. Drawing สำหรับ .NET! หากคุณต้องการปรับปรุงภาพประกอบในเอกสารด้วยคำบรรยาย คุณมาถูกที่แล้ว ในบทช่วยสอนนี้ เราจะแบ่งกระบวนการออกเป็นขั้นตอนที่สามารถจัดการได้โดยใช้ไลบรารี Aspose. Drawing
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- ความรู้พื้นฐานเกี่ยวกับภาษาการเขียนโปรแกรม C#
-  ติดตั้งไลบรารี Aspose. Drawing แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/drawing/net/).
- เอกสารหรือรูปภาพที่คุณต้องการเพิ่มคำบรรยายภาพ
## นำเข้าเนมสเปซ
ตรวจสอบให้แน่ใจว่าคุณมีเนมสเปซที่จำเป็นรวมอยู่ในโปรเจ็กต์ของคุณ:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## ขั้นตอนที่ 1: โหลดรูปภาพ
 เริ่มต้นด้วยการโหลดรูปภาพที่คุณต้องการเพิ่มคำบรรยายภาพ แทนที่`"Your Document Directory"` และ`"gears.png"` ด้วยไดเร็กทอรีจริงและชื่อไฟล์รูปภาพของคุณ
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // รหัสของคุณที่นี่
}
```
## ขั้นตอนที่ 2: สร้างวัตถุกราฟิก
 สร้างก`Graphics` วัตถุจากรูปภาพเพื่อดำเนินการวาดภาพ
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## ขั้นตอนที่ 3: กำหนดตำแหน่งคำบรรยายภาพ
กำหนดจุดเริ่มต้นและจุดสิ้นสุดสำหรับไฮไลต์แต่ละรายการพร้อมกับค่าไฮไลต์และหน่วย
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
## ขั้นตอนที่ 4: วาดคำบรรยายภาพ
 ดำเนินการ`DrawCallOut` วิธีการวาดคำบรรยายภาพบนภาพ
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## ขั้นตอนที่ 5: บันทึกรูปภาพ
บันทึกภาพพร้อมคำบรรยายลงในไดเร็กทอรีที่คุณต้องการ
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## วาดซอร์สโค้ดคำบรรยายภาพ
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
## บทสรุป

ยินดีด้วย! คุณได้เพิ่มคำบรรยายภาพลงในรูปภาพของคุณสำเร็จแล้วโดยใช้ Aspose. Drawing สำหรับ .NET คุณสามารถทดลองใช้ตำแหน่งและค่าต่างๆ เพื่อปรับแต่งข้อความเสริมของคุณเพิ่มเติมได้

## คำถามที่พบบ่อย

### ฉันสามารถใช้ Aspose. Drawing กับภาพประกอบประเภทอื่นได้หรือไม่

ใช่ Aspose. Drawing รองรับการดำเนินการวาดภาพที่หลากหลายสำหรับภาพประกอบประเภทต่างๆ

### Aspose. Drawing เข้ากันได้กับรูปแบบรูปภาพที่แตกต่างกันหรือไม่

อย่างแน่นอน! Aspose. Drawing รองรับรูปแบบรูปภาพยอดนิยม เช่น PNG, JPEG, GIF และอื่นๆ

### ฉันจะหาตัวอย่างและเอกสารประกอบเพิ่มเติมได้ที่ไหน

 สำรวจเอกสารที่ครอบคลุม[ที่นี่](https://reference.aspose.com/drawing/net/).

### ฉันจะได้รับความช่วยเหลือได้อย่างไรหากฉันประสบปัญหา

 เยี่ยมชม[Aspose.กระดานสนทนาการวาดภาพ](https://forum.aspose.com/c/diagram/17) เพื่อสนับสนุนชุมชน

### ฉันสามารถลองใช้ Aspose. Drawing ก่อนซื้อได้หรือไม่

 แน่นอน! เริ่มต้นด้วยการทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).