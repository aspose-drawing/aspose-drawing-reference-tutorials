---
date: 2026-02-07
description: دليل خطوة بخطوة لقص الصورة إلى PNG باستخدام Aspose.Drawing، البديل لـ
  System.Drawing لمطوري .NET. يتضمن القص الدفعي والتقنيات الأساسية.
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: كيفية قص الصورة إلى PNG باستخدام Aspose.Drawing لـ .NET
url: /ar/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية قص الصورة إلى PNG باستخدام Aspose.Drawing لـ .NET

إذا كنت بحاجة إلى **crop image to PNG** بسرعة وموثوقية في بيئة .NET، فأنت في المكان الصحيح. في هذا الدرس سنستعرض الخطوات الدقيقة لتحميل صورة، تعريف منطقة القص، وحفظ النتيجة كملف PNG—كل ذلك باستخدام Aspose.Drawing، **alternative to System.Drawing** حديث يعمل عبر الأنظمة.

## إجابات سريعة
- **What library should I use?** Aspose.Drawing for .NET (a full‑featured alternative to System.Drawing.Common)  
- **How long does the basic crop take?** Usually under a second for a single image on a modern CPU  
- **Can I crop to PNG?** Yes – save the cropped bitmap as a PNG file (see Step 6)  
- **Do I need a license?** A free trial works for development; a commercial license is required for production  
- **Is batch processing possible?** Absolutely – wrap the same steps in a loop to process multiple files  

## ما هو “crop image to PNG”؟

قص الصورة يعني استخراج منطقة مستطيلة من الـ bitmap الأصلي. عندما تحفظ تلك المنطقة كملف PNG، تحتفظ بالشفافية وتستفيد من الضغط غير الفاقد—مثالي للصور المصغرة، الأيقونات، أو أي عنصر واجهة مستخدم.

## لماذا Aspose.Drawing هو بديل لـ System.Drawing؟

- **Cross‑platform support** – runs on Windows, Linux, and macOS without native GDI+ dependencies.  
- **Rich pixel‑format handling** – 32‑bit, 24‑bit, indexed, and more.  
- **Performance‑focused API** – ideal for both single‑image edits and large‑scale batch jobs.  

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود:

- **Aspose.Drawing library** مدمجة في مشروع .NET الخاص بك. يمكنك تنزيلها [here](https://releases.aspose.com/drawing/net/).  
- مجلد يحتوي على الصور المصدرية التي تريد قصها. استبدل `"Your Document Directory"` في مقتطفات الشيفرة بالمسار الفعلي على جهازك.

## استيراد المساحات الاسمية

```csharp
using System.Drawing;
```

مساحة الاسم `System.Drawing` تمنحنا الوصول إلى `Bitmap` و `Graphics` والأنواع ذات الصلة التي يوسعها Aspose.Drawing.

## دليل خطوة بخطوة

### الخطوة 1: إنشاء لوحة Bitmap

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

نبدأ بلوحة فارغة بحجم يكفي لاستيعاب النتيجة المقصوصة. عدّل العرض والارتفاع ليتطابقا مع أبعاد المنطقة التي تخطط لاستخراجها.

### الخطوة 2: إنشاء كائن Graphics

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

كائن `Graphics` يتيح لنا الرسم على اللوحة. `InterpolationMode` يتحكم في كيفية حساب قيم البكسل أثناء التحجيم أو التحويل—`NearestNeighbor` يعمل جيدًا للحواف الحادة.

### الخطوة 3: تحميل الصورة المراد قصها

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

حمّل الصورة المصدر. تأكد من أن المسار يشير إلى ملف موجود؛ وإلا سيُطرح استثناء.

### الخطوة 4: تعريف المستطيلات المصدرية والوجهة

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` يحدد للـ API أي جزء من الصورة الأصلية يجب الاحتفاظ به. هنا نختار المنطقة العلوية اليسرى بحجم 50 × 40 بكسل. بتعيين نفس المستطيل إلى `destinationRectangle`، نحافظ على حجم المنطقة المقصوصة كما هو.

### الخطوة 5: تنفيذ عملية القص

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` ينسخ الجزء المحدد من `image` إلى الـ `bitmap` الفارغ. هذه هي عملية **crop image to PNG** الأساسية.

### الخطوة 6: حفظ الصورة المقصوصة (Crop Image to PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

أخيرًا، اكتب اللوحة إلى القرص كملف PNG. PNG يحافظ على أي قناة ألفا ويوفر جودة غير فقدانية—مثالي لأصول الواجهة.

## كيفية قص الصور في سيناريو دفعي

عند وجود العشرات أو المئات من الصور، ضع المقتطف بالكامل داخل حلقة `foreach` تتكرر على مجموعة من مسارات الملفات. نفس منطق `Graphics.DrawImage` يُطبق، مما يجعل **batch image cropping** امتدادًا بسيطًا لهذا الدرس.

## المشكلات الشائعة والنصائح

- **Pixel format mismatches** – ensure the source image and the canvas bitmap share a compatible pixel format to avoid color shifts.  
- **Disposal of GDI objects** – wrap `Bitmap` and `Graphics` in `using` statements or call `Dispose()` manually; otherwise you may leak unmanaged resources.  
- **Coordinate errors** – rectangle coordinates are zero‑based. Selecting a rectangle that exceeds the source image bounds will raise an exception.  

## الأسئلة المتكررة

**س: هل يمكنني قص صور بأي تنسيق باستخدام Aspose.Drawing؟**  
ج: نعم، يدعم Aspose.Drawing مجموعة واسعة من التنسيقات (PNG, JPEG, BMP, GIF, TIFF, إلخ)، لذا يمكنك قص أي نوع صورة تقريبًا.

**س: هل تتوفر خيارات قص متقدمة؟**  
ج: بالتأكيد. يمكنك دمج `GraphicsPath`، وتحويلات `Matrix`، أو استخدام فئة `ImageProcessor` لعمليات اختيار أكثر تعقيدًا مثل القص الدائري.

**س: هل يمكنني تطبيق عمليات قص متعددة على صورة واحدة؟**  
ج: نعم. بعد أول قص، يمكنك إعادة استخدام الـ bitmap الناتج كمصدر جديد وتكرار العملية لسلسلة من القصات.

**س: هل Aspose.Drawing مناسب لمعالجة الصور دفعيًا؟**  
ج: بالفعل. API الخفيف الوزن وعدم الاعتماد على مكونات أصلية يجعله مثاليًا لمعالجة مجموعات صور كبيرة على الخوادم.

**س: كيف يمكنني الحصول على دعم لاستفسارات متعلقة بـ Aspose.Drawing؟**  
ج: توجه إلى [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) لطلب المساعدة والتواصل مع المجتمع.

---

**Last Updated:** 2026-02-07  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}