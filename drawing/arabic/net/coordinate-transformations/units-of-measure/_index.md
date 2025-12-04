---
title: وحدات القياس في Aspose.Drawing لـ .NET
linktitle: وحدات القياس في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: استكشف تعدد استخدامات Aspose.Drawing لـ .NET في هذا البرنامج التعليمي المتعمق، وإتقان وحدات القياس للرسومات الدقيقة.
weight: 14
url: /ar/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# وحدات القياس في Aspose.Drawing لـ .NET

## مقدمة

مرحبًا بك في عالم Aspose.Drawing لـ .NET، حيث تلتقي الدقة والمرونة في معالجة الرسومات. في هذا البرنامج التعليمي، سوف نتعمق في تعقيدات وحدات القياس داخل Aspose.Drawing، مما يوفر لك دليلًا خطوة بخطوة للاستفادة من قوة هذه المكتبة الرائعة.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.Drawing for .NET: تأكد من تثبيت المكتبة. يمكنك تنزيله[هنا](https://releases.aspose.com/drawing/net/).

- دليل المستندات: احصل على دليل مخصص حيث تريد حفظ المستندات التي تم إنشاؤها.

- المعرفة الأساسية لـ C#: يوصى بالفهم الأساسي لـ C# لتحقيق أقصى استفادة من هذا الدليل.

## استيراد مساحات الأسماء

قبل أن نبدأ، فلنستورد مساحات الأسماء الضرورية لاستخدام Aspose.Drawing بفعالية:

```csharp
using System.Drawing;
```

الآن، دعونا نقسم كل مثال إلى خطوات متعددة:

## النقاط كوحدات القياس

1. إنشاء صورة نقطية: قم بتهيئة صورة نقطية بعرض وارتفاع محددين.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. إنشاء رسومات: قم بإنشاء كائن رسومي من الصورة النقطية للرسم عليه.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. تعيين وحدة الصفحة على النقاط: حدد النقاط كوحدة قياس (نقطة واحدة = 1/72 بوصة).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. رسم مستطيل: ارسم مستطيلًا باستخدام النقاط كوحدة.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## ملليمتر كوحدات القياس

1. ضبط وحدة الصفحة على المليمترات: قم بتغيير وحدة القياس إلى المليمترات (1 مم = 1/25.4 بوصة).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. رسم المستطيل بالملليمتر: ارسم مستطيلًا آخر باستخدام المليمتر كوحدة.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## بوصة كوحدات القياس

1. ضبط وحدة الصفحة على البوصة: قم بتبديل وحدة القياس إلى البوصة.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. رسم مستطيل بالبوصة: ارسم مستطيلًا باستخدام البوصة كوحدة.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## احفظ النتيجة

بعد إكمال الأمثلة، احفظ الصورة الناتجة في دليل المستندات الخاص بك:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

لقد نجحت الآن في التنقل بين وحدات القياس المتنوعة في Aspose.Drawing لـ .NET، وإنشاء تمثيل مرئي للمستطيلات باستخدام النقاط والمليمترات والبوصات.

## خاتمة

في هذا البرنامج التعليمي، اكتشفنا كيفية تعامل Aspose.Drawing for .NET مع وحدات القياس المختلفة. ومن خلال معالجة النقاط والمليمترات والبوصات، يمكنك تحقيق الدقة والقدرة على التكيف في إبداعاتك الرسومية. قم بتجربة هذه المفاهيم لفتح الإمكانات الكاملة لـ Aspose.Drawing.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.Drawing لـ .NET مع أطر عمل .NET الأخرى؟

ج1: نعم، Aspose.Drawing متوافق مع أطر عمل .NET المختلفة، مما يوفر المرونة في بيئة التطوير الخاصة بك.

### س2: هل هناك نسخة تجريبية مجانية متاحة؟

 ج2: نعم، يمكنك استكشاف Aspose.Drawing باستخدام نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### Q3: كيف يمكنني الحصول على دعم Aspose.Drawing لـ .NET؟

 ج3: قم بزيارة[Aspose.منتدى الرسم](https://forum.aspose.com/c/drawing/44) لدعم المجتمع والمناقشات.

### س4: هل يمكنني شراء ترخيص مؤقت للمشاريع قصيرة المدى؟

 ج4: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على الوثائق التفصيلية الخاصة بـ Aspose.Drawing؟

 ج5: الوثائق الشاملة متاحة[هنا](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
