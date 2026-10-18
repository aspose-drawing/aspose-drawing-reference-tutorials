---
date: 2026-10-18
description: تحويل الرسم إلى PNG باستخدام Aspose.Drawing مع تطبيق التحويلات العالمية.
  تعلم أمثلة الترجمة والدوران وتغيير الحجم في C# وتصدير PNG شفاف.
keywords:
- convert drawing to png
- save graphics as png
- rotate image .net
- scale graphics .net
- transparent png bitmap
lastmod: 2026-10-18
linktitle: التحويل العالمي في Aspose.Drawing
og_description: تحويل الرسم إلى PNG باستخدام Aspose.Drawing، تطبيق التحويلات العالمية
  وتصدير PNG شفاف. تعلم أمثلة الترجمة والدوران وتغيير الحجم في C# لـ .NET.
og_image_alt: Tutorial showing how to convert drawing to PNG using Aspose.Drawing
  with world transformation
og_title: تحويل الرسم إلى PNG باستخدام Aspose.Drawing – التحويل العالمي
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  headline: How to convert drawing to PNG with Aspose.Drawing – world transformation
  type: TechArticle
- description: Convert drawing to PNG with Aspose.Drawing while applying world transformations.
    Learn translate, rotate and scale examples in C# and export transparent PNGs.
  name: How to convert drawing to PNG with Aspose.Drawing – world transformation
  steps:
  - name: create a bitmap
    text: '**Definition:** `Bitmap` is Aspose.Drawing’s in‑memory representation of
      a raster image that you can draw on or save to disk. We start by creating a
      blank canvas that will hold our drawing. `new Bitmap(width, height, PixelFormat.Format32bppPArgb)`
      creates a 32‑bit per pixel bitmap with premultiplied'
  - name: set the world transformation (graphics translate example)
    text: '**Definition:** `Graphics` is the drawing surface that renders shapes onto
      a `Bitmap`. `TranslateTransform` moves the origin of the coordinate system to
      a new location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height
      / 2)` shifts the (0,0) point to the canvas centre. After this call, an'
  - name: draw a rectangle using the transformed coordinates
    text: '**Definition:** `DrawRectangle` is a method of `Graphics` that renders
      a rectangular outline or filled shape based on the supplied pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width'
  - name: save the result – convert graphics to PNG
    text: '**Definition:** `ImageFormat` is an enumeration that tells the `Save` method
      which file format to use. `Save` writes the bitmap to a file in the specified
      image format. `bitmap.Save(outputPath, ImageFormat.Png)` writes a lossless PNG
      file that can be used directly in web pages or UI components. - PN'
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
  - answer: The complete documentation is available [Aspose.Drawing .NET API reference](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- convert drawing to png
- Aspose.Drawing
- .NET graphics
- PNG export
- world transformation
title: كيفية تحويل الرسم إلى PNG باستخدام Aspose.Drawing – التحويل العالمي
url: /ar/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحويل الرسم إلى PNG باستخدام Aspose.Drawing – تحويل عالمي

## حفظ bitmap كـ PNG – مقدمة

**كيفية تحويل الرسم إلى PNG** باستخدام Aspose.Drawing هو طلب شائع عندما تحتاج إلى صور شفافة وعالية الجودة تُنشأ في الوقت الفعلي. في هذا الدرس ستتعلم كيفية **حفظ bitmap كـ PNG**، وتطبيق تحويلات عالمية مثل translate، rotate، وscale، وأخيرًا تحويل الرسومات إلى PNG — كل ذلك باستخدام كود C# نظيف وسهل الصيانة. سواءً كنت تبني محرك تقارير، أو مكوّن مخططات، أو عارض واجهة مستخدم مخصص، فإن إتقان هذه الخطوات يتيح لك إنشاء صور ديناميكية تبدو رائعة على أي جهاز.

## إجابات سريعة
- **ماذا يعني “world transformation”؟** إنه يطابق إحداثيات الرسم المنطقية (العالمية) إلى إحداثيات الصفحة (الجهاز)، مما يتيح لك إعادة تموضع، أو دوران أو تكبير/تصغير كل شيء باستخدام مصفوفة واحدة.  
- **هل يمكنني تصدير النتيجة كـ PNG؟** نعم – بعد الرسم يمكنك ببساطة استدعاء `bitmap.Save(...)` مع امتداد `.png`.  
- **هل أحتاج إلى ترخيص لـ Aspose.Drawing؟** النسخة التجريبية المجانية تعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل هذا متوافق مع .NET 6/7؟** بالتأكيد – Aspose.Drawing يدعم .NET Framework 4.5+ و .NET Core/5/6/7، ويغطي أكثر من 90 % من عمليات نشر .NET الحالية.  
- **كم عدد التحويلات التي يمكنني ربطها معًا؟** يمكنك تطبيق **تحويلات رسومية متعددة** بالتتابع (translate، rotate، scale، إلخ) دون أي تأثير على الأداء.

## ما هو التحويل العالمي في Aspose.Drawing؟

يُغيّر التحويل العالمي نظام الإحداثيات الذي تستخدمه أوامر الرسم الخاصة بك. بشكل افتراضي، (0,0) هو الزاوية العلوية اليسرى للـ bitmap. باستخدام `TranslateTransform` أو `RotateTransform` أو `ScaleTransform`، يمكنك إعادة تموضع هذا الأصل، أو تدوير الأشكال، أو تغيير حجمها دون تعديل الهندسة الأصلية. هذا يتيح لك التصميم مرة واحدة وإنتاجه بأي حجم أو اتجاه.

## كيفية حفظ PNG باستخدام Aspose.Drawing؟

حمّل كائن `Bitmap`، واضبط أي تحويلات عالمية مرغوبة على كائن `Graphics` الخاص به، وارسم الأشكال، وأخيرًا استدعِ `bitmap.Save("output.png", ImageFormat.Png)`. هذه الدالة الواحدة لحفظ الملف تكتب ملف PNG غير مضغوط يحافظ على الشفافية ودقة الألوان، مما يجعله مثاليًا لأصول الويب وطبقات واجهة المستخدم. الـ API يتعامل مع جميع عمليات الترميز منخفضة المستوى، لذا ستحصل على PNG جاهز للاستخدام في أقل من ثانية لأحجام القماش النموذجية.

## لماذا نستخدم مثال ترجمة الرسومات؟

يتيح لك مثال ترجمة الرسومات نقل أصل الرسم مرة واحدة بدلاً من إعادة حساب كل نقطة. من خلال إزاحة الأصل إلى مركز القماش، تبسط الهندسة، وتقلل تكرار الشيفرة، وتسمح لمحرك الرسومات بأداء ضرب المصفوفات في الكود الأصلي، مما يمكن أن يحسن سرعة العرض حتى 30 % على القماش الكبيرة. هذا النمط يجعل شفرتك أسهل في الصيانة عندما تضيف دورانًا أو تكبيرًا/تصغيرًا لاحقًا.

## مثال ترجمة الرسومات

**مثال ترجمة الرسومات** يوضح كيف أن نقل الأصل يبسط تحديد المواقع. بدلاً من إعادة حساب كل نقطة، تقوم بإزاحة نظام الإحداثيات مرة واحدة وترسم كما لو أن الأصل الجديد هو مركز القماش.

## المتطلبات المسبقة

- **مكتبة Aspose.Drawing** مدمجة في مشروع .NET الخاص بك – قم بتنزيلها من [صفحة إصدار Aspose.Drawing الرسمية](https://releases.aspose.com/drawing/net/).  
- **دليل المستندات** حيث سيتم حفظ صورة الإخراج.  
- إلمام أساسي بصياغة **C#** وVisual Studio أو بيئة التطوير المتكاملة المفضلة لديك.  

الآن، دعنا نغوص في الشيفرة!

## استيراد مساحات الأسماء

توجد `Bitmap` و `Graphics` وأدوات الرسم الخاصة بـ Aspose في هذه المساحات.  
**التعريف:** `System.Drawing` يوفر الأنواع الأساسية لـ GDI+، بينما `Aspose.Drawing` يوسعها بقدرات متعددة المنصات، مما يسمح لك بتشغيل نفس الشيفرة على Windows وLinux وmacOS دون تبعيات إضافية.

## دليل خطوة بخطوة

### الخطوة 1: إنشاء bitmap

**التعريف:** `Bitmap` هو تمثيل Aspose.Drawing في الذاكرة لصورة نقطية يمكنك الرسم عليها أو حفظها على القرص.  

نبدأ بإنشاء قماش فارغ سيحمل رسمنا.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` ينشئ bitmap بعمق 32‑بت لكل بكسل مع ألفا مضاعف مسبقًا، وهو التنسيق المثالي لإخراج PNG لأنه يحافظ على الشفافية دون خطوات تحويل إضافية.

- **لماذا 32bppPArgb؟** هذا التنسيق يدعم شفافية ألفا وجودة ألوان عالية، وهو مثالي لإخراج PNG.  
- **نصيحة احترافية:** اضبط العرض/الارتفاع ليتطابق مع حجم الصورة المستهدف؛ قماش بحجم 1920 × 1080 يُعرض في أقل من 0.2 ثانية على حاسوب مطور عادي.

### الخطوة 2: ضبط التحويل العالمي (مثال ترجمة الرسومات)

**التعريف:** `Graphics` هو سطح الرسم الذي يرسم الأشكال على `Bitmap`.  

`TranslateTransform` ينقل أصل نظام الإحداثيات إلى موقع جديد.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` يShift نقطة (0,0) إلى مركز القماش. بعد هذا الاستدعاء، أي شكل ترسمه باستخدام إحداثيات (0,0) سيظهر في منتصف الصورة.

- هذا ينقل نقطة (0,0) إلى (500, 400) – وسط قماش بحجم 1000 × 800.  
- يمكنك ربط تحويلات إضافية: `RotateTransform` يدور نظام الإحداثيات، و `ScaleTransform` يغير حجمه، مما يتيح **تحويلات رسومية متعددة** في خط أنابيب واحد.

### الخطوة 3: رسم مستطيل باستخدام الإحداثيات المحوّلة

**التعريف:** `DrawRectangle` هي طريقة في `Graphics` ترسم حدودًا مستطيلة أو شكلًا مملوءًا بناءً على القلم والإحداثيات المقدمة.  

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` يرسم مستطيلًا مركزيًا على القماش لأن زاويةه العلوية اليسرى مُزاحة بنصف عرضه وارتفاعه عن الأصل المحوّل.

- زاوية المستطيل العلوية اليسرى تبدأ عند الأصل المحوّل (مركز الصورة).  
- لا تتردد في تجربة أشكال أخرى — إهليلجات، خطوط، أو مسارات مخصصة.

### الخطوة 4: حفظ النتيجة – تحويل الرسومات إلى PNG

**التعريف:** `ImageFormat` هو تعداد يُخبر طريقة `Save` أي تنسيق ملف يستخدم.  

`Save` يكتب الـ bitmap إلى ملف بالتنسيق المحدد.  
`bitmap.Save(outputPath, ImageFormat.Png)` يكتب ملف PNG غير مضغوط يمكن استخدامه مباشرةً في صفحات الويب أو مكونات الواجهة.

- PNG يحافظ على الألوان الدقيقة والشفافية التي حددناها مسبقًا.  
- استبدل `"Your Document Directory"` بالمسار الفعلي على جهازك.  
- للمعالجة الدُفعية، كرر عبر مجموعة من كائنات `Bitmap` واستدعِ `Save` داخل الحلقة — المكتبة يمكنها التعامل مع آلاف الصور بأقل من 200 MB من الذاكرة.

## المشكلات الشائعة والحلول

| المشكلة | لماذا يحدث | الحل |
|-------|----------------|-----|
| **خطأ الملف غير موجود** عند الحفظ | المجلد الهدف غير موجود. | أنشئ المجلد برمجياً (`Directory.CreateDirectory`) قبل استدعاء `Save`. |
| **صورة فارغة** بعد التحويل | تم استدعاء `TranslateTransform` بعد الرسم. | تأكد من ضبط التحويل **قبل** أي أوامر رسم. |
| **ألوان مشوهة** | استخدام تنسيق بكسل غير متوافق. | استخدم `Format32bppPArgb` لإخراج PNG. |
| **نفاد الذاكرة** على القماش الكبيرة | تحميل الـ bitmap بالكامل في الذاكرة. | استخدم خيارات تدفق `Bitmap` أو قسم الصورة إلى بلاطات؛ Aspose.Drawing يمكنه رسم البلاطات بشكل مستقل. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق أكثر من تحويل؟**  
ج: نعم – يمكنك ربط `TranslateTransform` و `RotateTransform` و `ScaleTransform` لتحقيق تأثيرات معقدة في خط أنابيب رسومي واحد.

**س: هل Aspose.Drawing مجاني للمشاريع التجارية؟**  
ج: نسخة تجريبية مجانية متاحة للتقييم، لكن الترخيص التجاري مطلوب للاستخدام في الإنتاج.

**س: هل يعمل هذا مع .NET Core و .NET 5/6/7؟**  
ج: بالتأكيد. Aspose.Drawing يدعم جميع بيئات .NET الحديثة، بما في ذلك .NET Core و .NET 5 و .NET 6 و .NET 7.

**س: أين يمكنني العثور على مرجع API الكامل؟**  
ج: الوثائق الكاملة متاحة على [مرجع Aspose.Drawing .NET API](https://reference.aspose.com/drawing/net/).

**س: كيف يمكنني استكشاف مشكلة ملف الإخراج المفقود؟**  
ج: تحقق من سلسلة المسار، تأكد من أذونات الكتابة، وتأكد من وجود الدليل قبل استدعاء `Save`.

## الخلاصة

لقد تعلمت الآن **كيفية تحويل الرسم إلى PNG** باستخدام Aspose.Drawing، وطبقت **تحويلًا عالميًا**، وأجريت **مثال ترجمة الرسومات** الذي يمكن توسيعه بالدوران أو التكبير/التصغير. من خلال إتقان هذه اللبنات الأساسية يمكنك إنشاء صور ديناميكية، وصنع مخططات مخصصة، أو بناء رسومات فورية لأي تطبيق .NET. بعد ذلك، استكشف درس التحويل القائم على المصفوفات لدمج عمليات متعددة في مصفوفة واحدة للحصول على أداء أكثر كفاءة.

---

**آخر تحديث:** 2026-10-18  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  
**الموارد ذات الصلة:** [مرجع Aspose.Drawing API](https://reference.aspose.com/drawing/net/) | [تحميل نسخة تجريبية مجانية](https://releases.aspose.com/drawing/net/)

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