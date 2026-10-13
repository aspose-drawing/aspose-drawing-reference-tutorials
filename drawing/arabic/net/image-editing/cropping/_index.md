---
date: 2026-10-13
description: تعرف على كيفية قص الصور دفعيًا إلى PNG باستخدام Aspose.Drawing API، البديل
  متعدد المنصات لـ System.Drawing لمطوري .NET.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: دليل قص الصور – Aspose.Drawing
og_description: تعرف على كيفية قص الصور دفعيًا إلى PNG بسرعة باستخدام Aspose.Drawing،
  البديل متعدد المنصات لـ System.Drawing لمطوري .NET. اتبع إرشادات خطوة بخطوة لمعالجة
  ملفات متعددة بكفاءة.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: كيفية قص الصور دفعيًا إلى PNG مع Aspose.Drawing لـ .NET
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: كيفية قص الصور دفعيًا إلى PNG باستخدام Aspose.Drawing لـ .NET
url: /ar/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية قص الصور دفعيًا إلى PNG باستخدام Aspose.Drawing لـ .NET

إذا كنت بحاجة إلى **قص الصورة إلى PNG** بسرعة، وبشكل موثوق، وعلى نطاق واسع في بيئة .NET، فأنت في المكان الصحيح. في هذا الدرس سنستعرض الخطوات الدقيقة لتحميل صورة، تعريف منطقة القص، وحفظ النتيجة كملف PNG—كل ذلك باستخدام Aspose.Drawing، **بديل حديث لـ System.Drawing** يعمل عبر المنصات. ستشاهد أيضًا كيف يمكن توسيع تدفق الصورة الواحدة إلى خط أنابيب **قص دفعي** كامل.

## إجابات سريعة
- **ما المكتبة التي يجب أن أستخدمها؟** Aspose.Drawing لـ .NET (بديل كامل المميزات لـ System.Drawing.Common)  
- **كم يستغرق القص الأساسي؟** عادةً أقل من ثانية لصورة واحدة على معالج حديث  
- **هل يمكنني القص إلى PNG؟** نعم – احفظ الـ bitmap المقصوص كملف PNG (انظر الخطوة 6)  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتطوير؛ الترخيص التجاري مطلوب للإنتاج  
- **هل المعالجة الدفعية ممكنة؟** بالتأكيد – ضع نفس الخطوات داخل حلقة لمعالجة ملفات متعددة في ثوانٍ  

## كيفية قص الصور دفعيًا إلى PNG؟

حمّل كل ملف مصدر باستخدام `new Bitmap(path)`، أنشئ `Bitmap` فارغًا مطابقًا لمنطقة القص، ارسم المستطيل المحدد باستخدام `Graphics.DrawImage`، وأخيرًا استدعِ `Save("output.png", ImageFormat.Png)`. ضع هذه الأسطر الستة داخل حلقة `foreach` تتنقل عبر دليل، وستحصل على حل قص دفعي كامل يعالج عشرات الصور في ثوانٍ.

## لماذا نستخدم Aspose.Drawing للقص الدفعي؟

Aspose.Drawing يعمل على **Windows وLinux وmacOS**، يعالج **صورًا بأكثر من 500 بكسل في أقل من 0.5 ثانية** على معالج خادم نموذجي، ويدعم **أكثر من 50 تنسيق صورة** مع الحفاظ الكامل لقناة ألفا. وبما أنه يلغي الاعتماد على مكتبات GDI+ الأصلية، يمكنك نشر نفس الكود إلى حاويات، Azure App Service، أو AWS Lambda دون مكتبات إضافية، مما يجعله مثاليًا لأنابيب الصور على نطاق واسع.

## ما هو “قص الصورة إلى PNG”؟

عملية `crop image to PNG` تستخرج منطقة مستطيلة من bitmap المصدر وتكتب تلك المنطقة إلى ملف PNG. يحافظ PNG على أي قناة ألفا، ويقدم ضغطًا بدون فقد، مما يجعل الصورة الناتجة مثالية للصور المصغرة، الأيقونات، أصول واجهة المستخدم، أو أي حالة تتطلب جودة وشفافية.

## لماذا Aspose.Drawing بديل لـ System.Drawing؟

Aspose.Drawing يُعد بديلاً فوريًا لـ System.Drawing من خلال توفير توافق كامل عبر المنصات، وإلغاء الحاجة إلى مكتبات GDI+ الأصلية. يدعم مجموعة واسعة من صيغ البكسل، يقدم معالجة صور عالية الأداء، ويتضمن ميزات متقدمة مثل معالجة قناة ألفا ودعم صيغ واسع، مما يجعله مناسبًا لكل من التعديلات البسيطة والمعالجة الدفعية على نطاق كبير.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- **مكتبة Aspose.Drawing** مدمجة في مشروع .NET الخاص بك. يمكنك تنزيلها من [صفحة تحميل Aspose.Drawing](https://releases.aspose.com/drawing/net/).  
- مجلد يحتوي على الصور المصدرية التي تريد قصها. استبدل `"Your Document Directory"` في مقتطفات الشيفرة بالمسار الفعلي على جهازك.

## استيراد المساحات الاسمية

مساحة الاسم `System.Drawing` تُتيح لنا الوصول إلى `Bitmap` و`Graphics` والأنواع المرتبطة التي يوسعها Aspose.Drawing.

```csharp
using System.Drawing;
```

## دليل خطوة بخطوة

### الخطوة 1: إنشاء لوحة bitmap

`Bitmap` هو تمثيل Aspose.Drawing للصور في الذاكرة، يوفر وصولًا على مستوى البكسل وتحكمًا في الصيغة.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

نبدأ بلوحة فارغة بحجم يكفي لاستيعاب النتيجة المقصوصة. اضبط العرض والارتفاع لتطابق أبعاد المنطقة التي تخطط لاستخراجها.

### الخطوة 2: إنشاء كائن graphics

`Graphics` هو سطح الرسم الذي يتيح لك رسم أشكال أو نصوص أو صور أخرى على الـ Bitmap.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

كائن `Graphics` يسمح لنا بالرسم على اللوحة. يتحكم `InterpolationMode` في كيفية حساب قيم البكسل أثناء التحجيم أو التحويل—`NearestNeighbor` يعمل جيدًا للحواف الحادة.

### الخطوة 3: تحميل الصورة للقص

`Image` (أو `Bitmap`) يحمل الملف المصدر في الذاكرة، جاهزًا للتعديل.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

حمّل الصورة المصدر. تأكد من أن المسار يشير إلى ملف موجود؛ وإلا سيتم رمي استثناء.

### الخطوة 4: تعريف مستطيلات المصدر والوجهة

كائنات `Rectangle` تصف المنطقة من الصورة المصدر التي سيتم الاحتفاظ بها ومكان وضعها على لوحة الوجهة.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` يخبر الـ API أي جزء من الصورة الأصلية يجب الاحتفاظ به. هنا نختار المنطقة العلوية اليسرى بحجم 50 × 40 بكسل. بتعيين نفس المستطيل إلى `destinationRectangle`، نحافظ على المنطقة المقصوصة بحجمها الأصلي.

### الخطوة 5: تنفيذ عملية القص

`Graphics.DrawImage` ينسخ الجزء المحدد من `image` إلى الـ `bitmap` الفارغ الخاص بنا.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

هذه هي العملية الأساسية لـ **crop image to PNG**. الطريقة تحترم مستطيل المصدر وتكتب البكسلات المحددة فقط إلى الـ bitmap الوجهة.

### الخطوة 6: حفظ الصورة المقصوصة (crop image to PNG)

`Bitmap.Save` يكتب الـ bitmap الموجود في الذاكرة إلى ملف باستخدام الصيغة المحددة.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

أخيرًا، احفظ اللوحة على القرص كملف PNG. يحافظ PNG على أي قناة ألفا ويقدم جودة بدون فقد—مثالي لأصول واجهة المستخدم.

## كيفية قص الصور دفعيًا داخل حلقة؟

تكرّر كل مسار ملف باستخدام `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`، أعد تنفيذ الخطوات 1‑6 داخل الحلقة، واحفظ كل نتيجة في مجلد الهدف. هذا النمط يتوسع خطيًا، ويمكن موازاته باستخدام `Parallel.ForEach` للحصول على إنتاجية أسرع، ويعالج الصور بكفاءة وسرعة.

## الأخطاء الشائعة والنصائح

- **تعارض صيغ البكسل** – تأكد من أن الصورة المصدرية والـ bitmap المتطابقة تشتركان في صيغة بكسل متوافقة لتجنب تغير الألوان.  
- **إفلات كائنات GDI** – ضع `Bitmap` و`Graphics` داخل عبارات `using` أو استدعِ `Dispose()` يدويًا؛ وإلا قد تتسرب موارد غير مُدارة.  
- **أخطاء الإحداثيات** – إحداثيات المستطيل تبدأ من الصفر. اختيار مستطيل يتجاوز حدود الصورة المصدر سيؤدي إلى استثناء.

## الأسئلة المتكررة

**س: هل يمكنني قص صور بأي تنسيق باستخدام Aspose.Drawing؟**  
ج: نعم، يدعم Aspose.Drawing مجموعة واسعة من الصيغ (PNG, JPEG, BMP, GIF, TIFF, إلخ)، لذا يمكنك قص أي نوع صورة تقريبًا.

**س: هل توجد خيارات قص متقدمة؟**  
ج: بالتأكيد. يمكنك دمج `GraphicsPath`، وتحويلات `Matrix`، أو استخدام فئة `ImageProcessor` لعمليات قص أكثر تعقيدًا مثل القص الدائري.

**س: هل يمكنني تطبيق عمليات قص متعددة على صورة واحدة؟**  
ج: نعم. بعد أول قص، يمكنك إعادة استخدام الـ bitmap الناتج كمصدر جديد وتكرار العملية لسلسلة من القصات.

**س: هل Aspose.Drawing مناسب للمعالجة الدفعية للصور؟**  
ج: بالتأكيد. واجهته الخفيفة وخلوه من الاعتمادات الأصلية يجعله مثاليًا لمعالجة مجموعات صور كبيرة على الخوادم.

**س: كيف يمكنني الحصول على دعم للاستفسارات المتعلقة بـ Aspose.Drawing؟**  
ج: توجه إلى [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على المساعدة والتواصل مع المجتمع.

---

**آخر تحديث:** 2026-10-13  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [تحميل، تحويل BMP إلى PNG وتنسيقات أخرى باستخدام Aspose.Drawing](/drawing/net/image-editing/load-save/)
- [كيفية ترخيص Aspose.Drawing لـ .NET – كيفية ترخيص aspose.drawing](/drawing/net/licensing/)
- [كيفية رسم مستطيل – تحويل نظام الإحداثيات (تحويل الصفحة) باستخدام Aspose.Drawing API لـ .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}