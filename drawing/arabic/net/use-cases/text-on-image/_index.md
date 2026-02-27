---
date: 2026-02-27
description: تعلم كيفية إنشاء صورة بطاقة عيد ميلاد باستخدام Aspose.Drawing لـ .NET.
  يوضح لك هذا الدليل كيفية رسم نص على الصورة، وضع نص فوق الصورة، وإضافة تسمية توضيحية
  إلى الصورة بسرعة.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية إنشاء صورة بطاقة عيد ميلاد باستخدام Aspose.Drawing
url: /ar/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء صورة بطاقة عيد ميلاد باستخدام Aspose.Drawing

## المقدمة
في عالم .NET الديناميكي، تبرز Aspose.Drawing كأداة قوية للتعامل مع الصور بسهولة. سواء كنت بحاجة إلى **create birthday card image**، أو إضافة علامة مائية، أو مجرد وضع نص فوق صورة، فإن هذا الدليل يشرح لك الخطوات الدقيقة لرسم سلسلة نصية على صورة باستخدام C#. في نهاية هذا الدليل ستحصل على بطاقة عيد ميلاد مخصصة جاهزة للمشاركة.

## إجابات سريعة
- **What library should I use?** Aspose.Drawing for .NET  
- **Can I add a caption to photo?** Yes – use `Graphics.DrawString` with custom fonts.  
- **Is a license required for production?** Yes, a commercial license is needed.  
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **How long does implementation take?** Typically under 10 minutes for a simple card.

## ما هي صورة بطاقة عيد الميلاد؟
صورة بطاقة عيد الميلاد هي صورة مخصصة تجمع بين خلفية وصورة مع نص مخصص—مثل تحية، اسم المستلم، أو رسالة احتفالية. باستخدام Aspose.Drawing، يمكنك إنشاء هذه البطاقات برمجيًا دون الحاجة إلى أدوات التصميم اليدوية.

## لماذا تستخدم Aspose.Drawing لوضع نص فوق صورة؟
- **Cross‑platform support:** Works on Windows, Linux, and macOS.  
- **Rich drawing API:** Full control over fonts, colors, and layout.  
- **No external dependencies:** Replaces `System.Drawing.Common` with a fully managed library.  
- **High performance:** Optimized for bulk image processing.

## المتطلبات المسبقة
قبل الغوص في الدليل، تأكد من توفر ما يلي:

1. مكتبة Aspose.Drawing: قم بتحميل وتثبيت مكتبة Aspose.Drawing من [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/).  
2. بيئة التطوير: بيئة تطوير .NET تعمل، مثل Visual Studio أو Visual Studio Code، مع تثبيت .NET 6 SDK أو أحدث.

الآن، دعنا نتبع الدليل خطوة بخطوة لإضافة نص إلى صورة وحفظها كبطاقة عيد ميلاد.

## استيراد المساحات الاسمية
ابدأ باستيراد المساحات الاسمية اللازمة إلى مشروع C# الخاص بك:

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
هنا، نقوم بتحميل الصورة من مسار الملف المحدد ونُنشئ كائن الرسومات للمعالجة اللاحقة.

## الخطوة 2: تعيين خصائص النص
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
حدد خصائص النص مثل اللون، الخط، والمسافة الداخلية. عدل هذه المعلمات وفقًا لتفضيلات التصميم الخاصة بك.

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
احسب الحجم المطلوب للنص عن طريق قياس كل كلمة على حدة. يضمن ذلك وضعًا صحيحًا ويتجنب تداخل النص.

## الخطوة 4: رسم النص على الصورة
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
الآن، ضع النص على الصورة بناءً على الحجم المحسوب وارسمه باستخدام الخط واللون المحددين.

## الخطوة 5: حفظ الصورة
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
احفظ الصورة المعدلة في الدليل الذي ترغب به. الملف الناتج هو صورة بطاقة عيد ميلاد جاهزة للإرسال.

## حالات الاستخدام الشائعة والنصائح
- **Add caption to photo:** Replace `text` with any caption you need, such as “Celebrating 30 Years!”.  
- **Draw text on bitmap:** The same approach works for `Bitmap` objects created from scratch.  
- **Overlay multiple lines:** Loop through an array of strings and adjust the `Rectangle` Y‑coordinate for each line.  
- **Pro tip:** Use `Graphics.SmoothingMode = SmoothingMode.AntiAlias` for even smoother text rendering.

## الخلاصة
Aspose.Drawing يبسط مهام معالجة الصور في .NET، موفرًا للمطورين مجموعة أدوات قوية. إضافة نص إلى الصور—سواء لإنشاء **create birthday card image**، أو **draw string on image**، أو **add caption to photo**—هي مجرد مثال واحد على مرونته في التعامل مع العناصر الرسومية.

## الأسئلة المتكررة
### هل Aspose.Drawing متوافق مع جميع صيغ الصور؟
يدعم Aspose.Drawing مجموعة واسعة من صيغ الصور، بما في ذلك الصيغ الشائعة مثل JPEG و PNG و GIF. راجع [documentation](https://reference.aspose.com/drawing/net/) للحصول على القائمة الكاملة.

### هل يمكنني استخدام Aspose.Drawing للمشاريع التجارية؟
نعم، Aspose.Drawing مناسب لكل من المشاريع الشخصية والتجارية. للحصول على تفاصيل الترخيص، زر [purchase page](https://purchase.aspose.com/buy).

### هل تتوفر تراخيص مؤقتة لأغراض الاختبار؟
نعم، يمكنك الحصول على ترخيص مؤقت للاختبار بزيارة [Temporary License](https://purchase.aspose.com/temporary-license/).

### أين يمكنني العثور على دعم المجتمع لـ Aspose.Drawing؟
تفاعل مع المجتمع واحصل على الدعم في [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).

### كيف أبدأ مع Aspose.Drawing؟
ابدأ بتحميل المكتبة من [here](https://releases.aspose.com/drawing/net/) واستكشف [documentation](https://reference.aspose.com/drawing/net/) الشاملة.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-02-27  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

---