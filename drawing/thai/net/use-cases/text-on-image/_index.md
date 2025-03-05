---
title: การเพิ่มข้อความบนรูปภาพใน Aspose. Drawing
linktitle: การเพิ่มข้อความบนรูปภาพใน Aspose. Drawing
second_title: Aspose. Drawing .NET API - ทางเลือกแทน System. Drawing.Common
description: สำรวจการรวมข้อความเข้ากับรูปภาพอย่างราบรื่นด้วย Aspose. Drawing สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการปรับแต่งภาพอย่างง่ายดาย ดาวน์โหลดเดี๋ยวนี้!
type: docs
weight: 12
url: /th/net/use-cases/text-on-image/
---
## การแนะนำ
ในโลกแบบไดนามิกของการพัฒนา .NET Aspose. Drawing โดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับจัดการรูปภาพได้อย่างง่ายดาย การเพิ่มข้อความลงในรูปภาพเป็นข้อกำหนดทั่วไป ไม่ว่าจะเป็นการใส่ลายน้ำ คำอธิบายประกอบ หรือการสร้างกราฟิกส่วนบุคคล ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้ประโยชน์จาก Aspose. Drawing เพื่อรวมข้อความเข้ากับรูปภาพของคุณได้อย่างราบรื่นโดยใช้ C#
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:
1.  Aspose. Drawing Library: ดาวน์โหลดและติดตั้งไลบรารี Aspose. Drawing จากไฟล์[Aspose. Drawing สำหรับเอกสาร .NET](https://reference.aspose.com/drawing/net/).
2. สภาพแวดล้อมการพัฒนา: มีสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้ รวมถึง Visual Studio หรือ IDE อื่น ๆ ที่เข้ากันได้
ตอนนี้ เรามาเริ่มด้วยคำแนะนำทีละขั้นตอนกันดีกว่า
## นำเข้าเนมสเปซ
เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## ขั้นตอนที่ 1: โหลดรูปภาพ
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
ที่นี่ เราโหลดรูปภาพจากพาธของไฟล์ที่ระบุ และเริ่มต้นออบเจ็กต์กราฟิกสำหรับการประมวลผลต่อไป
## ขั้นตอนที่ 2: ตั้งค่าคุณสมบัติข้อความ
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
กำหนดคุณสมบัติของข้อความ เช่น สี แบบอักษร และช่องว่างภายใน ปรับพารามิเตอร์เหล่านี้ตามความต้องการของคุณ
## ขั้นตอนที่ 3: วัดขนาดตัวอักษร
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
คำนวณขนาดที่ต้องการสำหรับข้อความโดยการวัดแต่ละคำแยกกัน เพื่อให้แน่ใจว่าตำแหน่งที่เหมาะสมและหลีกเลี่ยงการทับซ้อนกันของข้อความ
## ขั้นตอนที่ 4: วาดข้อความบนรูปภาพ
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
ตอนนี้ วางตำแหน่งข้อความบนรูปภาพตามขนาดที่คำนวณแล้ววาดโดยใช้แบบอักษรและสีที่ระบุ
## ขั้นตอนที่ 5: บันทึกรูปภาพ
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
บันทึกภาพที่แก้ไขไปยังไดเร็กทอรีที่คุณต้องการ
คำแนะนำทีละขั้นตอนนี้สาธิตขั้นตอนง่ายๆ ในการเพิ่มข้อความลงในรูปภาพโดยใช้ Aspose. Drawing สำหรับ .NET ทดลองใช้แบบอักษร สี และเนื้อหาข้อความที่แตกต่างกันเพื่อให้ได้เอฟเฟ็กต์ภาพที่ต้องการ
## บทสรุป
Aspose. Drawing ช่วยให้งานจัดการรูปภาพใน .NET ง่ายขึ้น ช่วยให้นักพัฒนามีชุดเครื่องมือที่มีประสิทธิภาพ การเพิ่มข้อความลงในรูปภาพเป็นเพียงตัวอย่างหนึ่งของความสามารถ ซึ่งแสดงให้เห็นถึงความเก่งกาจของไลบรารีในการจัดการองค์ประกอบกราฟิก
## คำถามที่พบบ่อย
### Aspose. Drawing เข้ากันได้กับทุกรูปแบบภาพหรือไม่
 Aspose. Drawing รองรับรูปแบบรูปภาพที่หลากหลาย รวมถึงรูปแบบยอดนิยม เช่น JPEG, PNG และ GIF อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/drawing/net/) สำหรับรายการทั้งหมด
### ฉันสามารถใช้ Aspose. Drawing สำหรับโครงการเชิงพาณิชย์ได้หรือไม่
ใช่ Aspose. Drawing เหมาะสำหรับทั้งโครงการส่วนตัวและเชิงพาณิชย์ สำหรับรายละเอียดใบอนุญาต โปรดไปที่[หน้าซื้อ](https://purchase.aspose.com/buy).
### ใบอนุญาตชั่วคราวมีไว้เพื่อการทดสอบหรือไม่
 ใช่ คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับการทดสอบได้โดยไปที่[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/).
### ฉันจะรับการสนับสนุนจากชุมชนสำหรับ Aspose. Drawing ได้ที่ไหน
 มีส่วนร่วมกับชุมชนและได้รับการสนับสนุนใน[Aspose.กระดานสนทนาการวาดภาพ](https://forum.aspose.com/c/diagram/17).
### ฉันจะเริ่มต้นใช้งาน Aspose. Drawing ได้อย่างไร
 เริ่มต้นด้วยการดาวน์โหลดไลบรารี่จาก[ที่นี่](https://releases.aspose.com/drawing/net/) และสำรวจอย่างครอบคลุม[เอกสารประกอบ](https://reference.aspose.com/drawing/net/).