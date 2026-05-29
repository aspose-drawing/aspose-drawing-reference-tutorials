---
date: 2026-05-29
description: تعلم كيفية حفظ PNG ورسم المنحنيات الكاردينالية في .NET باستخدام Aspose.Drawing.
  احفظ المنحنى كملف PNG، أنشئ رسومات ناعمة، وقم بإنشاء صورة bitmap إلى ملف بسهولة.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: رسم المنحنيات الكاردينالية في Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية حفظ PNG ورسم المنحنيات الكاردينالية باستخدام Aspose.Drawing
url: /ar/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية حفظ PNG ورسم منحنيات كاردينال باستخدام Aspose.Drawing

## المقدمة

في هذا الدرس ستكتشف **كيفية حفظ PNG** أثناء رسم منحنيات كاردينال سلسة باستخدام Aspose.Drawing لـ .NET. سواء كنت تبني مكوّنًا للرسوم البيانية، أو محررًا للمخططات، أو تحتاج ببساطة إلى تصدير منحنى مخصص كملف PNG، فإن الخطوات أدناه ستقودك عبر إنشاء قماش bitmap، ورسم المنحنى بقلم، وحفظ النتيجة على القرص. سترى أيضًا لماذا Aspose.Drawing يُعد بديلاً موثوقًا عبر المنصات لـ System.Drawing.Common.

## إجابات سريعة
- **ماذا يفعل الأسلوب الأساسي؟** `Graphics.DrawCurve` يُحوّل سلسلة من النقاط إلى منحنى كاردينال سلس.  
- **ما الصيغة المستخدمة لحفظ الصورة؟** PNG عبر `Bitmap.Save`.  
- **هل أحتاج إلى ترخيص لحفظ الصور؟** النسخة التجريبية تعمل للتطوير؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل يمكنني تغيير توتر المنحنى؟** نعم، تُتيح التحميلات الزائدة لـ `DrawCurve` تحديد التوتر.  
- **هل Aspose.Drawing متوافق مع .NET 6+؟** بالتأكيد – يدعم .NET Framework و .NET Core/5/6.

## ما معنى “كيفية حفظ PNG” في سياق Aspose.Drawing؟

حفظ PNG يعني تحويل الـ bitmap الموجود في الذاكرة والذي ترسم عليه إلى ملف PNG فعلي على القرص. تقوم العملية بكتابة بيانات البكسل باستخدام ضغط غير فقدان، مع الحفاظ على الألوان الدقيقة وأي معلومات قناة ألفا. تتولى طريقة `Bitmap.Save` في Aspose.Drawing تشفير PNG تلقائيًا، لذا لا تحتاج إلى إدارة تفاصيل الصيغة بنفسك.

## لماذا رسم منحنى كاردينال باستخدام Aspose.Drawing؟

يُنتج منحنى كاردينال منحنىً سلسًا يتبع مجموعة نقاط التحكم بدقة، مما يجعله مثاليًا لتصوير البيانات، ورسومات واجهة المستخدم، والأشكال المخصصة. يدعم Aspose.Drawing **أكثر من 30 صيغة صورة** ويمكنه معالجة رسومات متعددة الصفحات دون تحميل الملف بالكامل في الذاكرة، ما يمنحك السرعة والمرونة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- Visual Studio (أي نسخة حديثة) مثبتة.  
- مكتبة Aspose.Drawing لـ .NET. يمكنك تنزيلها [هنا](https://releases.aspose.com/drawing/net/).  
- معرفة أساسية ببرمجة C#.

## استيراد المساحات الاسمية

في ملف C# الخاص بك، ابدأ باستيراد المساحة الاسمية اللازمة:

تحتوي مساحة الاسم `Aspose.Drawing` على جميع الأنواع الأساسية مثل `Bitmap` و `Graphics` و `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## الخطوة 1: إنشاء Bitmap (قماش)

أولاً، أنشئ bitmap سيعمل كقماش لرسمك. هذا الـ bitmap هو المكان الذي سيُرسم فيه المنحنى قبل **حفظ الصورة**.

Bitmap يمثل صورة في الذاكرة ذات تنسيق بكسل وأبعاد محددة.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## الخطوة 2: إنشاء كائن Graphics

بعد ذلك، احصل على كائن `Graphics` من الـ bitmap. هذا الكائن يوفر سطح الرسم.

Graphics يوفر سطح رسم لتصيير الأشكال والنصوص والصور على bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 3: تعريف Pen ورسم المنحنى

عرّف `Pen` باللون والعرض المطلوبين، ثم ارسم منحنى كاردينال باستخدام `DrawCurve`. يوضح هذا تقنية **رسم المنحنى بالقلم** ويعمل كمثال **على منحنى كاردينال**.

Pen يضمّن اللون والعرض ونمط الخط المستخدم لرسم الخطوط والمنحنيات.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## الخطوة 4: حفظ الصورة (حفظ المنحنى كـ PNG)

أخيرًا، احفظ الـ bitmap كملف PNG. هذا هو جوهر **كيفية حفظ PNG** في هذا الدرس.

Bitmap.Save يكتب الصورة إلى ملف بالصيغ المحددة، مثل PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **نصيحة احترافية:** استخدم `Path.Combine` لإنشاء مسارات الملفات بأمان عبر الأنظمة.

تهانينا! لقد نجحت في رسم منحنى كاردينال وحفظ النتيجة كصورة PNG باستخدام Aspose.Drawing لـ .NET. لا تتردد في تجربة مصفوفات نقاط مختلفة، ألوان أقلام، أو عرض خطوط لتخصيص منحنياتك.

## حالات الاستخدام الشائعة

- **تصوير البيانات** – مخططات خطية سلسة تحتاج إلى نقاط تحكم دقيقة.  
- **مكوّنات واجهة مستخدم مخصصة** – رسم أزرار، أشرطة تمرير، أو حدود زخرفية.  
- **رسومات قابلة للتصدير** – إنشاء أصول PNG في الوقت الفعلي للتقارير أو محتوى الويب.

## استكشاف الأخطاء وإصلاحها & نصائح

- **الصورة تظهر فارغة؟** تأكد من أن تنسيق بكسل الـ bitmap يدعم الشفافية (`Format32bppPArgb`) وأنك تستدعي `graphics.Clear(Color.Transparent)` إذا لزم الأمر.  
- **شكل المنحنى غير متوقع؟** اضبط معامل التوتر باستخدام التحميل الزائد `DrawCurve(pen, points, tension)`.  
- **أخطاء في الوصول إلى الملف؟** تحقق من وجود الدليل الهدف وأن تطبيقك يملك صلاحيات الكتابة.

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.Drawing في مشاريع تجارية؟**  
ج1: نعم، Aspose.Drawing مناسب للمشاريع الشخصية والتجارية. راجع تفاصيل الترخيص في [صفحة الشراء](https://purchase.aspose.com/buy).

**س2: كيف أحصل على ترخيص مؤقت للاختبار؟**  
ج2: احصل على ترخيص مؤقت لأغراض الاختبار [هنا](https://purchase.aspose.com/temporary-license/).

**س3: أين يمكنني العثور على دعم إضافي؟**  
ج3: زر منتدى [Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على دعم المجتمع والنقاشات.

**س4: هل هناك نسخة تجريبية مجانية؟**  
ج4: نعم، استكشف الميزات مع نسخة [التجربة المجانية](https://releases.aspose.com/) قبل الشراء.

**س5: كيف يمكنني الوصول إلى الوثائق؟**  
ج5: راجع [الوثائق الشاملة](https://reference.aspose.com/drawing/net/) للحصول على معلومات مفصلة وأمثلة.

---

**آخر تحديث:** 2026-05-29  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [Save Bitmap as PNG & Draw Closed Curves with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Save Bitmap C# – Draw Bezier Splines with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Save Bitmap as PNG with Solid Brushes in Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}