---
title: تحجيم الصور في Aspose.Drawing
linktitle: تحجيم الصور في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: تعرف على كيفية تغيير حجم الصور بسهولة في .NET باستخدام Aspose.Drawing. يضمن دليلنا خطوة بخطوة التكامل السلس، مما يوفر إمكانات قوية لمعالجة الصور.
weight: 14
url: /ar/net/image-editing/scale/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحجيم الصور في Aspose.Drawing

## مقدمة

مرحبًا بك في هذا الدليل الشامل حول تغيير حجم الصور باستخدام Aspose.Drawing for .NET! في العالم الديناميكي لتطوير البرمجيات، تعد معالجة الصور وقياسها متطلبًا شائعًا. يعمل Aspose.Drawing على تبسيط هذه العملية، حيث يقدم أدوات ووظائف قوية للعمل مع الصور في تطبيقات .NET الخاصة بك.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:

1.  Aspose.Drawing for .NET: تأكد من تثبيت مكتبة Aspose.Drawing في مشروعك. يمكنك تنزيله[هنا](https://releases.aspose.com/drawing/net/).

2. بيئة التطوير: قم بإعداد بيئة تطوير .NET، مثل Visual Studio.

3. الفهم الأساسي لـ C#: يعد الإلمام بلغة البرمجة C# أمرًا ضروريًا لتنفيذ الأمثلة.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية. تعتبر هذه الخطوة ضرورية للوصول إلى وظائف Aspose.Drawing بسلاسة.

```csharp
using System.Drawing;
```

## الخطوة 1: إنشاء صورة نقطية

ابدأ بإنشاء كائن نقطي سيكون بمثابة لوحة قماشية لصورتك. حدد العرض والارتفاع وتنسيق البكسل وفقًا لمتطلباتك.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## الخطوة 2: إنشاء كائن رسومي

بعد ذلك، قم بإنشاء كائن رسومي من الصورة النقطية التي تم إنشاؤها مسبقًا. سيوفر هذا الكائن إمكانيات الرسم اللازمة لمعالجة الصور.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 3: ضبط وضع الاستيفاء

لتحسين جودة الصورة التي تم تغيير حجمها، اضبط وضع الاستيفاء. في هذا المثال، نستخدم وضع الاستيفاء NearestNeighbor.

```csharp
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

## الخطوة 4: تحميل الصورة

 قم بتحميل الصورة التي تريد تغيير حجمها إلى كائن نقطي. يستبدل`"Your Document Directory" + @"Images\aspose_logo.png"` مع المسار إلى صورتك.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

## الخطوة 5: تغيير حجم الصورة

حدد مستطيلاً يمثل توسيع الصورة. في هذا المثال، يتم تغيير حجم الصورة 5 مرات، سواء في العرض أو الارتفاع.

```csharp
Rectangle expansionRectangle = new Rectangle(0, 0, image.Width * 5, image.Height * 5);
graphics.DrawImage(image, expansionRectangle);
```

## الخطوة 6: احفظ الصورة التي تم تغيير حجمها

احفظ الصورة التي تم تغيير حجمها إلى الموقع المطلوب. اضبط مسار الملف وفقًا لبنية مشروعك.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Scale_out.png");
```

تهانينا! لقد نجحت في تغيير حجم الصورة باستخدام Aspose.Drawing لـ .NET.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا عملية تغيير حجم الصور باستخدام Aspose.Drawing. تمكن هذه المكتبة المطورين من التعامل بكفاءة مع مهام معالجة الصور ضمن تطبيقات .NET الخاصة بهم. باتباع الدليل الموضح خطوة بخطوة، اكتسبت رؤى قيمة حول تنفيذ تغيير حجم الصورة.

لا تتردد في تجربة المزيد واستكشاف الميزات الأخرى التي يوفرها Aspose.Drawing لرفع قدرات معالجة الصور لديك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.Drawing لـ .NET في كل من تطبيقات الويب وسطح المكتب؟

ج1: نعم، Aspose.Drawing متعدد الاستخدامات ويمكن استخدامه في العديد من تطبيقات .NET، بما في ذلك الويب وسطح المكتب.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.Drawing؟

 ج2: نعم، يمكنك الحصول على ترخيص مؤقت[هنا](https://purchase.aspose.com/temporary-license/) لأغراض الاختبار والتقييم.

### س3: أين يمكنني العثور على دعم إضافي لـ Aspose.Drawing؟

 ج3: لأية استفسارات أو مساعدة، قم بزيارة[Aspose.منتدى الرسم](https://forum.aspose.com/c/diagram/17).

### س 4: هل هناك أي قيود على تنسيقات الصور التي يدعمها Aspose.Drawing؟

 A4: يدعم Aspose.Drawing نطاقًا واسعًا من تنسيقات الصور، بما في ذلك JPEG وPNG وGIF وBMP والمزيد. الرجوع إلى[توثيق](https://reference.aspose.com/drawing/net/) للحصول على قائمة مفصلة.

### س5: هل يمكنني تطبيق أوضاع الاستيفاء المخصصة لتغيير حجم الصورة؟

ج5: نعم، يوفر Aspose.Drawing المرونة، مما يسمح لك بالاختيار من بين أوضاع الاستيفاء المتنوعة لتغيير حجم الصورة.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
