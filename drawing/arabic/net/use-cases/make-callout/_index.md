---
date: 2026-08-01
description: تعلم كيفية إضافة التعليقات التوضيحية إلى الصور باستخدام Aspose.Drawing
  for .NET – دليل خطوة بخطوة مع نماذج الشيفرة، نصائح، وأسئلة شائعة.
keywords:
- how to add callouts
- Aspose.Drawing callout tutorial
- .NET image annotation
lastmod: 2026-08-01
linktitle: إنشاء التعليقات التوضيحية في Aspose.Drawing
og_description: اكتشف كيفية إضافة التعليقات التوضيحية في Aspose.Drawing for .NET.
  يغطي هذا البرنامج التعليمي المتطلبات المسبقة، التنفيذ خطوة بخطوة، نصائح، وأسئلة
  شائعة للمطورين.
og_image_alt: Screenshot showing callout annotation on an image using Aspose.Drawing
og_title: كيفية إضافة التعليقات التوضيحية باستخدام Aspose.Drawing for .NET – دليل
  سريع
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to add callouts to images using Aspose.Drawing for .NET –
    step‑by‑step guide with code placeholders, tips, and FAQs.
  headline: How to Add Callouts with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of drawing operations for diagrams,
      charts, and custom graphics beyond simple callouts.
    question: Can I use Aspose.Drawing for other types of illustrations?
  - answer: Absolutely! Aspose.Drawing handles PNG, JPEG, GIF, BMP, TIFF, and many
      more formats.
    question: Is Aspose.Drawing compatible with different image formats?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find more examples and documentation?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      for community assistance and official support.
    question: How do I get support if I encounter issues?
  - answer: Certainly! Get started with a free trial [here](https://releases.aspose.com/).
    question: Can I try Aspose.Drawing before purchasing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- callout
- Aspose.Drawing
- .NET graphics
- image annotation
title: كيفية إضافة التعليقات التوضيحية باستخدام Aspose.Drawing for .NET
url: /ar/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة Callouts باستخدام Aspose.Drawing لـ .NET

## مقدمة
إذا كنت تبحث عن **كيفية إضافة callouts** إلى صورك أو مخططاتك باستخدام Aspose.Drawing لـ .NET، فقد وصلت إلى المكان الصحيح. في هذا البرنامج التعليمي سنستعرض كل خطوة — من تحميل صورة bitmap، إنشاء قماش `Graphics`، تعريف هندسة الـ callout، إلى رسم الـ callouts المُنسقة — لتصبح مرئياتك أوضح وأكثر إفادة.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Drawing لـ .NET (قابلة للتنزيل من الموقع الرسمي).  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6+.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **كم يستغرق التنفيذ؟** عادةً أقل من 10 دقائق لإضافة callout أساسي.  
- **هل يمكن تخصيص الألوان والخطوط؟** نعم — كل شيء يُدار عبر كائنات GDI+ القياسية (Pen، Font، Brush).

## ما هو Callout؟
Callout هو توضيح رسومي يجمع بين خط (أو سهم) مع تسمية نصية لتسليط الضوء على جزء محدد من الصورة. يُستخدم عادةً في المخططات التقنية، لقطات الشاشة، والعروض لتوجيه الانتباه إلى عنصر معين، شرح ميزة، أو تقديم معلومات قياس، مما يجعل التواصل البصري أوضح وأكثر فاعلية.

## لماذا تستخدم Aspose.Drawing للـ Callouts؟
تم بناء Aspose.Drawing لمعالجة الصور بأداء عالٍ ويدعم مجموعة واسعة من الصيغ، مما يجعله مثالياً لإضافة Callouts إلى رسومات كبيرة أو معقدة. يمكن لهندسته الفعّالة من حيث الذاكرة معالجة ملفات تصل إلى **500 ميغابايت** دون تحميل الـ bitmap بالكامل إلى الذاكرة، كما يوفّر تحكمًا دقيقًا في primitive الرسم، الألوان، وعرض النص، لضمان توضيحات حادة ومظهر احترافي.

## المتطلبات المسبقة
قبل البدء، تأكد من وجود ما يلي:

- معرفة أساسية بلغة البرمجة C#.  
- تثبيت مكتبة Aspose.Drawing. يمكنك تنزيلها [هنا](https://releases.aspose.com/drawing/net/).  
- مستند أو صورة تريد إضافة Callouts إليها.

## استيراد مساحات الأسماء
توفر مساحات الأسماء التالية وصولاً إلى الفئات الأساسية للرسم:

`System.Drawing` يقدم أنواع GDI+ مثل `Bitmap`، `Graphics`، `Pen`، `Font`، و `Brush`. استوردها قبل بدء كتابة الشيفرة.

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## كيفية إضافة Callouts في Aspose.Drawing
حمّل الصورة المصدر، أنشئ قماش `Graphics`، عرّف نقاط البداية/النهاية، واستدعِ طريقة مساعدة ترسم الخط، رأس السهم، والتسمية — كل ذلك في بضع أسطر مختصرة. يعمل هذا النهج مع ملفات PNG، JPEG، BMP، و GIF ويسمح لك بتخصيص الألوان، الخطوط، وأنماط الخط بالكامل.

## الخطوة 1: تحميل الصورة
`Image` تمثل صورة نقطية وتوفر طرقًا للتحميل، الحفظ، ومعالجة بيانات الـ bitmap. ابدأ بتحميل الصورة التي تريد إضافة Callouts إليها. استبدل `"Your Document Directory"` و `"gears.png"` بمسار الدليل الفعلي واسم ملف الصورة الخاص بك.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## الخطوة 2: إنشاء كائن Graphics
`Graphics` يوفر طرق سطح الرسم لتصوير الأشكال، النصوص، والصور على الـ bitmap. يتيح لك كائن `Graphics` المستخرج من الصورة تنفيذ عمليات الرسم.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## الخطوة 3: تعريف مواضع Callout
`PointF` يعرّف نقطة في الفضاء الثنائي الأبعاد باستخدام إحداثيات عائمة. حدّد نقاط البداية (المرساة) والنهاية (التسمية) لكل Callout. يجب أن تكون هذه الإحداثيات داخل حدود الصورة؛ وإلا سيُقصّ Callout.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## الخطوة 4: رسم Callouts
نفّذ طريقة `DrawCallOut` لتصوير الخط، رأس السهم الاختياري، والتسمية النصية. تستخدم الطريقة `Pen` للخط، `Font` للتسمية، و `SolidBrush` لألوان التعبئة.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## الخطوة 5: حفظ الصورة
احفظ الـ bitmap المُعَلَّم على القرص. يمكنك اختيار أي صيغة مدعومة مثل PNG أو JPEG.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## شفرة مصدر Draw Callout
الشيفرة الكاملة التي تجمع جميع الخطوات معًا موجودة في العنصر النائب أدناه. أدرج تفاصيل تنفيذك الخاصة حيثما هو موضح.

```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## المشكلات الشائعة والنصائح
- **إحداثيات المرساة غير صحيحة** – تأكد من أن نقاط البداية والنهاية داخل حدود الصورة؛ وإلا قد يتم قص الـ Callout.  
- **تداخل النص** – عدّل `spaceSize` أو حجم الخط إذا تصادمت التسمية مع رسومات أخرى.  
- **الأداء** – بالنسبة للصور الكبيرة جدًا، فكر في تحرير كائنات `Pen`، `Font`، و `Brush` بعد الانتهاء لتفريغ الموارد.

## الخاتمة
الآن لديك نمط جاهز للإنتاج **لإضافة callouts** إلى أي صورة باستخدام Aspose.Drawing لـ .NET. لا تتردد في تجربة ألوان مختلفة، أنماط خطوط، وعائلات خطوط لتتناسب مع هوية علامتك التجارية.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing لأنواع أخرى من الرسوم التوضيحية؟**  
ج: نعم، يدعم Aspose.Drawing مجموعة واسعة من عمليات الرسم للمخططات، الرسوم البيانية، والرسومات المخصصة بخلاف الـ callouts البسيطة.

**س: هل Aspose.Drawing متوافق مع صيغ صور مختلفة؟**  
ج: بالتأكيد! يتعامل Aspose.Drawing مع PNG، JPEG، GIF، BMP، TIFF، والعديد من الصيغ الأخرى.

**س: أين يمكنني العثور على المزيد من الأمثلة والوثائق؟**  
ج: استكشف الوثائق الشاملة [هنا](https://reference.aspose.com/drawing/net/).

**س: كيف أحصل على الدعم إذا واجهت مشكلات؟**  
ج: زر منتدى [Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على مساعدة المجتمع والدعم الرسمي.

**س: هل يمكنني تجربة Aspose.Drawing قبل الشراء؟**  
ج: بالطبع! ابدأ بالنسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

---

**آخر تحديث:** 2026-08-01  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [كيفية رسم أقواس وأشكال أخرى باستخدام Aspose.Drawing لـ .NET](/drawing/net/lines-curves-and-shapes/)
- [دورة تحويل المصفوفات: تحويلات المصفوفة في Aspose.Drawing لـ .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [كيفية ربط المسارات باستخدام Pen في Aspose.Drawing .NET](/drawing/net/pens/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}