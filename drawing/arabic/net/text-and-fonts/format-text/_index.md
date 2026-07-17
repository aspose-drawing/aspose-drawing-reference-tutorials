---
date: 2026-07-17
description: تعلم كيفية منع تجاوز النص عن طريق ضبط محاذاة النص في Aspose.Drawing for
  .NET وإضافة نص إلى الصور. دليل خطوة بخطوة مع أمثلة.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: ضبط محاذاة النص باستخدام Aspose.Drawing for .NET
og_description: منع تجاوز النص عن طريق ضبط محاذاة النص في Aspose.Drawing for .NET.
  تعلم كيفية رسم سلسلة نصية على الصورة، تمركز النص داخل المستطيل، واستبدال System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: منع تجاوز النص – ضبط محاذاة النص باستخدام Aspose.Drawing for .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: منع تجاوز النص – ضبط محاذاة النص باستخدام Aspose.Drawing for .NET
url: /ar/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# منع تجاوز النص – ضبط محاذاة النص باستخدام Aspose.Drawing

## مقدمة

عندما تحتاج إلى **منع تجاوز النص** أثناء إنشاء الرسومات في .NET، توفر لك Aspose.Drawing تحكمًا دقيقًا في موضع النص، ومحاذاته، وتغليفه. سواء كنت تبني مولد شارات، تقريرًا ديناميكيًا، أو أي مخرجات تعتمد على الصور، فإن إتقان محاذاة النص يضمن بقاء النص داخل المستطيل المقصود ويظهر بشكل مصقول. في هذا الدليل سنستعرض إنشاء لوحة bitmap، تكوين `StringFormat`، رسم مستطيل بنص مركزي، معالجة التجاوز، وأخيرًا حفظ الصورة.

## إجابات سريعة
- **ماذا يعني “ضبط محاذاة النص”؟** يحدد كيفية وضع النص أفقياً وعمودياً داخل مستطيل الرسم.  
- **أي فئة تتحكم في المحاذاة؟** `StringFormat` تتيح لك ضبط `Alignment` و `LineAlignment`.  
- **هل يمكنني رسم سلسلة ومستطيل معًا؟** نعم—استخدم `Graphics.DrawRectangle` ثم `Graphics.DrawString`.  
- **كيف أمنع تجاوز النص؟** عدل حجم المستطيل أو قسّم النص إلى عدة أسطر يدويًا.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يتطلب الاستخدام غير التجريبي ترخيص تجاري لـ Aspose.Drawing.

## ما هو **set text alignment** في Aspose.Drawing؟

`set text alignment` يضبط وضع النص الأفقي (`StringAlignment`) والعمودي (`LineAlignment`) داخل `Rectangle` أو منطقة الرسم. من خلال تعديل هذه الخصائص يمكنك التحكم فيما إذا كان النص يظهر محاذيًا لليسار، أو مركزيًا، أو محاذيًا لليمين، أو محاذيًا للأعلى، أو للوسط، أو للأسفل، مما يتيح تخطيطًا دقيقًا في الرسومات، والشارات، والتقارير التي تُنشئها Aspose.Drawing.

## لماذا تستخدم Aspose.Drawing لمحاذاة النص؟

تزيل Aspose.Drawing قيود GDI+ التي تعاني منها `System.Drawing.Common`. تدعم **5 إصدارات رئيسية من .NET** – .NET Framework 4.6+، .NET Core 2.0+، .NET 5، .NET 6، و .NET 7 – ويمكنها إنشاء صور تصل إلى **4000 × 4000 px** (≈ 100 MB) دون استنزاف الذاكرة. توفر مضاد التعرج، وتوسيع DPI عالي، وتوافق كامل مع حاويات Linux إمكانية توليد رسومات بكسل‑مثالية في أي سيناريو نشر.

## المتطلبات المسبقة

1. **Aspose.Drawing Library** – حمّلها [هنا](https://releases.aspose.com/drawing/net/).  
2. **بيئة التطوير** – Visual Studio 2022 (أو أي بيئة تطوير C#).  
3. **معرفة أساسية بـ .NET** – يجب أن تكون مرتاحًا مع مشاريع C# وحزم NuGet.

## استيراد المساحات الاسمية

لبدء العمل، استورد المساحات الاسمية المطلوبة. هذه تمنحك الوصول إلى الرسومات، وعرض النص، والرسوم الأولية.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## كيفية منع تجاوز النص باستخدام Aspose.Drawing؟

Bitmap هي فئة تمثل صورة مخزنة في الذاكرة، بينما `RectangleF` يحدد مساحة مستطيلة ذات نقاط عائمة للرسم. باستخدام `StringFormat` مع ضبط `Trimming` إلى `StringTrimming.EllipsisCharacter`، يتم استبدال الأحرف الزائدة تلقائيًا بنقطة ثلاثية، مما يضمن عدم تجاوز النص لحدود المستطيل. قياس السلسلة أولاً يتيح لك اتخاذ قرار إما بتصغير المستطيل أو تقسيم النص إلى أسطر متعددة، لضمان تخطيط نظيف دون تسرب.

حمّل bitmap الخاص بك، عرّف `RectangleF` بالحجم المناسب، واستخدم `StringFormat` مع ضبط `Trimming` إلى `StringTrimming.EllipsisCharacter` لقطع الأحرف الزائدة تلقائيًا. للتحكم الكامل، قسّ النص باستخدام `Graphics.MeasureString` وصغّر المستطيل أو قسّم النص إلى أسطر قبل الرسم. يضمن هذا النهج عدم خروج أي حرف خارج الحدود البصرية.

## الخطوة 1: إنشاء كائنات Bitmap و Graphics  

Bitmap تمثّل صورة في الذاكرة، بينما Graphics توفر طرق الرسم لتلك الصورة. إنشاء bitmap يوفّر لك لوحة يمكنك الرسم عليها. كائن `Graphics` هو سطح الرسم، ونفعّل فيه جودة نص عالية باستخدام `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## الخطوة 2: تعريف **StringFormat** وتنسيق الشكل  

StringFormat يحدد خيارات تخطيط النص مثل المحاذاة، وتباعد الأسطر، والقص. هنا نـ**ضبط محاذاة النص** عبر تكوين كائن `StringFormat`. كما نجهّز الفُرش، والأقلام، والخط الذي سيُستَخدم عند رسم السلسلة.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## الخطوة 3: إنشاء وتنسيق النص – **how to draw string** و **draw rectangle with text**

Graphics.DrawString يرسم النص على اللوحة، وGraphics.DrawRectangle يرسم شكل المستطيل. نقوم بتكوين النص، وتعريف المستطيل الذي سيحتويه، ثم نرسم كلًا من حدود المستطيل والسلسلة نفسها.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### كيفية التعامل مع تجاوز النص

إذا تجاوز `text` المقدم حدود المستطيل، لديك خياران شائعان:

1. **تغيير حجم المستطيل** – زيادة `rectangle.Width` أو `rectangle.Height`.  
2. **تقسيم النص** – قسّم السلسلة إلى أسطر تتناسب، ثم استدعِ `DrawString` لكل سطر مع تعديل إحداثيات Y.

## كيفية رسم النص على صورة باستخدام Aspose.Drawing؟

Graphics.DrawString يرسم النص المحدد باستخدام خط وخيارات تنسيق. أنشئ كائن `Graphics` من الـ bitmap الخاص بك، ثم استدعِ `DrawString` مع `StringFormat` المُعدّ. هذه الدعوة الواحدة تُظهر النص بالضبط في الموضع المطلوب، مع احترام المحاذاة، والقص، وأي مصفوفة تحويل تم تطبيقها. إضافة تلميح جودة عرض عالية يضمن بقاء المخرجات واضحة على شاشات DPI العالية.

## كيفية توسيط النص داخل المستطيل؟

StringAlignment يحدد المحاذاة الأفقية للنص داخل مستطيل التخطيط. اضبط `stringFormat.Alignment = StringAlignment.Center` و `stringFormat.LineAlignment = StringAlignment.Center`. هذا يوسّط النص أفقياً وعمودياً داخل المستطيل، مما يجعله مثاليًا للشارات، والأزرار، أو تراكب العلامات. التوسيط يعمل بشكل ثابت عبر أحجام الصور وإعدادات DPI المختلفة، موفرًا مظهرًا بصريًا متوازنًا.

## كيفية تحقيق محاذاة النص العمودية؟

LineAlignment يتحكم في وضع النص العمودي داخل المستطيل. استخدم `stringFormat.LineAlignment` مع القيم `StringAlignment.Near`، `Center`، أو `Far` لتحديد موضع النص في الأعلى، أو الوسط، أو الأسفل من المستطيل. يمكن دمج ذلك مع `Graphics.TranslateTransform` إذا احتجت إلى تدوير النص مع الحفاظ على المحاذاة العمودية. ضبط محاذاة السطر يضمن أن كتل النص متعددة الأسطر تتطابق تمامًا مع الموقع المتوقع، حتى بعد التحويلات.

## الخطوة 4: حفظ النتيجة – **add text to image**

أخيرًا، احفظ الـ bitmap إلى القرص. تُظهر هذه الخطوة **add text to image** في استدعاء واحد.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **النص يبدو غير واضح** | تأكد من ضبط `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`. |
| **النص مقطوع** | زد حجم المستطيل أو فعّل منطق التفاف الكلمات عبر قياس حجم السلسلة (`Graphics.MeasureString`). |
| **الخط غير موجود** | تحقق من تثبيت الخط على الجهاز المضيف أو دمج خط خاص باستخدام `PrivateFontCollection`. |
| **ألوان غير متوقعة** | راجع ألوان الفُرش والأقلام؛ تذكر أن `Color.FromKnownColor` يستخدم ألوان النظام المعرفة. |

## الأسئلة المتكررة

**س1: هل Aspose.Drawing متوافق مع جميع إصدارات .NET؟**  
ج1: نعم، تم تصميم Aspose.Drawing ليكون متوافقًا مع مجموعة واسعة من إصدارات .NET، مما يضمن مرونة للمطورين.

**س2: هل يمكنني تخصيص نمط الخط أكثر؟**  
ج2: بالتأكيد! عدّل معلمات كائن `Font` لتحقيق حجم الخط، والنمط، والعائلة المطلوبة.

**س3: كيف يمكنني معالجة تجاوز النص داخل المستطيل المحدد؟**  
ج3: يمكنك إدارة تجاوز النص إما بتعديل حجم المستطيل أو تنفيذ منطق مخصص للتعامل مع النص الطويل.

**س4: هل هناك خيارات تنسيق أخرى متاحة في Aspose.Drawing؟**  
ج4: نعم، توفر Aspose.Drawing مجموعة شاملة من الأدوات لمعالجة الرسومات، بما في ذلك خيارات تنسيق متعددة للنص، والأشكال، وأكثر.

**س5: أين يمكنني العثور على دعم إضافي لـ Aspose.Drawing؟**  
ج5: استكشف منتدى Aspose.Drawing [هنا](https://forum.aspose.com/c/drawing/44) للحصول على دعم المجتمع والنقاشات.

**أسئلة وإجابات إضافية**

**س: كيف أرسم سلسلة دون مستطيل محيط؟**  
ج: احذف استدعاء `DrawRectangle` ومرّر الموقع المطلوب كـ `PointF` إلى `Graphics.DrawString`.

**س: هل يمكنني تدوير النص مع الحفاظ على المحاذاة؟**  
ج: نعم—طبق تحويل `Matrix` على كائن `Graphics` قبل الرسم، ثم أعد ضبطه بعد ذلك.

**س: هل يمكن تصدير الصورة كـ JPEG بدلاً من PNG؟**  
ج: ببساطة غيّر امتداد الملف في `bitmap.Save` ويمكنك أيضًا تحديد `ImageFormat.Jpeg`.

---

**آخر تحديث:** 2026-07-17  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [كيفية رسم نص باستخدام Aspose.Drawing لـ .NET](/drawing/net/text-and-fonts/draw-text/)
- [إضافة نص على الصور في Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [كيفية رسم نص وخطوط باستخدام Aspose.Drawing لـ .NET](/drawing/net/text-and-fonts/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}