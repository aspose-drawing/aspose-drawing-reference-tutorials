---
date: 2026-02-27
description: เรียนรู้วิธีสร้างภาพการ์ดวันเกิดโดยใช้ Aspose.Drawing สำหรับ .NET คู่มือนี้จะแสดงวิธีวาดข้อความบนภาพ
  การวางข้อความทับรูปภาพ และการเพิ่มคำบรรยายให้กับรูปถ่ายอย่างรวดเร็ว.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: วิธีสร้างภาพการ์ดวันเกิดด้วย Aspose.Drawing
url: /th/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีสร้างภาพการ์ดวันเกิดด้วย Aspose.Drawing

## บทนำ
ในโลกที่เปลี่ยนแปลงอย่างรวดเร็วของการพัฒนา .NET, Aspose.Drawing โดดเด่นในฐานะเครื่องมือที่ทรงพลังสำหรับการจัดการภาพอย่างง่ายดาย ไม่ว่าคุณจะต้องการ **สร้างภาพการ์ดวันเกิด**, เพิ่มลายน้ำ, หรือเพียงแค่วางข้อความบนรูปภาพ, บทแนะนำนี้จะพาคุณผ่านขั้นตอนที่แม่นยำในการวาดสตริงบนภาพด้วย C#. เมื่อจบคู่มือนี้คุณจะมีการ์ดวันเกิดส่วนบุคคลพร้อมแชร์

## คำตอบด่วน
- **ควรใช้ไลบรารีอะไร?** Aspose.Drawing for .NET  
- **ฉันสามารถเพิ่มคำบรรยายให้กับรูปภาพได้หรือไม่?** ใช่ – ใช้ `Graphics.DrawString` กับฟอนต์ที่กำหนดเอง.  
- **ต้องการใบอนุญาตสำหรับการใช้งานจริงหรือไม่?** ใช่, จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์.  
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **การดำเนินการใช้เวลานานเท่าไหร่?** ปกติใช้เวลาน้อยกว่า 10 นาทีสำหรับการ์ดแบบง่าย.

## การ์ดวันเกิดคืออะไร?
การ์ดวันเกิดเป็นภาพที่ปรับแต่งส่วนบุคคลซึ่งรวมรูปภาพพื้นหลังกับข้อความที่กำหนดเอง—เช่น คำอวยพร, ชื่อผู้รับ, หรือข้อความฉลอง. ด้วย Aspose.Drawing, คุณสามารถสร้างการ์ดเหล่านี้โดยอัตโนมัติโดยไม่ต้องใช้เครื่องมือออกแบบกราฟิกด้วยมือ

## ทำไมต้องใช้ Aspose.Drawing เพื่อวางข้อความบนรูปภาพ?
- **รองรับหลายแพลตฟอร์ม:** ทำงานบน Windows, Linux, และ macOS.  
- **API การวาดที่ครบครัน:** ควบคุมฟอนต์, สี, และการจัดวางได้เต็มที่.  
- **ไม่มีการพึ่งพาภายนอก:** แทนที่ `System.Drawing.Common` ด้วยไลบรารีที่จัดการเต็มรูปแบบ.  
- **ประสิทธิภาพสูง:** ปรับให้เหมาะกับการประมวลผลภาพจำนวนมาก.

## ข้อกำหนดเบื้องต้น
ก่อนจะลงลึกในบทแนะนำ, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

1. ไลบรารี Aspose.Drawing: ดาวน์โหลดและติดตั้งไลบรารี Aspose.Drawing จาก [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/).  
2. สภาพแวดล้อมการพัฒนา: สภาพแวดล้อมการพัฒนา .NET ที่ทำงานได้ เช่น Visual Studio หรือ Visual Studio Code, พร้อมติดตั้ง .NET 6 SDK หรือใหม่กว่า

ตอนนี้, เราจะเดินผ่านคู่มือขั้นตอนต่อขั้นตอนเพื่อเพิ่มข้อความลงในภาพและบันทึกเป็นการ์ดวันเกิด

## นำเข้า Namespaces
เริ่มต้นโดยนำเข้า namespaces ที่จำเป็นเข้าสู่โปรเจกต์ C# ของคุณ:

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## ขั้นตอนที่ 1: โหลดภาพ
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
ที่นี่, เราโหลดภาพจากเส้นทางไฟล์ที่ระบุและเริ่มต้นอ็อบเจ็กต์ graphics เพื่อการประมวลผลต่อไป

## ขั้นตอนที่ 2: ตั้งค่าคุณสมบัติของข้อความ
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
กำหนดคุณสมบัติของข้อความ เช่น สี, ฟอนต์, และการเว้นขอบ. ปรับพารามิเตอร์เหล่านี้ตามความต้องการออกแบบของคุณ

## ขั้นตอนที่ 3: วัดขนาดข้อความ
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
คำนวณขนาดที่ต้องการสำหรับข้อความโดยวัดแต่ละคำแยกกัน. วิธีนี้ทำให้การวางตำแหน่งถูกต้องและหลีกเลี่ยงการทับซ้อนของข้อความ

## ขั้นตอนที่ 4: วาดข้อความบนภาพ
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
ตอนนี้, วางตำแหน่งข้อความบนภาพตามขนาดที่คำนวณและวาดโดยใช้ฟอนต์และสีที่ระบุ

## ขั้นตอนที่ 5: บันทึกภาพ
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
บันทึกภาพที่แก้ไขลงในไดเรกทอรีที่คุณต้องการ. ไฟล์ที่ได้เป็นภาพการ์ดวันเกิดพร้อมส่ง

## กรณีการใช้งานทั่วไป & เคล็ดลับ
- **เพิ่มคำบรรยายให้กับรูปภาพ:** แทนที่ `text` ด้วยคำบรรยายที่คุณต้องการ เช่น “Celebrating 30 Years!”.  
- **วาดข้อความบน bitmap:** วิธีเดียวกันทำงานกับอ็อบเจ็กต์ `Bitmap` ที่สร้างจากศูนย์.  
- **วางหลายบรรทัด:** วนลูปผ่านอาร์เรย์ของสตริงและปรับพิกัด Y ของ `Rectangle` สำหรับแต่ละบรรทัด.  
- **เคล็ดลับระดับมืออาชีพ:** ใช้ `Graphics.SmoothingMode = SmoothingMode.AntiAlias` เพื่อการเรนเดอร์ข้อความที่เรียบเนียนยิ่งขึ้น

## สรุป
Aspose.Drawing ทำให้การจัดการภาพใน .NET ง่ายขึ้น, มอบชุดเครื่องมือที่แข็งแกร่งให้กับนักพัฒนา. การเพิ่มข้อความลงในภาพ—ไม่ว่าจะเพื่อ **สร้างภาพการ์ดวันเกิด**, **วาดสตริงบนภาพ**, หรือ **เพิ่มคำบรรยายให้กับรูปภาพ**—เป็นเพียงตัวอย่างหนึ่งของความหลากหลายในการจัดการองค์ประกอบกราฟิก

## คำถามที่พบบ่อย
### Aspose.Drawing รองรับรูปแบบภาพทั้งหมดหรือไม่?
Aspose.Drawing รองรับรูปแบบภาพหลากหลาย รวมถึงรูปแบบที่นิยมเช่น JPEG, PNG, และ GIF. ดูที่ [documentation](https://reference.aspose.com/drawing/net/) สำหรับรายการเต็ม

### ฉันสามารถใช้ Aspose.Drawing สำหรับโครงการเชิงพาณิชย์ได้หรือไม่?
ใช่, Aspose.Drawing เหมาะสำหรับโครงการส่วนบุคคลและเชิงพาณิชย์. รายละเอียดใบอนุญาตดูได้ที่ [purchase page](https://purchase.aspose.com/buy)

### มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่?
ใช่, คุณสามารถรับใบอนุญาตชั่วคราวสำหรับการทดสอบโดยไปที่ [Temporary License](https://purchase.aspose.com/temporary-license/)

### ฉันจะหาแหล่งสนับสนุนชุมชนสำหรับ Aspose.Drawing ได้จากที่ไหน?
เข้าร่วมกับชุมชนและรับการสนับสนุนได้ที่ [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)

### ฉันจะเริ่มต้นกับ Aspose.Drawing อย่างไร?
เริ่มต้นโดยดาวน์โหลดไลบรารีจาก [here](https://releases.aspose.com/drawing/net/) และสำรวจ [documentation](https://reference.aspose.com/drawing/net/) อย่างครบถ้วน

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-02-27  
**ทดสอบด้วย:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

---