---
title: قص الصور في Aspose.Drawing
linktitle: قص الصور في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: إتقان اقتصاص الصور باستخدام Aspose.Drawing لـ .NET. يعمل هذا الدليل التفصيلي على تمكين المطورين من تحسين مهارات معالجة الصور دون عناء.
weight: 10
url: /ar/net/image-editing/cropping/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# قص الصور في Aspose.Drawing

## مقدمة

في عالم تطوير .NET، تبرز Aspose.Drawing كأداة قوية لمعالجة الصور. إحدى ميزاته المفيدة هي القدرة على اقتصاص الصور بدقة. في هذا البرنامج التعليمي، سنتعرف على عملية اقتصاص الصور باستخدام Aspose.Drawing for .NET. استعد لتعزيز مهاراتك في معالجة الصور!

## المتطلبات الأساسية

قبل الغوص في سحر الاقتصاص، تأكد من توفر المتطلبات الأساسية التالية:

-  مكتبة Aspose.Drawing: تأكد من دمج مكتبة Aspose.Drawing في مشروع .NET الخاص بك. إذا لم يكن الأمر كذلك، يمكنك تنزيله[هنا](https://releases.aspose.com/drawing/net/).

-  دليل المستندات: احصل على دليل مخصص لصور مشروعك. يستبدل`"Your Document Directory"` في مقتطفات التعليمات البرمجية مع المسار إلى مجلد صور مشروعك.

## استيراد مساحات الأسماء

لنبدأ باستيراد مساحات الأسماء الضرورية لتمهيد الطريق لمغامرة الاقتصاص الخاصة بنا:

```csharp
using System.Drawing;
```

الآن وبعد أن انتهينا من إعداد المرحلة، فلنقسّم عملية اقتصاص الصورة إلى خطوات يمكن التحكم فيها.

## الخطوة 1: إنشاء صورة نقطية

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

 ابدأ بإنشاء جديد`Bitmap`كائن بالعرض والارتفاع وتنسيق البكسل المطلوب. اضبط الأبعاد لتناسب متطلبات مشروعك المحدد.

## الخطوة 2: إنشاء كائن رسومي

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

 توليد أ`Graphics` كائن من الخاص بك`Bitmap` لتمكين عمليات الرسم. تعيين`InterpolationMode` لمعالجة الصور بشكل أكثر سلاسة، قم بتعديلها بناءً على تفضيلاتك.

## الخطوة 3: قم بتحميل الصورة للاقتصاص

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

 قم بتحميل الصورة التي تريد اقتصاصها إلى صورة جديدة`Bitmap` هدف. يستبدل`"Your Document Directory"` باستخدام المسار إلى مجلد صور مشروعك وضبط اسم الملف وفقًا لذلك.

## الخطوة 4: تحديد مستطيلات المصدر والوجهة

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

حدد المستطيل المصدر لتحديد جزء الصورة الذي تريد اقتصاصه. في هذا المثال، نقوم بتحديد الجزء العلوي الأيسر من الصورة بحجم 50 × 40 بكسل. يتم تعيين مستطيل الوجهة على نفس الأبعاد للحصول على اقتصاص مباشر.

## الخطوة 5: تنفيذ عملية المحاصيل

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

 تنفيذ عملية الاقتصاص باستخدام`DrawImage`طريقة. يأخذ هذا الأمر الصورة المصدر، والمستطيل الوجهة، والمستطيل المصدر، ووحدة قياس المستطيلات.

## الخطوة 6: احفظ الصورة التي تم اقتصاصها

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

وأخيرًا، احفظ الصورة التي تم اقتصاصها في الدليل المخصص لك. اضبط اسم الملف ومساره حسب الحاجة.

تهانينا! لقد نجحت في قص الصورة باستخدام Aspose.Drawing لـ .NET. قم بتجربة أبعاد ومواضع مختلفة لتخصيص عملية الاقتصاص وفقًا لاحتياجاتك المحددة.

## خاتمة

في هذا البرنامج التعليمي، قمنا باستكشاف عملية اقتصاص الصور خطوة بخطوة باستخدام Aspose.Drawing for .NET. يؤدي دمج هذه الوظيفة في مشاريعك إلى فتح عالم من الإمكانيات لمعالجة الصور وتحسينها.

## الأسئلة الشائعة

### س1: هل يمكنني قص الصور بأي تنسيق باستخدام Aspose.Drawing؟

ج1: نعم، يدعم Aspose.Drawing اقتصاص الصور بتنسيقات مختلفة، مما يضمن المرونة في مشروعاتك.

### س2: هل تتوفر خيارات اقتصاص متقدمة؟

ج2: بالتأكيد! يوفر Aspose.Drawing خيارات إضافية للاقتصاص المتقدم، مما يسمح لك بضبط معالجة الصور الخاصة بك.

### س3: هل يمكنني تطبيق عمليات قص متعددة في صورة واحدة؟

ج3: نعم، يمكنك ربط عمليات اقتصاص متعددة لتحقيق تحويلات معقدة للصور بسهولة.

### س 4: هل Aspose.Drawing مناسب لمعالجة الصور المجمعة؟

ج4: في الواقع، يتفوق Aspose.Drawing في معالجة الدفعات، مما يتيح التعامل الفعال مع صور متعددة دفعة واحدة.

### س5: كيف يمكنني الحصول على الدعم للاستعلامات المتعلقة بـ Aspose.Drawing؟

 ج5: توجه إلى[Aspose.منتدى الرسم](https://forum.aspose.com/c/diagram/17) لطلب المساعدة والتواصل مع المجتمع.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
