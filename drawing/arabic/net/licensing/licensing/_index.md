---
date: 2026-02-09
description: تعلم كيفية تعيين ترخيص Aspose.Drawing في .NET. اتقن طرق الترخيص لفتح
  جميع الميزات دون علامات مائية.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: تعيين ترخيص Aspose.Drawing – كيفية تعيين ترخيص Aspose.Drawing
url: /ar/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين ترخيص Aspose.Drawing

## المقدمة

إذا كنت تقوم بإنشاء تطبيقات .NET تعتمد على رسومات قوية ومعالجة الصور، فإن **تعيين ترخيص Aspose.Drawing** هو الخطوة الأولى لإزالة قيود التقييم والوصول إلى مجموعة الميزات الكاملة. في هذا البرنامج التعليمي ستتعلم ثلاث طرق عملية لتعيين ترخيص Aspose.Drawing — التحميل من ملف، التحميل من تدفق، واستخدام نموذج الاستخدام القائم على العداد — حتى تتمكن من دمج المكتبة بثقة.

## إجابات سريعة
- **ما هي الطريقة الأساسية لتفعيل Aspose.Drawing؟** تحميل ملف الترخيص باستخدام `License.SetLicense("Aspose.Drawing.lic")`.  
- **هل يمكنني تطبيق ترخيص في وقت التشغيل؟** نعم، يمكنك تحميل الترخيص من `Stream` للسيناريوهات الديناميكية.  
- **هل يتم دعم ترخيص بالعداد؟** بالتأكيد؛ استخدم `Metered.SetMeteredKey(publicKey, privateKey)` لتمكين الفوترة القائمة على الاستهلاك.  
- **هل أحتاج إلى ترخيص لإصدارات التطوير؟** النسخة التجريبية تعمل للاختبار، لكن الترخيص الصالح يزيل العلامات المائية ويفتح جميع الـ APIs.  
- **ما إصدارات .NET المتوافقة؟** يدعم Aspose.Drawing .NET Framework 4.x، .NET Core 3.1+، و .NET 5/6+.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

- **مكتبة Aspose.Drawing** – قم بتنزيل أحدث حزمة من [هنا](https://releases.aspose.com/drawing/net/).  
- **ملف الترخيص** – احصل على ملف `.lic` صالح من [Aspose](https://purchase.aspose.com/buy).  
- **بيئة تطوير .NET** – Visual Studio، Rider، أو أي IDE يستهدف .NET Framework/.NET Core.

## استيراد مساحات الأسماء

نحتاج إلى مساحات الأسماء القياسية في .NET بالإضافة إلى مساحة أسماء Aspose.Drawing للترخيص. أضف عبارات `using` التالية في أعلى ملف C# الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## تحميل الترخيص من ملف

تحميل الترخيص من ملف هو النهج الأكثر بساطة. اتبع هذه الخطوات الثلاث:

### الخطوة 1: تهيئة كائن الترخيص

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### الخطوة 2: تعيين الترخيص من ملف `.lic`

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### الخطوة 3: تأكيد النجاح

```csharp
Console.WriteLine("License set successfully.");
```

> **نصيحة احترافية:** ضع ملف `.lic` في نفس مجلد الملف التنفيذي أو قدم مسارًا مطلقًا لتجنب أخطاء “الملف غير موجود”.

## تحميل الترخيص من تدفق

عندما يكون ملف الترخيص مدمجًا كموارد أو مسترجعًا من موقع بعيد، يتيح لك تحميله من `Stream` مرونة.

### الخطوة 1: تهيئة كائن الترخيص

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### الخطوة 2: تحميل الترخيص باستخدام `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### الخطوة 3: تأكيد النجاح

```csharp
Console.WriteLine("License set successfully.");
```

> **تحذير:** تذكر تحرير `FileStream` (أو استخدم كتلة `using`) لتحرير مقابض الملفات.

## استخدام ترخيص بالعداد

الترخيص القائم على العداد مثالي لخدمات SaaS أو نماذج الدفع حسب الاستخدام. يتتبع الاستهلاك ويصدر الفواتير بناءً على الاستخدام الفعلي.

### الخطوة 1: تهيئة كائن Metered

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### الخطوة 2: تعيين المفاتيح العامة والخاصة

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### الخطوة 3: تنفيذ معالجة الصور الخاصة بك

```csharp
// Your image processing logic here
```

### الخطوة 4: استرجاع معلومات الاستهلاك

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### الخطوة 5: عرض تفاصيل الاستهلاك

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **مشكلة شائعة:** إذا نسيت استدعاء `SetMeteredKey`، سيعود الـ API إلى وضع التجربة وستظهر العلامات المائية في الناتج.

## لماذا يجب تعيين ترخيص Aspose.Drawing بشكل صحيح؟

- **يزيل العلامات المائية** التي تظهر في وضع التجربة.  
- **يفتح الـ APIs المتميزة** مثل الفلاتر المتقدمة للصور وتحويل PDF.  
- **يضمن الامتثال** لشروط ترخيص Aspose للتوزيع التجاري.  
- **يمكّن الفوترة القائمّة على العداد**، مما يسمح لك بالدفع فقط مقابل ما تستخدمه.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| خطأ “License file not found” | مسار خاطئ أو ملف مفقود في مجلد الإخراج | استخدم مسارًا مطلقًا أو اضبط خاصية *Copy to Output Directory* للملف إلى *Copy always*. |
| العلامة المائية لا تزال تظهر بعد تعيين الترخيص | الترخيص لم يتم تحميله قبل أول استدعاء للـ API | حمّل الترخيص **قبل** أي عملية Aspose.Drawing. |
| استهلاك العداد دائمًا صفر | المفاتيح غير مضبوطة أو متغيرات البيئة خاطئة | تحقق من المفاتيح العامة/الخاصة وتأكد من اتصال الإنترنت بخادم العداد الخاص بـ Aspose. |

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.Drawing بدون ترخيص؟**  
ج1: نعم، يعمل الترخيص التجريبي للتطوير والتقييم، لكنه يضيف علامات مائية ويحد من بعض الميزات.

**س2: كم مرة أحتاج لتجديد ترخيص Aspose.Drawing؟**  
ج2: الترخيص دائم للإصدار الذي تم شراؤه. التجديد مطلوب فقط للدعم والترقيات.

**س3: ما هو الترخيص القائم على العداد، ومتى يجب استخدامه؟**  
ج3: الترخيص القائم على العداد يفرض رسومًا بناءً على الاستخدام (العمليات أو البيانات المعالجة). وهو مثالي لخدمات السحابة أو نماذج الدفع حسب الاستخدام.

**س4: هل يمكنني استخدام Aspose.Drawing في المشاريع التجارية؟**  
ج4: بالتأكيد—بمجرد حصولك على ترخيص صالح، يمكنك دمج Aspose.Drawing في أي تطبيق تجاري.

**س5: أين يمكنني العثور على دعم المجتمع لـ Aspose.Drawing؟**  
ج5: زر [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على مساعدة المجتمع، أمثلة، ومناقشات.

## الخاتمة

إتقان كيفية **تعيين ترخيص Aspose.Drawing** — سواء من ملف، أو من تدفق، أو عبر الاستخدام القائم على العداد — يضمن لك الاستفادة القصوى من هذه المكتبة القوية للرسومات في .NET. اتبع الخطوات أعلاه، واحذر من المشكلات الشائعة، وستكون جاهزًا لبناء حلول معالجة صور قوية دون أي عوائق ترخيص.

---

**آخر تحديث:** 2026-02-09  
**تم الاختبار باستخدام:** Aspose.Drawing 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}