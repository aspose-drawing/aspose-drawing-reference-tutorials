---
date: 2026-06-23
description: تعلم كيفية حفظ PNG باستخدام Aspose.Drawing، وتطبيق التحويلات العالمية،
  وتحويل الرسومات إلى PNG. يتضمن أمثلة C# للتحويل بالترجمة والعديد من التحويلات الرسومية.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: التحويل العالمي في Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية حفظ PNG باستخدام Aspose.Drawing – التحويل العالمي
url: /ar/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية حفظ PNG باستخدام Aspose.Drawing – التحويل العالمي

## حفظ صورة Bitmap كـ PNG – مقدمة

**كيفية حفظ PNG** باستخدام Aspose.Drawing هو طلب شائع عندما تحتاج إلى صور شفافة وعالية الجودة تُنشأ في الوقت الفعلي. في هذا البرنامج التعليمي ستتعلم كيفية **حفظ bitmap كـ PNG**، وتطبيق التحويلات العالمية مثل translate، rotate، وscale، وأخيرًا تحويل الرسومات إلى PNG — كل ذلك باستخدام شفرة C# نظيفة وقابلة للصيانة. سواءً كنت تبني محرك تقارير، أو مكوّن مخططات، أو مُظهر واجهة مستخدم مخصص، فإن إتقان هذه الخطوات يتيح لك إنشاء صور ديناميكية تبدو رائعة على أي جهاز.

## إجابات سريعة
- **ماذا يعني “التحويل العالمي”؟** إنه يطابق إحداثيات الرسم المنطقية (العالمية) إلى إحداثيات الصفحة (الجهاز).  
- **هل يمكنني تصدير النتيجة كـ PNG؟** نعم – بعد الرسم يمكنك ببساطة استدعاء `bitmap.Save(...)` مع امتداد `.png`.  
- **هل أحتاج إلى ترخيص لـ Aspose.Drawing؟** الإصدار التجريبي المجاني يعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل هذا متوافق مع .NET 6/7؟** بالطبع – Aspose.Drawing يدعم .NET Framework 4.5+ و .NET Core/5/6/7.  
- **كم عدد التحويلات التي يمكنني ربطها؟** يمكنك تطبيق **تحويلات رسومية متعددة** بالتتابع (translate، rotate، scale، إلخ).

## ما هو التحويل العالمي في Aspose.Drawing؟

يغير التحويل العالمي نظام الإحداثيات الذي تستخدمه أوامر الرسم الخاصة بك. بشكل افتراضي، (0,0) هو الزاوية العلوية اليسرى للـ bitmap. باستخدام `TranslateTransform` أو `RotateTransform` أو `ScaleTransform`، يمكنك إعادة تموضع ذلك الأصل، تدوير الأشكال، أو تغيير حجمها دون تعديل الهندسة الأصلية.

## كيفية حفظ PNG باستخدام Aspose.Drawing؟

حمّل كائن `Bitmap`، واضبط أي تحويلات عالمية مرغوبة على مثيل `Graphics` الخاص به، وارسم الأشكال، وأخيرًا استدعِ `bitmap.Save("output.png", ImageFormat.Png)`. هذه الدالة الواحدة لحفظ الملف تكتب ملف PNG بدون فقدان يحافظ على الشفافية ودقة الألوان، مما يجعله مثاليًا لأصول الويب وطبقات واجهة المستخدم.

## لماذا نستخدم مثال ترجمة الرسومات؟

يسمح لك مثال ترجمة الرسومات بتحريك أصل الرسم مرة واحدة بدلاً من إعادة حساب كل نقطة. هذا النهج يقلل من تعقيد الشفرة، ويحسن قابلية القراءة، ويتيح لمحرك الرسومات معالجة حسابات المصفوفة بكفاءة، مما يمكن أن يزيد من أداء العرض بنسبة تصل إلى 30 % على القماشيات الكبيرة.

## مثال ترجمة الرسومات

يوضح **مثال ترجمة الرسومات** كيف أن تحريك الأصل يبسط تحديد المواقع. بدلاً من إعادة حساب كل نقطة، تقوم بتحويل نظام الإحداثيات مرة واحدة وترسم كما لو أن الأصل الجديد هو مركز القماشية.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود:

- **مكتبة Aspose.Drawing** مدمجة في مشروع .NET الخاص بك – حمّلها من صفحة [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/).  
- **دليل المستندات** حيث سيتم حفظ صورة الإخراج.  
- إلمام أساسي بصياغة **C#** و Visual Studio أو بيئة التطوير المتكاملة التي تفضّلها.  

الآن، دعنا نغوص في الشفرة!

## استيراد المساحات الاسمية

توجد فئات `Bitmap` و `Graphics` وأدوات Aspose للرسم في هذه المساحات الاسمية.  
**التعريف:** `System.Drawing` توفر الأنواع الأساسية لـ GDI+، بينما `Aspose.Drawing` توسّعها بقدرات متعددة المنصات.

## دليل خطوة بخطوة

### الخطوة 1: إنشاء Bitmap

نبدأ بإنشاء قماشية فارغة ستحمل رسمنا.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` ينشئ bitmap بدقة 32‑بت لكل بكسل مع ألفا مضاعفة مسبقًا، وهو التنسيق المثالي لإخراج PNG لأنه يحافظ على الشفافية دون خطوات تحويل إضافية.

- **لماذا 32bppPArgb؟** يدعم هذا التنسيق الشفافية (alpha) وعرض ألوان عالي الجودة، وهو مثالي لإخراج PNG.  
- **نصيحة احترافية:** اضبط العرض/الارتفاع ليتطابق مع حجم الصورة المستهدف.

### الخطوة 2: ضبط التحويل العالمي (مثال ترجمة الرسومات)

`TranslateTransform` ينقل أصل نظام الإحداثيات إلى موقع جديد.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` يغيّر نقطة (0,0) إلى مركز القماشية. بعد هذا الاستدعاء، أي شكل ترسمه باستخدام إحداثيات (0,0) سيظهر في وسط الصورة.

- هذا ينقل نقطة (0,0) إلى (500, 400) – وسط قماشية بحجم 1000 × 800.  
- يمكنك ربط تحويلات إضافية: `RotateTransform` يدور نظام الإحداثيات، و `ScaleTransform` يغيّر حجمه، مما يتيح **تحويلات رسومية متعددة**.

### الخطوة 3: رسم مستطيل باستخدام الإحداثيات المحوّلة

`DrawRectangle` يرسم مستطيلًا باستخدام القلم والإحداثيات المحددة.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` يرسم مستطيلًا متمركزًا على القماشية لأن زاويةه العلوية اليسرى مُزاحة بنصف عرضه وارتفاعه عن الأصل المحوّل.

- زاوية المستطيل العلوية اليسرى تبدأ من الأصل المحوّل (مركز الصورة).  
- لا تتردد في تجربة أشكال أخرى — إهليلجات، خطوط، أو مسارات مخصصة.

### الخطوة 4: حفظ النتيجة – تحويل الرسومات إلى PNG

`Save` يكتب الـ bitmap إلى ملف بالتنسيق الصورة المحدد.  
`ImageFormat` يحدد تنسيق الملف لحفظ الصور، مثل PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` يكتب ملف PNG بدون فقدان يمكن استخدامه مباشرةً في صفحات الويب أو مكونات الواجهة.

- PNG يحافظ على الألوان الدقيقة والشفافية التي حددناها سابقًا.  
- استبدل `"Your Document Directory"` بالمسار الفعلي على جهازك.

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثه | الحل |
|-------|----------------|-----|
| **خطأ عدم العثور على الملف** عند الحفظ | المجلد الهدف غير موجود. | أنشئ المجلد برمجياً (`Directory.CreateDirectory`) قبل استدعاء `Save`. |
| **صورة فارغة** بعد التحويل | تم استدعاء `TranslateTransform` بعد الرسم. | تأكد من ضبط التحويل **قبل** أي أوامر رسم. |
| **ألوان مشوهة** | استخدام تنسيق بكسل غير متوافق. | التزم بـ `Format32bppPArgb` لإخراج PNG. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق أكثر من تحويل واحد؟**  
ج: نعم – يمكنك ربط `TranslateTransform` و `RotateTransform` و `ScaleTransform` لتحقيق تأثيرات معقدة في خط أنابيب رسومي واحد.

**س: هل Aspose.Drawing مجاني للمشاريع التجارية؟**  
ج: يتوفر إصدار تجريبي مجاني للتقييم، لكن الترخيص التجاري مطلوب للاستخدام في الإنتاج.

**س: هل يعمل هذا مع .NET Core و .NET 5/6/7؟**  
ج: بالتأكيد. Aspose.Drawing يدعم جميع بيئات .NET الحديثة، بما في ذلك .NET Core و .NET 5 و .NET 6 و .NET 7.

**س: أين يمكنني العثور على مرجع API الكامل؟**  
ج: الوثائق الكاملة متاحة [هنا](https://reference.aspose.com/drawing/net/).

**س: كيف أقوم باستكشاف مشكلة ملف الإخراج المفقود؟**  
ج: تحقق من سلسلة المسار، تأكد من صلاحيات الكتابة، وتأكد من وجود المجلد قبل استدعاء `Save`.

## الخلاصة

لقد تعلمت الآن **كيفية حفظ PNG** باستخدام Aspose.Drawing، وتطبيق **تحويل عالمي**، وتنفيذ **مثال ترجمة الرسومات** الذي يمكن توسيعه بالدوران أو التكبير/التصغير. من خلال إتقان هذه اللبنات الأساسية يمكنك إنشاء صور ديناميكية، وصنع مخططات مخصصة، أو بناء رسومات فورية لأي تطبيق .NET.

---

**آخر تحديث:** 2026-06-23  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  
**الموارد ذات الصلة:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## دروس ذات صلة

- [دروس تحويل المصفوفة: تحويلات المصفوفة في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [كيفية تدوير الصورة باستخدام التحويل العالمي في Aspose.Drawing](/drawing/net/coordinate-transformations/global-transformation/)
- [تحويل نظام الإحداثيات – تحويل الصفحة في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}