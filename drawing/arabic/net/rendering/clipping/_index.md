---
date: 2025-12-05
description: تعرّف على كيفية تعيين منطقة القص، وكيفية قص الصورة، وحفظ الصورة المقصوصة،
  وتطبيق عرض نص مخصص باستخدام Aspose.Drawing لـ .NET في دليل خطوة بخطوة.
language: ar
linktitle: Set Clipping Region in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: تعيين منطقة القص في Aspose.Drawing – دليل .NET
url: /net/rendering/clipping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين منطقة القص في Aspose.Drawing

## المقدمة

عندما تحتاج إلى **تعيين منطقة القص** لإخفاء أو إظهار أجزاء محددة من الصورة، يجعل Aspose.Drawing لـ .NET العملية بسيطة وعالية الأداء. في هذا الدليل سنستعرض **كيفية قص الصورة**، وتطبيق **تصيير نص مخصص**، وأخيرًا **حفظ الصورة المقصوصة**—كل ذلك باستخدام كود واضح جاهز للإنتاج. في النهاية ستفهم لماذا يعتبر القص أداة أساسية في تصميم الرسومات وكيفية دمجه في مشاريع .NET الخاصة بك.

## إجابات سريعة
- **ماذا يفعل “تعيين منطقة القص”؟** يحد من عمليات الرسم إلى شكل محدد، مخفيًا كل ما هو خارج ذلك الشكل.  
- **أي مساحة اسمية توفر دعم القص؟** `System.Drawing.Drawing2D` (عبر `GraphicsPath`).  
- **هل يمكن قص أشكال متعددة؟** نعم – استدعِ `SetClip` بشكل متكرر مع مسارات مختلفة.  
- **كيف أحفظ الصورة المقصوصة؟** استخدم `Bitmap.Save` بعد الرسم داخل المنطقة المقصوصة.  
- **هل تصيير النص المخصص ممكن داخل القص؟** بالتأكيد – اجمع `StringFormat` مع منطقة القص.

## ما هو “تعيين منطقة القص”؟
إن تعيين منطقة القص يخبر محرك الرسومات بتقييد جميع أوامر الرسم اللاحقة إلى داخل شكل (مستطيل، إهليلج، مضلع، إلخ). أي شيء يُرسم خارج ذلك الشكل يتم تجاهله، مما يتيح تأثيرات بصرية دقيقة دون الحاجة إلى قص البكسلات يدويًا.

## لماذا نستخدم القص مع Aspose.Drawing؟
- **الأداء:** يتم التعامل مع القص أصلاً في المكتبة، متجنبًا عمليات البكسل المكلفة.  
- **المرونة:** يمكنك دمج أي `GraphicsPath` (إهليلج، مستطيل مستدير، مضلع مخصص) مع النصوص أو الصور أو الأشكال.  
- **متعدد المنصات:** يعمل بنفس الطريقة على .NET Framework، .NET Core، و .NET 5/6+.  
- **مركزية التصميم:** مثالي لإنشاء الشارات، العلامات المائية، أو مناطق التركيز في رسومات واجهة المستخدم.

## المتطلبات المسبقة
- معرفة أساسية بـ C# وتطوير .NET.  
- تثبيت Aspose.Drawing لـ .NET (حزمة NuGet `Aspose.Drawing`).  
- Visual Studio أو أي بيئة تطوير متوافقة مع C#.  
- فهم مفاهيم التصميم الجرافيكي الأساسية (الطبقات، الشفافية، إلخ).

## استيراد المساحات الاسمية
أضف المساحات الاسمية المطلوبة حتى يتمكن المترجم من العثور على فئات القص والرسم.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
using System.Drawing.Text;
```

## دليل خطوة بخطوة

### الخطوة 1: إنشاء Bitmap (اللوحة)
نبدأ بإنشاء bitmap فارغ سيحمل الصورة النهائية.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### الخطوة 2: إنشاء سياق Graphics
كائن `Graphics` يتيح لنا الرسم على الـ bitmap. كما نقوم بتمكين تصيير نص عالي الجودة.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
```

### الخطوة 3: تعريف منطقة القص
هنا **نقوم بتعيين منطقة القص** بإنشاء إهليلج داخل مستطيل. يوضح هذا **كيفية قص الصورة** إلى شكل غير مستطيل.

```csharp
Rectangle rectangle = new Rectangle(200, 200, 600, 400);
GraphicsPath clipPath = new GraphicsPath();
clipPath.AddEllipse(rectangle);
graphics.SetClip(clipPath);
```

### الخطوة 4: تطبيق تصيير نص مخصص
نقوم بتهيئة `StringFormat` لتوسيط النص أفقيًا وعموديًا—مثال على **تصيير نص مخصص** داخل المنطقة المقصوصة.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;
stringFormat.LineAlignment = StringAlignment.Center;
```

### الخطوة 5: رسم النص على منطقة القص
الآن يُرسم النص فقط داخل الإهليلج المحدد مسبقًا. أي شيء خارج الإهليلج يتم تجاهله تلقائيًا.

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
- **القص غير مطبق؟** تأكد من استدعاء `SetClip` **قبل** أي أوامر رسم.  
- **ألوان غير متوقعة؟** تحقق من تنسيق بكسل الـ bitmap (`Format32bppPArgb` يعمل جيدًا للشفافية).  
- **مخاوف الأداء:** أعد استخدام نفس `GraphicsPath` إذا احتجت إلى قص متعدد داخل حلقة.  
- **نصيحة احترافية:** دمج عدة كائنات `GraphicsPath` باستخدام `AddPath` لإنشاء قصوص مركبة معقدة.

## الأسئلة المتكررة

**س: هل يمكنني تطبيق مناطق قص متعددة في صورة واحدة؟**  
ج: نعم. استدعِ `graphics.SetClip` بمسار جديد؛ يتم استبدال القص السابق ما لم تستخدم `CombineMode.Intersect`.

**س: هل يدعم Aspose.Drawing تنسيقات بكسل أخرى للـ Bitmaps؟**  
ج: بالتأكيد. تنسيقات مثل `Format24bppRgb`، `Format32bppArgb`، و `Format8bppIndexed` كلها مدعومة.

**س: هل يمكنني تغيير منطقة القص أثناء التشغيل؟**  
ج: يمكنك تعديل المنطقة في الوقت الفعلي بإنشاء `GraphicsPath` جديد واستدعاء `SetClip` مرة أخرى.

**س: هل Aspose.Drawing مناسب لتطبيقات .NET المستندة إلى الويب؟**  
ج: نعم. يعمل في ASP.NET Core، Azure Functions، وغيرها من بيئات الخادم.

**س: ما هو تأثير الأداء للقص؟**  
ج: القص خفيف الوزن؛ يستخدم Aspose.Drawing تحسينات GDI+ الأصلية، لذا يكون الحمل الزائد قليلًا بالنسبة لأحجام الصور المعتادة.

## الخلاصة
لقد أتقنت الآن كيفية **تعيين منطقة القص**، **قص محتوى الصورة**، تطبيق **تصيير نص مخصص**، و**حفظ الصورة المقصوصة** باستخدام Aspose.Drawing لـ .NET. تمنحك هذه التقنيات تحكمًا دقيقًا في مخرجات الرسومات، مما يتيح تأثيرات بصرية متقدمة ببضع أسطر من الكود فقط. استكشف المزيد بدمج القص مع التدرجات، الأنماط، أو مدخلات المستخدم الديناميكية لإنشاء رسومات تفاعلية حقًا.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-05  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose  

---