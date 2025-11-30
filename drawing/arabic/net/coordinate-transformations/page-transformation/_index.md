---
date: 2025-11-30
description: تعلم كيفية تطبيق تحويل نظام الإحداثيات، ورسم صورة مستطيلة، وتحويل الصفحات
  باستخدام Aspose.Drawing لـ .NET.
language: ar
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: تحويل نظام الإحداثيات (تحويل الصفحة) في Aspose.Drawing لـ .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل نظام الإحداثيات (تحويل الصفحة) في Aspose.Drawing لـ .NET

## المقدمة

مرحبًا! في هذا البرنامج التعليمي ستكتشف **كيفية إجراء تحويل نظام إحداثيات** على صفحة باستخدام Aspose.Drawing لـ .NET. سواء كنت بحاجة إلى **رسم كائنات bitmap مستطيلة**، أو تكبير الرسومات، أو ببساطة ربط وحدات الصفحة بوحدات الجهاز، فإن الخطوات أدناه ستوجهك خلال العملية بالكامل—بوضوح، واختصار، وجاهزة للنسخ‑اللصق في مشروعك.

## إجابات سريعة
- **ما هو الصنف الأساسي للرسم؟** `Graphics` من Aspose.Drawing.
- **كيف أضبط وحدات الصفحة؟** استخدم `graphics.PageUnit = GraphicsUnit.Inch;`.
- **هل يمكنني رسم مستطيل على صفحة محوَّلة؟** نعم—أنشئ `Pen` واستدعِ `DrawRectangle`.
- **أين يتم حفظ الناتج؟** في المجلد الذي تحدده في `bitmap.Save`.
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم وجود ترخيص صالح لـ Aspose.Drawing للاستخدام التجاري.

## ما هو تحويل نظام الإحداثيات؟

**تحويل نظام الإحداثيات** يغيّر الطريقة التي تُطابق بها إحداثيات الصفحة المنطقية (مثل البوصات أو المليمترات) إحداثيات الجهاز الفعلية (البكسلات). من خلال تعديل التحويل، تتحكم في التكبير، والدوران، والإزاحة لجميع عمليات الرسم، مما يجعل من السهل تصميم رسومات لا تعتمد على الدقة.

## لماذا نستخدم Aspose.Drawing لتحويل الصفحات؟

- **توافق كامل مع .NET** – يعمل مع .NET Framework، .NET Core، و .NET 5/6.
- **واجهة برمجة رسومات غنية** – توفر نفس وظائف System.Drawing.Common دون قيود على المنصات.
- **معالجة بسيطة للوحدات** – انتقل بين البوصات، المليمترات، النقاط، إلخ، باستخدام خاصية واحدة.
- **إخراج عالي الجودة** – أنشئ PNG، JPEG، BMP، وصيغ أخرى مع تحكم دقيق.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود:

- **مكتبة Aspose.Drawing** – حمّل أحدث نسخة من الموقع الرسمي [هنا](https://releases.aspose.com/drawing/net/).
- **بيئة تطوير** – Visual Studio (أي نسخة) أو أي بيئة تطوير .NET أخرى.
- **صلاحية كتابة** – مجلد على جهازك حيث سيتم حفظ الصورة المحوَّلة (استبدل `"Your Document Directory"` في الشيفرة بالمسار الفعلي).

الآن بعد أن أصبح كل شيء جاهز، دعنا نتبع كل خطوة.

## استيراد المساحات الاسمية

أولًا، استدعِ المساحة الاسمية المطلوبة:

```csharp
using System.Drawing;
```

> *لماذا هذا مهم*: `System.Drawing` يحتوي على `Bitmap`، `Graphics`، `Pen`، وهياكل اللون التي سنستخدمها طوال البرنامج التعليمي.

## الخطوة 1: إنشاء Bitmap

أنشئ لوحة قماش فارغة ستستضيف الرسم المحوَّل. نحدد حجمًا **1000 × 800 بكسل** وتنسيق بكسل يدعم الشفافية.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> هذا الـ bitmap يعمل كسطح الرسم. تنسيق البكسل المختار (`Format32bppPArgb`) يضمن جودة عالية مع ألفا مسبق الضرب.

## الخطوة 2: إنشاء كائن Graphics

كائن `Graphics` يوفر طرق الرسم (خطوط، أشكال، نص). نحصل عليه من الـ bitmap الذي أنشأناه للتو.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> كائن `Graphics` هو جوهر جميع عمليات العرض؛ سيتبع إعدادات التحويل التي سنطبقها لاحقًا.

## الخطوة 3: مسح اللوحة

قبل رسم أي شيء، امسح اللوحة إلى لون خلفية محايد (رمادي في هذا المثال). تُظهر هذه الخطوة أيضًا كيفية ملء الـ bitmap بالكامل بلون صلب.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## الخطوة 4: ضبط التحويل (تطبيق تحويل الصفحة)

هنا **نطبق تحويل الصفحة** عن طريق ضبط `PageUnit` إلى البوصات. هذا يخبر محرك الرسومات أن يفسر جميع الإحداثيات اللاحقة كبوصات بدلاً من بكسلات.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *نصيحة*: تغيير `PageUnit` طريقة بسيطة لـ **كيفية تحويل إحداثيات الصفحة** دون الحاجة لحساب قيم البكسل يدويًا.

## الخطوة 5: رسم مستطيل (draw rectangle bitmap)

الآن نرسم مستطيلًا بأبعاد **1 بوصة × 1 بوصة** في الموضع (1, 1) بوصة. يتم ضبط عرض `Pen` إلى `0.1f` بوصة، مما يعطي خطًا رفيعًا لكنه مرئي.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> هذا يوضح **draw rectangle bitmap** بعد تطبيق التحويل—لاحظ أن حجم المستطيل معرف بالبوصات، وليس بالبكسلات.

## الخطوة 6: حفظ الصورة

أخيرًا، احفظ الـ bitmap المحوَّل على القرص. استبدل `"Your Document Directory"` بالمسار الفعلي للمجلد على جهازك.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> ملف الإخراج (`PageTransformation_out.png`) سيحتوي على المستطيل المرسوم باستخدام تحويل نظام الإحداثيات الذي ضبطناه مسبقًا.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|--------|-------|------|
| **الصورة تظهر فارغة** | لم يتم مسح اللوحة أو تم الرسم خارج المنطقة المرئية. | تحقق من `graphics.PageUnit` وقيم الإحداثيات؛ تأكد من أن المستطيل يقع داخل حدود الـ bitmap. |
| **التكبير غير صحيح** | استخدام `GraphicsUnit` غير المناسب. | أعد التحقق من أن `graphics.PageUnit` يطابق الوحدة التي تريدها (مثل `GraphicsUnit.Inch`). |
| **أخطاء مسار الملف** | المجلد غير موجود أو يحتوي على أحرف غير صالحة. | أنشئ المجلد المستهدف مسبقًا أو استخدم `Path.Combine` لبناء المسار بأمان. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.Drawing مجانًا؟**  
ج: Aspose.Drawing يقدم نسخة تجريبية مجانية يمكنك الوصول إليها [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.Drawing؟**  
ج: الوثائق متاحة [هنا](https://reference.aspose.com/drawing/net/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.Drawing؟**  
ج: للحصول على الدعم، زر [منتدى Aspose.Drawing](https://forum.aspose.com/c/diagram/17).

**س: هل توجد رخصة مؤقتة لـ Aspose.Drawing؟**  
ج: نعم، يمكنك الحصول على رخصة مؤقتة [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني شراء Aspose.Drawing؟**  
ج: يمكنك شراء Aspose.Drawing [هنا](https://purchase.aspose.com/buy).

## الخلاصة

لقد تعلمت الآن **كيفية تطبيق تحويل نظام إحداثيات**، **رسم كائنات draw rectangle bitmap**، و**حفظ النتيجة** باستخدام Aspose.Drawing لـ .NET. هذه اللبنات الأساسية تتيح لك إنشاء رسومات لا تعتمد على الدقة، مثالية للتقارير، وعناصر واجهة المستخدم، أو أي سيناريو يتطلب تحكمًا دقيقًا في الأحجام. جرّب قيم `GraphicsUnit` أخرى (مثل `Millimeter` أو `Point`) لترى كيف تؤثر على رسوماتك.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-11-30  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose