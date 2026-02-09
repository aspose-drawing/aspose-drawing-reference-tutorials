---
date: 2026-02-09
description: เรียนรู้วิธีตั้งค่าไลเซนส์ Aspose.Drawing ใน .NET ให้เชี่ยวชาญวิธีการจัดการไลเซนส์เพื่อเปิดใช้งานฟีเจอร์เต็มรูปแบบโดยไม่มีลายน้ำ.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: ตั้งค่าใบอนุญาต Aspose.Drawing – วิธีตั้งค่าใบอนุญาต Aspose.Drawing
url: /th/net/licensing/licensing/
weight: 10
---

 produce final output with translated content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าใบอนุญาต Aspose.Drawing

## บทนำ

หากคุณกำลังสร้างแอปพลิเคชัน .NET ที่พึ่งพากราฟิกและการจัดการภาพที่ทรงพลัง, **การตั้งค่าใบอนุญาต Aspose.Drawing** เป็นขั้นตอนแรกในการลบข้อจำกัดของการประเมินและเข้าถึงชุดคุณสมบัติเต็มรูปแบบ ในบทเรียนนี้คุณจะได้เรียนรู้สามวิธีที่ใช้งานได้จริงในการตั้งค่าใบอนุญาต Aspose.Drawing—การโหลดจากไฟล์, การโหลดจากสตรีม, และการใช้โมเดลการใช้งานตามมิเตอร์—เพื่อให้คุณสามารถรวมไลบรารีได้อย่างมั่นใจ.

## คำตอบด่วน
- **วิธีหลักในการเปิดใช้งาน Aspose.Drawing คืออะไร?** โหลดไฟล์ใบอนุญาตโดยใช้ `License.SetLicense("Aspose.Drawing.lic")`.  
- **ฉันสามารถใช้ใบอนุญาตในขณะรันไทม์ได้หรือไม่?** ได้, คุณสามารถโหลดใบอนุญาตจาก `Stream` สำหรับสถานการณ์ที่เปลี่ยนแปลงได้.  
- **รองรับใบอนุญาตแบบมิเตอร์หรือไม่?** แน่นอน; ใช้ `Metered.SetMeteredKey(publicKey, privateKey)` เพื่อเปิดใช้งานการเรียกเก็บตามการใช้งาน.  
- **ฉันต้องการใบอนุญาตสำหรับการสร้างเวอร์ชันพัฒนาไหม?** รุ่นทดลองใช้ได้สำหรับการทดสอบ, แต่ใบอนุญาตที่ถูกต้องจะลบลายน้ำและปลดล็อก API ทั้งหมด.  
- **เวอร์ชัน .NET ใดที่เข้ากันได้?** Aspose.Drawing รองรับ .NET Framework 4.x, .NET Core 3.1+, และ .NET 5/6+.

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่ม, ตรวจสอบให้แน่ใจว่าคุณมี:

- **Aspose.Drawing Library** – ดาวน์โหลดแพคเกจล่าสุดจาก [here](https://releases.aspose.com/drawing/net/).  
- **License File** – รับไฟล์ `.lic` ที่ถูกต้องจาก [Aspose](https://purchase.aspose.com/buy).  
- **.NET Development Environment** – Visual Studio, Rider, หรือ IDE ใด ๆ ที่รองรับ .NET Framework/.NET Core.

## นำเข้า Namespaces

เราต้องการ namespaces ของ .NET มาตรฐานพร้อมกับ namespace ของ Aspose.Drawing สำหรับการตั้งค่าใบอนุญาต เพิ่มคำสั่ง `using` ต่อไปนี้ที่ส่วนบนของไฟล์ C# ของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## การโหลดใบอนุญาตจากไฟล์

การโหลดใบอนุญาตจากไฟล์เป็นวิธีที่ตรงไปตรงมาที่สุด. ทำตามสามขั้นตอนต่อไปนี้:

### ขั้นตอนที่ 1: สร้างอ็อบเจกต์ License

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### ขั้นตอนที่ 2: ตั้งค่าใบอนุญาตจากไฟล์ `.lic`

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### ขั้นตอนที่ 3: ยืนยันความสำเร็จ

```csharp
Console.WriteLine("License set successfully.");
```

> **เคล็ดลับ:** วางไฟล์ `.lic` ไว้ในโฟลเดอร์เดียวกับไฟล์ executable ของคุณหรือระบุเส้นทางแบบเต็มเพื่อหลีกเลี่ยงข้อผิดพลาด “file not found”.

## การโหลดใบอนุญาตจาก Stream

เมื่อไฟล์ใบอนุญาตของคุณฝังเป็น resource หรือดึงมาจากตำแหน่งระยะไกล, การโหลดจาก `Stream` จะให้ความยืดหยุ่น.

### ขั้นตอนที่ 1: สร้างอ็อบเจกต์ License

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### ขั้นตอนที่ 2: โหลดใบอนุญาตโดยใช้ `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### ขั้นตอนที่ 3: ยืนยันความสำเร็จ

```csharp
Console.WriteLine("License set successfully.");
```

> **คำเตือน:** จำไว้ว่าต้องทำการ dispose `FileStream` (หรือใช้บล็อก `using`) เพื่อปล่อยไฟล์แฮนด์เดิล.

## การใช้ใบอนุญาตแบบมิเตอร์

ใบอนุญาตแบบมิเตอร์เหมาะสำหรับ SaaS หรือสถานการณ์จ่ายตามการใช้จริง. มันติดตามการใช้งานและเรียกเก็บเงินตามการใช้จริง.

### ขั้นตอนที่ 1: สร้างอ็อบเจกต์ Metered

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### ขั้นตอนที่ 2: ตั้งค่า Public และ Private Keys

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### ขั้นตอนที่ 3: ดำเนินการประมวลผลภาพของคุณ

```csharp
// Your image processing logic here
```

### ขั้นตอนที่ 4: ดึงข้อมูลการใช้งาน

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### ขั้นตอนที่ 5: แสดงรายละเอียดการใช้งาน

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **ข้อผิดพลาดทั่วไป:** หากคุณลืมเรียก `SetMeteredKey`, API จะกลับไปใช้โหมดทดลองและคุณจะเห็นลายน้ำในผลลัพธ์.

## ทำไมต้องตั้งค่าใบอนุญาต Aspose.Drawing อย่างถูกต้อง?

- **ลบลายน้ำ** ที่ปรากฏในโหมดทดลอง.  
- **ปลดล็อก API ระดับพรีเมี่ยม** เช่น ฟิลเตอร์ภาพขั้นสูงและการแปลงเป็น PDF.  
- **รับประกันการปฏิบัติตาม** ข้อกำหนดการให้ใบอนุญาตของ Aspose สำหรับการแจกจ่ายเชิงพาณิชย์.  
- **เปิดใช้งานการเรียกเก็บแบบมิเตอร์**, ทำให้คุณจ่ายเฉพาะที่ใช้.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|-----|
| “License file not found” error | เส้นทางไม่ถูกต้องหรือไฟล์หายในโฟลเดอร์ผลลัพธ์ | ใช้เส้นทางแบบเต็มหรือกำหนดคุณสมบัติ *Copy to Output Directory* ของไฟล์เป็น *Copy always*. |
| ลายน้ำยังคงปรากฏหลังตั้งค่าใบอนุญาต | ใบอนุญาตไม่ได้โหลดก่อนการเรียก API ครั้งแรก | โหลดใบอนุญาต **ก่อน** การดำเนินการ Aspose.Drawing ใด ๆ. |
| การใช้งานแบบมิเตอร์เป็นศูนย์เสมอ | คีย์ไม่ได้ตั้งค่าหรือค่าตัวแปรสภาพแวดล้อมผิด | ตรวจสอบ public/private keys และให้แน่ใจว่ามีการเชื่อมต่ออินเทอร์เน็ตกับเซิร์ฟเวอร์มิเตอร์ของ Aspose. |

## คำถามที่พบบ่อย

**Q1: ฉันสามารถใช้ Aspose.Drawing โดยไม่มีใบอนุญาตได้หรือไม่?**  
A1: ใช่, ใบอนุญาตทดลองสามารถใช้สำหรับการพัฒนาและการประเมิน, แต่จะเพิ่มลายน้ำและจำกัดบางฟีเจอร์.

**Q2: ฉันต้องต่ออายุใบอนุญาต Aspose.Drawing บ่อยแค่ไหน?**  
A2: ใบอนุญาตเป็นแบบถาวรสำหรับเวอร์ชันที่ซื้อ. การต่ออายุจำเป็นเฉพาะสำหรับการสนับสนุนและอัปเกรดเท่านั้น.

**Q3: ใบอนุญาตแบบมิเตอร์คืออะไรและควรใช้เมื่อใด?**  
A3: ใบอนุญาตแบบมิเตอร์เรียกเก็บตามการใช้งาน (การดำเนินการหรือข้อมูลที่ประมวลผล). เหมาะสำหรับบริการคลาวด์หรือโมเดลจ่ายตามการใช้.

**Q4: ฉันสามารถใช้ Aspose.Drawing ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A4: แน่นอน—เมื่อคุณมีใบอนุญาตที่ถูกต้อง, คุณสามารถฝัง Aspose.Drawing ในแอปพลิเคชันเชิงพาณิชย์ใด ๆ ได้.

**Q5: ฉันจะหาการสนับสนุนจากชุมชนสำหรับ Aspose.Drawing ได้จากที่ไหน?**  
A5: เยี่ยมชม [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) เพื่อรับความช่วยเหลือจากชุมชน, ตัวอย่าง, และการสนทนา.

## สรุป

การเชี่ยวชาญวิธี **ตั้งค่าใบอนุญาต Aspose.Drawing**—ไม่ว่าจะจากไฟล์, สตรีม, หรือผ่านการใช้งานแบบมิเตอร์—จะทำให้คุณใช้ประโยชน์สูงสุดจากไลบรารีกราฟิก .NET ที่ทรงพลังนี้. ทำตามขั้นตอนข้างต้น, ระวังข้อผิดพลาดทั่วไป, และคุณจะพร้อมสร้างโซลูชันการประมวลผลภาพที่แข็งแกร่งโดยไม่มีอุปสรรคด้านใบอนุญาต.

---

**Last Updated:** 2026-02-09  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}