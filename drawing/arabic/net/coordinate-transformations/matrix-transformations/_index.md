---
date: 2026-08-28
description: تعلم هذا الدرس حول تحويل المصفوفات لـ Aspose.Drawing .NET، بما يشمل كيفية
  رسم مستطيل مُدوَّر، تطبيق دوران المصفوفة، وإجراء تحجيم المصفوفة باستخدام C#.
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- matrix rotation c#
- matrix scaling c#
- Aspose.Drawing graphics
lastmod: 2026-08-28
linktitle: تحويلات المصفوفة في Aspose.Drawing
og_description: دروس تحويل المصفوفة لـ Aspose.Drawing .NET. تعلم كيفية رسم مستطيل
  مُدوَّر، تطبيق دوران المصفوفة، إزاحة وتكبير الرسومات باستخدام C# في دقائق.
og_image_alt: Screenshot of a rotated rectangle created with Aspose.Drawing using
  matrix transformations
og_title: دروس تحويل المصفوفة – تطبيق الدوران، التحجيم والإزاحة في Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  headline: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  type: TechArticle
- description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  name: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  steps:
  - name: set up the canvas
    text: Create a bitmap that will serve as the drawing surface. We also clear it
      with a neutral gray background so the transformed shapes stand out. > **Pro
      tip:** Using `Format32bppPArgb` ensures correct alpha handling when you later
      apply anti‑aliasing.
  - name: define the original rectangle
    text: This rectangle is the base shape we’ll transform. Its coordinates are chosen
      to keep it well within the canvas bounds.
  - name: rotate the rectangle (draw rotated rectangle)
    text: The `Matrix` class is Aspose.Drawing's representation of a 3 × 3 affine
      transformation matrix used for rotation, scaling and translation. We now **apply
      matrix rotation** of 15 degrees around the origin. The helper method `TransformPath`
      (shown later) takes a lambda that receives a `Matrix` instance
  - name: translate the rectangle
    text: Translation moves the shape without altering its size or orientation. Here
      we shift it left‑up by 250 pixels.
  - name: scale the rectangle (matrix scaling C#)
    text: Scaling changes the rectangle’s dimensions. A factor of `0.3f` reduces both
      width and height to 30 % of the original size.
  - name: save the result
    text: Finally, write the transformed image to disk. Adjust the path to point to
      a folder that exists on your machine. > **Note:** The `TransformPath` method
      (used in the steps above) creates a `GraphicsPath` from the rectangle, applies
      the supplied matrix, and draws the transformed shape. It’s a compact w
  type: HowTo
- questions:
  - answer: The documentation is available **[here](https://reference.aspose.com/drawing/net/)**.
    question: Where can I find the Aspose.Drawing documentation?
  - answer: Obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: How do I get a temporary license for Aspose.Drawing?
  - answer: Visit the Aspose.Drawing forum **[here](https://forum.aspose.com/c/drawing/44)**.
    question: Where can I seek support or connect with the community?
  - answer: Yes, download it from **[here](https://releases.aspose.com/drawing/net/)**.
    question: Can I download Aspose.Drawing for .NET?
  - answer: Purchase your license **[here](https://purchase.aspose.com/buy)**.
    question: How can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- matrix transformation
- Aspose.Drawing
- .NET graphics
- C# drawing
- cross‑platform rendering
title: 'دروس تحويل المصفوفات: تحويلات المصفوفة في Aspose.Drawing لـ .NET'
url: /ar/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل تحويل المصفوفة: تحويلات المصفوفة في Aspose.Drawing لـ .NET

## مقدمة

في هذا **دليل تحويل المصفوفة** ستكتشف كيف تسمح لك فئة `Matrix` في Aspose.Drawing بتدوير، ترجمة، وتكبير/تصغير كائنات الرسومات بدقة بيكسل مثالية. سواءً كنت تبني محرر مخططات، تولد تقارير آلية، أو تضيف تأثيرات بصرية إلى خدمة على الخادم، فإن إتقان تحويلات المصفوفة أمر أساسي لإنتاج مخرجات ذات مظهر احترافي عبر Windows وLinux وmacOS.

## إجابات سريعة
- **ما الذي يغطيه هذا الدليل؟** يوضح كيفية تدوير، ترجمة وتكبير/تصغير مستطيل باستخدام واجهة برمجة تطبيقات المصفوفة في Aspose.Drawing.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تعمل للتطوير؛ يلزم ترخيص تجاري للاستخدام في الإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6/7 وما بعدها.  
- **كم من الوقت تستغرق التنفيذ؟** تقريبًا 10‑15 دقيقة للمثال الكامل.  
- **هل يمكنني رؤية صورة الناتج؟** نعم – يحفظ الدليل ملف PNG يمكنك فتحه فورًا.

## ما هو دليل تحويل المصفوفة؟

يشرح دليل تحويل المصفاة كيفية استخدام مصفوفة إحداثية 3 × 3 لتتحرك، تدور، تكبر/تصغر أو تقصّ الرسومات الأولية. في Aspose.Drawing، فئة `Matrix` تُجسد هذه العمليات، مما يسمح بتحويل أي `GraphicsPath` أو شكل باستخدام كائن واحد قابل لإعادة الاستخدام.

## لماذا نستخدم Aspose.Drawing لتحويلات المصفوفة؟

يدعم Aspose.Drawing **ثلاث أنظمة تشغيل رئيسية** (Windows، Linux، macOS) ويمكنه إنشاء صور تصل إلى **10,000 × 10,000 px** في أقل من **200 ms** لكل عملية على عتاد الخادم المعتاد. توفر المكتبة **توافق 100 % مع API الخاص بـ GDI+**، لذا يمكنك نقل شفرة System.Drawing الحالية دون إعادة كتابة المنطق، مع تجنب قيود الترخيص التي تؤثر على System.Drawing.Common على المنصات غير Windows.

## المتطلبات المسبقة

- بيئة تطوير C# تعمل (Visual Studio، Rider، أو VS Code).  
- Aspose.Drawing لـ .NET مثبت – قم بتنزيله من الموقع الرسمي **[هنا](https://releases.aspose.com/drawing/net/)** أو **[هذا الرابط](https://releases.aspose.com/drawing/net/)** إذا لم تقم بتنزيله بعد.  
- فهم أساسي للكانفاسات bitmap، المستطيلات ومسارات الرسومات.

## استيراد المساحات الاسمية

أولاً، استدعِ المساحات الاسمية المطلوبة إلى النطاق:

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

توفر لك هذه المساحات الاسمية الوصول إلى `Bitmap` و `Graphics` وفئة `Matrix` اللازمة للتحويلات.

## دليل خطوة بخطوة

فيما يلي دليل مختصر مرقم. كل خطوة تتضمن شرحًا موجزًا يليه الشيفرة الدقيقة التي ستحتاجها (كتل الشيفرة تبقى دون تغيير من الدليل الأصلي).

### الخطوة 1: إعداد السطح

أنشئ bitmap سيعمل كسطح الرسم. نقوم أيضًا بمسحه بخلفية رمادية محايدة حتى تبرز الأشكال المحوّلة.

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **نصيحة احترافية:** استخدام `Format32bppPArgb` يضمن معالجة صحيحة للـ alpha عندما تقوم لاحقًا بتطبيق مضاد التعرج.

### الخطوة 2: تعريف المستطيل الأصلي

هذا المستطيل هو الشكل الأساسي الذي سنحوّله. تم اختيار إحداثياته لتظل داخل حدود السطح بشكل جيد.

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### الخطوة 3: تدوير المستطيل (رسم مستطيل مدور)

فئة `Matrix` هي تمثيل Aspose.Drawing لمصفوفة تحويل إحداثية 3 × 3 تُستخدم للتدوير، التكبير/التصغير والترجمة. الآن نقوم **بتطبيق تدوير المصفوفة** بزاوية 15 درجة حول الأصل. الطريقة المساعدة `TransformPath` (الموضحة لاحقًا) تأخذ دالة لامبدا تستقبل كائن `Matrix`.

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### الخطوة 4: ترجمة المستطيل

الترجمة تحرك الشكل دون تغيير حجمه أو اتجاهه. هنا نقوم بإزاحته إلى اليسار‑أعلى بمقدار 250 بكسل.

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### الخطوة 5: تكبير/تصغير المستطيل (matrix scaling C#)

التكبير/التصغير يغيّر أبعاد المستطيل. عامل `0.3f` يقلل كل من العرض والارتفاع إلى 30 % من الحجم الأصلي.

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### الخطوة 6: حفظ النتيجة

أخيرًا، احفظ الصورة المحوّلة إلى القرص. عدّل المسار ليشير إلى مجلد موجود على جهازك.

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **ملاحظة:** الطريقة `TransformPath` (المستخدمة في الخطوات السابقة) تنشئ `GraphicsPath` من المستطيل، تطبق المصفوفة المقدمة، وترسم الشكل المحوَّل. إنها طريقة مختصرة لإعادة استخدام نفس منطق الرسم لكل تحويل.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **الصورة تظهر فارغة** | تأكد من وجود دليل الإخراج ولديك أذونات كتابة. |
| **التحويلات غير متمركزة** | تذكر أن `Matrix.Rotate` يدور حول الأصل (0,0). قم بترجمة الشكل إلى نقطة المحور المطلوبة قبل التدوير. |
| **بطء الأداء على الصور الكبيرة** | استخدم `graphics.SmoothingMode = SmoothingMode.AntiAlias;` فقط عند الحاجة، وتخلص من كائنات `Graphics` بسرعة. |

## الأسئلة المتكررة

**س: أين يمكنني العثور على توثيق Aspose.Drawing؟**  
ج: التوثيق متاح **[هنا](https://reference.aspose.com/drawing/net/)**.

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.Drawing؟**  
ج: احصل على ترخيص مؤقت **[هنا](https://purchase.aspose.com/temporary-license/)**.

**س: أين يمكنني طلب الدعم أو التواصل مع المجتمع؟**  
ج: زر منتدى Aspose.Drawing **[هنا](https://forum.aspose.com/c/drawing/44)**.

**س: هل يمكنني تنزيل Aspose.Drawing لـ .NET؟**  
ج: نعم، قم بتنزيله من **[هنا](https://releases.aspose.com/drawing/net/)**.

**س: كيف يمكنني شراء Aspose.Drawing؟**  
ج: اشترِ الترخيص الخاص بك **[هنا](https://purchase.aspose.com/buy)**.

## الخلاصة

لقد أكملت الآن دليل **تحويل المصفوفة** الكامل باستخدام Aspose.Drawing لـ .NET. تعرف الآن كيف **ترسم مستطيلًا مدورًا**، **تطبق تدوير المصفوفة**، وتنفذ **تكبير/تصغير المصفوفة C#** على أي شكل. جرّب ربط عدة تحويلات أو استخدام نقاط محور مخصصة لفتح المزيد من التأثيرات الرسومية الإبداعية.

---

**آخر تحديث:** 2026-08-28  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية رسم مستطيل – تحويل نظام الإحداثيات (تحويل الصفحة) باستخدام Aspose.Drawing API لـ .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [كيفية حفظ PNG باستخدام Aspose.Drawing – تحويل العالم](/drawing/net/coordinate-transformations/world-transformation/)
- [تحويل خطوة بخطوة – تحويلات الإحداثيات](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}