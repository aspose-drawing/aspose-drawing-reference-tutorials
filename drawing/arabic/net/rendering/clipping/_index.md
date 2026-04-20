---
date: 2026-02-22
description: تعرّف على كيفية تعيين منطقة القص، وكيفية قص الصورة، وحفظ الصورة المقصوصة،
  وتطبيق عرض نص مخصص باستخدام Aspose.Drawing لـ .NET في دليل خطوة بخطوة.
linktitle: Set Clipping Region in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: تعيين منطقة القص في Aspose.Drawing – دليل .NET
url: /ar/net/rendering/clipping/
weight: 12
---

. Ensure no extra explanation.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين منطقة القص في Aspose.Drawing

## مقدمة

عند الحاجة إلى **تعيين منطقة القص** لإخفاء أو إظهار أجزاء محددة من صورة، يجعل Aspose.Drawing لـ .NET العملية بسيطة وفعّالة. في هذا الدليل سنستعرض **كيفية قص صورة**، تطبيق **عرض نص مخصص**، وأخيرًا **حفظ ملفات الصورة المقصوصة**—كل ذلك باستخدام كود واضح وجاهز للإنتاج. في النهاية ستفهم لماذا يعتبر القص أداة حيوية في التصميم الجرافيكي وكيفية دمجه في مشاريع .NET الخاصة بك.

## إجابات سريعة
- **ماذا يفعل “set clipping region”؟** يحد من عمليات الرسم إلى شكل محدد، ويخفي كل ما هو خارج ذلك الشكل.  
- **أي مساحة اسمية توفر دعم القص؟** `System.Drawing.Drawing2D` (عبر `GraphicsPath`).  
- **هل يمكن قص أشكال متعددة؟** نعم – استدعِ `SetClip` بشكل متكرر مع مسارات مختلفة.  
- **كيف أحفظ الصورة المقصوصة؟** استخدم `Bitmap.Save` بعد الرسم داخل المنطقة المقصوصة.  
- **هل يمكن عرض نص مخصص داخل القص؟** بالتأكيد – اجمع `StringFormat` مع منطقة القص.

## ما هو “set clipping region”؟
تعيين منطقة القص يخبر محرك الرسومات بتقييد جميع أوامر الرسم اللاحقة إلى داخل شكل (مستطيل، إهليلج، مضلع، إلخ). أي شيء يُرسم خارج ذلك الشكل يُهمل، مما يتيح تأثيرات بصرية دقيقة دون الحاجة إلى قص البكسلات يدويًا.

## لماذا نستخدم القص مع Aspose.Drawing؟
- **الأداء:** يتم التعامل مع القص أصلاً في المكتبة، مما يجنب عمليات البكسل المكلفة.  
- **المرونة:** يمكن دمج أي `GraphicsPath` (إهليلج، مستطيل مستدير، مضلع مخصص) مع نصوص، صور أو أشكال.  
- **متعدد المنصات:** يعمل بنفس الطريقة على .NET Framework، .NET Core، و .NET 5/6+.  
- **مركز على التصميم:** مثالي لإنشاء الشارات، العلامات المائية، أو مناطق التركيز في رسومات واجهة المستخدم.

## المتطلبات المسبقة
- معرفة أساسية بـ C# وتطوير .NET.  
- تم تثبيت Aspose.Drawing لـ .NET (حزمة NuGet `Aspose.Drawing`).  
- Visual Studio أو أي بيئة تطوير متوافقة مع C#.  
- فهم أساسيات مفاهيم التصميم الجرافيكي (الطبقات، الشفافية، إلخ).

## استيراد المساحات الاسمية
أضف المساحات الاسمية المطلوبة حتى يتمكن المترجم من العثور على فئات القص والرسم.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
using System.Drawing.Text;
```

## دليل خطوة بخطوة

### الخطوة 1: إنشاء Bitmap (اللوحة)
نبدأ بإنشاء bitmap فارغ سيحتوي على الصورة النهائية.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### الخطوة 2: إنشاء سياق Graphics
كائن `Graphics` يتيح لنا الرسم على الـ bitmap. كما نقوم بتمكين عرض النص بجودة عالية.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
```

### الخطوة 3: تعريف منطقة القص
هنا **نحدد منطقة القص** بإنشاء إهليلج داخل مستطيل. يوضح هذا **كيفية تعيين القص** ويظهر مثالًا كلاسيكيًا على **قص صورة إهليلجية**.

```csharp
Rectangle rectangle = new Rectangle(200, 200, 600, 400);
GraphicsPath clipPath = new GraphicsPath();
clipPath.AddEllipse(rectangle);
graphics.SetClip(clipPath);
```

### الخطوة 4: تطبيق عرض نص مخصص
نقوم بتكوين `StringFormat` لتوسيط النص أفقيًا وعموديًا—مثال على **دمج النص مع القص** داخل المنطقة المقصوصة.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;
stringFormat.LineAlignment = StringAlignment.Center;
```

### الخطوة 5: رسم النص على المنطقة المقصوصة
الآن يُرسم النص فقط داخل الإهليلج المحدد مسبقًا. أي شيء خارج الإهليلج يُهمل تلقائيًا.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.White));
Font arial = new Font("Arial", 20, FontStyle.Regular);
string text = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. ..."; // (Text truncated for brevity)
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### الخطوة 6: حفظ النتيجة (حفظ الصورة المقصوصة)
أخيرًا، نقوم بحفظ الـ bitmap على القرص. هذه هي خطوة **حفظ الصورة المقصوصة**.

```csharp
bitmap.Save("Your Document Directory" + @"Rendering\Clipping_out.png");
```

## المشكلات الشائعة والنصائح
- **لم يتم تطبيق القص؟** تأكد من استدعاء `SetClip` **قبل** أي أوامر رسم.  
- **ألوان غير متوقعة؟** تحقق من تنسيق بكسل الـ bitmap (`Format32bppPArgb` يعمل جيدًا للشفافية).  
- **قلق بشأن الأداء:** أعد استخدام نفس `GraphicsPath` إذا كنت بحاجة إلى قص عدة مرات داخل حلقة.  
- **نصيحة احترافية:** دمج عدة كائنات `GraphicsPath` باستخدام `AddPath` لإنشاء قصوص مركبة معقدة.

## حالات الاستخدام الشائعة
- **إنشاء شارة أو شعار:** قص الشعار داخل شارة دائرية أو ذات شكل مخصص.  
- **علامات مائية ديناميكية:** عرض نص العلامة المائية فقط داخل منطقة محددة، مع ترك باقي الصورة دون تعديل.  
- **عناصر واجهة مستخدم تفاعلية:** إبراز جزء من لقطة شاشة للواجهة عن طريق قص طبقة نصف شفافة.

## استكشاف الأخطاء وإصلاحها والمخاطر
| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| لا يوجد نص مرئي داخل الشكل البيضاوي | تم تطبيق القص بعد الرسم | انقل `SetClip` قبل أي استدعاءات `DrawString` |
| الخلفية الشفافة تتحول إلى سوداء | تنسيق بكسل غير صحيح | استخدم `Format32bppPArgb` لمعالجة ألفا بشكل صحيح |
| بطء العرض على الصور الكبيرة | إعادة إنشاء `GraphicsPath` في كل إطار | احفظ المسار في الذاكرة وأعد استخدامه |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق مناطق قص متعددة في صورة واحدة؟**  
ج: نعم. استدعِ `graphics.SetClip` بمسار جديد؛ يتم استبدال القص السابق ما لم تستخدم `CombineMode.Intersect`.

**س: هل يدعم Aspose.Drawing تنسيقات بكسل أخرى للـ Bitmaps؟**  
ج: بالتأكيد. تدعم المكتبة تنسيقات مثل `Format24bppRgb`، `Format32bppArgb`، و `Format8bppIndexed`.

**س: هل يمكنني تغيير منطقة القص أثناء التشغيل؟**  
ج: يمكنك تعديل المنطقة في أي وقت بإنشاء `GraphicsPath` جديد واستدعاء `SetClip` مرة أخرى.

**س: هل Aspose.Drawing مناسب لتطبيقات .NET المستندة إلى الويب؟**  
ج: نعم. يعمل في ASP.NET Core، Azure Functions، وغيرها من بيئات الخادم.

**س: ما هو تأثير الأداء للقص؟**  
ج: القص خفيف الوزن؛ يستخدم Aspose.Drawing تحسينات GDI+ الأصلية، لذا فإن العبء إضافي قليل بالنسبة لأحجام الصور المعتادة.

## الخلاصة
لقد أتقنت الآن كيفية **تعيين منطقة القص**، **قص محتوى الصورة**، تطبيق **عرض نص مخصص**، و**حفظ ملفات الصورة المقصوصة** باستخدام Aspose.Drawing لـ .NET. تمنحك هذه التقنيات تحكمًا دقيقًا في مخرجات الرسومات، مما يتيح تأثيرات بصرية متطورة ببضع أسطر من الكود فقط. استكشف المزيد بدمج القص مع التدرجات، الأنماط، أو مدخلات المستخدم الديناميكية لإنشاء رسومات تفاعلية حقًا.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-22  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose