---
date: 2025-11-29
description: تعلم كيفية إنشاء صورة نقطية باستخدام Aspose.Drawing، وتطبيق التحويلات
  العالمية، وتحويل الرسومات إلى PNG. دليل خطوة بخطوة لمطوري .NET.
language: ar
linktitle: World Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: إنشاء صورة نقطية باستخدام Aspose.Drawing – دليل تحويل العالم
url: /net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء Bitmap باستخدام Aspose.Drawing – التحويل العالمي

## مقدمة

مرحبًا! في هذا البرنامج التعليمي ستقوم **بإنشاء bitmap باستخدام Aspose.Drawing** وتستكشف التحويلات العالمية التي تتيح لك إزاحة، تدوير أو تحجيم الرسومات بسهولة. سواء كنت بحاجة إلى **مثال على إزاحة الرسومات**، أو تريد **تحويل الرسومات إلى PNG**، أو تخطط لـ **تحويلات رسومات متعددة**، سيوجهك هذا الدليل خلال كل خطوة بأسلوب واضح وحواري.

## إجابات سريعة
- **ماذا يعني “التحويل العالمي”؟** إنه يطابق إحداثيات الرسم المنطقية (العالمية) مع إحداثيات الصفحة (الجهاز).  
- **هل يمكنني تصدير النتيجة كملف PNG؟** نعم – بعد الرسم ما عليك سوى استدعاء `bitmap.Save(...)` مع امتداد `.png`.  
- **هل أحتاج إلى ترخيص لـ Aspose.Drawing؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **هل هذا متوافق مع .NET 6/7؟** بالتأكيد – يدعم Aspose.Drawing .NET Framework 4.5+ و .NET Core/5/6/7.  
- **كم عدد التحويلات التي يمكن ربطها معًا؟** يمكنك تطبيق **تحويلات رسومات متعددة** بالتسلسل (إزاحة، تدوير، تحجيم، إلخ).

## ما هو التحويل العالمي في Aspose.Drawing؟

يغيّر التحويل العالمي نظام الإحداثيات الذي تستخدمه أوامر الرسم. بشكل افتراضي، يكون (0,0) في الزاوية العلوية اليسرى للـ bitmap. باستخدام `TranslateTransform` أو `RotateTransform` أو `ScaleTransform`، يمكنك إعادة تموضع هذا الأصل، تدوير الأشكال، أو تغيير حجمها دون تعديل الهندسة الأصلية.

## لماذا نستخدم مثال إزاحة الرسومات؟

- **يبسط التموضع** – حرك الكائنات دون الحاجة لإعادة حساب كل نقطة.  
- **يحافظ على نظافة الكود** – استدعاء تحويل واحد يحل محل العديد من تعديلات الإحداثيات اليدوية.  
- **يعزز الأداء** – يتولى محرك الرسومات الحسابات داخليًا.  

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- **مكتبة Aspose.Drawing** مدمجة في مشروع .NET الخاص بك (حمّلها من [صفحة إصدارات Aspose.Drawing الرسمية](https://releases.aspose.com/drawing/net/)).  
- **دليل المستندات** حيث سيتم حفظ الصورة الناتجة.  
- إلمام أساسي بـ **C#** وبيئة Visual Studio أو أي بيئة تطوير تفضّلها.  

الآن، دعنا نغوص في الكود!

## استيراد المساحات الاسمية

أولاً، استدعِ المساحات الاسمية المطلوبة:

```csharp
using System.Drawing;
using Aspose.Drawing;
```

تمنحك هذه القدرة على الوصول إلى `Bitmap` و `Graphics` وأدوات Aspose للرسم.

## دليل خطوة بخطوة

### الخطوة 1: إنشاء Bitmap

نبدأ بإنشاء لوحة قماش فارغة ستحتوي على الرسم.

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

- **لماذا 32bppPArgb؟** يدعم هذا التنسيق الشفافية ألفا وجودة ألوان عالية، وهو مثالي لإخراج PNG.  
- **نصيحة احترافية:** عدّل العرض/الارتفاع ليتطابق مع حجم الصورة المستهدف.

### الخطوة 2: ضبط التحويل العالمي (مثال إزاحة الرسومات)

هنا نُحرك الأصل إلى مركز الـ bitmap بحيث تكون أوامر الرسم نسبية لتلك النقطة.

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

- هذا ينقل النقطة (0,0) إلى (500, 400) – وسط لوحة 1000 × 800.  
- يمكنك ربط تحويلات إضافية (مثل `RotateTransform` أو `ScaleTransform`) للحصول على **تحويلات رسومات متعددة**.

### الخطوة 3: رسم مستطيل باستخدام الإحداثيات المحوّلة

الآن أي شكل نرسمه سيتوضع نسبةً إلى الأصل الجديد.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

- يبدأ الزاوية العلوية اليسرى للمستطيل عند الأصل المحوّل (مركز الصورة).  
- لا تتردد في تجربة أشكال أخرى—إهليلجات، خطوط، أو مسارات مخصصة.

### الخطوة 4: حفظ النتيجة – تحويل الرسومات إلى PNG

أخيرًا، احفظ الـ bitmap كملف PNG.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

- يحافظ PNG على الألوان والشفافية التي حددناها مسبقًا.  
- استبدل `"Your Document Directory"` بالمسار الفعلي على جهازك.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **خطأ ملف غير موجود** عند الحفظ | المجلد الهدف غير موجود. | أنشئ المجلد برمجيًا (`Directory.CreateDirectory`) قبل استدعاء `Save`. |
| **صورة فارغة** بعد التحويل | تم استدعاء `TranslateTransform` بعد الرسم. | تأكد من ضبط التحويل **قبل** أي أوامر رسم. |
| **تشويه الألوان** | استخدام تنسيق بكسل غير متوافق. | استخدم `Format32bppPArgb` لإخراج PNG. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق أكثر من تحويل؟**  
ج: نعم – يمكنك ربط `TranslateTransform` و `RotateTransform` و `ScaleTransform` لتحقيق تأثيرات معقدة.

**س: هل Aspose.Drawing مجاني للمشاريع التجارية؟**  
ج: تتوفر نسخة تجريبية مجانية للتقييم، لكن الترخيص التجاري مطلوب للاستخدام الإنتاجي.

**س: هل يعمل هذا مع .NET Core و .NET 5/6/7؟**  
ج: بالتأكيد. يدعم Aspose.Drawing جميع إصدارات .NET الحديثة.

**س: أينني العثور على مرجع API الكامل؟**  
ج: الوثائق الكاملة متاحة [هنا](https://reference.aspose.com/drawing/net/).

**س: كيف أحل مشكلة عدم وجود ملف الإخراج؟**  
ج: تحقق من سلسلة المسار، تأكد من صلاحيات الكتابة، وتأكد من وجود الدليل قبل استدعاء `Save`.

## الخاتمة

لقد تعلمت الآن كيفية **إنشاء bitmap باستخدام Aspose.Drawing**، وتطبيق **تحويل عالمي**، و**تحويل الرسومات إلى PNG**. من خلال إتقان هذه الأساسيات، يمكنك بناء رسومات أغنى، توليد صور ديناميكية، ودمج تأثيرات بصرية متقدمة في أي تطبيق .NET.

---

**آخر تحديث:** 2025-11-29  
**تم الاختبار مع:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  
**موارد ذات صلة:** [مرجع Aspose.Drawing API](https://reference.aspose.com/drawing/net/) | [تحميل نسخة تجريبية مجانية](https://releases.aspose.com/drawing/net/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}