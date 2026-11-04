---
date: 2026-11-04
description: تعلم كيفية رسم رسومات مستطيلة أثناء إجراء coordinate system transformation
  في .NET باستخدام Aspose.Drawing API. يوضح هذا step‑by‑step guide كيفية تحويل inches
  إلى pixels وتعيين page units.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Coordinate system transformation في Aspose.Drawing
og_description: تعلم كيفية رسم رسومات مستطيلة أثناء تحويل inches إلى pixels وتعيين
  page units في Aspose.Drawing لـ .NET. اتبع step‑by‑step guide للحصول على page transformation
  دقيق.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: كيفية رسم مستطيل مع page transformation باستخدام Aspose.Drawing لـ .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: كيفية رسم مستطيل – coordinate system transformation (page transformation) في
  Aspose.Drawing لـ .NET
url: /ar/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم مستطيل – تحويل نظام الإحداثيات (تحويل الصفحة) في Aspose.Drawing لـ .NET

## مقدمة

في هذا الدرس ستتعلم **كيفية رسم مستطيل** رسوميًا أثناء إجراء تحويل نظام إحداثيات على مستوى الصفحة باستخدام Aspose.Drawing لـ .NET. سواءً كنت تبني محرك تقارير، أداة رسم بأسلوب CAD، أو أي تطبيق يحتاج إلى قياسات دقيقة من العالم الحقيقي، فإن هذا الدليل يرافقك خطوة بخطوة—من إنشاء صورة نقطية إلى حفظ ملف PNG النهائي. في النهاية ستكون قادرًا على تحويل البوصات إلى بكسل، مسح خلفية القماش، وضبط وحدات الصفحة لإنتاج جاهز للطباعة.

## إجابات سريعة
- **ما هو تحويل نظام الإحداثيات؟** يربط وحدات مستوى الصفحة (مثل البوصات) بوحدات البكسل على مستوى الجهاز بحيث يتم تحجيم الرسومات بشكل صحيح على أي جهاز إخراج.  
- **لماذا اختيار Aspose.Drawing؟** يوفر واجهة برمجة تطبيقات رسومات مُدارة بالكامل ومتعددة المنصات تستبدل System.Drawing.Common وتدعم أكثر من 30 تنسيق صورة.  
- **كم من الوقت يستغرق تنفيذ المثال؟** تقريبًا 5‑10 دقائق لرسم مستطيل أساسي مع تحويل الصفحة.  
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للنشر في بيئات الإنتاج.  
- **ما هي إطارات .NET المدعومة؟** .NET Framework 4.6+، .NET Core 3.1+، و .NET 5/6/7.

## ما هو Aspose.Drawing؟

Aspose.Drawing هي مكتبة رسومات .NET توفر **واجهة برمجة تطبيقات غير معتمدة على الجهاز** لإنشاء ومعالجة الصور النقطية، والمتجهات، ورسومات مستوى الصفحة دون الاعتماد على GDI+. تدعم **أكثر من 30 تنسيق صورة** ويمكنها معالجة صور تصل إلى **10,000 × 10,000 بكسل** مع الحفاظ على استهلاك منخفض للذاكرة.

## لماذا استخدام تحويل نظام الإحداثيات مع Aspose.Drawing؟

يتيح لك تحويل نظام الإحداثيات تصميم الرسومات بوحدات العالم الحقيقي بينما تتولى المكتبة تلقائيًا معالجة تحجيم البكسل لأي جهاز إخراج. يضمن هذا النهج أن يطبع مستطيل بطول 5 بوصات بدقة 5 بوصات على طابعة بدقة 300 DPI ويظهر بنسب متناسبة على شاشة بدقة 96 DPI، مما يلغي أخطاء التحويل اليدوي.

- **تصميم غير معتمد على الجهاز:** اكتب الكود مرة واحدة؛ تقوم Aspose.Drawing بتحجيمه للشاشات أو الطابعات أو ملفات PDF.  
- **رسم دقيق:** مثالي للمخططات التقنية، والرسومات الهندسية، أو أي سيناريو يتطلب قياسات دقيقة.  
- **موثوقية عبر المنصات:** يعمل بشكل ثابت على Windows وLinux وmacOS دون قيود GDI+ في System.Drawing.  
- **الأداء:** على معالج 2.5 GHz نموذجي، يكتمل رسم مستطيل بطول 5 بوصات بدقة 300 DPI في أقل من **15 ms**، ويمكن للمكتبة عرض **50 إطارًا في الثانية** في سيناريوهات المعاينة الفورية.

## المتطلبات المسبقة

- **مكتبة Aspose.Drawing:** قم بتنزيل أحدث نسخة من الموقع الرسمي [هنا](https://releases.aspose.com/drawing/net/).  
- **بيئة التطوير المتكاملة (IDE):** Visual Studio أو Rider أو أي محرر متوافق مع .NET.  
- **مجلد الإخراج:** استبدل `"Your Document Directory"` في كود العينة بالمجلد الذي تريد حفظ ملف PNG فيه.  
- **دعم ASP.NET اختياري:** يمكنك إضافة حزمة NuGet إلى مشروع ASP.NET Core واستخدام نفس الواجهة؛ يتبع النمط النهج المعتاد **how to use aspnet** لمكتبات .NET.

## كيفية رسم مستطيل مع تحويل الصفحة؟

حمّل صورة نقطية فارغة، اضبط وحدة الصفحة إلى البوصة، وارسم مستطيلًا باستخدام قلم أزرق رفيع—هذا يكمل رسم المستطيل في بضع أسطر من الكود فقط. خاصية `Graphics.PageUnit` تخبر المحرك بتفسير جميع الإحداثيات كبوصات، بحيث يمكنك التفكير بوحدات العالم الحقيقي بدلاً من البكسلات الخام، وتقوم المكتبة تلقائيًا **تحويل البوصات إلى بكسل** بناءً على DPI الصورة النقطية.

### الخطوة 1: استيراد مساحات الأسماء

العبارات `using` تمنحك الوصول إلى الفئات الأساسية للرسم.

```csharp
using System.Drawing;
```

### الخطوة 2: إنشاء صورة نقطية

`Bitmap` هو حاوية الصورة في الذاكرة التي ترسم عليها. يحتفظ بذاكرة البكسل ويعرض طرقًا لحفظ الملفات. إنشاء صورة نقطية يحدد حجم القماش وتنسيق البكسل.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### الخطوة 3: إنشاء كائن رسومات

`Graphics` يوفر سطح الرسم للصورة النقطية. يترجم أوامر الرسم عالية المستوى (خطوط، أشكال، نص) إلى عمليات بكسل على الصورة الأساسية.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### الخطوة 4: مسح خلفية القماش

مسح القماش بلون محايد يضمن بروز الأشكال. في هذا المثال نملأ الخلفية بالرمادي الفاتح، وهو أيضًا يوضح تقنية **مسح خلفية القماش**.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### الخطوة 5: ضبط التحويل (كيفية ضبط الوحدات)

`Graphics.PageUnit` يحدد وحدة القياس المستخدمة لإحداثيات الصفحة. ضبطها إلى `GraphicsUnit.Inch` يخبر Aspose.Drawing بـ **تحويل البوصات إلى بكسل** تلقائيًا بناءً على DPI الصورة (96 DPI افتراضيًا، 300 DPI للطباعة عالية الدقة). يمكنك أيضًا اختيار `GraphicsUnit.Millimeter` أو `GraphicsUnit.Point` أو `GraphicsUnit.Pixel` حسب متطلبات التخطيط.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### الخطوة 6: رسم مستطيل – رسم رسومات المستطيل

`Pen` يحدد اللون والعرض ونمط الخطوط المرسومة على سطح الرسومات. باستخدام قلم أزرق رفيع، نرسم مستطيلًا بأبعاد معبر عنها بالبوصة، مما يجعل الكود أكثر قابلية للقراءة للتصاميم الموجهة للطباعة.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### الخطوة 7: حفظ الصورة النقطية كـ PNG

أخيرًا، اكتب الصورة النقطية إلى ملف PNG في المجلد الذي حددته مسبقًا. حفظها كـ PNG يحافظ على جودة غير مضغوطة ويدعمها معظم المنصات.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## كيفية تحجيم الرسومات للطابعة؟

اضبط DPI الصورة النقطية إلى دقة الطابعة المستهدفة (مثلاً 300 DPI) قبل الرسم. يؤدي ذلك تلقائيًا إلى **تحجيم رسومات الطابعة** بحيث يساوي البوصة الواحدة في الكود بوصة واحدة على الصفحة المطبوعة، بينما يبقى الحجم المنطقي للمستطيل دون تغيير. بعد استدعاء `bitmap.SetResolution(300, 300)`, سيظهر نفس المستطيل أكبر على الورق لكنه يحتفظ بأبعاده الدقيقة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|----------------|-----|
| **ملف الإخراج غير مُنشأ** | مسار غير صحيح أو مجلد مفقود | تأكد من وجود دليل الهدف أو استدعِ `Directory.CreateDirectory` قبل الحفظ. |
| **المستطيل يظهر مشوهًا** | عدم توافق `PageUnit` أو DPI | تحقق من أن `graphics.PageUnit` يطابق الوحدة المطلوبة وأن DPI الصورة النقطية مضبوط بشكل مناسب (96 DPI افتراضيًا، 300 DPI للطباعة). |
| **استثناء الترخيص** | تشغيل بدون ترخيص صالح في بيئة الإنتاج | طبق ترخيص Aspose.Drawing المؤقت أو الدائم قبل إنشاء كائنات الرسومات. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing مجانًا؟**  
ج: نعم، نسخة تجريبية مجانية متاحة [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على وثائق مفصلة لـ Aspose.Drawing؟**  
ج: المرجع الكامل للواجهة موجود [هنا](https://reference.aspose.com/drawing/net/).

**س: كيف أحصل على دعم لـ Aspose.Drawing؟**  
ج: زر [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على مساعدة المجتمع والدعم الرسمي.

**س: هل تتوفر ترخيص مؤقت لـ Aspose.Drawing؟**  
ج: بالتأكيد—احصل على واحد [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني شراء ترخيص كامل لـ Aspose.Drawing؟**  
ج: يمكنك شراؤه [هنا](https://purchase.aspose.com/buy).

## الخلاصة

أنت الآن تعرف **كيفية رسم مستطيل** رسوميًا مع تحويل مستوى الصفحة باستخدام Aspose.Drawing لـ .NET. من خلال ضبط وحدة الصفحة إلى البوصة، مسح خلفية القماش، وحفظ النتيجة كملف PNG، تحصل على مخرجات دقيقة غير معتمدة على الجهاز مناسبة لكل من عرض الشاشة والطباعة عالية الدقة. جرّب وحدات أخرى، أو تدوير، أو أصول إحداثيات مخصصة لاكتشاف سيناريوهات رسم أكثر قوة.

---

**Last Updated:** 2026-11-04  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose

## دروس ذات صلة

- [كيفية ضبط الوحدة في Aspose.Drawing لـ .NET – وحدات القياس](/drawing/net/coordinate-transformations/units-of-measure/)
- [التحويل العالمي](/drawing/net/coordinate-transformations/global-transformation/)
- [تحويل خطوة بخطوة – تحويلات الإحداثيات](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}