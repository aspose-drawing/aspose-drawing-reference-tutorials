---
date: 2026-09-18
description: تعلم كيفية رسم مسار ودمج المسارات باستخدام الأقلام في Aspose.Drawing،
  ثم حفظ الصورة بصيغة PNG باستخدام كود C# بسيط.
keywords:
- save image as png
- server side image rendering
- raster image from vector
- export graphics to png
- alternative to system drawing
lastmod: 2026-09-18
linktitle: دمج المسارات باستخدام الأقلام في Aspose.Drawing
og_description: احفظ الصورة بصيغة PNG باستخدام Aspose.Drawing. تعلم رسم المسارات،
  تطبيق أنماط line‑join، وتصدير رسومات raster عالية الجودة من بيانات vector على server.
og_image_alt: Developer guide showing how to draw and join paths with pens, then save
  the result as a PNG file using Aspose.Drawing
og_title: كيفية رسم مسار، دمج المسارات باستخدام الأقلام وحفظ الصورة بصيغة PNG
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to draw path and join paths with pens in Aspose.Drawing,
    then save the image as PNG using simple C# code.
  headline: How to draw path, join paths with pens and save image as PNG
  type: TechArticle
- questions:
  - answer: Aspose.Drawing is a commercial product, but you can explore its capabilities
      with a **[free trial](https://releases.aspose.com/)**.
    question: Can I use Aspose.Drawing for free?
  - answer: Refer to the **[documentation](https://reference.aspose.com/drawing/net/)**
      for comprehensive guidance.
    question: Where can I find Aspose.Drawing documentation?
  - answer: Visit the **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)**
      for community help and official assistance.
    question: How can I get support for Aspose.Drawing?
  - answer: Yes, you can obtain a **[temporary license](https://purchase.aspose.com/temporary-license/)**
      for short‑term usage.
    question: Are temporary licenses available for Aspose.Drawing?
  - answer: Purchase Aspose.Drawing **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.
    question: Where can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- C# graphics
- save PNG
- vector to raster
- server side rendering
title: كيفية رسم مسار، دمج المسارات باستخدام الأقلام وحفظ الصورة بصيغة PNG
url: /ar/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم مسار، ربط المسارات بالأقلام وحفظ الصورة كـ PNG

## مقدمة

في هذا الدرس ستتعلم كيفية **رسم مسار** للكائنات، ربطها بأنماط تقاطع خطوط مختلفة، و**حفظ الصورة كـ PNG** باستخدام Aspose.Drawing لـ .NET. سواءً كنت تبني محرك تقارير، محرر تصميم، أو تحتاج إلى تصيير صور على الخادم لخدمة ويب، فإن إتقان رسم المسارات بالأقلام يمنحك تحكمًا دقيقًا في تحويل المتجهات إلى نقطية.

## إجابات سريعة
- **ما معنى “draw path”؟** ينشئ تعريفات خطوط أو أشكال قائمة على المتجهات يمكن لكائن `Graphics` عرضها.  
- **ما هي تقاطعات الخطوط المتاحة؟** `Bevel`، `Miter`، `Round`، و`BevelClipped`.  
- **هل يمكنني تصدير النتيجة كـ PNG؟** نعم—استخدم `Bitmap.Save` مع امتداد `.png`.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية تعمل للتقييم؛ الترخيص التجاري مطلوب للإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.6+، .NET Core 3.1+، و .NET 6+.

## ما هو “draw path” في Aspose.Drawing؟

**Draw path** يعني إنشاء `GraphicsPath` يحتوي على سلسلة من الخطوط أو المنحنيات أو الأشكال.  
`GraphicsPath` هو حاوية Aspose.Drawing للجيومتري المتجهية؛ يمكنك لاحقًا عرضها باستخدام `Pen` أو ملئها بفرشاة. يتيح لك هذا النهج تطبيق التحويلات، والقص، وأنماط تقاطع الخط المتسقة على الشكل بأكمله بدلاً من رسم كل مقطع على حدة.

## لماذا تستخدم Aspose.Drawing لتصيير الصور على الخادم؟

توفر Aspose.Drawing محرك تصيير قوي على الخادم يعمل على أي نظام تشغيل دون الاعتماد على GDI+، مما يجعله مثاليًا لخدمات السحابة، التطبيقات الحاوية، وواجهات برمجة التطبيقات الويب عالية الأداء حيث يلزم التوافق عبر المنصات والتشغيل بدون واجهة رسومية، مما يضمن أداءً قابلًا للتوسع.

- **توافق كامل مع .NET** – يدعم .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6/7.  
- **خيارات تقاطع خطوط غنية** – `Bevel`، `Miter`، `Round`، `BevelClipped`.  
- **إخراج نقطي عالي الجودة** – يمكن تصديره إلى **أكثر من 10 صيغ نقطية** (PNG، JPEG، BMP، GIF، TIFF، إلخ) مباشرةً من بيانات المتجه.  
- **بدون قيود GDI+** – مثالي لخدمات السحابة، الحاويات، والبيئات بدون واجهة رسومية.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من أن لديك:

1. **مكتبة Aspose.Drawing** – قم بتحميلها من **[صفحة تحميل Aspose.Drawing](https://releases.aspose.com/drawing/net/)**.  
2. **بيئة تطوير .NET** – Visual Studio، VS Code، أو أي بيئة تطوير تدعم C#.

الآن بعد أن كل شيء جاهز، دعنا نستعرض كل خطوة.

## استيراد مساحات الأسماء

مساحات الأسماء `System.Drawing` و `System.Drawing.Drawing2D` تحتوي على الأنواع الأساسية للرسومات المستخدمة في Aspose.Drawing.  

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## الخطوة 1: إنشاء صورة نقطية (bitmap) وكائن رسومات

`Bitmap` هو لوحة نقطية (Raster) في الذاكرة من Aspose.Drawing. تمثل صورة نقطية يمكنك الرسم عليها باستخدام سطح `Graphics`.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

نبدأ بلوحة فارغة (`Bitmap`) بحجم 1000 × 800 بكسل ونحصل على كائن `Graphics` سيقوم بتنفيذ أوامر الرسم الخاصة بنا.

## الخطوة 2: تعريف طريقة drawPath

`Pen` هو أداة Aspose.Drawing لتحديد حدود المتجهات؛ يحدد اللون، السماكة، ونمط تقاطع الخط.  

`LineJoin` يتحكم في كيفية ربط مقطعي خط عند الزاوية.  

`GraphicsPath` هو الحاوية المتجهية التي تحتفظ بسلسلة الخطوط التي سنربطها.

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

هذه الدالة المساعدة تغلف منطق الرسم:

- **Pen** – يحدد اللون والسماكة (30 px).  
- **GraphicsPath** – يحدد خطين متصلين يشكلان شكل “L”.  
- **LineJoin** – يتحكم في كيفية عرض الزاوية بين الخطين (`Bevel`، `Round`، إلخ).  

يمكنك استدعاء هذه الدالة بأي قيمة `LineJoin` لرؤية الاختلاف البصري.

## الخطوة 3: ربط المسارات باستخدام تقاطع الخط Bevel

`LineJoin.Bevel` يخلق زاوية مسطحة حيث يلتقي الخطان، وهو مفيد عندما تريد وصلة حادة غير متداخلة.

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

## الخطوة 4: ربط المسارات باستخدام تقاطع الخط Round

`LineJoin.Round` ينتج زاوية ناعمة ومستديرة—مثالية لمظهر أكثر صقلًا.

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

## الخطوة 5: حفظ النتيجة كـ PNG

استدعاء `Save` يكتب اللوحة إلى ملف بصيغة PNG، مكملًا سير عمل **حفظ الصورة كـ PNG**. عدل المسار ليتناسب مع بيئتك.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثها | الحل |
|-------|----------------|-----|
| **الصورة تظهر فارغة** | لم يتم مسح كائن `Graphics` أو حجم اللوحة صغير جدًا. | استدعِ `graphics.Clear(Color.White);` قبل الرسم، أو زد أبعاد اللوحة. |
| **الزاوية تبدو متعرجة** | استخدام لوحة منخفضة الدقة مع قلم سميك. | زد DPI للوحة (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) أو قلل سماكة القلم. |
| **خطأ ملف غير موجود** | مسار حفظ غير صالح. | استخدم `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing مجانًا؟**  
ج: Aspose.Drawing هو منتج تجاري، لكن يمكنك استكشاف إمكانياته من خلال **[تجربة مجانية](https://releases.aspose.com/)**.

**س: أين يمكنني العثور على وثائق Aspose.Drawing؟**  
ج: راجع **[الوثائق](https://reference.aspose.com/drawing/net/)** للحصول على إرشادات شاملة.

**س: كيف يمكنني الحصول على دعم لـ Aspose.Drawing؟**  
ج: زر **[منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44)** للحصول على مساعدة المجتمع والدعم الرسمي.

**س: هل تتوفر تراخيص مؤقتة لـ Aspose.Drawing؟**  
ج: نعم، يمكنك الحصول على **[ترخيص مؤقت](https://purchase.aspose.com/temporary-license/)** للاستخدام قصير الأمد.

**س: أين يمكنني شراء Aspose.Drawing؟**  
ج: اشترِ Aspose.Drawing من **[صفحة شراء Aspose.Drawing](https://purchase.aspose.com/buy)**.

## الخلاصة

في هذا الدليل غطينا كيفية **رسم مسار** للكائنات، تطبيق أنماط `LineJoin` المختلفة، و**حفظ الصورة كـ PNG** باستخدام Aspose.Drawing لـ .NET. من خلال إتقان هذه الخطوات يمكنك إنشاء رسومات متجهية متقدمة، أيقونات مخصصة، أو مخططات ديناميكية مباشرةً من كود الخادم، مما يوفر حلًا موثوقًا لـ **تصدير الرسومات إلى PNG** يعمل على أي منصة.

**آخر تحديث:** 2026-09-18  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية رسم قوس وحفظ الصورة كـ PNG باستخدام Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-arc/)
- [كيفية حفظ bitmap كـ PNG أثناء رسم خطوط متعددة باستخدام Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [كيفية حفظ bitmap كـ PNG باستخدام Aspose.Drawing API لـ .NET](/drawing/net/image-editing/display/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}