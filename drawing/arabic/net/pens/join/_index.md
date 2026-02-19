---
date: 2026-02-19
description: تعلم كيفية رسم مسار وربط المسارات بالأقلام في Aspose.Drawing، ثم حفظ
  الصورة بصيغة PNG باستخدام كود C# بسيط.
linktitle: Joining Paths with Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية رسم المسار وربط المسارات بالأقلام في Aspose.Drawing
url: /ar/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم مسار وربط المسارات باستخدام الأقلام في Aspose.Drawing

## مقدمة

مرحبًا بك في عالم **Aspose.Drawing for .NET**! في هذا البرنامج التعليمي، ستكتشف **كيفية رسم مسار** للكائنات، وربطها بأنماط مختلفة من تقاطع الخطوط، وأخيرًا **حفظ الصورة كملف PNG**. سواءً كنت تبني أداة تقارير، أو محرر تصميم، أو تحتاج فقط إلى رسومات متجهة واضحة، فإن إتقان رسم المسارات باستخدام الأقلام يمنحك تحكمًا دقيقًا في المخرجات البصرية.

## الإجابات السريعة
- **ماذا يعني “رسم مسار”?** ينشئ تعريفات خطوط أو أشكال قائمة على المتجهات يمكن لكائن `Graphics` عرضها.  
- **ما هي تقاطعات الخطوط المتاحة؟** `Bevel`، `Miter`، `Round`، و `BevelClipped`.  
- **هل يمكنني تصدير النتيجة كملف PNG؟** نعم—استخدم `Bitmap.Save` مع امتداد `.png`.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية تعمل للتقييم؛ الترخيص التجاري مطلوب للإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.6+، .NET Core 3.1+، و .NET 6+.

## ما هو “كيفية رسم مسار” في Aspose.Drawing؟

يعني رسم مسار إنشاء كائن `GraphicsPath` يحتوي على سلسلة من الخطوط أو المنحنيات أو الأشكال. بمجرد بناء المسار، تقوم برسمه على سطح `Graphics` باستخدام `Pen`. هذا النهج أكثر مرونة من رسم خطوط فردية لأنه يتيح لك تطبيق التحويلات والقص وتنسيقات التقاطع على الشكل بالكامل.

## لماذا تستخدم Aspose.Drawing لربط المسارات؟

- **توافق كامل مع .NET** – يعمل على Windows و Linux و macOS.  
- **خيارات تقاطع الخطوط الغنية** – إنشاء زوايا مائلة، مستديرة، أو مشطوفة بخاصية واحدة.  
- **إخراج نقطي عالي الجودة** – احفظ مباشرةً كـ PNG أو JPEG أو BMP دون خطوات تحويل إضافية.  
- **بدون قيود GDI+** – مثالي للتصيير على الخادم حيث قد تكون `System.Drawing.Common` مقيدة.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من وجود ما يلي:

1. **مكتبة Aspose.Drawing** – قم بتنزيلها **[هنا](https://releases.aspose.com/drawing/net/)**.  
2. **بيئة تطوير .NET** – Visual Studio أو VS Code أو أي IDE يدعم C#.

الآن بعد أن أصبح كل شيء جاهزًا، دعنا نتبع كل خطوة.

## استيراد الـ Namespaces

أضف المساحات الاسمية المطلوبة في أعلى ملفك حتى يعرف المترجم أين يجد فئات الرسومات:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## الخطوة 1: إنشاء كائن Bitmap و Graphics

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

نبدأ بسطح رسم فارغ (`Bitmap`) بحجم 1000 × 800 بكسل ونحصل على كائن `Graphics` سيقوم بتنفيذ أوامر الرسم.

## الخطوة 2: تعريف طريقة DrawPath

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

هذه الطريقة المساعدة تغلف منطق الرسم:

- **Pen** – يحدد اللون والسُمك (30 px).  
- **GraphicsPath** – يعرّف خطين متصلين يشكلان شكل “L”.  
- **LineJoin** – يتحكم في كيفية عرض الزاوية بين الخطين (`Bevel`، `Round`، إلخ).  

يمكنك استدعاء هذه الطريقة بأي قيمة `LineJoin` لرؤية الاختلاف البصري.

## الخطوة 3: ربط المسارات باستخدام Bevel LineJoin

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

استخدام `LineJoin.Bevel` ينتج زاوية مسطحة حيث يلتقي الخطان.

## الخطوة 4: ربط المسارات باستخدام Round LineJoin

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

`LineJoin.Round` ينتج زاوية ناعمة ومستديرة—مثالية لمظهر أكثر صقلًا.

## الخطوة 5: حفظ النتيجة كملف PNG

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

نداء `Save` يكتب الـ bitmap إلى ملف بصيغة PNG. عدّل المسار ليتوافق مع بيئتك.

## المشكلات الشائعة والحلول

| المشكلة | لماذا يحدث | الحل |
|-------|----------------|-----|
| **الصورة تظهر فارغة** | لم يتم مسح كائن `Graphics` أو حجم الـ bitmap صغير جدًا. | استدعِ `graphics.Clear(Color.White);` قبل الرسم، أو زد أبعاد الـ bitmap. |
| **الزاوية تبدو متعرجة** | استخدام bitmap منخفض الدقة مع قلم سُمكه كبير. | زد DPI للـ bitmap (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) أو قلل سُمك القلم. |
| **خطأ ملف غير موجود** | مسار حفظ غير صالح. | استخدم `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.Drawing مجانًا؟

ج1: Aspose.Drawing منتج تجاري، لكن يمكنك استكشاف قدراته عبر **[التجربة المجانية](https://releases.aspose.com/)**.

### س2: أين يمكنني العثور على توثيق Aspose.Drawing؟

ج2: راجع **[التوثيق](https://reference.aspose.com/drawing/net/)** للحصول على دليل شامل.

### س3: كيف يمكنني الحصول على دعم لـ Aspose.Drawing؟

ج3: زر **[منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44)** للحصول على مساعدة المجتمع والدعم الرسمي.

### س4: هل تتوفر تراخيص مؤقتة لـ Aspose.Drawing؟

ج4: نعم، يمكنك الحصول على **[ترخيص مؤقت](https://purchase.aspose.com/temporary-license/)** للاستخدام قصير الأمد.

### س5: أين يمكنني شراء Aspose.Drawing؟

ج5: اشترِ Aspose.Drawing **[هنا](https://purchase.aspose.com/buy)**.

## الخلاصة

في هذا الدليل غطينا **كيفية رسم مسار**، واستخدمنا أنماط `LineJoin` المختلفة، وحفظنا الرسم النهائي كملف PNG باستخدام Aspose.Drawing لـ .NET. من خلال إتقان هذه الخطوات يمكنك إنشاء رسومات متجهة متقدمة، أيقونات مخصصة، أو مخططات ديناميكية مباشرةً من كود الخادم.

---

**آخر تحديث:** 2026-02-19  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}