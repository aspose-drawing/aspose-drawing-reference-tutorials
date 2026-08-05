---
date: 2026-05-24
description: تعلم كيفية تحجيم الصور باستخدام Aspose.Drawing لـ .NET. يوضح هذا الدليل
  خطوة بخطوة كيفية تغيير حجم bitmap بلغة C# باستخدام nearest neighbor interpolation
  وحفظ ملفات الصور المحجّمة.
keywords:
- how to scale images
- nearest neighbor scaling
- change image size
- high performance scaling
- resize bitmap c#
linktitle: تحجيم الصور في Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to scale images with Aspose.Drawing for .NET. This guide
    shows step‑by‑step how to resize bitmap C# using nearest neighbor interpolation
    and save scaled image files.
  headline: How to Scale Images with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to scale images with Aspose.Drawing for .NET. This guide
    shows step‑by‑step how to resize bitmap C# using nearest neighbor interpolation
    and save scaled image files.
  name: How to Scale Images with Aspose.Drawing for .NET
  steps:
  - name: 'Aspose.Drawing for .NET - Ensure that you have the Aspose.Drawing library
      installed in your project. You can download it [here](https://releases.aspose.com/drawing/net/).'
    text: 'Aspose.Drawing for .NET - Ensure that you have the Aspose.Drawing library
      installed in your project. You can download it [here](https://releases.aspose.com/drawing/net/).'
  - name: 'Development Environment - Set up a .NET development environment, such as
      Visual Studio.'
    text: 'Development Environment - Set up a .NET development environment, such as
      Visual Studio.'
  - name: 'Basic Understanding of C# - Familiarity with the C# programming language
      is essential for implementing the examples.'
    text: 'Basic Understanding of C# - Familiarity with the C# programming language
      is essential for implementing the examples.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing is fully compatible with ASP.NET, ASP.NET Core, WPF,
      WinForms, and console applications.
    question: Can I use Aspose.Drawing for .NET in both web and desktop applications?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for testing and evaluation purposes.
    question: Is a temporary license available for Aspose.Drawing?
  - answer: For any queries or assistance, visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).
    question: Where can I find additional support for Aspose.Drawing?
  - answer: Aspose.Drawing supports a wide range of formats, including JPEG, PNG,
      GIF, BMP, TIFF, WebP, and SVG. See the full list in the [documentation](https://reference.aspose.com/drawing/net/).
    question: Are there any limitations on the image formats supported by Aspose.Drawing?
  - answer: Yes, Aspose.Drawing provides `NearestNeighbor`, `Bilinear`, `Bicubic`,
      and `HighQualityBicubic` modes, allowing you to balance speed and quality.
    question: Can I apply custom interpolation modes for image scaling?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية تحجيم الصور باستخدام Aspose.Drawing لـ .NET
url: /ar/net/image-editing/scale/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحجيم الصور باستخدام Aspose.Drawing لـ .NET

## مقدمة

في هذا الدرس الشامل ستكتشف **كيفية تحجيم الصور** بكفاءة باستخدام Aspose.Drawing لـ .NET. سواءً كنت تبني خدمة ويب تُنشئ صورًا مصغرة أو أداة سطح مكتب تكبر أصول فن البكسل، فإن تحجيم الصور هو متطلب أساسي. سنستعرض كل خطوة — من إنشاء لوحة رسم إلى تطبيق الاستيفاء بأقرب جار وأخيرًا حفظ النتيجة — حتى تتمكن من تنفيذ تحجيم عالي الأداء في دقائق.

## إجابات سريعة
- **ما المكتبة التي يجب أن أستخدمها؟** Aspose.Drawing for .NET  
- **أي استيفاء يعطي النتيجة الأكثر حدة؟** NearestNeighbor interpolation  
- **هل يمكنني تغيير حجم الصورة في C#؟** نعم – استخدم الفئات `Bitmap` و `Graphics`  
- **كيف أحفظ صورة مُحجَّمة؟** استدعِ `bitmap.Save(...)` مع المسار المطلوب  
- **هل يلزم وجود ترخيص؟** A temporary license is available for evaluation  

## ما هو تحجيم الصور في Aspose.Drawing؟

تحجيم الصورة هو عملية تغيير حجم bitmap إلى أبعاد أكبر أو أصغر مع الحفاظ على الجودة البصرية. توفر Aspose.Drawing واجهة برمجة تطبيقات بسيطة تتيح لمطوري C# التحكم في كل خطوة — من إنشاء لوحة الرسم إلى رسم الصورة المصدر داخل مستطيل الهدف.

## لماذا نستخدم Aspose.Drawing للتحجيم؟

توفر Aspose.Drawing **تحجيمًا عالي الأداء** لأعباء العمل المتطلبة: تدعم **أكثر من 30 تنسيق صورة** (بما في ذلك PNG و JPEG و BMP و TIFF و WebP) ويمكنها معالجة ملفات تصل إلى **500 ميغابايت** دون تحميل الصورة بالكامل في الذاكرة. كما تقدم المكتبة **أربع أوضاع استيفاء**، حيث يوفر **NearestNeighbor** نتائج بكسلية مثالية للرموز وفن الألعاب. وبما أنها حزمة NuGet واحدة، لا توجد **اعتمادات أصلية خارجية**، مما يجعل النشر إلى حاويات Linux أو Azure Functions سلسًا.

## المتطلبات المسبقة

قبل أن نغوص في الدرس، تأكد من توفر المتطلبات التالية:

1. Aspose.Drawing for .NET: تأكد من تثبيت مكتبة Aspose.Drawing في مشروعك. يمكنك تنزيلها [هنا](https://releases.aspose.com/drawing/net/).  
2. بيئة التطوير: قم بإعداد بيئة تطوير .NET، مثل Visual Studio.  
3. فهم أساسي لـ C#: الإلمام بلغة البرمجة C# ضروري لتنفيذ الأمثلة.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، ابدأ باستيراد مساحات الأسماء اللازمة. هذه الخطوة حاسمة للوصول إلى وظائف Aspose.Drawing بسلاسة.

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Drawing2D;
```

## الخطوة 1: إنشاء Bitmap (لوحة رسم)

تمثل الفئة `Bitmap` صورة في الذاكرة يمكنك الرسم عليها أو تعديلها.  
ابدأ بإنشاء كائن `Bitmap` سيعمل كلوحة رسم لصورتك. حدد العرض والارتفاع وتنسيق البكسل وفقًا لمتطلباتك. هذا هو النهج الكلاسيكي *إعادة تحجيم bitmap في C#*.

```csharp
using System.Drawing;
```

## الخطوة 2: إنشاء كائن Graphics

توفر الفئة `Graphics` طرق رسم لعرض الأشكال والنصوص والصور على bitmap.  
بعد ذلك، أنشئ كائن `Graphics` من الـ `Bitmap` الذي تم إنشاؤه مسبقًا. هذا الكائن يزودك بقدرات الرسم اللازمة لتعديل الصور، بما في ذلك القدرة على **drawimage with rectangle** لاحقًا.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## الخطوة 3: تعيين وضع الاستيفاء

`InterpolationMode` يحدد كيفية حساب قيم البكسل عند تغيير حجم الصورة.  
لتحسين جودة الصورة المحجَّمة، قم بتعيين وضع الاستيفاء. في هذا المثال، نستخدم وضع **NearestNeighbor**، وهو مثالي عندما تحتاج إلى تكبير بنمط فن البكسل الواضح.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 4: تحميل الصورة

طريقة `Image.FromFile` تقوم بتحميل ملف صورة موجود إلى الذاكرة كـ `Bitmap`.  
حمّل الصورة التي تريد تحجيمها إلى كائن `Bitmap`. استبدل `"Your Document Directory" + @"Images\aspose_logo.png"` بالمسار إلى صورتك.

```csharp
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

## الخطوة 5: تحجيم الصورة

`Rectangle` يحدد منطقة الوجهة التي سيتم رسم الصورة المصدر فيها.  
عرّف مستطيلًا يمثل توسيع الصورة. في هذا المثال، تم تحجيم الصورة 5 ×  في العرض والارتفاع، مما يوضح تقنية **drawimage with rectangle**.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

## الخطوة 6: حفظ الصورة المحجَّمة

`Bitmap.Save` يحفظ الـ bitmap الموجود في الذاكرة إلى ملف بالصيغة المستنتجة من امتداد الملف.  
احفظ الصورة المحجَّمة إلى الموقع المطلوب. عدّل مسار الملف وفقًا لبنية مشروعك. تُظهر هذه الخطوة كيفية **save scaled image** في صيغ شائعة مثل PNG.

```csharp
Rectangle expansionRectangle = new Rectangle(0, 0, image.Width * 5, image.Height * 5);
graphics.DrawImage(image, expansionRectangle);
```

تهانينا! لقد تعلمت بنجاح **كيفية تحجيم الصور** باستخدام Aspose.Drawing لـ .NET.

## المشكلات الشائعة والحلول

- **تظهر الصورة غير واضحة بعد التحجيم** – تأكد من استخدام `InterpolationMode.NearestNeighbor` للحصول على نتائج بكسلية مثالية؛ يمكنك التحويل إلى `Bilinear` أو `HighQualityBicubic` لتحجيم أكثر سلاسة للصور الفوتوغرافية.  
- **استثناءات نفاد الذاكرة على ملفات كبيرة** – تقوم Aspose.Drawing بمعالجة الصور على شكل بلاطات؛ زد قيمة الخاصية `MemoryLimit` إذا كنت بحاجة للتعامل مع ملفات أكبر من 500 ميغابايت.  
- **نسبة الأبعاد غير صحيحة** – استخدم نفس عامل التحجيم للعرض والارتفاع، أو احسب المستطيل بناءً على نسبة الأبعاد الأصلية لتجنب التشويه.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing لـ .NET في كل من تطبيقات الويب وسطح المكتب؟**  
ج: نعم، Aspose.Drawing متوافق تمامًا مع ASP.NET و ASP.NET Core و WPF و WinForms وتطبيقات سطر الأوامر.

**س: هل تتوفر رخصة مؤقتة لـ Aspose.Drawing؟**  
ج: نعم، يمكنك الحصول على رخصة مؤقتة [هنا](https://purchase.aspose.com/temporary-license/) لأغراض الاختبار والتقييم.

**س: أين يمكنني العثور على دعم إضافي لـ Aspose.Drawing؟**  
ج: لأي استفسارات أو مساعدة، زر [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

**س: هل هناك أي قيود على صيغ الصور التي يدعمها Aspose.Drawing؟**  
ج: يدعم Aspose.Drawing مجموعة واسعة من الصيغ، بما في ذلك JPEG و PNG و GIF و BMP و TIFF و WebP و SVG. راجع القائمة الكاملة في [الوثائق](https://reference.aspose.com/drawing/net/).

**س: هل يمكنني تطبيق أوضاع استيفاء مخصصة لتحجيم الصور؟**  
ج: نعم، توفر Aspose.Drawing أوضاع `NearestNeighbor` و `Bilinear` و `Bicubic` و `HighQualityBicubic`، مما يتيح لك موازنة السرعة والجودة.

## الخاتمة

في هذا الدرس استكشفنا سير العمل من البداية إلى النهاية لـ **كيفية تحجيم الصور** باستخدام Aspose.Drawing. الآن تعرف كيف تنشئ لوحة bitmap، وتضبط كائن graphics، وتختار وضع الاستيفاء الأمثل، وتحمل صورة المصدر، وترسمها داخل مستطيل محجَّم، وأخيرًا تحفظ النتيجة. من خلال الاستفادة من **تحجيم عالي الأداء** و **دعم أكثر من 30 صيغة** في Aspose.Drawing، يمكنك بناء خطوط معالجة صور قوية تعمل بكفاءة على أي منصة .NET.

لا تتردد في تجربة أوضاع استيفاء مختلفة، أو معالجة مجموعة من الملفات دفعةً في حلقة، أو دمج التحجيم مع ميزات أخرى في Aspose.Drawing مثل إضافة العلامات المائية أو تحويل مساحة الألوان.

---

**Last Updated:** 2026-05-24  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Scale_out.png");
```

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
