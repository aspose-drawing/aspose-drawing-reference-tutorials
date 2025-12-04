---
date: 2025-12-04
description: إتقان تحميل الصور، تحويل الصور دفعةً واحدةً، وتغيير الصيغ في .NET باستخدام
  Aspose.Drawing. تعلم كيفية تحويل BMP إلى PNG وأكثر.
language: ar
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: تحويل BMP إلى PNG وصيغ أخرى باستخدام Aspose.Drawing
url: /net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل BMP إلى PNG وغيرها من الصيغ باستخدام Aspose.Drawing

## مقدمة

مرحبًا بكم في دليلنا خطوة بخطوة حول كيفية **تحويل BMP إلى PNG** (والعديد من صيغ الصور الأخرى) باستخدام Aspose.Drawing لـ .NET. سواء كنت بحاجة إلى **تغيير صيغة الصورة** لملف واحد أو تشغيل **تحويل دفعة من الصور** عبر العشرات من الصور، يوضح لك هذا البرنامج التعليمي بالضبط كيفية تحميل الصور، تحويلها، وحفظها باستخدام شفرة نظيفة وقابلة للصيانة.

## إجابات سريعة
- **هل يمكن لـ Aspose.Drawing تحويل BMP إلى PNG؟** نعم – ما عليك سوى تحميل ملف BMP واستدعاء `Save` مع امتداد .png.  
- **هل يدعم التحويل الدفعي؟** بالتأكيد؛ قم بالتكرار عبر الملفات وأعد استخدام طريقة `LoadAndSave` نفسها.  
- **هل أحتاج إلى ترخيص للإنتاج؟** الترخيص مطلوب للاستخدام في الإنتاج؛ يتوفر ترخيص مؤقت للتقييم.  
- **ما إصدارات .NET المتوافقة؟** يعمل مع .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6/7.  
- **أين يمكنني تنزيل المكتبة؟** احصل على أحدث حزمة Aspose.Drawing من صفحة التحميل الرسمية.

## ما هو تحويل صيغ الصور في C# باستخدام Aspose.Drawing؟

Aspose.Drawing هي مكتبة .NET عالية الأداء ومُدارة بالكامل تُستبدل بـ `System.Drawing.Common` القديمة. تمنحك تحكمًا كاملًا في سيناريوهات **تحميل الصورة ASP.NET**، وتدعم أكثر من 100 صيغة صورة، وتُزيل القيود الخاصة بالمنصات.

## لماذا نستخدم Aspose.Drawing لتحويل الصور دفعيًا؟

- **موثوقية عبر المنصات** – لا توجد تبعيات GDI+.  
- **دعم صيغ غني** – BMP، GIF، JPG، PNG، TIFF، والعديد غيرها.  
- **واجهة برمجة تطبيقات متسقة** – نفس الشفرة تعمل على Windows وLinux وmacOS.  
- **الأداء** – مُحسّن لمعالجة الصور على نطاق واسع.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك:

- **Aspose.Drawing لـ .NET** – قم بتنزيله [هنا](https://releases.aspose.com/drawing/net/).  
- بيئة تطوير **.NET** تعمل (Visual Studio أو VS Code أو Rider).  

الآن بعد أن أصبح كل شيء جاهزًا، دعنا نستورد مساحات الأسماء المطلوبة ونبدأ بالبرمجة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، ابدأ باستيراد مساحة الأسماء اللازمة:

```csharp
using System.Drawing;
```

هذه الفئات توفر الوظائف الأساسية لتحميل وحفظ الصور.

## الخطوة 1: تحميل صورة

الخطوة الأولى هي تحميل ملف صورة. يوضح المثال أدناه تحميل صور بصيغ مختلفة، بما في ذلك BMP، التي سنحولها لاحقًا إلى PNG.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## كيفية تحويل BMP إلى PNG باستخدام Aspose.Drawing

طريقة `LoadAndSave` تتعامل مع كل من تحميل الملف المصدر وحفظه بالصيغ المطلوبة. بتمرير `"bmp"` كمعامل، ستقوم الطريقة تلقائيًا بإنشاء ملف PNG عندما تغير الامتداد في `outputPath`.

### الخطوة 2.1: تحميل الصورة

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### الخطوة 2.2: حفظ الصورة (تغيير صيغة الصورة)

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

كرر استدعاء `LoadAndSave` لكل صيغة صورة ترغب في معالجتها. من خلال تعديل امتداد `outputPath`، يمكنك **تحويل BMP إلى PNG**، **تغيير صيغة الصورة** إلى GIF أو JPG، إلخ، جميعًا باستخدام نفس الطريقة.

## الأخطاء الشائعة والنصائح

- **فواصل مسار الملفات** – استخدم `Path.Combine` لضمان الأمان عبر المنصات بدلاً من دمج السلاسل يدويًا.  
- **تحرير Bitmaps** – ضع `Bitmap` داخل كتلة `using` لتحرير الموارد الأصلية فورًا.  
- **إعدادات الجودة** – عند حفظ JPEGs، فكر في تحديد كائن `EncoderParameters` للتحكم في جودة الضغط.  
- **المعالجة الدفعية** – ضع ملفات الصور في مجلد وكرر عبر `Directory.GetFiles` لأتمتة التحويلات على نطاق واسع.

## الأسئلة المتكررة

### س1: هل Aspose.Drawing متوافق مع جميع صيغ الصور؟

ج1: يدعم Aspose.Drawing مجموعة واسعة من الصيغ، بما في ذلك BMP، GIF، JPG، PNG، وTIFF.

### س2: أين يمكنني العثور على وثائق مفصلة لـ Aspose.Drawing؟

ج2: اطلع على الوثائق الرسمية [هنا](https://reference.aspose.com/drawing/net/).

### س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Drawing؟

ج3: زر [هنا](https://purchase.aspose.com/temporary-license/) للحصول على تفاصيل الترخيص المؤقت.

### س4: ماذا أفعل إذا واجهت مشاكل أو كان لدي أسئلة أثناء التنفيذ؟

ج4: اطلب المساعدة من مجتمع Aspose.Drawing على [منتدى Aspose](https://forum.aspose.com/c/drawing/44).

### س5: أين يمكنني شراء مكتبة Aspose.Drawing؟

ج5: يمكنك شراؤها [هنا](https://purchase.aspose.com/buy).

**أسئلة إضافية**

**س: هل يمكنني استخدام هذا الكود في تطبيق ويب ASP.NET؟**  
ج: نعم – منطق `LoadAndSave` نفسه يعمل في ASP.NET أو MVC أو Razor Pages؛ فقط تأكد من أن مسارات الملفات قابلة للوصول لعملية الويب.

**س: هل من الممكن معالجة الصور بشكل متوازي لتسريع التحويل الدفعي؟**  
ج: بالتأكيد. ضع استدعاءات `LoadAndSave` داخل حلقة `Parallel.ForEach`، لكن تذكر التعامل مع تحرير `Bitmap` بطريقة آمنة للخطوط.

## الخلاصة

لقد تعلمت الآن كيفية **تحويل BMP إلى PNG**، إجراء **تحويل دفعي للصور**، و**تغيير صيغة الصورة** باستخدام Aspose.Drawing لـ .NET. طبّق هذه الأنماط لأتمتة خطوط معالجة الصور، إنشاء صور مصغرة، أو إعداد الأصول للتسليم عبر الويب. جرّب صيغًا مختلفة، دمج الشفرة في خدماتك، واستمتع بموثوقية مكتبة الرسم المُدارة بالكامل.

---

**آخر تحديث:** 2025-12-04  
**تم الاختبار مع:** Aspose.Drawing 24.12 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}