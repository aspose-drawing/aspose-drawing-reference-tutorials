---
title: رسم النص في Aspose.Drawing
linktitle: رسم النص في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: قم بتحسين تطبيقات .NET الخاصة بك بنص ديناميكي باستخدام Aspose.Drawing لـ .NET. اتبع دليلنا خطوة بخطوة لرسم النص وتخصيص الخطوط وإنشاء صور جذابة.
type: docs
weight: 10
url: /ar/net/text-and-fonts/draw-text/
---
## مقدمة

مرحبًا بك في هذا الدليل المفصل خطوة بخطوة حول رسم النص باستخدام Aspose.Drawing لـ .NET! إذا كنت تتطلع إلى تحسين تطبيقات .NET الخاصة بك بنص غني وجذاب بصريًا، فأنت في المكان الصحيح. في هذا البرنامج التعليمي، سنرشدك خلال عملية إنشاء نص ديناميكي في الصور باستخدام Aspose.Drawing.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.Drawing for .NET: تأكد من تثبيت المكتبة. يمكنك تنزيله من[Aspose.Drawing الوثائق](https://reference.aspose.com/drawing/net/).

- بيئة التطوير: قم بإعداد بيئة تطوير .NET، مثل Visual Studio، على جهازك.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية إلى مشروعك:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## الخطوة 1: إنشاء كائنات نقطية ورسومية

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

في هذه الخطوة، نقوم بإنشاء كائن نقطي بعرض وارتفاع محددين. تتم بعد ذلك تهيئة كائن الرسومات، وإعداد الصقل لتقديم نص سلس.

## الخطوة 2: إعداد الفرشاة والقلم والخط

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

هنا، نحدد SolidBrush للون النص، وقلمًا لرسم المستطيل حول النص، وكائن Font بنمط الخط المطلوب.

## الخطوة 3: تحديد النص والمستطيل

```csharp
string text = "Lorem ipsum..."; // (النص الذي تريده)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

حدد محتوى النص وأبعاد المستطيل الذي سيتم رسم النص فيه.

## الخطوة 4: ارسم المستطيل والنص

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

تتضمن هذه الخطوة رسم المستطيل باستخدام القلم المحدد ثم وضع النص داخل المستطيل باستخدام الخط والفرشاة المحددين.

## الخطوة 5: حفظ النتيجة

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

احفظ الصورة الناتجة في الدليل المطلوب. استبدل "دليل المستندات الخاص بك" بالمسار الذي تريد حفظ الصورة فيه.

لقد نجحت الآن في إنشاء صورة بنص ديناميكي باستخدام Aspose.Drawing لـ .NET! قم بتجربة الخطوط والألوان والأحجام المختلفة لتخصيص النص الخاص بك.

## خاتمة

في هذا البرنامج التعليمي، استكشفنا عملية رسم النص في Aspose.Drawing لـ .NET. من خلال الاستفادة من الميزات القوية للمكتبة، يمكنك بسهولة دمج النص الديناميكي في تطبيقات .NET الخاصة بك، مما يعزز الجاذبية البصرية وتجربة المستخدم.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام خطوط مخصصة مع Aspose.Drawing لـ .NET؟

A1: نعم، يمكنك تحديد الخطوط المخصصة عند إنشاء كائن الخط في التعليمات البرمجية الخاصة بك.

### س2: كيف يمكنني إضافة تأثيرات نصية مثل الخط الغامق أو المائل؟

 A2: ضبط خاصية FontStyle لكائن الخط. على سبيل المثال، استخدم`FontStyle.Bold` للنص الغامق.

### س3: هل Aspose.Drawing متوافق مع .NET Core؟

ج3: نعم، يدعم Aspose.Drawing .NET Core، مما يسمح لك باستخدامه في التطبيقات عبر الأنظمة الأساسية.

### س4: هل يمكنني رسم نص على صورة موجودة؟

 ج4: بالتأكيد! قم بتحميل الصورة الموجودة باستخدام`Bitmap.FromFile()`ثم تابع خطوات رسم النص.

### س5: هل يوجد منتدى مجتمعي لدعم Aspose.Drawing؟

 ج5: نعم، يمكنك العثور على الدعم ومناقشة القضايا على[Aspose.منتدى الرسم](https://forum.aspose.com/c/diagram/17).