---
date: 2026-05-03
description: تعلم هذا الدرس حول تحويل المصفوفة لـ Aspose.Drawing .NET، بما يشمل كيفية
  رسم مستطيل مُدوَّر، وتطبيق دوران المصفوفة، وإجراء تحجيم المصفوفة باستخدام C#.
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- cross platform drawing
- matrix rotation c#
- c# graphics matrix
linktitle: تحويلات المصفوفة في Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 'دليل تحويل المصفوفات: تحويلات المصفوفة في Aspose.Drawing لـ .NET'
url: /ar/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل تحويل المصفوفة: تحويلات المصفوفة في Aspose.Drawing لـ .NET

## مقدمة

مرحبًا بك في **matrix transformation tutorial** لـ Aspose.Drawing .NET! سواء كنت تبني محرر رسومات، أو تولد تقارير ديناميكية، أو مجرد تجربة التأثيرات الهندسية، فإن إتقان تحويلات المصفوفة يتيح لك **draw rotated rectangle**، **apply matrix rotation**، وحتى إجراء عمليات **matrix scaling C#** بدقة. خلال الدقائق القليلة القادمة ستتعرف على كيفية إعداد لوحة رسم، تحويل الأشكال، وحفظ النتيجة — كل ذلك باستخدام واجهة برمجة التطبيقات القوية Aspose.Drawing.

## إجابات سريعة

- **ما الذي يغطيه هذا الدرس؟** Performing rotate, translate, and scale matrix transformations on a rectangle with Aspose.Drawing.  
- **هل أحتاج إلى ترخيص؟** A free trial works for development; a commercial license is required for production.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **كم من الوقت سيستغرق التنفيذ؟** About 10‑15 minutes for a basic example.  
- **هل يمكنني رؤية صورة الإخراج؟** Yes – the tutorial saves a PNG you can open directly.

## ما هو درس تحويل المصفوفة؟

يشرح درس تحويل المصفوفة كيفية استخدام مصفوفة تحويل 3 × 3 لتحريك أو تدوير أو تحجيم أو قص أ primitive الرسومات. في Aspose.Drawing، تُغلف الفئة `Matrix` هذه العمليات، مما يتيح لك تعديل أي `GraphicsPath` أو شكل باستخدام كائن واحد قابل لإعادة الاستخدام.

## لماذا تستخدم Aspose.Drawing لتحويلات المصفوفة؟

- **رسم متعدد المنصات** – يعمل على Windows وLinux وmacOS دون قيود System.Drawing.Common.  
- **عرض عالي الأداء** – مُحسّن للصور الكبيرة والعمليات المتجهية المعقدة.  
- **تغطية كاملة لواجهة .NET API** – مماثل لمفاهيم GDI+، مما يجعل الانتقال سهلًا.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك:

- معرفة أساسية بلغة C#.  
- بيئة تطوير مثبت فيها Aspose.Drawing لـ .NET. إذا لم تقم بتنزيله بعد، احصل عليه [هنا](https://releases.aspose.com/drawing/net/).  
- إلمام بمفاهيم الرسومات مثل لوحات البت ماب والمستطيلات.

## استيراد المساحات الاسمية

أولاً، استورد مساحات الأسماء المطلوبة إلى النطاق:

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## دليل خطوة بخطوة

فيما يلي دليل مختصر مرقم. كل خطوة تتضمن شرحًا موجزًا يليه الكود الدقيق الذي ستحتاجه (كتل الكود تبقى دون تغيير من الدرس الأصلي).

### الخطوة 1: إعداد اللوحة

أنشئ صورة bitmap ستعمل كسطح الرسم. نقوم أيضًا بمسحها بخلفية رمادية محايدة لتبرز الأشكال المحوّلة.

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **نصيحة احترافية:** Using `Format32bppPArgb` ensures correct alpha handling when you later apply anti‑aliasing.

### الخطوة 2: تعريف المستطيل الأصلي

هذا المستطيل هو الشكل الأساسي الذي سنحوّله. تم اختيار إحداثياته لتبقى داخل حدود اللوحة بشكل جيد.

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### الخطوة 3: تدوير المستطيل (draw rotated rectangle)

نقوم الآن **apply matrix rotation** بزاوية 15 درجة حول الأصل. الطريقة المساعدة `TransformPath` (الموضحة لاحقًا) تأخذ دالة لامبدا تستقبل كائن `Matrix`.

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### الخطوة 4: إزاحة المستطيل

الإزاحة تنقل الشكل دون تعديل حجمه أو اتجاهه. هنا نقوم بتحريكه إلى اليسار‑أعلى بمقدار 250 بكسل.

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### الخطوة 5: تحجيم المستطيل (matrix scaling C#)

التحجيم يغيّر أبعاد المستطيل. عامل `0.3f` يقلل كل من العرض والارتفاع إلى 30 % من الحجم الأصلي.

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

> **ملاحظة:** طريقة `TransformPath` (المستخدمة في الخطوات السابقة) تنشئ `GraphicsPath` من المستطيل، تطبق المصفوفة المقدمة، وترسم الشكل المحوَّل. إنها طريقة مختصرة لإعادة استخدام نفس منطق الرسم لكل تحويل.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **الصورة تظهر فارغة** | تأكد من وجود دليل الإخراج وأن لديك أذونات كتابة. |
| **التحويلات غير مركزة** | تذكر أن `Matrix.Rotate` يدور حول الأصل (0,0). قم بإزاحة الشكل إلى نقطة المحور المطلوبة قبل الدوران. |
| **بطء الأداء على الصور الكبيرة** | استخدم `graphics.SmoothingMode = SmoothingMode.AntiAlias;` فقط عند الحاجة، وتخلص من كائنات `Graphics` بسرعة. |

## الأسئلة المتكررة

**س: أين يمكنني العثور على وثائق Aspose.Drawing؟**  
ج: الوثائق متاحة [هنا](https://reference.aspose.com/drawing/net/).

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.Drawing؟**  
ج: احصل على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني طلب الدعم أو التواصل مع المجتمع؟**  
ج: زر منتدى Aspose.Drawing [هنا](https://forum.aspose.com/c/drawing/).

**س: هل يمكنني تنزيل Aspose.Drawing لـ .NET؟**  
ج: نعم، قم بتنزيله من [هذا الرابط](https://releases.aspose.com/drawing/net/).

**س: كيف يمكنني شراء Aspose.Drawing؟**  
ج: اشترِ الترخيص الخاص بك [هنا](https://purchase.aspose.com/buy).

## الخلاصة

لقد أكملت الآن **matrix transformation tutorial** كاملًا باستخدام Aspose.Drawing لـ .NET. أنت الآن تعرف كيف **draw rotated rectangle**، **apply matrix rotation**، وتنفّذ **matrix scaling C#** على أي شكل. جرّب ربط عدة تحويلات معًا أو استخدام نقاط محور مخصصة لفتح المزيد من التأثيرات الرسومية الإبداعية.

---

**آخر تحديث:** 2026-05-03  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}