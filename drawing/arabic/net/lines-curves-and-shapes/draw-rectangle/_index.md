---
date: 2026-02-17
description: تعلم كيفية رسم مستطيل في .NET باستخدام Aspose.Drawing. يوضح لك هذا الدليل
  خطوة بخطوة كيفية إنشاء صورة bitmap، ورسم مستطيل على الصورة، وحفظ الصورة المرسومة.
linktitle: Drawing Rectangles in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية رسم مستطيل باستخدام Aspose.Drawing لـ .NET
url: /ar/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

 keep markdown formatting exactly.

Let's craft final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية رسم مستطيل باستخدام Aspose.Drawing لـ .NET

## المقدمة

في هذا الدرس ستكتشف **كيفية رسم مستطيل** في تطبيقات .NET الخاصة بك باستخدام مكتبة Aspose.Drawing. سواء كنت بحاجة إلى إنشاء مستطيل بسيط لعنصر واجهة المستخدم أو إنشاء رسم بياني معقد لتقرير، ستقودك الخطوات أدناه عبر إنشاء صورة bitmap، إعداد كائن graphics، رسم المستطيل على الـ bitmap، وأخيرًا حفظ الصورة المرسومة إلى القرص.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.Drawing for .NET  
- **ما الطريقة التي ترسم الشكل؟** `Graphics.DrawRectangle`  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية مجانية؛ الترخيص التجاري مطلوب للإنتاج.  
- **هل يمكنني تغيير حجم المستطيل؟** نعم – قم بضبط عرض، ارتفاع، ومعلمات الموقع.  
- **هل الكود متوافق مع .NET 6+؟** بالتأكيد، Aspose.Drawing يدعم إصدارات .NET الحديثة.

## ما معنى “كيفية رسم مستطيل” في سياق Aspose.Drawing؟

رسم مستطيل باستخدام Aspose.Drawing يعني استخدام فئة `Graphics` لتصوير حدود مستطيلة (أو شكل مملوء) على لوحة bitmap. يتيح لك هذا النهج التحكم الكامل في الحجم، اللون، سمك الخط، وصيغة الصورة، مما يجعله مثاليًا لإنشاء رسومات في الوقت الفعلي.

## لماذا نستخدم Aspose.Drawing لإنشاء المستطيلات؟

- **دعم متعدد المنصات** – يعمل على Windows وLinux وmacOS.  
- **بدون تبعيات GDI+** – يتجنب قيود `System.Drawing.Common`.  
- **مجموعة ميزات غنية** – رسم متقدم، مضاد للتعرج، وصيغ إخراج عالية الجودة.  
- **ترخيص سهل** – نسخة تجريبية متاحة، مع ترقية سلسة إلى ترخيص تجاري.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من وجود ما يلي:

- مكتبة Aspose.Drawing: تأكد من تثبيت مكتبة Aspose.Drawing لـ .NET. يمكنك تنزيلها [هنا](https://releases.aspose.com/drawing/net/).
- بيئة التطوير: احرص على وجود بيئة تطوير .NET تعمل، مثل Visual Studio، مُثبتة على جهازك.
- معرفة أساسية بـ .NET: تعرّف على أساسيات برمجة .NET.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية إلى مشروعك. هذه المساحات أساسية للعمل مع الرسومات وعمليات الرسم:

```csharp
using System.Drawing;
```

## الخطوة 1: إنشاء صورة Bitmap

أولاً، أنشئ كائن `Bitmap` سيعمل كسطح الرسم. هذه الـ bitmap هي المكان الذي سنقوم فيه **بتوليد محتوى صورة المستطيل**.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## الخطوة 2: إنشاء كائن Graphics

بعد ذلك، احصل على كائن `Graphics` من الـ bitmap. كائن graphics هو المحرك الذي يتيح لك **إنشاء عمليات كائن graphics** مثل رسم الأشكال، الخطوط، والنصوص.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## الخطوة 3: تعريف قلم (Pen) للمستطيل

عرّف كائن `Pen` لتحديد اللون والسماكة لحدود المستطيل.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## الخطوة 4: رسم المستطيل على Bitmap

الآن، استخدم كائن `Graphics` **لرسم المستطيل على bitmap**. اضبط قيم X، Y، العرض، والارتفاع لتناسب تصميمك.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## الخطوة 5: حفظ الصورة المرسومة

أخيرًا، اكتب الـ bitmap إلى ملف حتى تتمكن من عرض النتيجة. تُظهر هذه الخطوة قدرة **حفظ الصورة المرسومة**.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

تهانينا! لقد أكملت بنجاح **كيفية رسم مستطيل** باستخدام Aspose.Drawing لـ .NET.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|-------|------|
| صورة فارغة | لم يتم التخلص من الـ Bitmap أو لم يتم تفريغ الـ graphics | استدعِ `graphics.Dispose();` قبل الحفظ، أو استخدم كتلة `using`. |
| حواف منخفضة الجودة | وضع التنعيم الافتراضي | عيّن `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`. |
| أخطاء مسار الملف | دليل غير صالح | تأكد من وجود المجلد الهدف أو استخدم `Path.Combine` لإنشاء مسار آمن. |

## الأسئلة المتكررة

**س: هل يمكنني تعبئة المستطيل بلون صلب؟**  
ج: نعم، أنشئ `SolidBrush` واستدعِ `graphics.FillRectangle(brush, …)` قبل أو بعد رسم الحدود.

**س: كيف أرسم عدة مستطيلات؟**  
ج: استخدم حلقة تمر عبر مجموعة من هياكل `Rectangle` واستدعِ `DrawRectangle` لكل تكرار.

**س: هل هناك طريقة لتدوير المستطيل؟**  
ج: استخدم `graphics.RotateTransform(angle)` قبل الرسم، ثم أعد تعيين التحويل بعد ذلك.

**س: ما صيغ الصور المدعومة للحفظ؟**  
ج: تدعم الصيغ PNG, JPEG, BMP, GIF, و TIFF عبر معامل `ImageFormat` المناسب.

**س: هل يعمل Aspose.Drawing على .NET Core؟**  
ج: نعم، المكتبة متوافقة تمامًا مع .NET Core، .NET 5، .NET 6، والإصدارات اللاحقة.

## موارد إضافية

إذا واجهت أي تحديات أو كان لديك أسئلة، لا تتردد في طلب المساعدة على [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

### الأسئلة المتكررة

#### س1: هل يمكنني استخدام Aspose.Drawing مجانًا؟

A1: Aspose.Drawing مكتبة تجارية، ولكن يمكنك استكشاف ميزاتها عبر [نسخة تجريبية مجانية](https://releases.aspose.com/).

#### س2: أين يمكنني العثور على الوثائق التفصيلية؟

A2: راجع [الوثائق](https://reference.aspose.com/drawing/net/) للحصول على معلومات مفصلة.

#### س3: كيف يمكنني الحصول على ترخيص مؤقت؟

A3: احصل على [ترخيص مؤقت](https://purchase.aspose.com/temporary-license/) لأغراض الاختبار.

#### س4: هل Aspose.Drawing مناسب لمهام الرسومات المعقدة؟

A4: بالطبع! Aspose.Drawing يوفر ميزات متقدمة للتعامل مع عمليات رسومية معقدة.

#### س5: أين يمكنني شراء Aspose.Drawing؟

A5: زر [هنا](https://purchase.aspose.com/buy) لشراء ترخيص.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-02-17  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

---