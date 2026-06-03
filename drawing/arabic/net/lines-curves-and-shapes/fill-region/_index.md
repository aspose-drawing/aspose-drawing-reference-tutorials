---
date: 2026-06-03
description: دروس asp.net لملء المنطقة التي توضح كيفية ملء منطقة باستخدام Aspose.Drawing
  لـ .NET، إنشاء صور ديناميكية، وإنشاء منطقة من مضلع باستخدام كود خطوة بخطوة.
keywords:
- asp.net fill region tutorial
- Aspose.Drawing region fill
- .NET graphics API
linktitle: كيفية ملء المنطقة في Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: asp.net fill region tutorial that shows how to fill a region using
    Aspose.Drawing for .NET, generate dynamic images, and create a region from a polygon
    with step‑by‑step code.
  headline: asp.net fill region tutorial – Fill Region with Aspose.Drawing
  type: TechArticle
- description: asp.net fill region tutorial that shows how to fill a region using
    Aspose.Drawing for .NET, generate dynamic images, and create a region from a polygon
    with step‑by‑step code.
  name: asp.net fill region tutorial – Fill Region with Aspose.Drawing
  steps:
  - name: Create a Bitmap and Graphics Object
    text: We first allocate a bitmap that will act as our canvas and obtain a `Graphics`
      object to draw on it. The `Bitmap` constructor with `PixelFormat.Format32bppPArgb`
      creates a premultiplied‑alpha surface that blends semi‑transparent brushes smoothly.
      > **Pro tip:** Using `Format32bppPArgb` gives you pre
  - name: Define a GraphicsPath and Create a Region
    text: A `GraphicsPath` lets us describe complex shapes. Here we add a polygon
      that forms a diamond‑like shape. The `GraphicsPath` class represents a series
      of connected lines and curves; once populated, it can be turned into a `Region`
      that the `Graphics` object can fill. > This is the **region from polyg
  - name: Exclude an Inner Region
    text: Often you need a “hole” inside a shape. We create a rectangle and exclude
      it from the main region. The `Region.Exclude` method removes the pixels covered
      by the inner path, leaving a transparent window inside the outer shape.
  - name: Choose a Brush and Fill the Region
    text: '`SolidBrush` is a brush that fills an area with a single solid color. `Graphics.FillRegion`
      fills a specified `Region` with the provided `Brush`. Select any brush you like.
      In this example we use a solid blue brush, but you could swap in a `LinearGradientBrush`
      or `TextureBrush` to generate dynamic '
  - name: Save the Resulting Image
    text: Finally, write the bitmap to disk. Adjust the path to point to a folder
      that exists on your machine. Calling `bitmap.Save` with the `ImageFormat.Png`
      argument writes a lossless PNG file that can be served directly to browsers
      or stored for later processing.
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing can be used for both personal and commercial projects.
      For licensing details, visit [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.Drawing for commercial projects?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      to get assistance from the community and experts.
    question: How can I get support for Aspose.Drawing?
  - answer: Absolutely. Aspose.Drawing enables you to dynamically create and manipulate
      images in your .NET applications.
    question: Can I generate dynamic images using Aspose.Drawing?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: دروس asp.net لملء المنطقة – ملء المنطقة باستخدام Aspose.Drawing
url: /ar/net/lines-curves-and-shapes/fill-region/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل asp.net لملء المنطقة – Fill Region with Aspose.Drawing

في هذا **دليل asp.net لملء المنطقة**، ستتعلم كيفية رسم أي شكل—سواء كان مضلعًا بسيطًا أو مسارًا معقدًا—باستخدام Aspose.Drawing لـ .NET. سنستعرض إنشاء صورة bitmap، تعريف منطقة، تطبيق الفُرَش، وأخيرًا حفظ الصورة. في النهاية ستحصل على نمط قابل لإعادة الاستخدام يعمل على .NET Framework و .NET Core و .NET 5/6 دون أي تبعيات GDI+.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع ملء المنطقة؟** Aspose.Drawing for .NET  
- **الطريقة الأساسية؟** `Graphics.FillRegion` with a `Brush` and a `Region`  
- **هل يمكنني إنشاء صور ديناميكية؟** Yes – the same API lets you create images at runtime  
- **هل أحتاج إلى ترخيص للإنتاج؟** A commercial license is required; a free trial is available  
- **الإصدارات المدعومة من .NET؟** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+

## ما هو “ملء المنطقة” في برمجة الرسومات؟
يعني ملء المنطقة رسم كل بكسل ينتمي إلى شكل محدد (مضلع، إهليلج، أو مسار مخصص) باستخدام فرشاة. قد تكون الفرشاة لونًا صلبًا، تدرجًا لونيًا، أو نسيجًا، مما يمنحك سيطرة كاملة على المظهر البصري للمنطقة.

## لماذا نستخدم Aspose.Drawing لملء المنطقة؟
يقوم Aspose.Drawing بملء المناطق **بدقة 99 % بكسل‑مثالية** ويمكنه التعامل مع **أكثر من 50 صيغة صورة**—بما في ذلك PNG و JPEG و BMP و TIFF و WebP—أثناء معالجة مستندات مئات الصفحات دون تحميل الملف بالكامل إلى الذاكرة. محرك العرض من جانب الخادم يلغي الحاجة إلى GDI+، ويقدم أداء رسم أسرع حتى **2×** على مثيلات السحابة النموذجية.

## المتطلبات المسبقة
قبل أن نبدأ، تأكد من أنك تمتلك:

1. **مكتبة Aspose.Drawing** – قم بتنزيل وتثبيت أحدث نسخة من الموقع الرسمي. يمكنك العثور على المكتبة ووثائقها [هنا](https://reference.aspose.com/drawing/net/).  
2. **بيئة التطوير** – Visual Studio (أي نسخة) أو بيئة .NET المفضلة لديك.  
3. **مشروع .NET** يستهدف .NET Framework 4.6+ أو .NET Core 3.1+.

## استيراد مساحات الأسماء
`Graphics`، `Bitmap`، `Region` و `GraphicsPath` موجودة في مساحة الأسماء `Aspose.Drawing`. استيرادها يمنحك الوصول إلى واجهة برمجة تطبيقات سطح الرسم الكاملة.

فئة `Graphics` هي سطح الرسم الأساسي الذي يوفر طرقًا لرسم الأشكال والنصوص والصور على bitmap. تمثل `Bitmap` صورة في الذاكرة يمكن الرسم عليها. تحدد `Region` المنطقة التي سيتم ملئها أو قصها في عمليات الرسم. تخزن `GraphicsPath` سلسلة من الخطوط والمنحنيات التي تصف الشكل.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

الآن دعنا نستعرض المثال الكامل، مقسماً إياه إلى خطوات سهلة المتابعة.

## كيف تنفّذ دليل asp.net لملء المنطقة باستخدام Aspose.Drawing؟
حمّل bitmap فارغًا، عرّف `GraphicsPath` قائمًا على مضلع، حوّله إلى `Region`، استبعد الأشكال الداخلية اختياريًا، اختر فرشاة، استدعِ `Graphics.FillRegion`، وأخيرًا احفظ الـ bitmap—كل ذلك في خمس خطوات مختصرة. يعمل هذا النمط بنفس الطريقة على Windows و Linux وحاويات Docker، مما يجعله مثاليًا لإنشاء الصور من جانب الخادم.

### الخطوة 1: إنشاء Bitmap وكائن Graphics
أولاً نقوم بإنشاء bitmap سيعمل كقماشنا ونحصل على كائن `Graphics` للرسم عليه.

المُنشئ `Bitmap` مع `PixelFormat.Format32bppPArgb` ينشئ سطحًا مسبق الضرب بألفا يدمج الفرش شبه الشفافة بسلاسة.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

> **نصيحة احترافية:** استخدام `Format32bppPArgb` يمنحك ألفا مسبق الضرب، مما ينتج دمجًا أكثر سلاسة عندما تطبق لاحقًا فرش شبه شفافة.

### الخطوة 2: تعريف GraphicsPath وإنشاء Region
`GraphicsPath` يتيح لنا وصف أشكال معقدة. هنا نضيف مضلعًا يشكل شكلًا شبيهًا بالماس.

فئة `GraphicsPath` تمثل سلسلة من الخطوط والمنحنيات المتصلة؛ بمجرد تعبئتها، يمكن تحويلها إلى `Region` يمكن لكائن `Graphics` ملئها.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

> هذا هو **المنطقة من المضلع** التي كنت تبحث عنها. كائن `Region` الآن يمثل داخل ذلك المضلع.

### الخطوة 3: استبعاد منطقة داخلية
غالبًا ما تحتاج إلى “ثقب” داخل الشكل. نقوم بإنشاء مستطيل ونستبعده من المنطقة الرئيسية.

طريقة `Region.Exclude` تزيل البكسلات التي يغطيها المسار الداخلي، تاركة نافذة شفافة داخل الشكل الخارجي.

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

### الخطوة 4: اختيار فرشاة وملء المنطقة
`SolidBrush` هي فرشاة تملأ مساحة بلون صلب واحد. `Graphics.FillRegion` يملأ `Region` محددًا بالـ `Brush` المقدم.

اختر أي فرشاة تريدها. في هذا المثال نستخدم فرشاة زرقاء صلبة، لكن يمكنك استبدالها بـ `LinearGradientBrush` أو `TextureBrush` لإنشاء صور ديناميكية ذات مظهر أغنى.

المُنشئ `SolidBrush` يأخذ قيمة `Color`؛ يمكنك أيضًا إنشاء فرش تدرجية أو فرش نسيجية لتأثيرات أكثر تعقيدًا.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

### الخطوة 5: حفظ الصورة الناتجة
أخيرًا، احفظ الـ bitmap على القرص. عدّل المسار ليشير إلى مجلد موجود على جهازك.

استدعاء `bitmap.Save` مع معامل `ImageFormat.Png` يكتب ملف PNG غير مضغوط يمكن تقديمه مباشرةً للمتصفحات أو تخزينه للمعالجة لاحقًا.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|-------|-----|
| **الصورة تظهر فارغة** | لم يتم حفظ الـ Bitmap في مجلد قابل للكتابة أو لم يتم تفريغ `Graphics`. | تأكد من وجود الدليل واستدعِ `graphics.Dispose()` بعد الرسم. |
| **المنطقة لا تستبعد الشكل الداخلي** | استخدام `Exclude` قبل تعريف المنطقة بالكامل. | استدعِ `region.Exclude(innerPath);` **بعد** إنشاء المنطقة الخارجية، كما هو موضح. |
| **بطء الأداء على الصور الكبيرة** | استخدام `PixelFormat.Format32bppArgb` (غير مسبق الضرب). | التبديل إلى `Format32bppPArgb` للحصول على دمج ألفا أسرع. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing للمشاريع التجارية؟**  
ج: نعم، يمكن استخدام Aspose.Drawing لكل من المشاريع الشخصية والتجارية. للحصول على تفاصيل الترخيص، زر [هنا](https://purchase.aspose.com/buy).

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.Drawing؟**  
ج: زر [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على مساعدة من المجتمع والخبراء.

**س: هل يمكنني إنشاء صور ديناميكية باستخدام Aspose.Drawing؟**  
ج: بالتأكيد. يتيح لك Aspose.Drawing إنشاء وتعديل الصور ديناميكيًا في تطبيقات .NET الخاصة بك.

**س: هل تتوفر تراخيص مؤقتة؟**  
ج: نعم، يمكن الحصول على تراخيص مؤقتة [هنا](https://purchase.aspose.com/temporary-license/).

## الخلاصة

ملء المناطق باستخدام Aspose.Drawing هو تقنية بسيطة لكنها قوية تفتح الباب أمام **إنشاء صور ديناميكية**، إنشاء أشكال مخصصة، وإنتاج رسومات مصقولة برمجيًا. جرّب فرش مختلفة، تدرجات، ومسارات معقدة لاكتشاف الإمكانات الكاملة للمكتبة.

---

**آخر تحديث:** 2026-06-03  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose

## دروس ذات صلة

- [تحديد منطقة القص في Aspose.Drawing – دليل .NET](/drawing/net/rendering/clipping/)
- [كيفية إنشاء bitmap باستخدام Aspose.Drawing – رسم مضلعات في .NET](/drawing/net/lines-curves-and-shapes/draw-polygon/)
- [كيفية رسم مستطيل باستخدام Aspose.Drawing لـ .NET](/drawing/net/lines-curves-and-shapes/draw-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}