---
date: 2026-09-18
description: تعلم كيفية ضبط لون القلم في Aspose.Drawing لـ .NET، ورسم خطوط ملونة،
  وحفظ صور PNG باستخدام أمثلة شفرة بسيطة.
keywords:
- set pen color
- save png image
- cross platform drawing
- draw lines with pen
- high quality png
lastmod: 2026-09-18
linktitle: العمل مع الألوان في Aspose.Drawing
og_description: ضبط لون القلم في Aspose.Drawing لـ .NET وإنشاء صور PNG عالية الجودة.
  تعلم الرسم عبر الأنظمة، ورسم خطوط بالقلم، وحفظ صور PNG في دقائق.
og_image_alt: Screenshot of code setting pen color and saving a PNG with Aspose.Drawing
og_title: ضبط لون القلم في Aspose.Drawing – دليل لإنتاج صور PNG عالية الجودة
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored
    lines, and save PNG images with simple code examples.
  headline: How to set pen color in Aspose.Drawing
  type: TechArticle
- description: Learn how to set pen color in Aspose.Drawing for .NET, draw colored
    lines, and save PNG images with simple code examples.
  name: How to set pen color in Aspose.Drawing
  steps:
  - name: '**Aspose.Drawing Library** – download and install from the official site
      **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.'
    text: '**Aspose.Drawing Library** – download and install from the official site
      **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.'
  - name: '**A .NET development environment** – Visual Studio, VS Code, or any IDE
      you prefer.'
    text: '**A .NET development environment** – Visual Studio, VS Code, or any IDE
      you prefer.'
  - name: '**Basic C# knowledge** – familiarity with classes, objects, and namespaces.'
    text: '**Basic C# knowledge** – familiarity with classes, objects, and namespaces.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing integrates smoothly with other .NET libraries, providing
      a versatile environment for graphic manipulation.
    question: Can I use Aspose.Drawing with other .NET libraries?
  - answer: You can get a temporary license **[Aspose temporary license page](https://purchase.aspose.com/temporary-license/)**,
      allowing you to explore the full potential of Aspose.Drawing.
    question: How can I obtain a temporary license for Aspose.Drawing?
  - answer: Yes, Aspose.Drawing supports JPEG, GIF, BMP, TIFF, and more. Refer to
      the documentation for a complete list.
    question: Does Aspose.Drawing support image formats other than PNG?
  - answer: Absolutely! Aspose.Drawing works in both desktop and web applications,
      enabling dynamic graphic generation on servers.
    question: Can I use Aspose.Drawing for web development?
  - answer: Yes, you can explore a free trial **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**,
      letting you evaluate the library before purchasing.
    question: Is there a free trial available for Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- .NET graphics
- pen color
- PNG output
title: كيفية ضبط لون القلم في Aspose.Drawing
url: /ar/net/pens/colors/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعيين لون القلم في Aspose.Drawing

## مقدمة

في هذا البرنامج التعليمي ستتعلم كيفية **تعيين لون القلم** عند الرسم باستخدام Aspose.Drawing لـ .NET، إنشاء لوحة رسومات، رسم خطوط ملونة، و**حفظ ملفات صورة PNG** بجودة عالية. سواء كنت تبني أداة سطح مكتب، خدمة تقارير، أو واجهة برمجة تطبيقات ويب تُنشئ مخططات، فإن التحكم في ألوان الأقلام أمر أساسي للحصول على رسومات ذات مظهر احترافي.

## إجابات سريعة
- **ما هو الصنف الأساسي للرسم؟** `Graphics` created from a `Bitmap`.
- **كيف يمكنني تغيير لون القلم؟** Use `Color.FromKnownColor` or `Color.FromArgb`.
- **ما هو التنسيق الموصى به للإخراج غير الفاقد؟** PNG (`.png`).
- **هل أحتاج إلى ترخيص للتطوير؟** A temporary license is available for evaluation.
- **هل يمكنني استخدام هذا في ASP.NET Core؟** Yes, Aspose.Drawing works with .NET Core and .NET 5+.

## ما هو “تعيين لون القلم” في Aspose.Drawing؟

يعني تعيين لون القلم إسناد قيمة `Color` إلى كائن `Pen` قبل أي عملية رسم. اللون المختار يؤثر على درجة اللون، الشفافية، وسُمك الخطوط، الأشكال، وضربات النص المرسومة على اللوحة، مما يتيح تحكمًا بصريًا دقيقًا في النتيجة النهائية للصورة.

## لماذا نستخدم Aspose.Drawing لتعديل الألوان؟

توفر Aspose.Drawing **رسمًا متعدد المنصات** يعمل على Windows وLinux وmacOS دون قيود System.Drawing.Common. تدعم إخراج **PNG عالي الجودة** (حتى 32‑bit ARGB) وتقدم مجموعة غنية من واجهات برمجة الألوان، بما في ذلك أكثر من 50 لونًا معروفًا وتخصيص ARGB كامل. يمكن للمكتبة معالجة صور مئات الصفحات مع الحفاظ على استهلاك الذاكرة أقل من 50 MB، مما يجعلها مناسبة للتوليد على الخادم.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من وجود ما يلي:

1. **مكتبة Aspose.Drawing** – قم بتحميلها وتثبيتها من الموقع الرسمي **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**.  
2. **بيئة تطوير .NET** – Visual Studio، VS Code، أو أي بيئة تطوير تفضلها.  
3. **معرفة أساسية بـ C#** – الإلمام بالصنفوف، الكائنات، والمساحات الاسمية.

## استيراد مساحات الأسماء

مساحة الأسماء `Aspose.Drawing` هي المكتبة الأساسية التي توفر جميع الأنواع المتعلقة بالرسم مثل `Bitmap` و `Graphics` و `Pen` و `Color`، مما يمكّن المطورين من إنشاء الصور ومعالجتها وعرضها عبر الأنظمة دون الاعتماد على System.Drawing.Common.

```csharp
using System.Drawing;
```

## الخطوة 1: إنشاء bitmap (اللوحة)

الصنف `Bitmap` يمثل مخزن بكسلات في الذاكرة يمكن الرسم عليه؛ يدعم صيغ بكسل متعددة، بما في ذلك 32‑bit ARGB، الذي يحافظ على عمق اللون الكامل والشفافية الضرورية لإخراج PNG عالي الجودة.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## الخطوة 2: إنشاء كائن Graphics

كائن `Graphics` يعمل كسطح رسم مرتبط بـ `Bitmap`، ويقدم طرقًا مثل `DrawLine` و `DrawRectangle` و `DrawString` التي ترسم الأشكال والخطوط والنصوص على مخزن الصورة الأساسي.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 3: رسم خط بقلم أزرق (الخط الملون الأول)

الصنف `Pen` يحدد خصائص الخطوط والحدود، بما في ذلك اللون والعرض ونمط الشرط وتحديد المحاذاة، ويُستخدم من قبل طرق `Graphics` لتطبيق الخطوط على الأشكال والمسارات على اللوحة.

```csharp
Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawLine(bluePen, 100, 100, 900, 100);
```

## الخطوة 4: رسم خط بقلم أحمر مخصص

يوضح هذا المثال كيفية **رسم خطوط ملونة** باستخدام قيمة ARGB مخصصة، مما يمنحك تحكمًا كاملاً في الشفافية والدرجة الدقيقة للون.

```csharp
Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
graphics.DrawLine(redPen, 100, 200, 900, 200);
```

## الخطوة 5: حفظ الصورة كملف PNG

أخيرًا، نقوم **بحفظ صورة PNG** إلى المجلد المطلوب. يحافظ PNG على الشفافية ودقة الألوان، مما يجعله الصيغة المفضلة لـ **رسومات الويب** والتقارير.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **الصورة تظهر فارغة** | لم يتم تفريغ Graphics قبل الحفظ | استدعِ `graphics.Dispose();` أو ضع `Graphics` داخل كتلة `using`. |
| **ألوان غير صحيحة** | استخدام `FromKnownColor` مع تعداد خاطئ | تحقق من قيمة التعداد أو استخدم `FromArgb` للتحكم الدقيق. |
| **أخطاء مسار الملف** | دليل غير صالح أو أذونات مفقودة | تأكد من وجود المجلد المستهدف وأن التطبيق لديه صلاحية الكتابة. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing مع مكتبات .NET أخرى؟**  
ج: نعم، يندمج Aspose.Drawing بسلاسة مع مكتبات .NET الأخرى، مما يوفر بيئة متعددة الاستخدامات لتعديل الرسومات.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Drawing؟**  
ج: يمكنك الحصول على ترخيص مؤقت عبر **[Aspose temporary license page](https://purchase.aspose.com/temporary-license/)**، مما يتيح لك استكشاف الإمكانات الكاملة لـ Aspose.Drawing.

**س: هل يدعم Aspose.Drawing صيغ صور غير PNG؟**  
ج: نعم، يدعم Aspose.Drawing صيغ JPEG، GIF، BMP، TIFF، وغيرها. راجع الوثائق للحصول على القائمة الكاملة.

**س: هل يمكنني استخدام Aspose.Drawing لتطوير الويب؟**  
ج: بالتأكيد! يعمل Aspose.Drawing في تطبيقات سطح المكتب والويب على حدٍ سواء، مما يتيح إنشاء رسومات ديناميكية على الخوادم.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Drawing؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية عبر **[Aspose.Drawing download page](https://releases.aspose.com/drawing/net/)**، مما يتيح لك تقييم المكتبة قبل الشراء.

## الخلاصة

في هذا الدليل غطينا كيفية **تعيين لون القلم**، **رسم خطوط ملونة**، **إنشاء كائن Graphics**، و**حفظ النتيجة كملف PNG عالي الجودة** باستخدام Aspose.Drawing لـ .NET. هذه الأساسيات تفتح الباب أمام سيناريوهات أكثر تقدمًا مثل رسم الأشكال، عرض النص، وإنشاء المخططات بشكل ديناميكي. إذا واجهت تحديات، فإن **[الوثائق](https://reference.aspose.com/drawing/net/)** و**[منتدى الدعم](https://forum.aspose.com/c/drawing/44)** الخاص بـ Aspose.Drawing هما مكانان ممتازان للعثور على الإجابات.

---

**آخر تحديث:** 2026-09-18  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية حفظ bitmap كـ PNG أثناء رسم خطوط متعددة باستخدام Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [كيفية ربط المسارات باستخدام Pen في Aspose.Drawing .NET](/drawing/net/pens/)
- [تحسين جودة الصورة باستخدام Antialiasing في Aspose.Drawing](/drawing/net/rendering/antialiasing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}