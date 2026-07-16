---
date: 2026-02-25
description: تعلم كيفية ضبط محاذاة النص في Aspose.Drawing لـ .NET وإضافة النص إلى
  الصور. دليل خطوة بخطوة مع أمثلة.
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: ضبط محاذاة النص باستخدام Aspose.Drawing لـ .NET
url: /ar/net/text-and-fonts/format-text/
weight: 11
---

Need to keep markdown formatting exactly.

Let's construct final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ضبط محاذاة النص في Aspose.Drawing

## المقدمة

عندما يتعلق الأمر **set text alignment** وتنسيق النص في تطبيقات .NET الخاصة بك، فإن Aspose.Drawing هي المكتبة المفضلة للمطورين الذين يحتاجون إلى الدقة، الأداء، وواجهة برمجة تطبيقات غنية. سواء كنت تبني محرك تقارير، مولد شارات ديناميكي، أو أي حل يتطلب رسومات مكثفة، فإن القدرة على التحكم في كيفية محاذاة النص داخل الأشكال تجعل مخرجاتك تبدو مصقولة ومهنية. في هذا الدرس سنستعرض العملية بالكامل — من إنشاء لوحة bitmap إلى رسم مستطيل بالنص، معالجة التجاوز، وأخيرًا حفظ الصورة.

## إجابات سريعة
- **ما معنى “set text alignment”?** يحدد كيفية تموضع النص أفقياً وعمودياً داخل مستطيل الرسم.  
- **أي فئة تتحكم في المحاذاة؟** `StringFormat` تتيح لك تعيين `Alignment` و `LineAlignment`.  
- **هل يمكنني رسم سلسلة ومستطيل معًا؟** نعم—استخدم `Graphics.DrawRectangle` ثم `Graphics.DrawString`.  
- **كيف يمكنني منع تجاوز النص؟** قم بتعديل حجم المستطيل أو قسّم النص إلى عدة أسطر يدويًا.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم الحصول على ترخيص تجاري لـ Aspose.Drawing للاستخدام غير التجريبي.

## ما هو **set text alignment** في Aspose.Drawing؟

`set text alignment` يشير إلى تكوين تموضع النص الأفقي (`StringAlignment`) والعمودي (`LineAlignment`) داخل `Rectangle` أو أي منطقة رسم. من خلال تعديل هذه الإعدادات تتحكم فيما إذا كان النص يظهر محاذيًا إلى اليسار، في الوسط، إلى اليمين، أو محاذيًا إلى الأعلى، الوسط، أو الأسفل.

## لماذا تستخدم Aspose.Drawing لمحاذاة النص؟

- **توافق كامل مع .NET** – يعمل مع .NET Framework و .NET Core و .NET 5/6+.  
- **عرض بدقة بكسل مثالية** – مضاد التعرج ودعم DPI عالي مدمج.  
- **بدون قيود GDI+** – على عكس `System.Drawing.Common`، يعمل Aspose.Drawing على حاويات Linux دون تبعيات أصلية.  
- **تنسيق غني** – دمج الخطوط والفرش والأقلام وكائنات `StringFormat` المخصصة لتصاميم متقدمة.

## المتطلبات المسبقة

1. **Aspose.Drawing Library** – قم بتنزيلها [here](https://releases.aspose.com/drawing/net/).  
2. **بيئة التطوير** – Visual Studio 2022 (أو أي بيئة تطوير C#).  
3. **معرفة أساسية بـ .NET** – يجب أن تكون مرتاحًا مع مشاريع C# وحزم NuGet.

## استيراد Namespaces

لبدء العمل، استورد المساحات الاسمية المطلوبة إلى النطاق. هذه تمنحك الوصول إلى الرسومات، عرض النص، والكيانات الأساسية للرسم.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## الخطوة 1: إنشاء كائنات Bitmap و Graphics  

إنشاء bitmap يوفر لوحة يمكنك الرسم عليها. كائن `Graphics` هو سطح الرسم، ونحن نفعّل عرض نص عالي الجودة باستخدام `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## الخطوة 2: تعريف **StringFormat** وتنسيق  

هنا نقوم **set text alignment** عن طريق تكوين كائن `StringFormat`. كما نجهّز الفرش، الأقلام، والخط الذي سيُستخدم عند رسم السلسلة.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## الخطوة 3: إنشاء وتنسيق النص – **how to draw string** و **draw rectangle with text**

نُكوّن النص، نحدد المستطيل الذي سيحتويه، ثم نرسم كلًا من حدود المستطيل والسلسلة نفسها.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### كيفية التعامل مع تجاوز النص

إذا كان `text` المقدم يتجاوز حدود المستطيل، لديك خياران شائعان:

1. **تغيير حجم المستطيل** – زيادة `rectangle.Width` أو `rectangle.Height`.  
2. **تقسيم النص** – قسّم السلسلة إلى أسطر تتناسب، ثم استدعِ `DrawString` لكل سطر مع تعديل إحداثيات Y.

## الخطوة 4: حفظ الناتج – **add text to image**

أخيرًا، اكتب الـ bitmap إلى القرص. تُظهر هذه الخطوة **add text to image** في استدعاء واحد.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **النص يظهر ضبابيًا** | تأكد من تعيين `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`. |
| **النص مقطوع** | قم بزيادة حجم المستطيل أو فعّل منطق التفاف الكلمات عن طريق قياس حجم السلسلة (`Graphics.MeasureString`). |
| **الخط غير موجود** | تحقق من تثبيت الخط على الجهاز المضيف أو دمج خط خاص باستخدام `PrivateFontCollection`. |
| **ألوان غير متوقعة** | تحقق مرة أخرى من ألوان الفرشاة والقلم؛ تذكر أن `Color.FromKnownColor` يستخدم ألوان معرفة من النظام. |

## الأسئلة المتكررة

### Q1: هل Aspose.Drawing متوافق مع جميع إصدارات .NET؟

A1: نعم، تم تصميم Aspose.Drawing ليكون متوافقًا مع مجموعة واسعة من إصدارات .NET، مما يضمن المرونة للمطورين.

### Q2: هل يمكنني تخصيص نمط الخط أكثر؟

A2: بالطبع! قم بتعديل معلمات كائن `Font` لتحقيق حجم الخط، النمط، والعائلة المطلوبة.

### Q3: كيف يمكنني التعامل مع تجاوز النص داخل المستطيل المحدد؟

A3: يمكنك إدارة تجاوز النص عن طريق تعديل حجم المستطيل أو تنفيذ منطق مخصص للتعامل مع النص الطويل.

### Q4: هل هناك خيارات تنسيق أخرى متاحة في Aspose.Drawing؟

A4: نعم، يوفر Aspose.Drawing مجموعة شاملة من الأدوات لمعالجة الرسومات، بما في ذلك خيارات تنسيق متعددة للنص، الأشكال، وأكثر.

### Q5: أين يمكنني العثور على دعم إضافي لـ Aspose.Drawing؟

A5: استكشف منتدى Aspose.Drawing [here](https://forum.aspose.com/c/drawing/44) للحصول على دعم المجتمع والنقاشات.

**أسئلة وإجابات إضافية**

**س: كيف أرسم سلسلة بدون مستطيل محيط؟**  
ج: احذف استدعاء `DrawRectangle` ومرّر الموقع المطلوب `PointF` إلى `Graphics.DrawString`.

**س: هل يمكنني تدوير النص مع الحفاظ على المحاذاة؟**  
ج: نعم—طبق تحويل `Matrix` على كائن `Graphics` قبل الرسم، ثم أعد ضبطه بعد ذلك.

**س: هل يمكن تصدير الصورة كـ JPEG بدلاً من PNG؟**  
ج: ببساطة غيّر امتداد الملف في `bitmap.Save` واختر `ImageFormat.Jpeg` إذا رغبت.

---

**آخر تحديث:** 2026-02-25  
**تم الاختبار باستخدام:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}