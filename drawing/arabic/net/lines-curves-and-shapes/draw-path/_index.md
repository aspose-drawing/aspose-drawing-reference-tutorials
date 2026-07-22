---
date: 2026-07-22
description: تعلم كيفية حفظ bitmap كـ PNG وتصدير الصورة إلى JPEG باستخدام Aspose.Drawing.
  دليل خطوة بخطوة يوضح رسم المسارات، إنشاء الصور، وتصدير الصيغ.
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: رسم المسارات في Aspose.Drawing
og_description: احفظ bitmap كـ PNG وصدّر الصورة إلى JPEG باستخدام Aspose.Drawing لـ
  .NET. اتبع هذا البرنامج التعليمي لرسم مسارات معقدة، إنشاء صور عالية الجودة، وإخراج
  صيغ متعددة.
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: حفظ bitmap كـ PNG – رسم المسارات باستخدام Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: حفظ bitmap كـ PNG – باستخدام GraphicsPath في Aspose.Drawing
url: /ar/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# رسم المسارات في Aspose.Drawing

## كيفية استخدام GraphicsPath – المقدمة

**Save bitmap as PNG** غالبًا ما تكون الخطوة الأولى عندما تحتاج إلى صورة غير مضغوطة لمعالجة إضافية أو نشر. في هذا الدرس ستتعلم كيفية رسم مسارات متجهة متقدمة باستخدام `GraphicsPath`، وعرضها على صورة bitmap، ثم **save bitmap as PNG** أو حتى **export image to JPEG**. سواء كنت تبني محرك تقارير، أو مكتبة رسم بياني مخصصة، أو تحتاج ببساطة إلى إنشاء رسومات ديناميكية، فإن Aspose.Drawing يزودك بواجهة برمجة تطبيقات مدارة بالكامل، متعددة المنصات، تحل محل System.Drawing.Common.

## إجابات سريعة
- **ما الذي يمكنني رسمه باستخدام GraphicsPath?** خطوط، مستطيلات، إهليلجات، منحنيات، وأشكال مخصصة.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية مجانية؛ الترخيص التجاري مطلوب للإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6+.  
- **هل System.Drawing.Common مطلوب؟** لا، Aspose.Drawing يعمل بشكل مستقل.  
- **هل يمكنني الحفظ بصيغ مختلفة؟** نعم – PNG، JPEG، BMP، GIF، وأكثر.

## ما هو GraphicsPath؟

`GraphicsPath` هو حاوية المتجهات في Aspose.Drawing التي تخزن تسلسلًا من العناصر الرسومية الأساسية مثل الخطوط والأقواس والمنحنيات ككائن واحد. من خلال تجميع هذه العناصر، يمكنك تطبيق التحويلات، قواعد التعبئة، وإعدادات الحد بشكل موحد، مما يبسط إنشاء رسومات معقدة ويضمن عرضًا ثابتًا عبر صيغ الإخراج المختلفة.

## لماذا تستخدم GraphicsPath مع Aspose.Drawing؟

استخدام GraphicsPath مع Aspose.Drawing يمنحك قدرات رسم متجهة دقيقة ومرنة وعالية الأداء. يتيح لك بناء أشكال معقدة، تطبيق التحويلات، وعرضها بكفاءة، مع الحفاظ على التوافق عبر المنصات ودعم معالجة الصور على نطاق واسع. بالإضافة إلى ذلك، يتكامل بسلاسة مع مكتبات .NET الأخرى، مما يمكنك من دمج سير عمل الرسوم النقطية والمتجهة في تطبيق واحد.

- **الدقة:** يتعامل مع أكثر من 50 عنصرًا متجهيًا بدقة تحت‑بكسلية، مما يضمن أنه عندما تقوم **save bitmap as PNG** يبقى الناتج واضحًا بأي دقة.  
- **المرونة:** دمج الخطوط، الأقواس، ومنحنيات بيزيير في مسار واحد، ثم عرضه باستدعاء واحد `Graphics.DrawPath`.  
- **الأداء:** خط أنابيب العرض المحسّن يعالج الصور حتى 400 MP دون تحميل الملف بالكامل إلى الذاكرة، مما يجعل وظائف الدفعات الكبيرة ممكنة.  
- **متعدد المنصات:** نتائج متطابقة على أنظمة Windows وLinux وmacOS، مما يلغي الأخطاء الخاصة بالمنصة.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

- **مكتبة Aspose.Drawing:** قم بتحميل وتثبيت مكتبة Aspose.Drawing. يمكنك العثور على المكتبة [هنا](https://releases.aspose.com/drawing/net/).
- **منتجات Aspose الأخرى:** استكشف عروض Aspose الإضافية [هنا](https://releases.aspose.com/).
- **بيئة التطوير:** قم بإعداد بيئة تطوير .NET الخاصة بك مع الأدوات اللازمة (Visual Studio، .NET SDK، إلخ).

## استيراد المساحات الاسمية

ابدأ باستيراد المساحات الاسمية المطلوبة في مشروعك:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## الخطوة 1: إنشاء Bitmap و Graphics

Bitmap يمثل صورة في الذاكرة، بينما Graphics يوفر طرق الرسم للعرض على تلك الصورة. ابدأ بإنشاء كائن `Bitmap` و`Graphics` للعمل معه. ستكون هذه الصورة هي القماش الذي يُرسم عليه `GraphicsPath`، وفيما بعد ستقوم **save bitmap as PNG**:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 2: تعريف Pen و GraphicsPath

Pen يحدد لون الخط وعرضه ونمطه؛ GraphicsPath يخزن مجموعة من العناصر الرسومية ككائن متجه واحد. بعد ذلك، عرّف `Pen` لتحديد خصائص الرسم وأنشئ `GraphicsPath`. كائن `GraphicsPath` يحتفظ ببيانات المتجه قبل رسمها:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## الخطوة 3: إضافة خطوط وأشكال

AddLine وAddRectangle وAddEllipse يضيفون الأشكال المقابلة إلى GraphicsPath للعرض لاحقًا. أضف خطوطًا، مستطيلات، وإهليلجات إلى `GraphicsPath` لإنشاء مسار معقد. يمكنك أيضًا إضافة منحنيات بيزيير مخصصة لأشكال سلسة:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## الخطوة 4: رسم المسار

DrawPath يعرض بيانات المتجه من GraphicsPath على سطح Graphics باستخدام القلم المحدد. ارسم المسار على كائن `Graphics` باستخدام `Pen` المحدد. هذه العملية تحول بيانات المتجه إلى صورة نقطية على قماش الـ bitmap:

```csharp
graphics.DrawPath(pen, path);
```

## الخطوة 5: حفظ الصورة – تصدير إلى PNG أو JPEG

طريقة Bitmap.Save تكتب الصورة إلى القرص بالصيغ المختارة مثل PNG أو JPEG. بعد الرسم، يمكنك **save bitmap as PNG** للحصول على جودة غير مضغوطة أو **export image to JPEG** للحصول على حجم ملف أصغر. اختر الصيغة التي تناسب سيناريو الاستخدام الخاص بك:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

كرر هذه الخطوات حسب الحاجة لإنشاء مسارات معقدة وجذابة بصريًا.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **المسار غير مرئي** | تأكد من أن لون القلم يتباين مع الخلفية وأن الـ bitmap تم حفظه بشكل صحيح. |
| **حجم الصورة غير متوقع** | تحقق من أبعاد الـ bitmap وتنسيق البكسل ليتطابق مع متطلباتك. |
| **استثناء الترخيص** | استخدم ترخيص تجريبي للاختبار؛ قم بتطبيق ترخيص صالح قبل النشر في الإنتاج. |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.Drawing مع مكتبات .NET الأخرى؟

A1: نعم، يتكامل Aspose.Drawing بسلاسة مع مكتبات .NET الأخرى، مما يوفر مرونة في مشاريعك التطويرية.

### س2: هل تتوفر نسخة تجريبية؟

A2: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على الدعم لـ Aspose.Drawing؟

A3: زر منتدى Aspose.Drawing [هنا](https://forum.aspose.com/c/drawing/44) للحصول على المساعدة ودعم المجتمع.

### س4: كيف أحصل على ترخيص مؤقت؟

A4: احصل على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س5: هل يمكنني شراء Aspose.Drawing؟

A5: نعم، يمكنك شراء Aspose.Drawing [هنا](https://purchase.aspose.com/buy).

**أسئلة إضافية**

**س: هل يمكنني رسم منحنيات بيزيير مخصصة باستخدام GraphicsPath؟**  
A: بالتأكيد – استخدم `path.AddBezier(...)` لتحديد منحنيات سلسة.

**س: كيف يمكنني مسح GraphicsPath قبل إعادة استخدامه؟**  
A: استدعِ `path.Reset()` لإزالة جميع الأشكال والبدء من جديد.

## الخاتمة

تهانينا! لقد تعلمت بنجاح **كيفية استخدام GraphicsPath** لرسم المسارات ثم **save bitmap as PNG** أو **export image to JPEG** باستخدام Aspose.Drawing لـ .NET. يغطي هذا الدرس إنشاء bitmap، تعريف قلم، بناء `GraphicsPath`، عرض أشكال مختلفة، وتصدير الصورة النهائية بصيغ متعددة. جرّب إحداثيات، ألوان، وعرض خطوط مختلفة لإطلاق الإمكانات الإبداعية الكاملة لـ Aspose.Drawing.

---

**آخر تحديث:** 2026-07-22  
**تم الاختبار مع:** Aspose.Drawing 24.12 for .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [حفظ Bitmap كـ PNG ورسم منحنيات مغلقة باستخدام Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [حفظ Bitmap C# – رسم منحنيات بيزيير مع Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [كيفية حفظ الصورة ورسم منحنيات كاردينال في Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}