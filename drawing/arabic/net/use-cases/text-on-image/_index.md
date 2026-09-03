---
date: 2026-09-03
description: تعلم كيفية إنشاء نص فوق الصور باستخدام Aspose.Drawing لـ .NET. يوضح هذا
  الدليل خطوة بخطوة كيفية إضافة نص إلى الصورة، ورسم النص على الصورة، وقياس حجم السلسلة
  بكفاءة.
keywords:
- create text overlay
- add text to image
- draw text on image
- measure string size
- calculate text dimensions
lastmod: 2026-09-03
linktitle: إضافة نص على الصور في Aspose.Drawing
og_description: تعلم كيفية إنشاء نص فوق الصور باستخدام Aspose.Drawing لـ .NET. يغطي
  هذا الدليل إضافة نص إلى الصورة، ورسم النص على الصورة، وقياس حجم السلسلة في بضع خطوات
  سهلة.
og_image_alt: Tutorial showing how to create text overlay on images using Aspose.Drawing
  in .NET
og_title: كيفية إنشاء نص فوق الصور باستخدام Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create text overlay on images using Aspose.Drawing for
    .NET. This step‑by‑step guide shows you how to add text to image, draw text on
    image, and measure string size efficiently.
  headline: How to create text overlay on images with Aspose.Drawing
  type: TechArticle
- description: Learn how to create text overlay on images using Aspose.Drawing for
    .NET. This step‑by‑step guide shows you how to add text to image, draw text on
    image, and measure string size efficiently.
  name: How to create text overlay on images with Aspose.Drawing
  steps:
  - name: import namespaces
    text: 'Begin by importing the necessary namespaces into your C# project:'
  - name: load the image
    text: Here, we load the image from the specified file path and initialize the
      graphics object for further processing.
  - name: set text properties
    text: Define the text properties such as color, font, and padding. Adjust these
      parameters according to your preferences.
  - name: measure text size
    text: Calculate the required size for the text by measuring each word individually.
      This ensures proper placement and avoids text overlap.
  - name: draw text on image
    text: Now, position the text on the image based on the calculated size and draw
      it using the specified font and color.
  - name: save the image
    text: Save the modified image to your desired directory. This step‑by‑step guide
      demonstrates a straightforward process of adding text to images using Aspose.Drawing
      for .NET. Experiment with different fonts, colors, and text content to achieve
      the desired visual effect.
  type: HowTo
- questions:
  - answer: Measure the string width with `Graphics.MeasureString`, subtract it from
      the image width, divide by two, and use that X coordinate when calling `DrawString`.
    question: How do I center text horizontally on the image?
  - answer: Yes—use `StringFormat` with `FormatFlags.LineLimit` and pass a string
      containing `\n` to `DrawString`.
    question: Can I add multi‑line text with line breaks?
  - answer: Absolutely. Set the brush color using `Color.FromArgb(alpha, r, g, b)`
      where `alpha` controls opacity.
    question: Does Aspose.Drawing support transparent text?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- image processing
- Aspose.Drawing
- .NET graphics
title: كيفية إنشاء نص فوق الصور باستخدام Aspose.Drawing
url: /ar/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء تغطية نصية على الصور باستخدام Aspose.Drawing

## مقدمة
Aspose.Drawing هو API لـ .NET يوفر إمكانيات معالجة صور متقدمة دون الاعتماد على System.Drawing.Common. في عالم .NET الديناميكي، إنشاء تغطية نصية على الصور هو حاجة متكررة — سواء كنت تضع علامة مائية على الصور، أو تضيف تسميات توضيحية، أو تولد رسومات مخصصة. يشرح هذا الدرس العملية الكاملة لإضافة نص إلى الصور باستخدام C# و Aspose.Drawing، بحيث يمكنك تنفيذ الحل في دقائق.

## إجابات سريعة
- **ما هي الفئة الأساسية للرسم؟** `Graphics` من Aspose.Drawing تتعامل مع جميع عمليات الرسم.  
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت مجاني يعمل للاختبار؛ ترخيص كامل مطلوب للإنتاج.  
- **ما هي صيغ الصور المدعومة؟** أكثر من 30 صيغة، بما في ذلك JPEG و PNG و BMP و GIF.  
- **هل يمكنني قياس حجم النص قبل الرسم؟** نعم—استخدم `Graphics.MeasureString` لحساب الأبعاد الدقيقة.  
- **هل الـ API متوافق مع .NET 6؟** بالتأكيد، Aspose.Drawing يستهدف .NET Framework 4.5+ و .NET 5/6+.

## ما هو إنشاء تغطية نصية؟
إنشاء تغطية نصية يشير إلى عملية رسم محتوى نصي فوق صورة bitmap موجودة، مما ينتج أصلًا بصريًا موحدًا يمكن حفظه أو عرضه. عمليًا، يصبح النص جزءًا من بيانات البكسل، مما يسمح باستخدام الصورة الناتجة في أي مكان تُقبل فيه الصور القياسية، مثل صفحات الويب، التقارير، أو المواد المطبوعة. يمكن أن تشمل التغطية تنسيقًا، تموضعًا، وشفافية لتحقيق التأثير البصري المطلوب.

## لماذا نستخدم Aspose.Drawing لهذه المهمة؟
Aspose.Drawing يدعم أكثر من 30 صيغة صورة ويمكنه معالجة ملفات أكبر من 500 MB دون تحميل الصورة بالكامل في الذاكرة، مما يوفر حتى 2× أسرع في العرض مقارنةً بـ System.Drawing على دفعات كبيرة. API الخاص به مُدار بالكامل، مما يلغي الاعتماد على التعليمات البرمجية الأصلية ويسهل النشر عبر Windows و Linux و macOS.

## المتطلبات المسبقة
قبل الغوص في الدرس، تأكد من توفر ما يلي:
1. **مكتبة Aspose.Drawing** – قم بتنزيلها وتثبيتها من [توثيق Aspose.Drawing لـ .NET](https://reference.aspose.com/drawing/net/).  
2. **بيئة التطوير** – Visual Studio 2022، Rider، أو أي IDE يدعم .NET 6+.  
3. **صورة عينة** – أي ملف JPEG/PNG ترغب في التعليق عليه.

الآن، دعنا نتبع التنفيذ خطوة بخطوة.

## كيفية إنشاء تغطية نصية على صورة؟
ستبدأ بتحميل bitmap المصدر في كائن `Graphics`، ثم تعريف الخط، الفرشاة، والمسافة الداخلية. بعد قياس أبعاد النص لتجنب القطع، تحدد المستطيل وتُرسم السلسلة. أخيرًا، تحفظ الصورة المعدلة على القرص. الوصف المختصر التالي يوضح التسلسل الكامل الذي ستتبعه في الخطوات التفصيلية أدناه.

### الخطوة 1: استيراد المساحات الاسمية
ابدأ باستيراد المساحات الاسمية اللازمة في مشروع C# الخاص بك:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

### الخطوة 2: تحميل الصورة
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
هنا، نقوم بتحميل الصورة من مسار الملف المحدد ونُهيئ كائن الرسومات للمعالجة اللاحقة.

### الخطوة 3: تعيين خصائص النص
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
عرّف خصائص النص مثل اللون، الخط، والمسافة الداخلية. اضبط هذه المعلمات وفقًا لتفضيلاتك.

### الخطوة 4: قياس حجم النص
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
احسب الحجم المطلوب للنص عن طريق قياس كل كلمة على حدة. يضمن ذلك التموقع السليم ويتجنب تداخل النصوص.

### الخطوة 5: رسم النص على الصورة
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
الآن، ضع النص على الصورة بناءً على الحجم المحسوب وارسمه باستخدام الخط واللون المحددين.

### الخطوة 6: حفظ الصورة
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
احفظ الصورة المعدلة في الدليل الذي ترغب به.

هذا الدليل خطوة بخطوة يوضح عملية بسيطة لإضافة نص إلى الصور باستخدام Aspose.Drawing لـ .NET. جرّب خطوطًا وألوانًا ومحتويات نصية مختلفة لتحقيق التأثير البصري المطلوب.

## المشكلات الشائعة والحلول
- **النص يظهر ضبابيًا** – تأكد من أن دقة الصورة (DPI) تتطابق مع حجم الخط؛ استخدم `Graphics.SmoothingMode = SmoothingMode.AntiAlias`.  
- **قص غير متوقع** – تحقق من أن عرض السلسلة المقاسة لا يتجاوز حدود الصورة؛ أضف حشوة أو قلل حجم الخط حسب الحاجة.  
- **الترخيص غير موجود** – ضع ملف الترخيص في دليل التنفيذ أو اضبطه برمجياً باستخدام `new License().SetLicense("Aspose.Drawing.lic")`.

## الأسئلة المتكررة
### هل Aspose.Drawing متوافق مع جميع صيغ الصور؟
Aspose.Drawing يدعم مجموعة واسعة من صيغ الصور، بما في ذلك الشائعة مثل JPEG و PNG و GIF. راجع [التوثيق](https://reference.aspose.com/drawing/net/) للحصول على القائمة الكاملة.

### هل يمكنني استخدام Aspose.Drawing للمشاريع التجارية؟
نعم، Aspose.Drawing مناسب لكل من المشاريع الشخصية والتجارية. للحصول على تفاصيل الترخيص، زر [صفحة الشراء](https://purchase.aspose.com/buy).

### هل تتوفر تراخيص مؤقتة لأغراض الاختبار؟
نعم، يمكنك الحصول على ترخيص مؤقت للاختبار بزيارة [Temporary License](https://purchase.aspose.com/temporary-license/).

### أين يمكنني العثور على دعم المجتمع لـ Aspose.Drawing؟
تفاعل مع المجتمع واحصل على الدعم عبر [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

### كيف أبدأ باستخدام Aspose.Drawing؟
ابدأ بتنزيل المكتبة من [صفحة تنزيل Aspose.Drawing](https://releases.aspose.com/drawing/net/) واستكشف [التوثيق](https://reference.aspose.com/drawing/net/) الشامل.

**أسئلة وإجابات إضافية**

**س: كيف أُوسّط النص أفقيًا على الصورة؟**  
ج: قِس عرض السلسلة باستخدام `Graphics.MeasureString`، اطرحها من عرض الصورة، اقسم الناتج على اثنين، واستخدم إحداثي X الناتج عند استدعاء `DrawString`.

**س: هل يمكنني إضافة نص متعدد الأسطر مع فواصل سطر؟**  
ج: نعم—استخدم `StringFormat` مع `FormatFlags.LineLimit` ومرّر سلسلة تحتوي على `\n` إلى `DrawString`.

**س: هل Aspose.Drawing يدعم النص الشفاف؟**  
ج: بالتأكيد. اضبط لون الفرشاة باستخدام `Color.FromArgb(alpha, r, g, b)` حيث يتحكم `alpha` في الشفافية.

## الخاتمة
Aspose.Drawing يبسط مهام معالجة الصور في .NET، مقدماً مجموعة أدوات قوية يمكنها **معالجة أكثر من 30 صيغة صورة** و **التعامل مع ملفات أكبر من 500 MB** دون تحميل كامل للذاكرة. إضافة تغطية نصية هي مجرد مثال واحد على مرونته، مما يتيح لك إنشاء علامات مائية، تسميات توضيحية، ورسومات مخصصة بكفاءة.

---

**آخر تحديث:** 2026-09-03  
**تم الاختبار مع:** Aspose.Drawing 24.12 for .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية رسم النصوص والخطوط باستخدام Aspose.Drawing لـ .NET](/drawing/net/text-and-fonts/)
- [كيفية رسم النص باستخدام Aspose.Drawing لـ .NET](/drawing/net/text-and-fonts/draw-text/)
- [كيفية رسم مستطيل – تحويل نظام الإحداثيات (تحويل الصفحة) باستخدام Aspose.Drawing API لـ .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}