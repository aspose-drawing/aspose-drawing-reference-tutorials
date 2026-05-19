---
date: 2026-05-19
description: دليل خطوة بخطوة حول كيفية قص الصور دفعيًا إلى PNG باستخدام Aspose.Drawing،
  البديل عن System.Drawing لمطوري .NET.
keywords:
- how to batch crop
- crop image to png
- alternative to system drawing
- batch image cropping .net
linktitle: دورة قص الصور – Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  headline: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  type: TechArticle
- description: Step‑by‑step tutorial on how to batch crop images to PNG using Aspose.Drawing,
    the alternative to System.Drawing for .NET developers.
  name: How to Batch Crop Images to PNG Using Aspose.Drawing for .NET
  steps:
  - name: Create a Bitmap Canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a Graphics Object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the Image to Crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define Source and Destination Rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the Crop Operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. `Graphics.DrawImage` copies the defined portion of `image` onto our
      blank `bitmap`. This is the core **crop image to PNG** operation.'
  - name: Save the Cropped Image (Crop Image to PNG)
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
title: كيفية قص الصور دفعيًا إلى PNG باستخدام Aspose.Drawing لـ .NET
url: /ar/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية قص الصور دفعيًا إلى PNG باستخدام Aspose.Drawing لـ .NET

إذا كنت بحاجة إلى **قص صورة إلى PNG** بسرعة، وبشكل موثوق، وعلى نطاق واسع في بيئة .NET، فأنت في المكان الصحيح. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة لتحميل صورة، تعريف منطقة القص، وحفظ النتيجة كملف PNG—كل ذلك باستخدام Aspose.Drawing، وهو **بديل حديث لـ System.Drawing** يعمل عبر الأنظمة. سترى أيضًا كيف يمكنك توسيع تدفق الصورة الفردية إلى خط أنابيب **قص دفعي** كامل.

## إجابات سريعة
- **ما المكتبة التي يجب أن أستخدمها؟** Aspose.Drawing لـ .NET (بديل كامل المميزات لـ System.Drawing.Common)  
- **كم يستغرق القص الأساسي؟** عادةً أقل من ثانية لصورة واحدة على معالج حديث  
- **هل يمكن القص إلى PNG؟** نعم – احفظ الـ bitmap المقصوص كملف PNG (انظر الخطوة 6)  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتطوير؛ الترخيص التجاري مطلوب للإنتاج  
- **هل المعالجة الدفعية ممكنة؟** بالتأكيد – غلف نفس الخطوات داخل حلقة لمعالجة ملفات متعددة  

## كيفية قص الصور دفعيًا إلى PNG؟

حمّل كل ملف مصدر باستخدام `new Bitmap(path)`، أنشئ `Bitmap` فارغًا مطابقًا لمنطقة القص، ارسم المستطيل المحدد باستخدام `Graphics.DrawImage`، وأخيرًا استدعِ `Save("output.png", ImageFormat.Png)`. ضع هذه السطور الست داخل حلقة `foreach` تتنقل عبر دليل وستحصل على حل قص دفعي كامل يعالج عشرات الصور في ثوانٍ.

## لماذا نستخدم Aspose.Drawing للقص الدفعي؟

يدعم Aspose.Drawing **3 أنظمة تشغيل رئيسية** (Windows، Linux، macOS) ويمكنه معالجة **صور بأكثر من 500 بكسل في أقل من 0.5 ثانية** على خادم عادي. API الخاص به يتجنب الاعتماد على مكتبات GDI+ الأصلية، مما يعني أنه يمكنك نشر نفس الكود إلى حاويات، Azure App Service، أو AWS Lambda دون مكتبات إضافية. كما يقدم المكتبة **أكثر من 50 صيغة صورة** و**حفظ كامل لقناة ألفا**، مما يجعلها مثالية لقص PNG شفاف على نطاق واسع.

## ما هو “crop image to PNG”؟

عملية `crop image to PNG` تستخرج منطقة مستطيلة من bitmap المصدر وتكتب تلك المنطقة إلى ملف PNG. يحافظ PNG على أي قناة ألفا، ويوفر ضغطًا بدون فقد، مما يجعل الصورة الناتجة مثالية للصور المصغرة، الأيقونات، أصول واجهة المستخدم، أو أي حالة تتطلب جودة وشفافية.

## لماذا Aspose.Drawing بديل لـ System.Drawing؟

يعمل Aspose.Drawing كبديل جاهز للـ System.Drawing من خلال تقديم توافق كامل عبر الأنظمة، وإلغاء الحاجة إلى مكتبات GDI+ الأصلية. يدعم مجموعة واسعة من صيغ البكسل، يقدم معالجة صور عالية الأداء، ويتضمن ميزات متقدمة مثل التعامل مع قناة ألفا ودعم صيغ واسع، مما يجعله مناسبًا لكل من التعديلات البسيطة والمعالجة الدفعية الكبيرة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود:

- **مكتبة Aspose.Drawing** مدمجة في مشروع .NET الخاص بك. يمكنك تنزيلها [هنا](https://releases.aspose.com/drawing/net/).  
- مجلد يحتوي على الصور المصدرية التي تريد قصها. استبدل `"Your Document Directory"` في مقتطفات الشيفرة بالمسار الفعلي على جهازك.

## استيراد المساحات الاسمية

مساحة الاسم `System.Drawing` تمنحنا الوصول إلى `Bitmap`، `Graphics`، والأنواع المرتبطة التي يوسعها Aspose.Drawing.

```csharp
using System.Drawing;
```

## دليل خطوة بخطوة

### الخطوة 1: إنشاء لوحة Bitmap

`Bitmap` هو تمثيل Aspose.Drawing للصور في الذاكرة، يوفر وصولًا على مستوى البكسل وتحكمًا في الصيغة.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

نبدأ بلوحة فارغة بحجم يكفي للنتيجة المقصوصة. عدّل العرض والارتفاع ليتطابقا مع أبعاد المنطقة التي تخطط لاستخراجها.

### الخطوة 2: إنشاء كائن Graphics

`Graphics` هو سطح الرسم الذي يتيح لك رسم أشكال أو نصوص أو صور أخرى على Bitmap.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

كائن `Graphics` يسمح لنا بالرسم على اللوحة. `InterpolationMode` يتحكم في كيفية حساب قيم البكسل أثناء التحجيم أو التحويل—`NearestNeighbor` يعمل جيدًا للحواف الحادة.

### الخطوة 3: تحميل الصورة المراد قصها

`Image` (أو `Bitmap`) يحمل الملف المصدر في الذاكرة، جاهزًا للتعديل.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

حمّل الصورة المصدر. تأكد من أن المسار يشير إلى ملف موجود؛ وإلا سيُطرح استثناء.

### الخطوة 4: تعريف المستطيلات المصدرية والوجهة

كائنات `Rectangle` تصف المنطقة التي سيتم الاحتفاظ بها من الصورة المصدرية ومكان وضعها على لوحة الوجهة.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` يخبر الـ API أي جزء من الصورة الأصلية يجب الاحتفاظ به. هنا نختار المنطقة العلوية اليسرى بحجم 50 × 40 بكسل. بتعيين نفس المستطيل إلى `destinationRectangle` نحافظ على حجم المنطقة المقصوصة كما هو.

### الخطوة 5: تنفيذ عملية القص

`Graphics.DrawImage` ينسخ الجزء المحدد من `image` إلى `bitmap` الفارغ.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` ينسخ الجزء المحدد من `image` إلى `bitmap` الفارغ. هذه هي عملية **crop image to PNG** الأساسية.

### الخطوة 6: حفظ الصورة المقصوصة (Crop Image to PNG)

`Bitmap.Save` يكتب الـ bitmap الموجود في الذاكرة إلى ملف باستخدام الصيغة المحددة.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

أخيرًا، احفظ اللوحة على القرص كملف PNG. يحافظ PNG على أي قناة ألفا ويوفر جودة بدون فقد—مثالي لأصول واجهة المستخدم.

## كيفية قص الصور دفعيًا داخل حلقة؟

تكرّر كل مسار ملف باستخدام `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`، وكرر الخطوات 1‑6 داخل الحلقة، واحفظ كل نتيجة في مجلد الهدف. هذا النمط يتوسع خطيًا، ويمكن موازاته باستخدام `Parallel.ForEach` لمزيد من السرعة، ويعالج الصور بكفاءة وسرعة.

## المشكلات الشائعة والنصائح

- **تعارض صيغ البكسل** – تأكد من أن الصورة المصدرية ولوحة الـ bitmap تتشاركان صيغة بكسل متوافقة لتجنب تغير الألوان.  
- **تحرير كائنات GDI** – ضع `Bitmap` و `Graphics` داخل عبارات `using` أو استدعِ `Dispose()` يدويًا؛ وإلا قد تتسرب موارد غير مُدارة.  
- **أخطاء الإحداثيات** – إحداثيات المستطيل تبدأ من الصفر. اختيار مستطيل يتجاوز حدود الصورة المصدر سيؤدي إلى استثناء.  

## الأسئلة المتكررة

**س: هل يمكنني قص صور بأي صيغة باستخدام Aspose.Drawing؟**  
ج: نعم، يدعم Aspose.Drawing مجموعة واسعة من الصيغ (PNG، JPEG، BMP، GIF، TIFF، إلخ)، لذا يمكنك قص أي نوع تقريبًا من الصور.

**س: هل هناك خيارات قص متقدمة متاحة؟**  
ج: بالتأكيد. يمكنك دمج `GraphicsPath`، تحويلات `Matrix`، أو استخدام فئة `ImageProcessor` لتحديد اختيارات أكثر تعقيدًا مثل القص الدائري.

**س: هل يمكنني تطبيق عمليات قص متعددة على صورة واحدة؟**  
ج: نعم. بعد أول قص، يمكنك إعادة استخدام الـ bitmap الناتج كمصدر جديد وتكرار العملية لسلسلة من القصات.

**س: هل Aspose.Drawing مناسب لمعالجة الصور دفعيًا؟**  
ج: بالتأكيد. API الخفيف الوزن وعدم الاعتماد على مكتبات أصلية يجعله مثاليًا لمعالجة مجموعات صور كبيرة على الخوادم.

**س: كيف يمكنني الحصول على دعم لاستفسارات Aspose.Drawing؟**  
ج: توجه إلى [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44) لطلب المساعدة والتواصل مع المجتمع.

---

**آخر تحديث:** 2026-05-19  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية قص صورة إلى PNG باستخدام Aspose.Drawing لـ .NET](/drawing/net/image-editing/cropping/)
- [كيفية تحجيم الصور باستخدام Aspose.Drawing لـ .NET](/drawing/net/image-editing/scale/)
- [تحويل BMP إلى PNG وصيغ أخرى باستخدام Aspose.Drawing](/drawing/net/image-editing/load-save/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}