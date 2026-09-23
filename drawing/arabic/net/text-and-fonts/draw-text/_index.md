---
date: 2026-09-23
description: تعلم كيفية رسم النص على صورة باستخدام Aspose.Drawing for .NET. إنشاء
  صورة بالنص، إضافة النص إلى bitmap، وحفظ bitmap بصيغة PNG باستخدام خطوط مخصصة.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: كيفية رسم النص باستخدام Aspose.Drawing
og_description: تعلم كيفية رسم النص على صورة باستخدام Aspose.Drawing for .NET. يوضح
  هذا الدرس كيفية إنشاء صورة بالنص، إضافة النص إلى bitmap، وحفظ bitmap بصيغة PNG باستخدام
  خطوط مخصصة.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: رسم النص على صورة باستخدام Aspose.Drawing for .NET – دليل سريع
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: كيفية رسم النص على صورة باستخدام Aspose.Drawing for .NET
url: /ar/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم النص على صورة باستخدام Aspose.Drawing لـ .NET

## مقدمة

في هذا الدليل خطوة بخطوة ستتعلم **كيفية رسم النص على صورة** باستخدام Aspose.Drawing لـ .NET. سواء كنت بحاجة إلى إنشاء *صورة نصية ديناميكية*، أو إضافة نص إلى صورة bitmap موجودة، أو توليد رسم بياني بخطوط مخصصة، فإن هذا البرنامج التعليمي يشرح لك كل التفاصيل حتى تتمكن من بدء رسم النص خلال دقائق. تدعم المكتبة أكثر من 30 طريقة من GDI+، وتعمل على Windows وLinux وmacOS، وتحتوي على **صفر تبعيات خارجية**، مما يجعلها خيارًا موثوقًا لتوليد الصور على الخادم.

## إجابات سريعة
- **ما المكتبة المستخدمة؟** Aspose.Drawing لـ .NET  
- **المهمة الأساسية؟** رسم النص على صورة (إنشاء صورة بالنص)  
- **الطريقة الأساسية؟** `Graphics.DrawString` (رسم سلسلة نصية على الصورة)  
- **صيغة الإخراج؟** PNG (حفظ bitmap كـ PNG)  
- **المتطلبات المسبقة؟** بيئة تطوير .NET ومكتبة Aspose.Drawing  

## ما هو رسم النص باستخدام Aspose.Drawing؟

يعني رسم النص باستخدام Aspose.Drawing استخدام واجهة برمجة التطبيقات المتوافقة مع GDI+ في المكتبة لتصيير سلاسل Unicode على لوحة رستر. تقوم طريقة `Graphics.DrawString` بكتابة النص داخل bitmap، مما يتيح لك التحكم في الخط، اللون، المحاذاة، وإزالة التعرجات (anti‑aliasing). يتيح لك هذا النهج إنشاء صور عالية الجودة دون الحاجة لتثبيت System.Drawing.Common.

## لماذا تستخدم Aspose.Drawing لإضافة نص إلى الصور؟

توفر Aspose.Drawing طريقة موثوقة وعبر‑المنصات لتصيير النص على الصور دون الحاجة إلى مكتبات GDI+ الأصلية، مما يضمن جودة وأداء ثابتين على أي نظام تشغيل. تدعم مضاد التعرجات المتقدم، الأحرف Unicode، والخطوط المخصصة، وتندمج بسلاسة مع تطبيقات .NET، مما يجعلها مثالية لتوليد الصور على الخادم وأدوات سطح المكتب على حد سواء.

- **موثوقية عبر المنصات** – تعمل على Windows وLinux وmacOS.  
- **تصيير متقدم** – مضاد التعرجات وتنعيم النص على مستوى البكسل الفرعي لإخراج واضح.  
- **بدون تبعيات خارجية** – تضم المكتبة كل ما تحتاجه *لإنشاء صورة بالنص*.

## المتطلبات المسبقة

قبل البدء، تأكد من أنك تمتلك:

- **Aspose.Drawing لـ .NET** – قم بتنزيله من [توثيق Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **بيئة تطوير .NET** مثل Visual Studio أو VS Code.  

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء المطلوبة:

توفر هذه المساحات الأنواع الأساسية لـ GDI+ مثل `Bitmap` و`Graphics` وأدوات تصيير النص.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## الخطوة 1: إنشاء كائنات bitmap و graphics

`Bitmap` هو حاوية الصورة النقطية raster في Aspose.Drawing لبيانات البكسل، و`Graphics` يوفر طرق الرسم لتصيير الأشكال والنص عليها.

`Bitmap` يمثل صورة في الذاكرة، بينما `Graphics` يوفر طرق الرسم لتصييرها على ذلك bitmap.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

هنا نقوم بإنشاء `Bitmap` سيحمل الصورة النهائية و`Graphics` يتيح لنا الرسم عليها. تلميح مضاد التعرجات يضمن أن النص يبدو ناعمًا.

## الخطوة 2: إعداد الفرشاة والقلم والخط

`Brush` يحدد لون التعبئة، `Pen` يرسم حدود الأشكال، و`Font` يحدد نوع الخط، الحجم، والنمط لتصيير النص.

`Brush` يملأ الأشكال باللون، `Pen` يرسم حدود الأشكال، و`Font` يحدد نوع الخط والحجم لتصيير النص.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** يحدد لون النص.  
- **Pen** يُستخدم لاحقًا لرسم مستطيل حول النص (اختياري).  
- **Font** يحدد نوع الخط، الحجم، والنمط لعملية *رسم سلسلة نصية على الصورة*.

## الخطوة 3: تعريف النص والمستطيل

`Rectangle` يحدد صندوق الحدود حيث سيتم وضع النص، مع تحديد إحداثيات X/Y والعرض/الارتفاع.

`Rectangle` يحدد موقع وحجم المنطقة المستطيلة، يُستخدم هنا لتحديد حدود النص المرسوم.

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

يحدد `Rectangle` مكان وضع النص. عدل الإحداثيات والحجم لتتناسب مع تخطيطك.

## الخطوة 4: رسم المستطيل والنص

`Graphics.DrawString` يصدر النص المحدد داخل المستطيل المعطى باستخدام الخط والفرشاة المحددين.

`Graphics.DrawString` يصدر سلسلة نصية داخل مستطيل محدد باستخدام الخط والفرشاة المحددين.

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

أولاً نرسم حدود المنطقة بمستطيل أزرق، ثم **نضيف النص إلى bitmap** عن طريق استدعاء `DrawString`. هذا هو جوهر *رسم النص* على الصورة.

## الخطوة 5: حفظ النتيجة

يتم حفظ الصورة كملف PNG، مما يلبي متطلب *حفظ bitmap كـ PNG*. استبدل مسار العنصر النائب بالمجلد الفعلي الذي تريد تخزين الملف فيه.

`bitmap.Save` يكتب الصورة إلى ملف بالتنسيق المختار، مثل PNG.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## حالات الاستخدام الشائعة

- **إنشاء شهادات** بأسماء مخصصة.  
- **إنشاء صور مصغرة مائية** لمعارض الويب.  
- **بناء مخططات ديناميكية** تشمل تسميات أو تعليقات توضيحية.  

## استكشاف الأخطاء وإصلاحها والنصائح

- **الخط غير موجود؟** تأكد من تثبيت الخط على الجهاز المضيف أو استخدم مجموعة خطوط خاصة.  
- **النص مقطوع؟** زد حجم المستطيل أو قلل حجم الخط.  
- **مخاوف الأداء؟** أعد استخدام نفس كائن `Graphics` لعمليات رسم متعددة عندما يكون ذلك ممكنًا.  

## الأسئلة المتكررة

**س: كيف أغير صيغة الإخراج إلى JPEG؟**  
ج: استبدل امتداد `.png` بـ `.jpg` في طريقة `Save` ويمكنك اختيارياً تحديد `ImageCodecInfo` لجودة JPEG.

**س: هل يمكنني رسم نص متعدد الأسطر؟**  
ج: نعم، أدرج أحرف فاصل السطر (`\n`) في السلسلة أو استخدم `StringFormat` مع `FormatFlags.LineLimit`.

**س: هل هناك طريقة لقياس حجم النص قبل الرسم؟**  
ج: استخدم `Graphics.MeasureString` للحصول على الأبعاد الدقيقة للنص المرسوم.

**س: هل تدعم Aspose.Drawing الأحرف Unicode؟**  
ج: بالتأكيد. قدم خطًا يحتوي على الرموز المطلوبة وستقوم المكتبة بتصييره بشكل صحيح.

**س: ما نسخة Aspose.Drawing التي تم استخدامها للاختبار؟**  
ج: تم اختبار الأمثلة باستخدام Aspose.Drawing 24.11 لـ .NET.

---

**آخر تحديث:** 2026-09-23  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [إنشاء رسومات Bitmap C# – حفظ صورة PNG والعمل مع الخطوط المثبتة في Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [كيفية حفظ bitmap كـ PNG باستخدام Aspose.Drawing API لـ .NET](/drawing/net/image-editing/display/)
- [نص على صورة](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}