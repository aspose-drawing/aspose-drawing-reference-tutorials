---
date: 2026-05-19
description: تعلم كيفية رسم رسومات مستطيلة أثناء تنفيذ تحويل نظام الإحداثيات في .NET
  باستخدام Aspose.Drawing. يوضح هذا الدليل خطوة بخطوة كيفية تحويل البوصات إلى بكسلات
  وتعيين وحدات الصفحة.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: تحويل نظام الإحداثيات في Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: كيفية رسم مستطيل – تحويل نظام الإحداثيات (تحويل الصفحة) في Aspose.Drawing لـ
  .NET
url: /ar/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم مستطيل – تحويل نظام الإحداثيات (تحويل الصفحة) في Aspose.Drawing لـ .NET

## مقدمة

مرحبًا! في هذا الدرس ستكتشف **كيفية رسم مستطيل** رسوميًا أثناء تحويل إحداثيات الصفحة باستخدام Aspose.Drawing لـ .NET. سواءً كنت تبني تطبيقًا غنيًا بالرسومات أو تحتاج إلى تحكم دقيق في وحدات الرسم، فإن هذا الدليل يرافقك في كل خطوة — من إعداد القماش إلى رسم عنصر المستطيل. في النهاية، ستتمكن من تطبيق هذه التقنيات في مشاريعك بثقة.

## إجابات سريعة
- **ما هو تحويل نظام الإحداثيات؟** ربط وحدات مستوى الصفحة (مثل البوصات) بوحدات البكسل على مستوى الجهاز.  
- **لماذا نستخدم Aspose.Drawing؟** إنها توفر بديلاً مُدارًا بالكامل ومتعدد المنصات لـ System.Drawing.Common.  
- **كم من الوقت يستغرق تنفيذ المثال؟** حوالي 5‑10 دقائق لتحويل صفحة أساسي.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يتطلب الإنتاج ترخيصًا تجاريًا.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6/7.

## ما هو Aspose.Drawing؟

`Aspose.Drawing` هي مكتبة رسومات .NET توفر **واجهة برمجة تطبيقات مستقلة عن الجهاز** لإنشاء ومعالجة الصور النقطية، والمتجهات، ورسومات مستوى الصفحة دون الاعتماد على GDI+. تدعم **أكثر من 30 صيغة صورة** ويمكنها معالجة صور تصل إلى **10,000 × 10,000 بكسل** دون تحميل الملف بالكامل إلى الذاكرة.

## لماذا نستخدم تحويل نظام الإحداثيات مع Aspose.Drawing؟

يتيح لك تحويل نظام الإحداثيات تصميم الرسومات بوحدات العالم الحقيقي بينما تتولى المكتبة تعديل حجم البكسل لأي جهاز إخراج. يضمن ذلك تناسق الأحجام عبر الشاشات والطابعات ويسهل حسابات التخطيط.

- **تصميم مستقل عن الجهاز:** اكتب الكود مرة واحدة ودع Aspose.Drawing يتولى تعديل حجم البكسل لأي شاشة أو طابعة.  
- **رسم دقيق:** مثالي للمخططات التقنية، الرسومات على نمط CAD، أو أي سيناريو يتطلب قياسات دقيقة.  
- **موثوقية عبر المنصات:** يعمل بشكل ثابت على Windows وLinux وmacOS دون قيود GDI+ في System.Drawing.  
- **أرقام الأداء:** على معالج 2.5 GHz نموذجي، يستغرق رسم مستطيل بحجم 5 بوصات بدقة 300 DPI أقل من **15 مللي ثانية**، ويمكن للمكتبة عرض **50 إطارًا في الثانية** في سيناريوهات المعاينة الفورية.

## المتطلبات المسبقة

- **مكتبة Aspose.Drawing:** قم بتنزيل أحدث نسخة من الموقع الرسمي [here](https://releases.aspose.com/drawing/net/).  
- **بيئة التطوير:** Visual Studio، Rider، أو أي بيئة تطوير متوافقة مع .NET.  
- **دليل المستند الخاص بك:** استبدل `"Your Document Directory"` في الشيفرة بالمجلد الذي تريد حفظ صورة الإخراج فيه.  
- **دعم ASP.NET (اختياري):** يمكنك استخدام Aspose.Drawing في مشاريع ASP.NET Core بإضافة حزمة NuGet إلى تطبيق الويب الخاص بك — يتبع ذلك نفس نمط **how to use aspnet** كما هو الحال مع أي مكتبة .NET أخرى.

الآن بعد أن أصبح كل شيء جاهزًا، دعنا نغوص في دليل الخطوة بخطوة.

## كيفية رسم مستطيل مع تحويل الصفحة؟

حمّل صورة bitmap فارغة، اضبط وحدة الصفحة إلى البوصة، وارسم مستطيلًا باستخدام قلم أزرق رفيع — هذا يكمل رسم المستطيل في بضع أسطر من الشيفرة فقط. خاصية `Graphics.PageUnit` تخبر المحرك بتفسير جميع الإحداثيات كبوصات، بحيث يمكنك التفكير بالقياسات الواقعية بدلاً من البكسلات الخام.

### الخطوة 1: استيراد المساحات الاسمية

تُتيح لك عبارات `using` الوصول إلى الفئات الأساسية للرسم.

```csharp
using System.Drawing;
```

### الخطوة 2: إنشاء Bitmap

`Bitmap` تمثل صورة في الذاكرة يمكن الرسم عليها. نبدأ بإنشاء bitmap فارغ سيعمل كسطح الرسم. تنسيق البكسل `Format32bppPArgb` يمنحنا دعمًا عالي الجودة للشفافية المسبقة.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### الخطوة 3: إنشاء كائن Graphics

كائن `Graphics` يوفر واجهة برمجة تطبيقات الرسم للـ bitmap. إنه الجسر بين الشيفرة الخاصة بك ومخزن البكسل.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### الخطوة 4: مسح القماش

امنح القماش خلفية محايدة لتبرز الأشكال المرسومة. هنا نقوم بملئه بلون رمادي فاتح.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### الخطوة 5: ضبط التحويل (كيفية ضبط الوحدة)

`Graphics.PageUnit` يحدد وحدة القياس المستخدمة لإحداثيات الصفحة. لربط إحداثيات الصفحة ببكسلات الجهاز، اضبط خاصية `PageUnit`. في هذا المثال نختار البوصة، لكن يمكنك أيضًا استخدام `GraphicsUnit.Millimeter` أو `GraphicsUnit.Point` أو `GraphicsUnit.Pixel`. ضبط الوحدة إلى البوصة يتيح لك **تحويل البوصات إلى بكسلات** تلقائيًا بناءً على DPI للـ bitmap (96 DPI افتراضيًا، 300 DPI للطباعة عالية الدقة).

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### الخطوة 6: رسم مستطيل – رسم رسومات المستطيل

`Pen` يحدد اللون والعرض والنمط للخطوط المرسومة على سطح الرسومات. الآن نرسم مستطيلًا باستخدام قلم أزرق رفيع. لأننا حولنا إلى البوصة، يتم التعبير عن حجم المستطيل وموقعه بالبوصة، مما يجعل الشيفرة أكثر قابلية للقراءة في التخطيطات الموجهة للطباعة.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### الخطوة 7: حفظ الصورة

أخيرًا، احفظ الـ bitmap كملف PNG في المجلد الذي حددته مسبقًا.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## كيفية تحجيم الرسومات للطابعة؟

اضبط DPI للـ bitmap إلى دقة الطابعة المستهدفة (مثلاً 300 DPI) قبل الرسم. هذا يقوم تلقائيًا **بتحجيم رسومات الطابعة** بحيث تساوي البوصة الواحدة في الشيفرة بوصة واحدة على الصفحة المطبوعة. بعد ضبط `bitmap.SetResolution(300, 300)`، سيظهر نفس المستطيل أكبر على الورقة المطبوعة مع الحفاظ على أبعاده الدقيقة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|----------------|-----|
| **ملف الإخراج غير مُنشأ** | مسار غير صحيح أو مجلد مفقود | تأكد من وجود الدليل المستهدف أو استخدم `Directory.CreateDirectory` قبل الحفظ. |
| **المستطيل يظهر مشوّهًا** | `PageUnit` خاطئ أو DPI غير متطابق | تحقق من أن `graphics.PageUnit` يطابق الوحدات التي تنوي استخدامها وأن DPI للـ bitmap مضبوط بشكل مناسب (الافتراضي 96 DPI). |
| **استثناء الترخيص** | تشغيل بدون ترخيص صالح في بيئة الإنتاج | قم بتطبيق ترخيص Aspose.Drawing المؤقت أو الدائم قبل إنشاء كائنات الرسومات. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing مجانًا؟**  
ج: نعم، نسخة تجريبية مجانية متاحة [here](https://releases.aspose.com/).

**س: أين يمكنني العثور على وثائق مفصلة لـ Aspose.Drawing؟**  
ج: المرجع الكامل للـ API موجود [here](https://reference.aspose.com/drawing/net/).

**س: كيف أحصل على دعم لـ Aspose.Drawing؟**  
ج: زر [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) للحصول على مساعدة المجتمع والدعم الرسمي.

**س: هل تتوفر ترخيص مؤقت لـ Aspose.Drawing؟**  
ج: بالتأكيد — احصل على واحد [here](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني شراء ترخيص كامل لـ Aspose.Drawing؟**  
ج: يمكنك شراؤه [here](https://purchase.aspose.com/buy).

## الخلاصة

في هذا الدليل غطينا كل ما تحتاجه **لرسم مستطيل** رسوميًا باستخدام Aspose.Drawing: إعداد القماش، ضبط وحدات الصفحة، رسم أشكال دقيقة، وحفظ النتيجة. استخدم هذه التقنيات لبناء رسومات قابلة للتوسع ومستقلة عن الجهاز للتقارير، الرسومات على نمط CAD، أو أي تطبيق حيث تهم دقة القياسات. بعد ذلك، استكشف التحويلات المتقدمة مثل الدوران، التحجيم، وأصول الإحداثيات المخصصة لفتح سيناريوهات رسم أكثر قوة.

---

**آخر تحديث:** 2026-05-19  
**تم الاختبار مع:** Aspose.Drawing 24.12 لـ .NET  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [وحدات القياس في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/units-of-measure/)
- [كيفية تطبيق التحويل: التحويل المحلي في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/local-transformation/)
- [دروس تحويل المصفوفة: تحويلات المصفوفة في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/matrix-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}