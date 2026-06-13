---
date: 2026-06-13
description: تعلم كيفية حفظ bitmap كـ PNG ورسم خطوط متعددة في تطبيقات .NET باستخدام
  Aspose.Drawing. يغطي هذا الدليل خطوة بخطوة رسم الخطوط في .NET، وتقنيات رسم bitmap
  للخطوط، وأفضل الممارسات.
keywords:
- save bitmap as png
- draw multiple lines
- how to draw lines
linktitle: رسم خطوط متعددة باستخدام Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  headline: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG and draw multiple lines in .NET applications
    using Aspose.Drawing. This step‑by‑step guide covers .NET line drawing, draw line
    bitmap techniques, and best practices.
  name: How to save bitmap as PNG while drawing multiple lines with Aspose.Drawing
  steps:
  - name: Create a Bitmap (draw line bitmap)
    text: The `Bitmap` class represents an in‑memory raster image that you can draw
      onto. Start by creating a new bitmap with the desired width and height. This
      will be the canvas on which you draw your lines.
  - name: Get Graphics Object
    text: The `Graphics` object provides drawing methods such as lines, shapes, and
      text for a bitmap. Obtain a `Graphics` object from the created bitmap. This
      object provides methods for drawing on the bitmap.
  - name: Define a Pen
    text: A `Pen` defines the color, width, and style of lines drawn by the `Graphics`
      object. Create a `Pen` object that defines the attributes of the line you want
      to draw. In this case, we've chosen a blue color with a thickness of 2 pixels.
  - name: Draw Lines
    text: Use the `DrawLine` method to draw lines on the bitmap. The coordinates `(x1,
      y1)` to `(x2, y2)` represent the starting and ending points of each line. By
      calling the method twice, we effectively **draw multiple lines** that form a
      simple “V” shape.
  - name: Save the Image
    text: The `Bitmap.Save` method writes the in‑memory image to a file in the format
      you specify—PNG being the most common loss‑less option. Specify the directory
      where you want to save the output image. Make sure to replace `"Your Document
      Directory"` with the actual path.
  type: HowTo
- questions:
  - answer: Yes, simply modify the `Color` parameter when creating the `Pen` object.
    question: Can I change the color of the lines?
  - answer: Aspose.Drawing supports rectangles, ellipses, curves, polygons, and more.
      Check the official documentation for a complete list.
    question: What other shapes can I draw with Aspose.Drawing?
  - answer: Absolutely. It works in ASP.NET Core, MVC, and other web frameworks, allowing
      server‑side image generation without additional dependencies.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Wrap your drawing code in a `try‑catch` block and consult the Aspose.Drawing
      forum (https://forum.aspose.com/c/drawing/44) for community support.
    question: How should I handle errors while using Aspose.Drawing?
  - answer: Yes, you can use Aspose.Drawing for commercial projects. Visit the [purchase
      page](https://purchase.aspose.com/buy) for licensing details.
    question: Can I use Aspose.Drawing for a commercial project?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية حفظ bitmap كـ PNG أثناء رسم خطوط متعددة باستخدام Aspose.Drawing
url: /ar/net/lines-curves-and-shapes/draw-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ الصورة النقطية كـ PNG أثناء رسم خطوط متعددة باستخدام Aspose.Drawing

## مقدمة

في هذا الدرس ستتعلم **كيفية حفظ bitmap كـ PNG** ورسم خطوط متعددة باستخدام Aspose.Drawing لـ .NET. سواء كنت تنشئ مخططًا بسيطًا أو عنصر تحكم UI مخصصًا أو تولد رسومات على الخادم، فإن القدرة على عرض خطوط حادة ومضادة للتعرج ثم حفظها كملفات PNG هي مهارة أساسية. سنستعرض سير العمل بالكامل — من إعداد القماش إلى تصدير الصورة النهائية — حتى تتمكن من البدء في بناء مكونات بصرية على الفور.

## إجابات سريعة
- **ما الذي يمكنني رسمه؟** أي خط مستقيم أو خط متعدد أو شكل على bitmap.  
- **أي مكتبة؟** Aspose.Drawing لـ .NET (لا حاجة إلى System.Drawing.Common).  
- **كم عدد الخطوط؟** ارسم ما تشاء — يمكن تكرار استدعاء `Graphics.DrawLine` نفسه.  
- **المتطلبات المسبقة؟** بيئة تطوير .NET ومكتبة Aspose.Drawing.  
- **صيغة الإخراج؟** PNG، JPEG، BMP، أو أي صيغة يدعمها Aspose.Drawing.

## ما هو رسم خطوط متعددة؟

رسم خطوط متعددة يعني عرض قطعتين أو أكثر من الخطوط المستقيمة على نفس قماش الصورة. في Aspose.Drawing يمكنك تحقيق ذلك بإعادة استخدام كائن `Graphics` واحد واستدعاء `DrawLine` لكل زوج إحداثيات، مما يوفر عرضًا سريعًا وفعالًا للذاكرة لكل من المخرجات النقطية والمتجهة.

## لماذا تستخدم Aspose.Drawing لرسم الخطوط في .NET؟

توفر Aspose.Drawing واجهة برمجة تطبيقات حديثة وعبر المنصات تدعم **أكثر من 30 صيغة إخراج** ويمكنها معالجة صور تصل إلى **10,000 × 10,000 بكسل** دون تحميل الملف بالكامل إلى الذاكرة. تقدم مضادًا للتعرج مدمجًا، تحكمًا دقيقًا بالبكسل، وتوافقًا كاملًا مع .NET Core/5+، مما يلغي الاعتماديات القديمة لـ `System.Drawing.Common`.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

- مكتبة Aspose.Drawing: قم بتنزيل وتثبيت مكتبة Aspose.Drawing من [هنا](https://releases.aspose.com/drawing/net/).
- بيئة التطوير: تأكد من إعداد بيئة تطوير .NET على جهازك.
- دليل المستندات: أنشئ دليلًا على نظامك حيث تريد حفظ الصور الناتجة.

## استيراد مساحات الأسماء

في تطبيق .NET الخاص بك، تحتاج إلى استيراد مساحات الأسماء الضرورية للعمل مع Aspose.Drawing. أضف مساحات الأسماء التالية في بداية الكود:

```csharp
using System.Drawing;
```

الآن، دعنا نقسم المثال إلى خطوات متعددة لإرشادك خلال عملية رسم الخطوط باستخدام Aspose.Drawing.

## كيفية رسم خطوط متعددة في Aspose.Drawing

حمّل bitmap، احصل على كائن `Graphics`، اضبط `Pen`، استدعِ `DrawLine` لكل قطعة، وأخيرًا احفظ القماش كـ PNG — كل ذلك في خمس خطوات مختصرة يمكن تكرارها أو توسيعها لرسم أكثر تعقيدًا. كل خطوة موضحة بمقاطع شفرة توضح استدعاءات API المطلوبة وإعدادات اختيارية مثل مضاد التعرج.

### الخطوة 1: إنشاء Bitmap (رسم bitmap للخط)

فئة `Bitmap` تمثل صورة نقطية في الذاكرة يمكنك الرسم عليها.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, PixelFormat.Format32bppPArgb);
```

ابدأ بإنشاء bitmap جديد بالعرض والارتفاع المطلوبين. سيكون هذا القماش الذي ترسم عليه خطوطك.

### الخطوة 2: الحصول على كائن Graphics

كائن `Graphics` يوفر أساليب رسم مثل الخطوط والأشكال والنصوص لـ bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

احصل على كائن `Graphics` من الـ bitmap الذي أنشأته. هذا الكائن يوفر طرقًا للرسم على الـ bitmap.

### الخطوة 3: تعريف Pen

`Pen` يحدد اللون والعرض والنمط للخطوط التي يرسمها كائن `Graphics`.  
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

أنشئ كائن `Pen` يحدد خصائص الخط الذي تريد رسمه. في هذه الحالة اخترنا لونًا أزرق بسُمك 2 بكسل.

### الخطوة 4: رسم الخطوط

استخدم طريقة `DrawLine` لرسم الخطوط على الـ bitmap. الإحداثيات `(x1, y1)` إلى `(x2, y2)` تمثل نقطة البداية والنهاية لكل خط. باستدعاء الطريقة مرتين، نقوم فعليًا **برسم خطوط متعددة** تشكل شكل "V" بسيط.  
```csharp
graphics.DrawLine(pen, 10, 700, 500, 10);
graphics.DrawLine(pen, 500, 10, 990, 700);
```

### الخطوة 5: حفظ الصورة

طريقة `Bitmap.Save` تكتب الصورة الموجودة في الذاكرة إلى ملف بالصِيغة التي تحددها — PNG هو الخيار الأكثر شيوعًا غير الفاقد.  
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawLines_out.png");
```

حدد الدليل الذي تريد حفظ الصورة الناتجة فيه. تأكد من استبدال `"Your Document Directory"` بالمسار الفعلي.

## كيفية حفظ bitmap كـ PNG

حفظ bitmap كـ PNG هو عملية سطر واحد: استدعِ `bitmap.Save("output.png", ImageFormat.Png)` على كائن `Bitmap` الذي رسمت عليه بالفعل. تحدد فئة `ImageFormat` صيغة الملف لحفظ الصور، مثل PNG أو JPEG أو BMP. تتعامل Aspose.Drawing تلقائيًا مع الضغط وتحافظ على الشفافية، مما يجعل PNG مثاليًا لأصول الويب وواجهة المستخدم.

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثه | الحل |
|-------|----------------|-----|
| **الصورة تظهر فارغة** | كائن Graphics غير مرتبط بالـ bitmap أو تنسيق بكسل غير صحيح. | تأكد من استخدام `Graphics.FromImage(bitmap)` وإنشاء الـ bitmap بتنسيق بكسل مدعوم. |
| **الخطوط متعرجة** | تم تعطيل مضاد التعرج. | اضبط `graphics.SmoothingMode = SmoothingMode.AntiAlias;` قبل الرسم (يتطلب `using System.Drawing.Drawing2D;`). |
| **المسار غير موجود عند الحفظ** | سلسلة دليل غير صالحة. | استخدم `Path.Combine` لبناء المسار وتحقق من وجود المجلد. |

تتحكم تعداد `SmoothingMode` في جودة عرض الخطوط، حيث يوفر `AntiAlias` حوافًا أكثر سلاسة.

## الأسئلة المتكررة

**س: هل يمكنني تغيير لون الخطوط؟**  
ج: نعم، ما عليك سوى تعديل معامل `Color` عند إنشاء كائن `Pen`.

**س: ما الأشكال الأخرى التي يمكنني رسمها باستخدام Aspose.Drawing؟**  
ج: تدعم Aspose.Drawing المستطيلات، والدوائر، والمنحنيات، والمتعددات، والمزيد. راجع الوثائق الرسمية للحصول على القائمة الكاملة.

**س: هل Aspose.Drawing مناسبة لتطبيقات الويب؟**  
ج: بالتأكيد. تعمل في ASP.NET Core و MVC وأطر الويب الأخرى، مما يسمح بتوليد الصور من جانب الخادم دون اعتماديات إضافية.

**س: كيف يجب أن أتعامل مع الأخطاء أثناء استخدام Aspose.Drawing؟**  
ج: غلف شفرة الرسم بكتلة `try‑catch` واستشر منتدى Aspose.Drawing (https://forum.aspose.com/c/drawing/44) للحصول على دعم المجتمع.

**س: هل يمكنني استخدام Aspose.Drawing في مشروع تجاري؟**  
ج: نعم، يمكنك استخدام Aspose.Drawing في المشاريع التجارية. زر [صفحة الشراء](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

## الخلاصة

في هذا الدليل غطينا كل ما تحتاجه **لحفظ bitmap كـ PNG أثناء رسم خطوط متعددة** باستخدام Aspose.Drawing لـ .NET: إنشاء bitmap، الحصول على سياق رسومي، ضبط القلم، رسم الخطوط، وحفظ النتيجة. مع هذه الأساسيات يمكنك التوسع إلى مخططات ديناميكية، عناصر UI مخصصة، أو توليد رسومات من جانب الخادم — أي سيناريو يتطلب عرض خطوط عالية الجودة وقابلة للتوسع.

---

**آخر تحديث:** 2026-06-13  
**تم الاختبار مع:** Aspose.Drawing 24.12 لـ .NET  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [حفظ Bitmap كـ PNG ورسم منحنيات مغلقة باستخدام Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [حفظ Bitmap C# – رسم منحنيات بيزيه باستخدام Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [حفظ Bitmap كـ PNG باستخدام فرش صلبة في Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}