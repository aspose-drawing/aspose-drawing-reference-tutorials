---
title: تحويل الصفحة في Aspose.Drawing لـ .NET
linktitle: تحويل الصفحة في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: تعرف على تحويلات الصفحة خطوة بخطوة في .NET باستخدام Aspose.Drawing. عزز مهاراتك في الرسم باستخدام هذا البرنامج التعليمي الشامل.
type: docs
weight: 13
url: /ar/net/coordinate-transformations/page-transformation/
---
## مقدمة

مرحبًا بك في هذا البرنامج التعليمي الشامل حول تحويل الصفحة باستخدام Aspose.Drawing لـ .NET. إذا كنت تتطلع إلى تحسين مهاراتك في العمل مع الرسومات وتحويلات الصور النقطية، فأنت في المكان الصحيح. في هذا البرنامج التعليمي، سنرشدك خلال عملية تحويل الصفحات باستخدام Aspose.Drawing، مما يضمن لك فهم كل خطوة بوضوح.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  مكتبة Aspose.Drawing: قم بتنزيل وتثبيت مكتبة Aspose.Drawing. يمكنك العثور على أحدث إصدار[هنا](https://releases.aspose.com/drawing/net/).

- بيئة التطوير: قم بإعداد بيئة التطوير الخاصة بك باستخدام Visual Studio أو أي أداة تطوير .NET مفضلة أخرى.

- دليل المستندات الخاص بك: استبدل "دليل المستندات الخاص بك" في الكود بالدليل الفعلي الذي تريد حفظ الصورة المحولة فيه.

الآن بعد أن قمنا بترتيب متطلباتنا الأساسية، فلنتابع الدليل خطوة بخطوة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية:

```csharp
using System.Drawing;
```

## الخطوة 1: إنشاء صورة نقطية

ابدأ بإنشاء صورة نقطية جديدة ذات أبعاد وتنسيق بكسل محددين:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

يؤدي هذا إلى تهيئة لوحة قماشية فارغة للتحويل الخاص بك.

## الخطوة 2: إنشاء كائن رسومي

قم بإنشاء كائن رسومي من الصورة النقطية للرسم عليه:

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 3: مسح القماش

قم بمسح اللوحة القماشية عن طريق ملئها بلون معين (في هذه الحالة، اللون الرمادي):

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## الخطوة 4: تعيين التحويل

قم بتعيين التحويل الذي يربط إحداثيات الصفحة بإحداثيات الجهاز. في هذا المثال، نستخدم البوصات:

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

## الخطوة 5: ارسم مستطيلاً

استخدم كائن الرسومات لرسم مستطيل بقلم محدد:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

## الخطوة 6: احفظ الصورة

احفظ الصورة المحولة في الدليل المحدد الخاص بك:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

تهانينا! لقد نجحت في تحويل الصفحة باستخدام Aspose.Drawing لـ .NET.

## خاتمة

في هذا البرنامج التعليمي، قمنا بتغطية الخطوات الأساسية لإجراء تحويل الصفحة باستخدام Aspose.Drawing. باتباع هذه الخطوات، يمكنك دمج هذه التحويلات في تطبيقات .NET الخاصة بك بسلاسة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.Drawing مجانًا؟

 ج1: يقدم Aspose.Drawing نسخة تجريبية مجانية يمكنك الوصول إليها[هنا](https://releases.aspose.com/).

### س2: أين يمكنني العثور على الوثائق التفصيلية الخاصة بـ Aspose.Drawing؟

 ج2: الوثائق متاحة[هنا](https://reference.aspose.com/drawing/net/).

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.Drawing؟

 ج3: للحصول على الدعم، قم بزيارة[Aspose.منتدى الرسم](https://forum.aspose.com/c/diagram/17).

### س4: هل يتوفر ترخيص مؤقت لـ Aspose.Drawing؟

 ج4: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني شراء Aspose.Drawing؟

 ج5: يمكنك شراء Aspose.Drawing[هنا](https://purchase.aspose.com/buy).