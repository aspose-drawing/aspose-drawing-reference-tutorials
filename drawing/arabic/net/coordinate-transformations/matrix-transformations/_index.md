---
date: 2025-11-29
description: تعلم هذا الدرس حول تحويل المصفوفات لـ Aspose.Drawing .NET، والذي يغطي
  كيفية رسم مستطيل مُدوَّر، تطبيق دوران المصفوفة، وإجراء تحجيم المصفوفة باستخدام C#.
language: ar
linktitle: Matrix Transformations in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 'دروس تحويل المصفوفات: تحويلات المصفوفة في Aspose.Drawing لـ .NET'
url: /net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل تحويل المصفوفات: تحويلات المصفوفة في Aspose.Drawing لـ .NET

## المقدمة

مرحبًا بك في هذا **دليل تحويل المصفوفات** الخاص بـ Aspose.Drawing .NET! سواءً كنت تبني محرر رسومات، أو تُنشئ تقارير ديناميكية، أو مجرد تجربة تأثيرات هندسية، فإن إتقان تحويلات المصفوفة يتيح لك **رسم مستطيلات مدورة**، **تطبيق تدوير المصفوفة**، وحتى إجراء عمليات **تحجيم المصفوفة C#** بدقة. خلال الدقائق القليلة القادمة ستتعرف على كيفية إعداد لوحة رسم، تحويل الأشكال، وحفظ النتيجة — كل ذلك باستخدام واجهة برمجة التطبيقات القوية Aspose.Drawing.

## إجابات سريعة
- **ما الذي يغطيه هذا الدرس؟** تنفيذ عمليات تدوير، إزاحة، وتكبير/تصغير للمصفوفة على مستطيل باستخدام Aspose.Drawing.  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6/7.  
- **كم من الوقت سيستغرق التنفيذ؟** حوالي 10‑15 دقيقة لتطبيق مثال أساسي.  
- **هل يمكنني رؤية صورة الإخراج؟** نعم – يحفظ الدرس صورة PNG يمكنك فتحها مباشرة.

## ما هو دليل تحويل المصفوفة؟

يشرح دليل تحويل المصفاة كيفية استخدام مصفوفة تحويل 3 × 3 لتحريك، تدوير، تكبير/تصغير، أو قص الرسومات الأولية. في Aspose.Drawing، تُجسّد فئة `Matrix` هذه العمليات، مما يتيح لك تعديل أي `GraphicsPath` أو شكل باستخدام كائن واحد قابل لإعادة الاستخدام.

## لماذا نستخدم Aspose.Drawing لتحويلات المصفوفة؟

- **توافق متعدد المنصات** – يعمل على Windows وLinux وmacOS دون قيود System.Drawing.Common.  
- **أداء عالي في التصيير** – مُحسّن للصور الكبيرة والعمليات المتجهية المعقدة.  
- **تغطية كاملة لواجهة .NET** – مماثلة لمفاهيم GDI+، مما يجعل الانتقال سهلًا.

## المتطلبات المسبقة

قبل المتابعة، تأكد من وجود:

- معرفة أساسية بلغة C#.  
- بيئة تطوير تحتوي على Aspose.Drawing لـ .NET مثبتة. إذا لم تقم بتحميله بعد، احصل عليه [من هنا](https://releases.aspose.com/drawing/net/).  
- إلمام بمفاهيم الرسومات مثل لوحات البت ماب والمستطيلات.

## استيراد المساحات الاسمية

أولًا، استورد المساحات الاسمية المطلوبة:

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

تمنحك هذه المساحات الاسمية الوصول إلى `Bitmap` و`Graphics` وفئة `Matrix` اللازمة للتحويلات.

## دليل خطوة بخطوة

### الخطوة 1: إعداد اللوحة

أنشئ bitmap سيعمل كسطح الرسم. نقوم أيضًا بمسحه بخلفية رمادية محايدة لتبرز الأشكال المحوّلة.

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **نصيحة احترافية:** استخدام `Format32bppPArgb` يضمن معالجة صحيحة للشفافية عند تطبيق مضاد التعرج لاحقًا.

### الخطوة 2: تعريف المستطيل الأصلي

هذا المستطيل هو الشكل الأساسي الذي سنحوّله. تم اختيار إحداثياته لتبقى داخل حدود اللوحة.

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### الخطوة 3: تدوير المستطيل (رسم مستطيل مدور)

نقوم الآن **بتطبيق تدوير المصفوفة** بزاوية 15 درجة حول الأصل. الطريقة المساعدة `TransformPath` (الموضحة لاحقًا) تستقبل دالة لامبدا تُعطي كائن `Matrix`.

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### الخطوة 4: إزاحة المستطيل

الإزاحة تحرك الشكل دون تغيير حجمه أو اتجاهه. هنا نقوم بنقله إلى اليسار‑أعلى بمقدار 250 بكسل.

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### الخطوة 5: تحجيم المستطيل (matrix scaling C#)

التحجيم يغيّر أبعاد المستطيل. العامل `0.3f` يقلل كل من العرض والارتفاع إلى 30 % من الحجم الأصلي.

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### الخطوة 6: حفظ النتيجة

أخيرًا، اكتب الصورة المحوّلة إلى القرص. عدّل المسار ليتوافق مع مجلد موجود على جهازك.

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **ملاحظة:** طريقة `TransformPath` (المستخدمة في الخطوات السابقة) تُنشئ `GraphicsPath` من المستطيل، تُطبق المصفوفة المُعطاة، وتُرسم الشكل المحوَّل. إنها طريقة مختصرة لإعادة استخدام منطق الرسم نفسه لكل تحويل.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **الصورة تظهر فارغة** | تأكد من وجود دليل الإخراج وأن لديك صلاحيات الكتابة. |
| **التحويلات تبدو غير مركزة** | تذكر أن `Matrix.Rotate` يدور حول الأصل (0,0). قم بإزاحة الشكل إلى نقطة المحور المطلوبة قبل التدوير. |
| **بطء الأداء مع صور كبيرة** | استخدم `graphics.SmoothingMode = SmoothingMode.AntiAlias;` فقط عند الحاجة، وتأكد من تحرير كائنات `Graphics` فورًا. |

## الأسئلة المتكررة

**س: أين يمكنني العثور على وثائق Aspose.Drawing؟**  
ج: الوثائق متاحة [هنا](https://reference.aspose.com/drawing/net/).

**س: كيف أحصل على ترخيص مؤقت لـ Aspose.Drawing؟**  
ج: احصل على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني طلب الدعم أو التواصل مع المجتمع؟**  
ج: زر منتدى Aspose.Drawing [هنا](https://forum.aspose.com/c/drawing/44).

**س: هل يمكنني تحميل Aspose.Drawing لـ .NET؟**  
ج: نعم، حمّله من [هذا الرابط](https://releases.aspose.com/drawing/net/).

**س: كيف يمكنني شراء Aspose.Drawing؟**  
ج: اشترِ الترخيص الخاص بك [هنا](https://purchase.aspose.com/buy).

## الخاتمة

لقد أكملت الآن **دليل تحويل المصفوفات** الكامل باستخدام Aspose.Drawing لـ .NET. تعرفت على كيفية **رسم مستطيلات مدورة**، **تطبيق تدوير المصفوفة**، وإجراء **تحجيم المصفوفة C#** على أي شكل. جرّب ربط عدة تحويلات أو استخدام نقاط محورية مخصصة لاكتشاف تأثيرات رسومية إبداعية أكثر.

---

**آخر تحديث:** 2025-11-29  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}