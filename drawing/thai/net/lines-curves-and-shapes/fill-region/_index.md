---
date: 2026-02-17
description: เรียนรู้วิธีเติมพื้นที่โดยใช้ Aspose.Drawing สำหรับ .NET, สร้างภาพไดนามิก,
  และสร้างพื้นที่จากรูปหลายเหลี่ยมด้วยโค้ดขั้นตอนต่อขั้นตอน.
linktitle: How to Fill Region in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: วิธีเติมพื้นที่ใน Aspose.Drawing สำหรับ .NET
url: /th/net/lines-curves-and-shapes/fill-region/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเติมพื้นที่ใน Aspose.Drawing

การสร้างกราฟิกที่สวยงามมักเกี่ยวข้องกับ **การเติมพื้นที่** ด้วยสี, ลวดลาย หรือไล่สี Aspose.Drawing สำหรับ .NET ให้ API ที่สะอาดและมีประสิทธิภาพสูงเพื่อจัดการงานนี้ ไม่ว่าคุณจะสร้างเครื่องมือรายงาน, เครื่องมือออกแบบ, หรือสร้างภาพแบบไดนามิกแบบเรียลไทม์ ในบทเรียนนี้คุณจะได้เห็น **วิธีเติมพื้นที่** อย่างละเอียด ตั้งแต่การตั้งค่า bitmap จนถึงการบันทึกรูปภาพขั้นสุดท้าย

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดจัดการการเติมพื้นที่?** Aspose.Drawing สำหรับ .NET  
- **เมธอดหลัก?** `Graphics.FillRegion` พร้อมกับ `Brush` และ `Region`  
- **สามารถสร้างภาพไดนามิกได้หรือไม่?** ได้ – API เดียวกันช่วยให้คุณสร้างภาพได้ในขณะรันไทม์  
- **ต้องการไลเซนส์สำหรับการใช้งานในโปรดักชันหรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์; มีรุ่นทดลองฟรีให้ใช้  
- **รองรับเวอร์ชัน .NET ใดบ้าง?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+

## “การเติมพื้นที่” ในการเขียนโปรแกรมกราฟิกคืออะไร?
การเติมพื้นที่หมายถึงการทาสีทุกพิกเซลที่อยู่ในรูปทรงที่กำหนด (เช่น โพลิกอน, วงรี, พาธที่กำหนดเอง) ด้วยแปรง (brush) แปรงนั้นอาจเป็นสีทึบ, ไล่สี, หรือแม้แต่เทกซ์เจอร์ ทำให้คุณควบคุมลักษณะการแสดงผลของพื้นที่ได้อย่างเต็มที่

## ทำไมต้องใช้ Aspose.Drawing สำหรับการเติมพื้นที่?
- **พฤติกรรมสม่ำเสมอ** บน .NET Framework, .NET Core, และ .NET 5/6 – ไม่มีข้อแตกต่างของแพลตฟอร์ม  
- **ประสิทธิภาพสูง** ด้วย pipeline การเรนเดอร์ที่ปรับแต่งมาเพื่อการสร้างภาพบนเซิร์ฟเวอร์  
- **API ครบถ้วน** รองรับพาธซับซ้อน, การยกเว้นรูปทรงภายใน, และแปรงขั้นสูง  
- **ไม่มีการพึ่งพาภายนอก** – ไม่ต้องใช้ GDI+ บนเซิร์ฟเวอร์ ทำให้การปรับใช้ง่ายขึ้น

## ข้อกำหนดเบื้องต้น

ก่อนจะเริ่มทำตามขั้นตอน โปรดตรวจสอบว่าคุณมี:

1. **Aspose.Drawing Library** – ดาวน์โหลดและติดตั้งเวอร์ชันล่าสุดจากเว็บไซต์อย่างเป็นทางการ คุณสามารถหาไลบรารีและเอกสารได้ [ที่นี่](https://reference.aspose.com/drawing/net/)  
2. **สภาพแวดล้อมการพัฒนา** – Visual Studio (รุ่นใดก็ได้) หรือ IDE .NET ที่คุณชื่นชอบ  
3. **โครงการ .NET** ที่ตั้งเป้าหมายเป็น .NET Framework 4.6+ หรือ .NET Core 3.1+

## นำเข้า Namespaces

เริ่มต้นด้วยการนำเข้า namespaces ที่มีคลาสกราฟิกที่เราจะใช้

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

ต่อไปเราจะเดินผ่านตัวอย่างเต็มรูปแบบโดยแบ่งเป็นขั้นตอนง่าย ๆ

## คู่มือแบบขั้นตอน

### ขั้นตอนที่ 1: สร้าง Bitmap และ Graphics Object
เราจะจัดสรร bitmap ที่ทำหน้าที่เป็นผ้าใบและรับอ็อบเจ็กต์ `Graphics` เพื่อวาดบนมัน

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

> **เคล็ดลับ:** การใช้ `Format32bppPArgb` จะให้ค่า alpha ที่ทำให้การผสมสีราบรื่นขึ้นเมื่อคุณใช้แปรงที่มีความโปร่งใสในภายหลัง

### ขั้นตอนที่ 2: กำหนด GraphicsPath และสร้าง Region
`GraphicsPath` ช่วยให้เราบรรยายรูปทรงที่ซับซ้อนได้ ที่นี่เราจะเพิ่มโพลิกอนที่มีลักษณะเป็นรูปเพชร

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

> นี่คือ **region จากโพลิกอน** ที่คุณกำลังมองหา `Region` ตอนนี้แทนพื้นที่ภายในของโพลิกอนนั้น

### ขั้นตอนที่ 3: ยกเว้นพื้นที่ภายใน
บ่อยครั้งที่คุณต้องการ “รู” ภายในรูปทรง เราจะสร้างสี่เหลี่ยมและยกเว้นออกจาก region หลัก

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

### ขั้นตอนที่ 4: เลือก Brush และเติม Region
เลือกแปรงใดก็ได้ที่คุณต้องการ ในตัวอย่างนี้เราใช้แปรงสีฟ้าแบบทึบ แต่คุณสามารถเปลี่ยนเป็น `LinearGradientBrush` หรือ `TextureBrush` เพื่อสร้างภาพไดนามิกที่มีภาพลักษณ์หลากหลายได้

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

### ขั้นตอนที่ 5: บันทึกรูปภาพที่ได้
สุดท้ายให้เขียน bitmap ลงดิสก์ ปรับเส้นทางให้ชี้ไปยังโฟลเดอร์ที่มีอยู่บนเครื่องของคุณ

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

## ปัญหาที่พบบ่อยและวิธีแก้
| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| **ภาพแสดงเป็นสีขาว** | Bitmap ไม่ได้บันทึกลงโฟลเดอร์ที่เขียนได้หรือ `Graphics` ไม่ได้ flush | ตรวจสอบให้แน่ใจว่าโฟลเดอร์มีอยู่และเรียก `graphics.Dispose()` หลังการวาด |
| **Region ไม่ยกเว้นรูปทรงภายใน** | ใช้ `Exclude` ก่อนที่ region จะถูกกำหนดครบ | เรียก `region.Exclude(innerPath);` **หลัง** สร้าง region ภายนอกเสร็จแล้วตามตัวอย่าง |
| **ประสิทธิภาพช้าบนภาพขนาดใหญ่** | ใช้ `PixelFormat.Format32bppArgb` (ไม่เป็น premultiplied) | เปลี่ยนเป็น `Format32bppPArgb` เพื่อการผสม alpha ที่เร็วขึ้น |

## คำถามที่พบบ่อย

**ถาม: สามารถใช้ Aspose.Drawing ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
ตอบ: ได้, Aspose.Drawing สามารถใช้ได้ทั้งในโครงการส่วนบุคคลและเชิงพาณิชย์ สำหรับรายละเอียดไลเซนส์ดูที่ [นี่](https://purchase.aspose.com/buy)

**ถาม: มีรุ่นทดลองฟรีหรือไม่?**  
ตอบ: มี, คุณสามารถเข้าถึงรุ่นทดลองฟรีได้ [ที่นี่](https://releases.aspose.com/)

**ถาม: จะขอรับการสนับสนุนสำหรับ Aspose.Drawing อย่างไร?**  
ตอบ: เยี่ยมชม [ฟอรั่ม Aspose.Drawing](https://forum.aspose.com/c/drawing/44) เพื่อรับความช่วยเหลือจากชุมชนและผู้เชี่ยวชาญ

**ถาม: สามารถสร้างภาพไดนามิกด้วย Aspose.Drawing ได้หรือไม่?**  
ตอบ: แน่นอน, Aspose.Drawing ช่วยให้คุณสร้างและจัดการภาพแบบไดนามิกในแอปพลิเคชัน .NET ของคุณ

**ถาม: มีไลเซนส์ชั่วคราวหรือไม่?**  
ตอบ: มี, สามารถขอรับไลเซนส์ชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

## สรุป

การเติมพื้นที่ด้วย Aspose.Drawing เป็นเทคนิคที่ตรงไปตรงมาแต่มีพลัง ช่วยให้คุณ **สร้างภาพไดนามิก**, สร้างรูปทรงกำหนดเอง, และผลิตกราฟิกที่ดูเป็นมืออาชีพโดยใช้โค้ด ทดลองใช้แปรง, ไล่สี, และพาธที่ซับซ้อนต่าง ๆ เพื่อเปิดศักยภาพเต็มที่ของไลบรารีนี้

---

**อัปเดตล่าสุด:** 2026-02-17  
**ทดสอบกับ:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}