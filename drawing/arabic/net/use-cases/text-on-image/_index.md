---
title: إضافة نص على الصور في Aspose.Drawing
linktitle: إضافة نص على الصور في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: استكشف التكامل السلس للنص في الصور باستخدام Aspose.Drawing for .NET. اتبع دليلنا خطوة بخطوة لمعالجة الصور بسهولة. التحميل الان!
weight: 12
url: /ar/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة نص على الصور في Aspose.Drawing

## مقدمة
في العالم الديناميكي لتطوير .NET، يبرز Aspose.Drawing كأداة قوية لمعالجة الصور بسهولة. تعد إضافة نص إلى الصور متطلبًا شائعًا، سواء كان ذلك لوضع علامة مائية أو تعليقات توضيحية أو إنشاء رسومات مخصصة. في هذا البرنامج التعليمي، سنستكشف كيفية الاستفادة من Aspose.Drawing لدمج النص بسلاسة في صورك باستخدام لغة C#.
## المتطلبات الأساسية
قبل الغوص في البرنامج التعليمي، تأكد من أن لديك ما يلي:
1.  مكتبة Aspose.Drawing: قم بتنزيل وتثبيت مكتبة Aspose.Drawing من[Aspose.Drawing لوثائق .NET](https://reference.aspose.com/drawing/net/).
2. بيئة التطوير: تمتع ببيئة تطوير .NET عاملة، بما في ذلك Visual Studio أو أي بيئة تطوير متكاملة أخرى متوافقة.
الآن، دعونا نبدأ مع الدليل خطوة بخطوة.
## استيراد مساحات الأسماء
ابدأ باستيراد مساحات الأسماء الضرورية إلى مشروع C# الخاص بك:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## الخطوة 1: تحميل الصورة
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
هنا، نقوم بتحميل الصورة من مسار الملف المحدد وتهيئة كائن الرسومات لمزيد من المعالجة.
## الخطوة 2: تعيين خصائص النص
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
تحديد خصائص النص مثل اللون والخط والحشو. اضبط هذه المعلمات وفقًا لتفضيلاتك.
## الخطوة 3: قياس حجم النص
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
احسب الحجم المطلوب للنص عن طريق قياس كل كلمة على حدة. وهذا يضمن الموضع المناسب ويتجنب تداخل النص.
## الخطوة 4: رسم النص على الصورة
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
الآن، ضع النص على الصورة بناءً على الحجم المحسوب وارسمه باستخدام الخط واللون المحددين.
## الخطوة 5: احفظ الصورة
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
احفظ الصورة المعدلة في الدليل الذي تريده.
يوضح هذا الدليل خطوة بخطوة عملية مباشرة لإضافة نص إلى الصور باستخدام Aspose.Drawing for .NET. قم بتجربة خطوط وألوان ومحتوى نصي مختلف لتحقيق التأثير المرئي المطلوب.
## خاتمة
يعمل Aspose.Drawing على تبسيط مهام معالجة الصور في .NET، مما يوفر للمطورين مجموعة أدوات قوية. تعد إضافة نص إلى الصور مجرد مثال واحد على إمكانياتها، حيث تعرض تنوع المكتبة في التعامل مع العناصر الرسومية.
## أسئلة مكررة
### هل Aspose.Drawing متوافق مع جميع تنسيقات الصور؟
 يدعم Aspose.Drawing مجموعة واسعة من تنسيقات الصور، بما في ذلك التنسيقات الشائعة مثل JPEG وPNG وGIF. الرجوع إلى[توثيق](https://reference.aspose.com/drawing/net/) للحصول على قائمة كاملة.
### هل يمكنني استخدام Aspose.Drawing للمشاريع التجارية؟
نعم، Aspose.Drawing مناسب لكل من المشاريع الشخصية والتجارية. للحصول على تفاصيل الترخيص، قم بزيارة[صفحة الشراء](https://purchase.aspose.com/buy).
### هل التراخيص المؤقتة متاحة لأغراض الاختبار؟
 نعم يمكنك الحصول على ترخيص مؤقت للاختبار من خلال الزيارة[ترخيص مؤقت](https://purchase.aspose.com/temporary-license/).
### أين يمكنني العثور على دعم مجتمعي لـ Aspose.Drawing؟
 الانخراط مع المجتمع والحصول على الدعم على[Aspose.منتدى الرسم](https://forum.aspose.com/c/drawing/44).
### كيف أبدأ مع Aspose.Drawing؟
 ابدأ بتنزيل المكتبة من[هنا](https://releases.aspose.com/drawing/net/) واستكشاف شاملة[توثيق](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
