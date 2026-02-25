---
date: 2026-02-25
description: تعلم كيفية رسم النص وإنشاء صور نصية ديناميكية باستخدام Aspose.Drawing
  لـ .NET. يوضح لك هذا الدليل خطوة بخطوة كيفية إضافة النص إلى صورة bitmap، ورسم سلسلة
  نصية على الصورة، وحفظ الـ bitmap كملف PNG.
linktitle: How to Draw Text with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية رسم النص باستخدام Aspose.Drawing لـ .NET
url: /ar/net/text-and-fonts/draw-text/
weight: 10
---

 keep code block placeholders unchanged.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم النص باستخدام Aspose.Drawing لـ .NET

## المقدمة

في هذا الدليل خطوة بخطوة ستتعلم **كيفية رسم النص** على الصور باستخدام Aspose.Drawing لـ .NET. سواء كنت بحاجة إلى إنشاء *صورة نصية ديناميكية*، أو إضافة نص إلى صورة bitmap موجودة، أو توليد رسم بياني بخطوط مخصصة، فإن هذا البرنامج التعليمي يشرح لك كل التفاصيل حتى تتمكن من بدء رسم النص في دقائق.

## إجابات سريعة
- **ما المكتبة المستخدمة؟** Aspose.Drawing لـ .NET  
- **المهمة الأساسية؟** رسم النص على صورة (إنشاء صورة بالنص)  
- **الطريقة الرئيسية؟** `Graphics.DrawString` (رسم سلسلة على الصورة)  
- **صيغة الإخراج؟** PNG (حفظ bitmap كملف PNG)  
- **المتطلبات المسبقة؟** بيئة تطوير .NET ومكتبة Aspose.Drawing  

## ما هو رسم النص باستخدام Aspose.Drawing؟
توفر Aspose.Drawing واجهة برمجة تطبيقات مُدارة بالكامل تحاكي نموذج GDI+ الكلاسيكي مع إضافة دعم متعدد المنصات. تتيح لك عرض نصوص، أشكال، وصور عالية الجودة دون الاعتماد على System.Drawing.Common.

## لماذا تستخدم Aspose.Drawing لإضافة نص إلى الصور؟
- **موثوقية عبر المنصات** – تعمل على Windows وLinux وmacOS.  
- **عرض متقدم** – مضاد التعرج وتنعيم النص على مستوى البكسل الفرعي للحصول على مخرجات حادة.  
- **بدون تبعيات خارجية** – المكتبة تشمل كل ما تحتاجه *لإنشاء صورة بالنص*.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- **Aspose.Drawing لـ .NET** – حمّله من [توثيق Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **بيئة تطوير .NET** مثل Visual Studio أو VS Code.  

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء المطلوبة:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## الخطوة 1: إنشاء كائنات Bitmap و Graphics

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

هنا نقوم بإنشاء `Bitmap` سيحمل الصورة النهائية و`Graphics` التي تسمح لنا بالرسم عليها. تضمن إشارة مضاد التعرج أن النص يبدو ناعماً.

## الخطوة 2: إعداد Brush و Pen و Font

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** يحدد لون النص.  
- **Pen** يُستخدم لاحقاً لرسم مستطيل حول النص (اختياري).  
- **Font** يحدد نوع الخط، الحجم، والنمط لعملية *رسم السلسلة على الصورة*.

## الخطوة 3: تعريف النص والمستطيل

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

يحدد `Rectangle` مكان وضع النص. عدّل الإحداثيات والحجم لتتناسب مع تخطيطك.

## الخطوة 4: رسم المستطيل والنص

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

أولاً نحدّد المنطقة بمستطيل أزرق، ثم **نضيف النص إلى bitmap** عبر استدعاء `DrawString`. هذا هو جوهر *رسم النص* على الصورة.

## الخطوة 5: حفظ النتيجة

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

يتم حفظ الصورة كملف PNG، مُلبياً متطلب *حفظ bitmap كملف PNG*. استبدل مسار العنصر النائب بالمسار الفعلي للمجلد الذي تريد تخزين الملف فيه.

## حالات الاستخدام الشائعة

- **إنشاء شهادات** بأسماء مخصصة.  
- **إنشاء صور مصغرة مائية** لمعارض الويب.  
- **بناء مخططات ديناميكية** تشمل تسميات أو تعليقات توضيحية.  

## استكشاف الأخطاء وإصلاحها والنصائح

- **الخط غير موجود؟** تأكد من تثبيت الخط على الجهاز المضيف أو استخدم مجموعة خطوط خاصة.  
- **النص مقطوع؟** زد حجم المستطيل أو قلل حجم الخط.  
- **مخاوف الأداء؟** أعد استخدام كائن `Graphics` نفسه لعمليات رسم متعددة عندما يكون ذلك ممكنًا.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام خطوط مخصصة مع Aspose.Drawing لـ .NET؟

ج1: نعم، يمكنك تحديد خطوط مخصصة عند إنشاء كائن `Font` في الشيفرة الخاصة بك.

### س2: كيف يمكنني إضافة تأثيرات نصية مثل الغامق أو المائل؟

ج2: عدّل خاصية `FontStyle` لكائن `Font`. على سبيل المثال، استخدم `FontStyle.Bold` للنص الغامق.

### س3: هل Aspose.Drawing متوافق مع .NET Core؟

ج3: نعم، يدعم Aspose.Drawing .NET Core، مما يتيح لك استخدامه في تطبيقات متعددة المنصات.

### س4: هل يمكنني رسم نص على صورة موجودة؟

ج4: بالتأكيد! حمّل الصورة الموجودة باستخدام `Bitmap.FromFile()` ثم تابع خطوات رسم النص.

### س5: هل هناك منتدى مجتمع لدعم Aspose.Drawing؟

ج5: نعم، يمكنك العثور على الدعم ومناقشة القضايا في [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

## أسئلة شائعة

**س: كيف أغيّر صيغة الإخراج إلى JPEG؟**  
ج: استبدل امتداد `.png` بـ `.jpg` في طريقة `Save` ويمكنك اختيار `ImageCodecInfo` لتحديد جودة JPEG.

**س: هل يمكنني رسم نص متعدد الأسطر؟**  
ج: نعم، أدرج أحرف السطر الجديد (`\n`) في السلسلة أو استخدم `StringFormat` مع `FormatFlags.LineLimit`.

**س: هل هناك طريقة لقياس حجم النص قبل الرسم؟**  
ج: استخدم `Graphics.MeasureString` للحصول على الأبعاد الدقيقة للنص المرسوم.

**س: هل يدعم Aspose.Drawing الأحرف Unicode؟**  
ج: بالتأكيد. قدم خطًا يحتوي على الحروف المطلوبة وستقوم المكتبة بعرضها بشكل صحيح.

**س: أي نسخة من Aspose.Drawing تم استخدامها للاختبار؟**  
ج: تم اختبار الأمثلة باستخدام Aspose.Drawing 24.11 لـ .NET.

---

**آخر تحديث:** 2026-02-25  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}