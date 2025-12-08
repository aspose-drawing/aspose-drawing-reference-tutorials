---
date: 2025-12-06
description: تعلم كيفية حفظ ملفات صور PNG أثناء سرد الخطوط المثبتة، وعرض عائلات الخطوط،
  وإنشاء رسومات من صورة نقطية، ورسم النص باستخدام الخطوط باستخدام Aspose.Drawing لـ
  .NET.
language: ar
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: حفظ صورة PNG والعمل مع الخطوط المثبتة في Aspose.Drawing
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ صورة PNG والعمل مع الخطوط المثبتة في Aspose.Drawing

## المقدمة

إذا كنت بحاجة إلى **حفظ صورة PNG** تُظهر أيضًا معلومات حول الخطوط المثبتة على الجهاز، فإن Aspose.Drawing لـ .NET يوفّر لك طريقة نظيفة وعبر‑المنصات للقيام بذلك. في هذا الدرس سنستعرض كيفية سرد الخطوط المثبتة، عرض عائلات الخطوط، إنشاء رسومات من bitmap، ورسم نص بالخطوط—كل ذلك مع حفظ النتيجة كصورة PNG في النهاية. بنهاية الدرس ستحصل على مقتطف يمكن إعادة استخدامه وإدراجه في أي مشروع .NET.

## الإجابات السريعة
- **ما الذي ينشئه هذا الدرس؟** صورة PNG تسرد عائلات الخطوط المثبتة.  
- **ما المكتبة المطلوبة؟** Aspose.Drawing لـ .NET (لا حاجة لـ System.Drawing.Common).  
- **هل يمكنني استخدام خطوط مخصصة؟** نعم – فقط قم بتحميلها إلى `InstalledFontCollection`.  
- **هل يمكن تعديل دقة الإخراج؟** بالتأكيد – غيّر حجم الـ bitmap أو تنسيق البكسل.  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** ترخيص مؤقت يكفي للتقييم؛ ترخيص كامل مطلوب للإنتاج.

## ما معنى “حفظ صورة PNG” في سياق Aspose.Drawing؟
حفظ صورة PNG يعني تحويل سطح الرسم الخاص بك (ـ `Bitmap`) إلى ملف بامتداد `.png`. تتولى Aspose.Drawing عملية الترميز لك، لذا كل ما عليك هو استدعاء `bitmap.Save(...)` مع المسار المطلوب.

## لماذا ندرج الخطوط المثبتة ونظهر عائلات الخطوط؟
معرفة الخطوط المتوفرة يتيح لك إنشاء رسومات ديناميكية تتكيف مع بيئة المستخدم النهائي. هذا مفيد بشكل خاص لتوليد تقارير، شهادات، أو أي محتوى بصري يجب أن يتطابق مع هوية الشركة دون الحاجة لنقل ملفات الخطوط.

## المتطلبات المسبقة

- **مكتبة Aspose.Drawing** – حمّل أحدث نسخة من [صفحة تحميل Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **بيئة التطوير المتكاملة (IDE)** – Visual Studio أو Rider أو أي محرر متوافق مع .NET.  
- **معرفة أساسية بـ C#** – يجب أن تكون مرتاحًا مع الفئات، الكائنات، والحلقات البسيطة.

## استيراد مساحات الأسماء
للتعامل مع الخطوط والرسومات، استورد مساحات الأسماء التالية في أعلى ملف C# الخاص بك:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## دليل خطوة بخطوة

### الخطوة 1: إنشاء bitmap (القماش)
أولاً، ننشئ bitmap سيحمل الصورة النهائية. حجم الـ bitmap وتنسيق البكسل يحددان جودة صورة PNG المحفوظة.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### الخطوة 2: إنشاء رسومات من bitmap
بعد ذلك، نحصل على كائن `Graphics` من الـ bitmap. يتيح لنا هذا الكائن رسم الأشكال، النصوص، والصور على القماش.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### الخطوة 3: إعداد الفرشاة والخط (رسم نص بالخطوط)
نحتاج إلى فرشاة لتحديد لون النص وكائن `Font` يحدد نوع الخط، الحجم، والنمط.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### الخطوة 4: سرد الخطوط المثبتة وعرض عائلات الخطوط
الآن نعرض عدد عائلات الخطوط وبعض الأسماء مباشرة على الـ bitmap. يوضح ذلك قدرة **سرد الخطوط المثبتة** و**عرض عائلات الخطوط**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### الخطوة 5: حفظ صورة PNG
أخيرًا، نكتب الـ bitmap إلى القرص كملف PNG. هذه هي عملية **حفظ صورة PNG** الأساسية.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **نصيحة احترافية:** استخدم `Path.Combine` لإنشاء مسارات الملفات لتجنب مشاكل فواصل الدليل على أنظمة التشغيل المختلفة.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|---------|-------|------|
| **عدم عرض الخطوط** | `InstalledFontCollection` غير مُعبّأة (مثلاً تشغيل على خادم بدون واجهة رسومية ولا يحتوي على خطوط). | قم بتثبيت الخطوط المطلوبة على الخادم أو دمج خطوط مخصصة في تطبيقك. |
| **الملف المحفوظ تالف** | تنسيق بكسل غير صحيح أو نقص في أذونات الكتابة. | تأكد من وجود المجلد الهدف وأن التطبيق لديه صلاحية كتابة؛ احتفظ بـ `Format32bppPArgb`. |
| **النص يبدو غير واضح** | إعدادات DPI منخفضة. | قم بزيادة أبعاد الـ bitmap أو اضبط `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام خطوط مخصصة غير مثبتة على الجهاز؟**  
ج: نعم. حمّل ملف الخط إلى `PrivateFontCollection` وأنشئ `Font` من تلك المجموعة.

**س: كيف أتعامل مع الاستثناءات المتعلقة بالخطوط؟**  
ج: ضع إنشاء الخط داخل كتلة `try/catch` وتفقد `ArgumentException` للخطوط المفقودة.

**س: هل Aspose.Drawing مناسب لتطبيقات الويب؟**  
ج: بالتأكيد. المكتبة تعمل في ASP.NET Core، Azure Functions، وغيرها من بيئات الخادم.

**س: هل يمكنني تغيير لون النص أو نمطه؟**  
ج: نعم. استخدم أنواع مختلفة من `Brush` (مثل `LinearGradientBrush`) وعدّل تعداد `FontStyle`.

**س: من أين يمكنني الحصول على ترخيص مؤقت للاختبار؟**  
ج: حمّل ترخيص تجريبي من [صفحة الترخيص المؤقت لـ Aspose](https://purchase.aspose.com/temporary-license/).

## الخلاصة

باتباع هذه الخطوات تعلمت كيفية **حفظ صورة PNG** التي تُدرج ديناميكيًا **الخطوط المثبتة**، **عرض عائلات الخطوط**، **إنشاء رسومات من bitmap**، و**رسم نص بالخطوط** باستخدام Aspose.Drawing لـ .NET. لا تتردد في تجربة خطوط أخرى، ألوان، وأحجام bitmap لتتناسب مع متطلبات مشروعك البصرية.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-06  
**تم الاختبار باستخدام:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose