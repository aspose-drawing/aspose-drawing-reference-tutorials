---
date: 2026-02-17
description: تعلم كيفية ملء المنطقة باستخدام Aspose.Drawing لـ .NET، وإنشاء صور ديناميكية،
  وإنشاء منطقة من مضلع عبر كود خطوة‑بخطوة.
linktitle: How to Fill Region in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية ملء المنطقة في Aspose.Drawing لـ .NET
url: /ar/net/lines-curves-and-shapes/fill-region/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية ملء المنطقة في Aspose.Drawing

إنشاء رسومات جذابة بصريًا غالبًا ما يتضمن **كيفية ملء المنطقة** بالألوان أو الأنماط أو التدرجات. توفر لك Aspose.Drawing لـ .NET واجهة برمجة تطبيقات نظيفة وعالية الأداء للتعامل مع هذه المهمة، سواءً كنت تبني محرك تقارير، أداة تصميم، أو تولد صورًا ديناميكية في الوقت الفعلي. في هذا الدرس ستتعرف على **كيفية ملء المنطقة** خطوة بخطوة، من إعداد الـ bitmap إلى حفظ الصورة النهائية.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع ملء المنطقة؟** Aspose.Drawing لـ .NET  
- **الطريقة الأساسية؟** `Graphics.FillRegion` مع `Brush` و `Region`  
- **هل يمكنني توليد صور ديناميكية؟** نعم – نفس الواجهة تسمح بإنشاء الصور أثناء التشغيل  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية  
- **الإصدارات المدعومة من .NET؟** .NET Framework 4.6+، .NET Core 3.1+، .NET 5/6+

## ما معنى “ملء المنطقة” في برمجة الرسومات؟
ملء المنطقة يعني رسم كل بكسل ينتمي إلى شكل محدد (مضلع، إهليلج، مسار مخصص) باستخدام فرشاة. يمكن أن تكون الفرشاة لونًا صلبًا، تدرجًا لونيًا، أو حتى نسيجًا، مما يمنحك تحكمًا كاملاً في المظهر البصري للمنطقة.

## لماذا نستخدم Aspose.Drawing لملء المنطقة؟
- **سلوك متسق** عبر .NET Framework و .NET Core و .NET 5/6 – بدون اختلافات منصة.  
- **أنبوب معالجة محسّن للأداء**، مثالي لتوليد الصور على الخادم.  
- **واجهة برمجة تطبيقات غنية** تدعم المسارات المعقدة، استبعاد الأشكال الداخلية، والفرش المتقدمة.  
- **بدون تبعيات خارجية** – لا تحتاج إلى GDI+ على الخادم، مما يبسط عملية النشر.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

1. **مكتبة Aspose.Drawing** – قم بتحميل وتثبيت أحدث نسخة من الموقع الرسمي. يمكنك العثور على المكتبة ووثائقها [هنا](https://reference.aspose.com/drawing/net/).  
2. **بيئة التطوير** – Visual Studio (أي نسخة) أو أي IDE مفضل لـ .NET.  
3. **مشروع .NET** يستهدف .NET Framework 4.6+ أو .NET Core 3.1+.

## استيراد المساحات الاسمية

ابدأ باستيراد المساحات الاسمية التي تحتوي على فئات الرسومات التي سنستخدمها.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

الآن دعنا نستعرض المثال الكامل، مقسِّمًا إياه إلى خطوات سهلة المتابعة.

## دليل خطوة بخطوة

### الخطوة 1: إنشاء Bitmap وكائن Graphics
نقوم أولاً بإنشاء bitmap سيعمل كقماشة الرسم ثم الحصول على كائن `Graphics` للرسم عليه.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

> **نصيحة احترافية:** استخدام `Format32bppPArgb` يمنحك ألفا مضاعفة مسبقًا، ما ينتج عنه دمج أكثر سلاسة عند تطبيق فرشاة شبه شفافة لاحقًا.

### الخطوة 2: تعريف GraphicsPath وإنشاء Region
تتيح لنا `GraphicsPath` وصف أشكال معقدة. هنا نضيف مضلعًا يشبه الشكل الماسي.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

> هذا هو **المنطقة من المضلع** التي كنت تبحث عنها. الآن يمثل كائن `Region` داخل ذلك المضلع.

### الخطوة 3: استبعاد منطقة داخلية
غالبًا ما تحتاج إلى “ثقب” داخل الشكل. نقوم بإنشاء مستطيل ونستبعده من المنطقة الرئيسية.

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

### الخطوة 4: اختيار فرشاة وملء المنطقة
اختر أي فرشاة تريدها. في هذا المثال نستخدم فرشاة صلبة زرقاء، لكن يمكنك استبدالها بـ `LinearGradientBrush` أو `TextureBrush` لتوليد صور ديناميكية ذات مظهر أغنى.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

### الخطوة 5: حفظ الصورة الناتجة
أخيرًا، اكتب الـ bitmap إلى القرص. عدل المسار ليتطابق مع مجلد موجود على جهازك.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|-------|-----|
| **الصورة تظهر فارغة** | عدم حفظ الـ bitmap في مجلد قابل للكتابة أو عدم تفريغ `Graphics`. | تأكد من وجود المجلد واستدعِ `graphics.Dispose()` بعد الرسم. |
| **المنطقة لا تستبعد الشكل الداخلي** | استخدام `Exclude` قبل تعريف المنطقة بالكامل. | استدعِ `region.Exclude(innerPath);` **بعد** إنشاء المنطقة الخارجية، كما هو موضح. |
| **بطء الأداء مع صور كبيرة** | استخدام `PixelFormat.Format32bppArgb` (غير مضاعف مسبقًا). | التحول إلى `Format32bppPArgb` لتسريع دمج الألفا. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing في المشاريع التجارية؟**  
ج: نعم، يمكن استخدام Aspose.Drawing في المشاريع الشخصية والتجارية. للحصول على تفاصيل الترخيص، زر [هنا](https://purchase.aspose.com/buy).

**س: هل تتوفر نسخة تجريبية مجانية؟**  
ج: نعم، يمكنك الحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.Drawing؟**  
ج: زر منتدى [Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على مساعدة من المجتمع والخبراء.

**س: هل يمكنني توليد صور ديناميكية باستخدام Aspose.Drawing؟**  
ج: بالتأكيد. يتيح لك Aspose.Drawing إنشاء وتعديل الصور ديناميكيًا في تطبيقات .NET الخاصة بك.

**س: هل تتوفر تراخيص مؤقتة؟**  
ج: نعم، يمكن الحصول على تراخيص مؤقتة [هنا](https://purchase.aspose.com/temporary-license/).

## الخلاصة

ملء المناطق باستخدام Aspose.Drawing تقنية بسيطة لكنها قوية تفتح لك باب **توليد صور ديناميكية**، إنشاء أشكال مخصصة، وإنتاج رسومات مصقولة برمجيًا. جرّب فرش مختلفة، تدرجات، ومسارات معقدة لاكتشاف الإمكانات الكاملة للمكتبة.

---

**آخر تحديث:** 2026-02-17  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}