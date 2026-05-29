---
date: 2026-05-29
description: เรียนรู้วิธีตั้งค่าใบอนุญาต Aspose.Drawing ใน .NET และลบลายน้ำ Aspose.
  เชี่ยวชาญวิธีการให้ใบอนุญาตเพื่อเปิดใช้งานคุณสมบัติเต็มรูปแบบโดยไม่มีลายน้ำ.
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
linktitle: การให้ใบอนุญาตใน Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  headline: Remove Aspose Watermark – Set Aspose.Drawing License
  type: TechArticle
- description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  name: Remove Aspose Watermark – Set Aspose.Drawing License
  steps:
  - name: Confirm Success
    text: '> **Pro tip:** Place the `.lic` file in the same folder as your executable
      or provide an absolute path to avoid “file not found” errors.'
  - name: Confirm Success
    text: '> **Warning:** Remember to dispose the `FileStream` (or use a `using` block)
      to free file handles.'
  - name: Display the Consumption Details
    text: '> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will
      fall back to trial mode and you’ll see watermarks in the output.'
  type: HowTo
- questions:
  - answer: Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.
    question: What is the primary way to activate Aspose.Drawing?
  - answer: Yes, you can load the license from a `Stream` for dynamic scenarios.
    question: Can I apply a license at runtime?
  - answer: Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable
      consumption‑based billing.
    question: Is a metered license supported?
  - answer: A trial works for testing, but a valid license removes watermarks and
      unlocks all APIs.
    question: Do I need a license for development builds?
  - answer: Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.
    question: Which .NET versions are compatible?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: ลบลายน้ำ Aspose – ตั้งค่าใบอนุญาต Aspose.Drawing
url: /th/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าใบอนุญาต Aspose.Drawing

## บทนำ

หากคุณกำลังสร้างแอปพลิเคชัน .NET ที่พึ่งพากราฟิกและการจัดการภาพที่มีประสิทธิภาพ การ **ตั้งค่าใบอนุญาต Aspose.Drawing** คือขั้นตอนแรกในการลบลายน้ำของ Aspose และเข้าถึงชุดฟีเจอร์เต็มรูปแบบ ในบทแนะนำนี้คุณจะได้เรียนรู้สามวิธีที่ใช้งานได้จริงในการตั้งค่าใบอนุญาต Aspose.Drawing — โหลดจากไฟล์, โหลดจากสตรีม, และใช้โมเดลการใช้งานตามมิเตอร์ — เพื่อให้คุณสามารถรวมไลบรารีได้อย่างมั่นใจและทำให้ผลลัพธ์ของคุณสะอาด

## คำตอบเร็ว
- **วิธีหลักในการเปิดใช้งาน Aspose.Drawing คืออะไร?** โหลดไฟล์ใบอนุญาตโดยใช้ `License.SetLicense("Aspose.Drawing.lic")`.  
- **ฉันสามารถใช้ใบอนุญาตในระหว่างการทำงานได้หรือไม่?** ได้ คุณสามารถโหลดใบอนุญาตจาก `Stream` สำหรับสถานการณ์แบบไดนามิก.  
- **รองรับใบอนุญาตแบบมิเตอร์หรือไม่?** แน่นอน; ใช้ `Metered.SetMeteredKey(publicKey, privateKey)` เพื่อเปิดใช้งานการเรียกเก็บตามการใช้งาน.  
- **ฉันต้องการใบอนุญาตสำหรับการสร้างเวอร์ชันพัฒนาหรือไม่?** เวอร์ชันทดลองทำงานสำหรับการทดสอบ แต่ใบอนุญาตที่ถูกต้องจะลบลายน้ำและเปิดใช้งาน API ทั้งหมด.  
- **เวอร์ชัน .NET ใดที่รองรับ?** Aspose.Drawing รองรับ .NET Framework 4.x, .NET Core 3.1+, และ .NET 5/6+.

## ข้อกำหนดเบื้องต้น

- **Aspose.Drawing Library** – ดาวน์โหลดแพคเกจล่าสุดจาก [here](https://releases.aspose.com/drawing/net/).  
- **License File** – รับไฟล์ `.lic` ที่ถูกต้องจาก [Aspose](https://purchase.aspose.com/buy).  
- **.NET Development Environment** – Visual Studio, Rider หรือ IDE ใด ๆ ที่รองรับ .NET Framework/.NET Core.

## นำเข้า Namespaces

เราต้องการ namespaces มาตรฐานของ .NET รวมถึง namespace ของ Aspose.Drawing สำหรับการตั้งค่าใบอนุญาต เพิ่มคำสั่ง `using` ต่อไปนี้ที่ส่วนบนของไฟล์ C# ของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## วิธีโหลดใบอนุญาตจากไฟล์?

`License` class แทนส่วนประกอบการให้ใบอนุญาตของ Aspose.Drawing ซึ่งเมื่อสร้างอินสแตนซ์แล้วจะทำให้คุณสามารถใช้ใบอนุญาตกับไลบรารีได้ การโหลดใบอนุญาตจากไฟล์เป็นวิธีที่ตรงไปตรงมาที่สุด; คุณเพียงแค่ชี้เมธอด `SetLicense` ไปที่ไฟล์ `.lic` แล้วไลบรารีจะลบลายน้ำทั้งหมดสำหรับช่วงเวลาที่เหลือของเซสชันแอปพลิเคชัน วิธีนี้ทำงานได้ทั้งในสภาพแวดล้อมเดสก์ท็อปและเซิร์ฟเวอร์และไม่ต้องการการกำหนดค่าเพิ่มเติมนอกจากการทำให้ไฟล์เข้าถึงได้ในระหว่างการทำงาน

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## วิธีโหลดใบอนุญาตจากสตรีม?

เมื่อไฟล์ใบอนุญาตฝังเป็นรีซอร์สหรือดึงมาจากเครือข่าย การโหลดมันจาก `Stream` จะให้ความยืดหยุ่นขณะยังคงรับประกันว่าลายน้ำจะถูกลบโดยการส่งอ็อบเจ็กต์ `Stream` ไปยังเมธอด `SetLicense` คุณจะทำให้ใบอนุญาตอยู่นอกโฟลเดอร์การปรับใช้ ซึ่งสามารถเพิ่มความปลอดภัยและทำให้การแจกจ่ายในคอนเทนเนอร์หรือคลาวด์ง่ายขึ้น กระบวนการนี้เหมือนกับการโหลดจากไฟล์ ยกเว้นว่าคุณต้องจัดการวงจรชีวิตของสตรีมเอง

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## วิธีเปิดใช้งานใบอนุญาตแบบมิเตอร์?

`Metered` class จัดการการเปิดใช้งานแบบมิเตอร์สำหรับ Aspose.Drawing ทำให้สามารถเรียกเก็บตามการใช้จริงได้ การให้ใบอนุญาตแบบมิเตอร์ทำให้คุณจ่ายเฉพาะสำหรับการดำเนินการที่ทำจริง ซึ่งเหมาะกับ SaaS หรือโมเดลจ่ายตามการใช้ หลังจากที่คุณระบุคีย์สาธารณะและส่วนตัว ทุกการเรียกใช้การประมวลผลภาพจะถูกติดตามและเรียกเก็บโดยอัตโนมัติ และไลบรารีจะทำงานในโหมดฟีเจอร์เต็มโดยไม่มีลายน้ำตลอดระยะเวลาของเซสชัน

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## ทำไมต้องตั้งค่าใบอนุญาต Aspose.Drawing อย่างถูกต้อง?

การตั้งค่าใบอนุญาตอย่างถูกต้องทำให้ไลบรารีทำงานในโหมดฟีเจอร์เต็ม, ลบลายน้ำของรุ่นทดลอง, และสอดคล้องกับเงื่อนไขการให้ใบอนุญาตของ Aspose. ใบอนุญาตที่ตั้งค่าอย่างเหมาะสมยังเปิดใช้งาน API พรีเมี่ยม, ปรับปรุงประสิทธิภาพโดยปิดการตรวจสอบการประเมิน, และให้คุณใช้การเรียกเก็บแบบมิเตอร์ได้ หากไม่โหลดใบอนุญาตก่อนการเรียก API ครั้งแรก ไลบรารีจะกลับไปทำงานในโหมดทดลอง ทำให้ภาพทั้งหมดที่สร้างมีลายน้ำ

- **ลบลายน้ำ** ที่ปรากฏในโหมดทดลอง.  
- **ปลดล็อก API พรีเมี่ยม** เช่น ฟิลเตอร์ภาพขั้นสูงและการแปลง PDF.  
- **รับประกันการปฏิบัติตาม** ข้อกำหนดการให้ใบอนุญาตของ Aspose สำหรับการจัดจำหน่ายเชิงพาณิชย์.  
- **เปิดใช้งานการเรียกเก็บแบบมิเตอร์**, ให้คุณจ่ายเฉพาะสิ่งที่ใช้.  

Aspose.Drawing รองรับ **รูปแบบภาพกว่า 30 ประเภท** (รวมถึง PNG, JPEG, BMP, TIFF, และ WebP) และสามารถประมวลผล **เอกสาร PDF หลายร้อยหน้าโดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ** ส่งมอบการแปลงที่มีประสิทธิภาพสูงบนฮาร์ดแวร์ระดับกลาง

## การโหลดใบอนุญาตจากไฟล์

การโหลดใบอนุญาตจากไฟล์เป็นวิธีที่ตรงไปตรงมาที่สุด ทำตามสามขั้นตอนต่อไปนี้:

### ขั้นตอนที่ 1: เริ่มต้นอ็อบเจ็กต์ License

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### ขั้นตอนที่ 2: ตั้งค่าใบอนุญาตจากไฟล์ `.lic`

```csharp
Console.WriteLine("License set successfully.");
```

### ขั้นตอนที่ 3: ยืนยันความสำเร็จ

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro tip:** วางไฟล์ `.lic` ไว้ในโฟลเดอร์เดียวกับไฟล์ executable ของคุณหรือระบุเส้นทางเต็มเพื่อหลีกเลี่ยงข้อผิดพลาด “file not found”.

## การโหลดใบอนุญาตจากสตรีม

เมื่อไฟล์ใบอนุญาตฝังเป็นรีซอร์สหรือดึงมาจากตำแหน่งระยะไกล การโหลดมันจาก `Stream` จะให้ความยืดหยุ่น

### ขั้นตอนที่ 1: เริ่มต้นอ็อบเจ็กต์ License

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### ขั้นตอนที่ 2: โหลดใบอนุญาตโดยใช้ `FileStream`

```csharp
Console.WriteLine("License set successfully.");
```

### ขั้นตอนที่ 3: ยืนยันความสำเร็จ

```csharp
Console.WriteLine("License set successfully.");
```

> **Warning:** อย่าลืมทำการ dispose `FileStream` (หรือใช้บล็อก `using`) เพื่อปล่อยตัวจัดการไฟล์

## การใช้ใบอนุญาตแบบมิเตอร์

การให้ใบอนุญาตแบบมิเตอร์เหมาะสำหรับ SaaS หรือโมเดลจ่ายตามการใช้ มันติดตามการใช้และเรียกเก็บตามการใช้งานจริง

### ขั้นตอนที่ 1: เริ่มต้นอ็อบเจ็กต์ Metered

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### ขั้นตอนที่ 2: ตั้งค่ากุญแจสาธารณะและส่วนตัว

```csharp
// Your image processing logic here
```

### ขั้นตอนที่ 3: ดำเนินการประมวลผลภาพของคุณ

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### ขั้นตอนที่ 4: ดึงข้อมูลการใช้

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### ขั้นตอนที่ 5: แสดงรายละเอียดการใช้

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Common pitfall:** หากคุณลืมเรียก `SetMeteredKey` API จะกลับไปทำงานในโหมดทดลองและคุณจะเห็นลายน้ำในผลลัพธ์.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| “License file not found” error | เส้นทางไม่ถูกต้องหรือไฟล์หายในโฟลเดอร์เอาต์พุต | ใช้เส้นทางแบบเต็มหรือกำหนดคุณสมบัติ *Copy to Output Directory* ของไฟล์เป็น *Copy always*. |
| ลายน้ำยังคงปรากฏหลังจากตั้งค่าใบอนุญาต | ใบอนุญาตไม่ได้โหลดก่อนเรียก API ครั้งแรก | โหลดใบอนุญาต **ก่อน** การดำเนินการ Aspose.Drawing ใด ๆ |
| การใช้แบบมิเตอร์เป็นศูนย์เสมอ | กุญแจไม่ได้ตั้งค่าหรือค่าตัวแปรสภาพแวดล้อมผิด | ตรวจสอบกุญแจสาธารณะ/ส่วนตัวและให้แน่ใจว่ามีการเชื่อมต่ออินเทอร์เน็ตกับเซิร์ฟเวอร์มิเตอร์ของ Aspose. |

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้ Aspose.Drawing โดยไม่ต้องมีใบอนุญาตได้หรือไม่?**  
A1: ได้, ใบอนุญาตทดลองทำงานสำหรับการพัฒนาและการประเมินผล, แต่จะเพิ่มลายน้ำและจำกัดบางฟีเจอร์.

**Q2: ฉันต้องต่ออายุใบอนุญาต Aspose.Drawing บ่อยแค่ไหน?**  
A2: ใบอนุญาตเป็นแบบถาวรสำหรับเวอร์ชันที่ซื้อไว้ การต่ออายุจำเป็นเฉพาะสำหรับการสนับสนุนและอัปเกรดเท่านั้น.

**Q3: ใบอนุญาตแบบมิเตอร์คืออะไรและควรใช้เมื่อใด?**  
A3: ใบอนุญาตแบบมิเตอร์เรียกเก็บตามการใช้ (การดำเนินการหรือข้อมูลที่ประมวลผล) เหมาะอย่างยิ่งสำหรับบริการคลาวด์หรือโมเดลจ่ายตามการใช้.

**Q4: ฉันสามารถใช้ Aspose.Drawing ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A4: แน่นอน—เมื่อคุณมีใบอนุญาตที่ถูกต้อง คุณสามารถฝัง Aspose.Drawing ลงในแอปพลิเคชันเชิงพาณิชย์ใด ๆ ได้.

**Q5: ฉันจะหาแหล่งสนับสนุนชุมชนสำหรับ Aspose.Drawing ได้จากที่ไหน?**  
A5: เยี่ยมชม [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) เพื่อรับความช่วยเหลือจากชุมชน, ตัวอย่าง, และการสนทนา.

## สรุป

การเชี่ยวชาญวิธี **ตั้งค่าใบอนุญาต Aspose.Drawing**—ไม่ว่าจะจากไฟล์, สตรีม, หรือผ่านการใช้งานแบบมิเตอร์—จะทำให้คุณใช้ประโยชน์สูงสุดจากไลบรารีกราฟิก .NET ที่ทรงพลังนี้พร้อมกับ **ลบลายน้ำของ Aspose** อย่างสมบูรณ์ ทำตามขั้นตอนข้างต้น, ระวังข้อผิดพลาดทั่วไป, แล้วคุณก็พร้อมสร้างโซลูชันการประมวลผลภาพที่แข็งแกร่งโดยไม่มีอุปสรรคด้านใบอนุญาต

---

**อัปเดตล่าสุด:** 2026-05-29  
**ทดสอบกับ:** Aspose.Drawing 24.11 for .NET  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [วิธีให้ใบอนุญาต Aspose.Drawing สำหรับ .NET – วิธีให้ใบอนุญาต aspose.drawing](/drawing/net/licensing/)
- [วิธีปรับขนาดภาพด้วย Aspose.Drawing สำหรับ .NET](/drawing/net/image-editing/scale/)
- [วิธีวาดข้อความและแบบอักษรด้วย Aspose.Drawing สำหรับ .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}