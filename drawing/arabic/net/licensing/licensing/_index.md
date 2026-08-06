---
date: 2026-05-29
description: تعلم كيفية تعيين ترخيص Aspose.Drawing في .NET وإزالة علامة Aspose المائية.
  إتقان طرق الترخيص لفتح جميع الميزات دون علامات مائية.
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
linktitle: الترخيص في Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  headline: Remove Aspose Watermark – Set Aspose.Drawing License
  type: TechArticle
- description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  name: Remove Aspose Watermark – Set Aspose.Drawing License
  steps:
  - name: Confirm Success
    text: '> **Pro tip:** Place the `.lic` file in the same folder as your executable
      or provide an absolute path to avoid “file not found” errors.'
  - name: Confirm Success
    text: '> **Warning:** Remember to dispose the `FileStream` (or use a `using` block)
      to free file handles.'
  - name: Display the Consumption Details
    text: '> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will
      fall back to trial mode and you’ll see watermarks in the output.'
  type: HowTo
- questions:
  - answer: Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.
    question: What is the primary way to activate Aspose.Drawing?
  - answer: Yes, you can load the license from a `Stream` for dynamic scenarios.
    question: Can I apply a license at runtime?
  - answer: Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable
      consumption‑based billing.
    question: Is a metered license supported?
  - answer: A trial works for testing, but a valid license removes watermarks and
      unlocks all APIs.
    question: Do I need a license for development builds?
  - answer: Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.
    question: Which .NET versions are compatible?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: إزالة علامة Aspose المائية – تعيين ترخيص Aspose.Drawing
url: /ar/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين ترخيص Aspose.Drawing

## مقدمة

إذا كنت تقوم بإنشاء تطبيقات .NET تعتمد على رسومات قوية ومعالجة الصور، فإن **تعيين ترخيص Aspose.Drawing** هو الخطوة الأولى لإزالة علامة Aspose المائية والوصول إلى مجموعة الميزات الكاملة. في هذا البرنامج التعليمي ستتعلم ثلاث طرق عملية لتعيين ترخيص Aspose.Drawing — التحميل من ملف، التحميل من تدفق (Stream)، واستخدام نموذج الترخيص القائم على الاستهلاك — حتى تتمكن من دمج المكتبة بثقة والحفاظ على نظافة المخرجات.

## إجابات سريعة
- **ما هي الطريقة الأساسية لتفعيل Aspose.Drawing؟** تحميل ملف الترخيص باستخدام `License.SetLicense("Aspose.Drawing.lic")`.  
- **هل يمكنني تطبيق الترخيص أثناء التشغيل؟** نعم، يمكنك تحميل الترخيص من `Stream` للسيناريوهات الديناميكية.  
- **هل يدعم الترخيص القائم على الاستهلاك؟** بالتأكيد؛ استخدم `Metered.SetMeteredKey(publicKey, privateKey)` لتمكين الفوترة بناءً على الاستهلاك.  
- **هل أحتاج إلى ترخيص لإصدارات التطوير؟** النسخة التجريبية تعمل للاختبار، لكن الترخيص الصالح يزيل العلامات المائية ويفتح جميع الـ APIs.  
- **ما إصدارات .NET المتوافقة؟** يدعم Aspose.Drawing .NET Framework 4.x، .NET Core 3.1+، و .NET 5/6+.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- **مكتبة Aspose.Drawing** – قم بتنزيل أحدث حزمة من [هنا](https://releases.aspose.com/drawing/net/).  
- **ملف الترخيص** – احصل على ملف `.lic` صالح من [Aspose](https://purchase.aspose.com/buy).  
- **بيئة تطوير .NET** – Visual Studio أو Rider أو أي IDE يستهدف .NET Framework/.NET Core.

## استيراد المساحات الاسمية

نحتاج إلى مساحات الأسماء القياسية في .NET بالإضافة إلى مساحة الأسماء Aspose.Drawing للترخيص. أضف عبارات `using` التالية في أعلى ملف C# الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## كيفية تحميل الترخيص من ملف؟

تمثل فئة `License` مكون الترخيص في Aspose.Drawing الذي، عند إنشائه، يسمح لك بتطبيق الترخيص على المكتبة. تحميل الترخيص من ملف هو الأسهل؛ ما عليك سوى تمرير مسار ملف `.lic` إلى طريقة `SetLicense` وتزيل المكتبة جميع العلامات المائية التجريبية لبقية جلسة التطبيق. تعمل هذه الطريقة في بيئات سطح المكتب والخادم ولا تتطلب أي إعدادات إضافية بخلاف التأكد من إمكانية الوصول إلى الملف أثناء التشغيل.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## كيفية تحميل الترخيص من تدفق (Stream)؟

عندما يكون ملف الترخيص مضمّنًا كموارد أو يتم استرجاعه عبر الشبكة، يمنحك التحميل من `Stream` مرونة مع الحفاظ على إزالة العلامة المائية. بتمرير كائن `Stream` إلى طريقة `SetLicense`، تبقي الترخيص خارج مجلد النشر، مما يحسن الأمان ويسهل التوزيع في الحاويات أو السحابة. العملية مماثلة للتحميل من ملف، باستثناء أنك تدير دورة حياة الـ `Stream` بنفسك.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## كيفية تفعيل ترخيص القائم على الاستهلاك؟

تتعامل فئة `Metered` مع تفعيل الترخيص القائم على الاستهلاك لـ Aspose.Drawing، مما يتيح الفوترة بناءً على الاستهلاك. يتيح الترخيص القائم على الاستهلاك الدفع فقط مقابل العمليات التي تقوم بها، وهو مثالي لخدمات SaaS أو نماذج الدفع حسب الاستخدام. بعد توفير المفتاحين العام والخاص، يتم تتبع كل استدعاء لمعالجة الصور وفوترة ذلك تلقائيًا، وتعمل المكتبة في وضع كامل الميزات دون علامات مائية طوال مدة الجلسة.

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## لماذا يجب تعيين ترخيص Aspose.Drawing بشكل صحيح؟

يضمن تعيين الترخيص بشكل صحيح تشغيل المكتبة في وضع كامل الميزات، إزالة العلامات المائية التجريبية، والامتثال لشروط ترخيص Aspose. يفتح الترخيص المطبق بشكل صحيح الـ APIs المتميزة، يحسن الأداء بإلغاء فحوصات التقييم، ويسمح لك باستخدام الفوترة القائم على الاستهلاك إذا رغبت. عدم تحميل الترخيص قبل أول استدعاء API سيؤدي إلى عودة المكتبة إلى الوضع التجريبي، مما ينتج عنه علامات مائية على جميع الصور المولدة.

- **يزيل العلامات المائية** التي تظهر في الوضع التجريبي.  
- **يفتح الـ APIs المتميزة** مثل الفلاتر المتقدمة للصور وتحويل PDF.  
- **يضمن الامتثال** لشروط ترخيص Aspose للتوزيع التجاري.  
- **يتيح الفوترة القائم على الاستهلاك**، مما يجعلك تدفع فقط مقابل ما تستخدمه.  

يدعم Aspose.Drawing **أكثر من 30 تنسيق صورة** (بما في ذلك PNG، JPEG، BMP، TIFF، وWebP) ويمكنه معالجة **مستندات PDF مئات الصفحات دون تحميل الملف بالكامل في الذاكرة**، مما يقدم تحويلًا عالي الأداء على أجهزة ذات موارد محدودة.

## تحميل الترخيص من ملف

تحميل الترخيص من ملف هو الأسهل. اتبع الخطوات الثلاث التالية:

### الخطوة 1: تهيئة كائن الترخيص

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### الخطوة 2: تعيين الترخيص من ملف `.lic`

```csharp
Console.WriteLine("License set successfully.");
```

### الخطوة 3: تأكيد النجاح

```csharp
Console.WriteLine("License set successfully.");
```

> **نصيحة احترافية:** ضع ملف `.lic` في نفس مجلد الملف التنفيذي أو قدم مسارًا مطلقًا لتجنب أخطاء “الملف غير موجود”.

## تحميل الترخيص من تدفق (Stream)

عندما يكون ملف الترخيص مضمّنًا كموارد أو يتم استرجاعه من موقع بعيد، يمنحك التحميل من `Stream` مرونة.

### الخطوة 1: تهيئة كائن الترخيص

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### الخطوة 2: تحميل الترخيص باستخدام `FileStream`

```csharp
Console.WriteLine("License set successfully.");
```

### الخطوة 3: تأكيد النجاح

```csharp
Console.WriteLine("License set successfully.");
```

> **تحذير:** تذكر إغلاق `FileStream` (أو استخدم كتلة `using`) لتحرير مقابض الملفات.

## استخدام الترخيص القائم على الاستهلاك

الترخيص القائم على الاستهلاك مثالي لخدمات SaaS أو نماذج الدفع حسب الاستخدام. يتتبع الاستهلاك ويفوّضك بناءً على الاستخدام الفعلي.

### الخطوة 1: تهيئة كائن Metered

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### الخطوة 2: تعيين المفاتيح العامة والخاصة

```csharp
// Your image processing logic here
```

### الخطوة 3: تنفيذ معالجة الصور الخاصة بك

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### الخطوة 4: استرجاع معلومات الاستهلاك

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### الخطوة 5: عرض تفاصيل الاستهلاك

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **خطأ شائع:** إذا نسيت استدعاء `SetMeteredKey`، سيعود الـ API إلى الوضع التجريبي وستظهر العلامات المائية في المخرجات.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| خطأ “لم يتم العثور على ملف الترخيص” | مسار غير صحيح أو ملف مفقود في مجلد الإخراج | استخدم مسارًا مطلقًا أو اضبط خاصية *Copy to Output Directory* إلى *Copy always*. |
| لا تزال العلامة المائية تظهر بعد تعيين الترخيص | لم يتم تحميل الترخيص قبل أول استدعاء API | حمّل الترخيص **قبل** أي عملية Aspose.Drawing. |
| استهلاك الترخيص القائم على الاستهلاك دائمًا صفر | المفاتيح غير مضبوطة أو متغيرات البيئة خاطئة | تحقق من المفاتيح العامة/الخاصة وتأكد من وجود اتصال بالإنترنت لخادم Aspose القائم على الاستهلاك. |

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.Drawing بدون ترخيص؟**  
ج1: نعم، النسخة التجريبية تعمل للتطوير والتقييم، لكنها تضيف علامات مائية وتحد من بعض الميزات.

**س2: كم مرة يجب أن أجدد ترخيص Aspose.Drawing؟**  
ج2: الترخيص دائم للإصدار الذي تم شراؤه. التجديد مطلوب فقط للدعم والترقيات.

**س3: ما هو الترخيص القائم على الاستهلاك ومتى يجب استخدامه؟**  
ج3: الترخيص القائم على الاستهلاك يُحاسب بناءً على الاستخدام (العمليات أو البيانات المعالجة). وهو مثالي للخدمات السحابية أو نماذج الدفع حسب الاستخدام.

**س4: هل يمكنني استخدام Aspose.Drawing في مشاريع تجارية؟**  
ج4: بالتأكيد—بمجرد حصولك على ترخيص صالح، يمكنك دمج Aspose.Drawing في أي تطبيق تجاري.

**س5: أين يمكنني العثور على دعم المجتمع لـ Aspose.Drawing؟**  
ج5: زر [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على مساعدة المجتمع، أمثلة، ومناقشات.

## الخاتمة

إتقان كيفية **تعيين ترخيص Aspose.Drawing**—سواء من ملف، أو من تدفق، أو عبر الاستخدام القائم على الاستهلاك—يضمن استفادتك القصوى من هذه المكتبة القوية لمعالجة الرسومات في .NET مع **إزالة علامة Aspose المائية** تمامًا. اتبع الخطوات أعلاه، احذر الأخطاء الشائعة، وستكون جاهزًا لبناء حلول معالجة صور قوية دون عوائق ترخيص.

---

**آخر تحديث:** 2026-05-29  
**تم الاختبار مع:** Aspose.Drawing 24.11 لـ .NET  
**المؤلف:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
