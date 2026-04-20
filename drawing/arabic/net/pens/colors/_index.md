---
date: 2026-02-22
description: تعلم كيفية تعيين لون القلم في Aspose.Drawing لـ .NET، ورسم خطوط ملونة،
  وحفظ صور PNG باستخدام أمثلة شفرة بسيطة.
linktitle: Working with Colors in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية تعيين لون القلم في Aspose.Drawing لـ .NET
url: /ar/net/pens/colors/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعيين لون القلم في Aspose.Drawing

## المقدمة

مرحبًا بكم في دليلنا خطوة بخطوة حول كيفية **تعيين لون القلم** عند الرسم باستخدام Aspose.Drawing لـ .NET. في هذا البرنامج التعليمي ستتعلم إنشاء كائن رسومي، رسم خطوط ملونة، و**حفظ صورة PNG**—كل ذلك بأمثلة شفرة واضحة وعملية. سواء كنت تبني أداة سطح مكتب أو خدمة ويب تُنشئ مخططات، فإن إتقان ألوان الأقلام أمر أساسي لإنتاج رسومات ذات مظهر احترافي.

## إجابات سريعة
- **ما هو الصنف الأساسي للرسم؟** `Graphics` يتم إنشاؤه من `Bitmap`.
- **كيف يمكنني تغيير لون القلم؟** استخدم `Color.FromKnownColor` أو `Color.FromArgb`.
- **ما هو التنسيق الموصى به للإخراج بدون فقدان؟** PNG (`.png`).
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت متاح للتقييم.
- **هل يمكنني استخدامه في ASP.NET Core؟** نعم، Aspose.Drawing يعمل مع .NET Core و .NET 5+.

## ما هو “تعيين لون القلم” في Aspose.Drawing؟

تعيين لون القلم يعني إعطاء قيمة `Color` لكائن `Pen` قبل الرسم. يحدد اللون كيفية ظهور الخطوط أو الأشكال أو النص على القماش. Aspose.Drawing يعكس واجهة برمجة التطبيقات System.Drawing المألوفة، لذا يمكنك استخدام `Color.FromKnownColor`، `Color.FromArgb`، أو خصائص `Color` المعرفة مسبقًا.

## لماذا نستخدم Aspose.Drawing لتعديل الألوان؟

* **دعم متعدد المنصات** – يعمل على Windows و Linux و macOS دون قيود System.Drawing.Common.  
* **توافق كامل مع .NET** – يندمج بسلاسة مع مشاريع .NET 6 و .NET Core و .NET Framework.  
* **واجهات برمجة ألوان غنية** – إنشاء سهل لألوان ARGB مخصصة، الألوان المعروفة، وفرش التدرج.  
* **إخراج PNG عالي الجودة** – مثالي للرسومات على الويب، التقارير، والصور المصغرة.

## المتطلبات المسبقة

قبل الغوص في الشفرة، تأكد من وجود ما يلي:

1. **مكتبة Aspose.Drawing** – قم بتحميلها وتثبيتها من الموقع الرسمي **[here](https://releases.aspose.com/drawing/net/)**.  
2. **بيئة تطوير .NET** – Visual Studio أو VS Code أو أي بيئة تطوير تفضلها.  
3. **معرفة أساسية بـ C#** – الإلمام بالصفوف (classes)، الكائنات (objects)، والمساحات الاسمية (namespaces).

## استيراد مساحات الأسماء

في ملف C# الخاص بك، استورد مساحة الأسماء التي تمنحك الوصول إلى الكائنات الأساسية للرسم في Aspose.Drawing.

```csharp
using System.Drawing;
```

## الخطوة 1: إنشاء Bitmap (القماش)

`Bitmap` يمثل مخزن البكسلات الذي سنرسم عليه. هنا ننشئ قماشًا بحجم 1000 × 800 ببتات بصيغة ARGB 32‑بت.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## الخطوة 2: إنشاء كائن Graphics

كائن `Graphics` هو سطح الرسم الذي يتيح لك رسم الأشكال والنصوص والصور على الـ bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 3: رسم خط بقلم أزرق (أول خط ملون)

نقوم **بتعيين لون القلم** إلى الأزرق باستخدام `Color.FromKnownColor`. يتم ضبط عرض القلم على 2 بكسل.

```csharp
Pen bluePen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawLine(bluePen, 100, 100, 900, 100);
```

## الخطوة 4: رسم خط بقلم أحمر مخصص

يوضح هذا المثال كيفية **رسم خطوط ملونة** باستخدام قيمة ARGB مخصصة، مما يمنحك تحكمًا كاملًا في الشفافية والدرجة الدقيقة للون.

```csharp
Pen redPen = new Pen(Color.FromArgb(255, 255, 0, 0), 2);
graphics.DrawLine(redPen, 100, 200, 900, 200);
```

## الخطوة 5: حفظ الصورة كـ PNG

أخيرًا، نقوم **بحفظ صورة PNG** إلى المجلد المطلوب. عدل المسار ليتطابق مع دليل إخراج مشروعك.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Colors_out.png");
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **الصورة تظهر فارغة** | لم يتم تفريغ الـ Graphics قبل الحفظ | استدعِ `graphics.Dispose();` أو ضع الـ `Graphics` داخل كتلة `using`. |
| **ألوان غير صحيحة** | استخدام `FromKnownColor` مع تعداد (enum) غير صحيح | تحقق من قيمة التعداد أو استخدم `FromArgb` للتحكم الدقيق. |
| **أخطاء مسار الملف** | دليل غير صالح أو أذونات مفقودة | تأكد من وجود المجلد المستهدف وأن التطبيق لديه صلاحية الكتابة. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing مع مكتبات .NET أخرى؟**  
ج: نعم، Aspose.Drawing يندمج بسلاسة مع مكتبات .NET الأخرى، موفرًا بيئة متعددة الاستخدامات لتعديل الرسومات.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Drawing؟**  
ج: يمكنك الحصول على ترخيص مؤقت **[here](https://purchase.aspose.com/temporary-license/)**، مما يتيح لك استكشاف كامل إمكانيات Aspose.Drawing.

**س: هل يدعم Aspose.Drawing صيغ صور غير PNG؟**  
ج: نعم، Aspose.Drawing يدعم صيغ صور متعددة بما فيها JPEG و GIF و BMP وغيرها. راجع الوثائق للقائمة الكاملة.

**س: هل يمكنني استخدام Aspose.Drawing لتطوير الويب؟**  
ج: بالتأكيد! Aspose.Drawing متعدد الاستخدامات ويمكن استعماله في تطبيقات سطح المكتب والويب على حد سواء، مضيفًا ميزات رسومية ديناميكية إلى مواقعك.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Drawing؟**  
ج: نعم، يمكنك تجربة نسخة تجريبية مجانية **[here](https://releases.aspose.com/drawing/net/)**، لتجربة قدرات Aspose.Drawing قبل الشراء.

## الخاتمة

في هذا البرنامج التعليمي غطينا كيفية **تعيين لون القلم**، **رسم خطوط ملونة**، **إنشاء كائن رسومي**، و**حفظ النتيجة كـ PNG** باستخدام Aspose.Drawing لـ .NET. هذه الأساسيات تفتح الباب أمام سيناريوهات أكثر تقدمًا مثل رسم الأشكال، عرض النص، وتوليد المخططات ديناميكيًا. إذا واجهت أي صعوبات، فإن **[الوثائق](https://reference.aspose.com/drawing/net/)** و**[منتدى الدعم](https://forum.aspose.com/c/drawing/44)** لـ Aspose.Drawing هما مكانان ممتازان للعثور على الإجابات.

---

**آخر تحديث:** 2026-02-22  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}