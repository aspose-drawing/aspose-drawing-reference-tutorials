---
date: 2026-02-07
description: تعلم كيفية تكبير الصور باستخدام Aspose.Drawing لـ .NET. يوضح هذا الدليل
  خطوة بخطوة كيفية تغيير حجم صورة bitmap بلغة C# باستخدام استيفاء أقرب جار وحفظ ملفات
  الصور المكبرة.
linktitle: Scaling Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية تحجيم الصور باستخدام Aspose.Drawing لـ .NET
url: /ar/net/image-editing/scale/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تحجيم الصور باستخدام Aspose.Drawing لـ .NET

## المقدمة

مرحبًا بكم في هذا الدليل الشامل حول **كيفية تحجيم الصور** باستخدام Aspose.Drawing لـ .NET! في عالم تطوير البرمجيات الديناميكي، يُعد تعديل وتحجيم الصور مطلبًا شائعًا. تُبسّط Aspose.Drawing هذه العملية، حيث تُقدّم أدوات ووظائف قوية للعمل مع الصور في تطبيقات .NET الخاصة بك.

## إجابات سريعة
- **ما المكتبة التي يجب أن أستخدمها؟** Aspose.Drawing لـ .NET  
- **أي طريقة استيفاء تعطي النتيجة الأكثر حدة؟** استيفاء NearestNeighbor  
- **هل يمكنني تغيير حجم الصورة في C#؟** نعم – استخدم فئتي Bitmap و Graphics  
- **كيف أحفظ صورةً محوّلة؟** استدعِ `bitmap.Save(...)` مع المسار المطلوب  
- **هل تحتاج إلى ترخيص؟** ترخيص مؤقت متاح للتقييم  

## ما هو تحجيم الصورة في Aspose.Drawing؟
تحجيم الصورة هو عملية تغيير أبعاد الـ bitmap لتصبح أكبر أو أصغر مع الحفاظ على الجودة البصرية. تُوفر Aspose.Drawing واجهة برمجة تطبيقات بسيطة لتغيير حجم الصورة؛ يمكن لمطوري C# التحكم في كل خطوة — من إنشاء القماش إلى رسم الصورة داخل مستطيل.

## لماذا نستخدم Aspose.Drawing للتحجيم؟
- **عَرْضُ رسومي عالي الأداء** – مُحسّن للصور الكبيرة.  
- **خيارات استيفاء غنية** – بما في ذلك أقرب جار (nearest neighbor) لتحجيم بكسل‑دقيق.  
- **دعم كامل لـ .NET** – يعمل مع .NET Framework و .NET Core و .NET 5/6+.  
- **بدون تبعيات خارجية** – حزمة NuGet واحدة تحل محل System.Drawing.Common.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

1. Aspose.Drawing لـ .NET: تأكد من تثبيت مكتبة Aspose.Drawing في مشروعك. يمكنك تنزيلها [هنا](https://releases.aspose.com/drawing/net/).  
2. بيئة تطوير: إعداد بيئة تطوير .NET، مثل Visual Studio.  
3. فهم أساسي لـ C#: الإلمام بلغة البرمجة C# ضروري لتطبيق الأمثلة.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية. هذه الخطوة أساسية للوصول إلى وظائف Aspose.Drawing بسلاسة.

```csharp
using System.Drawing;
```

## الخطوة 1: إنشاء Bitmap (قماش)

ابدأ بإنشاء كائن `Bitmap` سيعمل كقماش لصورتك. حدد العرض والارتفاع وتنسيق البكسل وفقًا لمتطلباتك. هذا هو النهج الكلاسيكي *resize bitmap C#*.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## الخطوة 2: إنشاء كائن Graphics

بعد ذلك، أنشئ كائن `Graphics` من الـ `Bitmap` الذي أنشأته مسبقًا. يوفر هذا الكائن إمكانات الرسم اللازمة لتعديل الصورة، بما في ذلك القدرة على **drawimage with rectangle** لاحقًا.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 3: ضبط وضع الاستيفاء

لتحسين جودة الصورة المحوّلة، اضبط وضع الاستيفاء. في هذا المثال، نستخدم وضع **NearestNeighbor interpolation**، وهو مثالي عندما تحتاج إلى تكبير بنمط بكسل‑آرت واضح.

```csharp
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

## الخطوة 4: تحميل الصورة

حمّل الصورة التي تريد تحجيمها في كائن `Bitmap`. استبدل `"Your Document Directory" + @"Images\aspose_logo.png"` بالمسار إلى صورتك.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

## الخطوة 5: تحجيم الصورة

عرّف مستطيلًا يمثل توسيع الصورة. في هذا المثال، تُحجم الصورة 5 مرات في العرض والارتفاع. يوضح ذلك تقنية **drawimage with rectangle**.

```csharp
Rectangle expansionRectangle = new Rectangle(0, 0, image.Width * 5, image.Height * 5);
graphics.DrawImage(image, expansionRectangle);
```

## الخطوة 6: حفظ الصورة المحوّلة

احفظ الصورة المحوّلة إلى الموقع المطلوب. عدّل مسار الملف وفقًا لبنية مشروعك. تُظهر هذه الخطوة كيفية **save scaled image** بصيغ شائعة مثل PNG.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Scale_out.png");
```

تهانينا! لقد تعلمت بنجاح **كيفية تحجيم الصور** باستخدام Aspose.Drawing لـ .NET.

## الخاتمة

في هذا الدرس، استكشفنا عملية تحجيم الصور باستخدام Aspose.Drawing. تُتيح هذه المكتبة للمطورين التعامل بفعالية مع مهام تعديل الصور داخل تطبيقات .NET الخاصة بهم. باتباع الدليل خطوة بخطوة، اكتسبت رؤى قيّمة حول تنفيذ تحجيم الصور، بما في ذلك تغيير حجم الصورة C#، إعادة تحجيم bitmap C#، استخدام استيفاء nearest neighbor، رسم الصورة داخل مستطيل، وحفظ الصورة المحوّلة.

لا تتردد في تجربة المزيد واستكشاف الميزات الأخرى التي تُوفرها Aspose.Drawing لتعزيز قدرات معالجة الصور لديك.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.Drawing لـ .NET في كل من تطبيقات الويب وسطح المكتب؟

ج1: نعم، Aspose.Drawing مرنة ويمكن استخدامها في مختلف تطبيقات .NET، بما في ذلك الويب وسطح المكتب.

### س2: هل يتوفر ترخيص مؤقت لـ Aspose.Drawing؟

ج2: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/) للاختبار والتقييم.

### س3: أين يمكنني العثور على دعم إضافي لـ Aspose.Drawing؟

ج3: لأي استفسارات أو مساعدة، زر منتدى [Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

### س4: هل هناك أي قيود على صيغ الصور التي يدعمها Aspose.Drawing؟

ج4: يدعم Aspose.Drawing مجموعة واسعة من صيغ الصور، بما في ذلك JPEG و PNG و GIF و BMP وغيرها. راجع [الوثائق](https://reference.aspose.com/drawing/net/) للحصول على القائمة التفصيلية.

### س5: هل يمكنني تطبيق أوضاع استيفاء مخصصة لتحجيم الصور؟

ج5: نعم، توفر Aspose.Drawing مرونة تسمح لك باختيار أوضاع استيفاء مختلفة لتحجيم الصور.

## أسئلة شائعة

**س: كيف يختلف استيفاء أقرب جار عن الاستيفاء الثنائي الخطية؟**  
ج: أقرب جار ينسخ قيمة البكسل الأقرب، محافظًا على الحواف الصلبة، بينما الاستيفاء الثنائي الخطية يحسب متوسطًا مرجّحًا للحصول على نتائج أكثر سلاسة.

**س: هل يمكنني تحجيم الصور دون الحفاظ على نسبة الأبعاد؟**  
ج: نعم—عن طريق تحديد قيم عرض وارتفاع مختلفة في المستطيل، يمكنك تمديد أو ضغط الصورة حسب الحاجة.

**س: هل يمكن تحجيم عدة صور داخل حلقة؟**  
ج: بالتأكيد. ضع منطق إنشاء الـ bitmap والرسم والحفظ داخل حلقة `foreach` تت iterates على ملفات المصدر الخاصة بك.

---

**آخر تحديث:** 2026-02-07  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}