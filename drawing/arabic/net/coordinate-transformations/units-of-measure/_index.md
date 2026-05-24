---
date: 2026-05-24
description: تعلم كيفية تعيين الوحدة في Aspose.Drawing لـ .NET، تحويل وحدات الرسومات
  بسهولة، وإتقان القياسات الدقيقة لتصيير الرسومات.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: وحدات القياس في Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية تعيين الوحدة في Aspose.Drawing لـ .NET – وحدات القياس
url: /ar/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعيين الوحدة في Aspose.Drawing لـ .NET – وحدات القياس

## مقدمة

مرحبًا بك في عالم Aspose.Drawing لـ .NET، حيث يلتقي الدقة والمرونة في معالجة الرسومات. في هذا الدرس ستكتشف **كيفية تعيين الوحدة** لرسوماتك، وتتعلم **تحويل وحدات الرسومات** بين النقاط، المليمترات، والبوصات، وتطلع على أمثلة واقعية تجعل صورك مثالية على مستوى البكسل. سواءً كنت تبني تقارير، صورًا مصغرة، أو مخططات مخصصة، فإن إتقان وحدات القياس أمر أساسي لضمان عرض متسق عبر الأجهزة.

## إجابات سريعة
- **ما هي الطريقة الأساسية لتغيير الوحدات؟** استدعِ `graphics.PageUnit = PageUnit.Point` (أو `.Millimeter`، `.Inch`) على كائن `Graphics`.  
- **أي وحدة تساوي 1/72 بوصة؟** النقاط.  
- **كم عدد المليمترات في البوصة؟** 25.4 mm = 1 inch.  
- **هل أحتاج إلى مكتبات إضافية لاستخدام الوحدات؟** لا، مكتبة Aspose.Drawing الأساسية توفر جميع ثوابت الوحدات.  
- **هل يمكنني خلط الوحدات في صورة واحدة؟** عيّن الوحدة مرة واحدة لكل مثيل `Graphics`؛ وارسم كل شيء باستخدام تلك الوحدة لضمان الاتساق.

## المتطلبات المسبقة

قبل أن نغوص في الدرس، تأكد من توفر المتطلبات المسبقة التالية:

- Aspose.Drawing لـ .NET: تأكد من تثبيت المكتبة. يمكنك تنزيلها [هنا](https://releases.aspose.com/drawing/net/).
- دليل المستندات: احرص على وجود دليل مخصص حيث تريد حفظ المستندات التي تم إنشاؤها.
- معرفة أساسية بـ C#: يُنصح بفهم أساسي للغة C# لتحقيق أقصى استفادة من هذا الدليل.

## استيراد مساحات الأسماء

قبل أن نبدأ، لنستورد مساحات الأسماء الضرورية لاستخدام Aspose.Drawing بفعالية:

```csharp
using System.Drawing;
```

الآن، لنقسم كل مثال إلى خطوات متعددة:

## كيفية تعيين الوحدة إلى النقاط؟

تمثل فئة `Bitmap` صورة في الذاكرة تُستخدم كقماش للرسم. قم بتحميل الـ bitmap الخاص بك، أنشئ كائن `Graphics`، واضبط وحدة الصفحة إلى النقاط — هذا يخبر Aspose.Drawing بتفسير جميع الإحداثيات كقيم 1/72 بوصة. استخدام النقاط يمنحك تحكمًا دقيقًا للرسومات الجاهزة للطباعة ويسمح لك بتحديد عرض الخطوط بدقة عالية.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### الخطوة 1: إنشاء Bitmap  
تمثل فئة `Bitmap` صورة في الذاكرة تُستخدم كقماش للرسم.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### الخطوة 2: إنشاء كائن Graphics  
`Graphics` توفر طرق رسم لتصوير الأشكال والنصوص على `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### الخطوة 3: ضبط وحدة الصفحة إلى النقاط  
`PageUnit` هي تعداد يحدد وحدة القياس لإحداثيات الصفحة. `PageUnit.Point` يعرّف النقاط كوحدة قياس (1 نقطة = 1/72 بوصة). هذا الإعداد ينطبق على جميع استدعاءات الرسم اللاحقة.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### الخطوة 4: رسم مستطيل بالنقاط  
عند رسم مستطيل بعد ضبط الوحدة، تُفسَّر الأبعاد التي تحددها كنقاط، مما يضمن حجمًا دقيقًا.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## كيفية تعيين الوحدة إلى المليمترات؟

`PageUnit` هي تعداد يحدد وحدة القياس لإحداثيات الصفحة. التحويل إلى المليمترات مفيد عندما تحتاج إلى أبعاد مترية، على سبيل المثال عند إنشاء مخططات هندسية. تتعامل Aspose.Drawing مع 1 مم كـ 1/25.4 بوصة، مما يتيح لك محاذاة الرسومات مع القياسات الفعلية المستخدمة في التصنيع والوثائق التقنية.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### الخطوة 1: ضبط وحدة الصفحة إلى المليمترات  
عيّن `PageUnit.Millimeter` لكائن `Graphics`؛ جميع الإحداثيات الآن تتطابق مع النظام المتري.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### الخطوة 2: رسم مستطيل بالمليمترات  
عرض وارتفاع المستطيل الآن يُعبَّران بالمليمترات، مما يسهل محاذاته مع القياسات الفعلية ويضمن أن المخرجات المطبوعة تتطابق مع الأحجام الواقعية.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## كيفية تعيين الوحدة إلى البوصات؟

`Graphics` توفر طرق رسم لتصوير الأشكال والنصوص على `Bitmap`. البوصة هي الوحدة الافتراضية للعديد من أدوات التصميم الأمريكية. ضبط الوحدة إلى البوصة يتيح لك التفكير بمصطلحات مألوفة عند ترتيب عناصر واجهة المستخدم، ويسهل الانتقال من تصميم الشاشة إلى الطباعة حيث تُستخدم البوصة بشكل شائع.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### الخطوة 1: ضبط وحدة الصفحة إلى البوصات  
`PageUnit.Inch` يغيّر نظام الإحداثيات بحيث تكون الوحدة الواحدة مساوية لـ 1 بوصة، مما يوفر طريقة بسيطة لتحديد حجم العناصر لتصاميم موجهة للطباعة.

CODE_BLOCK_PLACEHOLDER_10_END

### الخطوة 2: رسم مستطيل بالبوصات  
الآن أي شكل ترسمه يستخدم البوصة كأساس للقياس، وهو مثالي لتصاميم الطباعة وللتواصل حول الأبعاد مع أصحاب المصلحة الذين يعتادون على الوحدات الإمبراطورية.

CODE_BLOCK_PLACEHOLDER_11_END

## حفظ النتيجة

بعد إكمال الأمثلة، احفظ الصورة الناتجة في دليل المستندات الخاص بك. طريقة `Bitmap.Save` تكتب الملف بالتنسيق الذي تحدده (PNG، JPEG، إلخ).

CODE_BLOCK_PLACEHOLDER_12_END

الآن، لقد نجحت في التعامل مع وحدات القياس المتنوعة في Aspose.Drawing لـ .NET، وإنشاء تمثيل بصري للمستطيلات باستخدام النقاط، المليمترات، والبوصات.

## لماذا تستخدم نظام الوحدات في Aspose.Drawing؟

يدعم Aspose.Drawing **أكثر من 30 تنسيق صورة** ويمكنه معالجة الصور حتى **5000 × 5000 بكسل** دون تحميل الملف بالكامل إلى الذاكرة، مما يوفر أداءً عاليًا لتوليد الرسومات على نطاق واسع. من خلال ضبط الوحدة صراحةً، تلغي التخمين، تقلل أخطاء التحويل، وتضمن أن مخرجاتك تتطابق مع الأبعاد الفيزيائية الدقيقة عبر جميع المنصات.

## المشكلات الشائعة والحلول

- **حجم غير متوقع بعد الحفظ** – تأكد من ضبط `graphics.PageUnit` **قبل** أي استدعاءات رسم؛ تغيير الوحدة لاحقًا لا يعيد تعديل الأحجام الحالية للأشكال.  
- **مخرجات غير واضحة على شاشات عالية الدقة DPI** – زد من دقة الـ bitmap (مثال: `new Bitmap(width, height, 300)`) لتتناسب مع DPI المستهدف.  
- **وحدات مختلطة في صورة واحدة** – أنشئ مثيلات `Graphics` منفصلة لكل وحدة أو قم بالتحويل اليدوي قبل الرسم.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.Drawing لـ .NET مع أطر .NET أخرى؟
A1: نعم، Aspose.Drawing متوافق مع أطر .NET المختلفة، مما يوفر مرونة في بيئة التطوير الخاصة بك.

### س2: هل هناك نسخة تجريبية مجانية متاحة؟
A2: نعم، يمكنك تجربة Aspose.Drawing من خلال نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س3: كيف أحصل على الدعم لـ Aspose.Drawing لـ .NET؟
A3: زر [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على دعم المجتمع والنقاشات.

### س4: هل يمكنني شراء ترخيص مؤقت للمشاريع قصيرة الأجل؟
A4: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على وثائق مفصلة لـ Aspose.Drawing؟
A5: الوثائق الشاملة متاحة [هنا](https://reference.aspose.com/drawing/net/).

---

**آخر تحديث:** 2026-05-24  
**تم الاختبار باستخدام:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [تحويل نظام الإحداثيات – تحويل الصفحة في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [درس تحويل المصفوفة: تحويلات المصفوفة في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [كيفية تطبيق التحويل: التحويل المحلي في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}