---
title: تحميل الصور وحفظها في Aspose.Drawing
linktitle: تحميل الصور وحفظها في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: تحميل الصور الرئيسية وحفظها في .NET باستخدام Aspose.Drawing. استكشف تنسيقات BMP، وGIF، وJPG، وPNG، وTIFF دون عناء.
weight: 13
url: /ar/net/image-editing/load-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحميل الصور وحفظها في Aspose.Drawing

## مقدمة

مرحبًا بك في دليلنا خطوة بخطوة حول إتقان تحميل الصور وحفظها باستخدام Aspose.Drawing for .NET! إذا كنت تتطلع إلى تحسين مهاراتك في التعامل مع تنسيقات الصور المختلفة دون عناء، فأنت في المكان الصحيح. Aspose.Drawing for .NET هي مكتبة قوية تعمل على تبسيط عملية العمل مع الصور، وفي هذا البرنامج التعليمي، سنتعمق في تحميل الصور وحفظها بتنسيقات مختلفة.

## المتطلبات الأساسية

قبل أن نبدأ رحلة التعلم هذه، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.Drawing for .NET: تأكد من تثبيت المكتبة. يمكنك تنزيله[هنا](https://releases.aspose.com/drawing/net/).

- بيئة .NET: يفترض هذا البرنامج التعليمي أن لديك معرفة عملية بتطوير .NET.

الآن بعد أن أصبحنا جاهزين، فلنستكشف مساحات الأسماء الأساسية ونتعمق في الدليل التفصيلي خطوة بخطوة.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، ابدأ باستيراد مساحات الأسماء الضرورية:

```csharp
using System.Drawing;
```

توفر مساحات الأسماء هذه الفئات والأساليب الأساسية اللازمة لمعالجة الصور.

## الخطوة 1: تحميل صورة

لنبدأ بتحميل الصورة. يقوم هذا المثال بتحميل الصور بتنسيقات مختلفة مثل BMP وGIF وJPG وPNG وTIFF.

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

## الخطوة 2: تنفيذ طريقة LoadAndSave

 الآن، قم بتفكيك`LoadAndSave` الطريقة إلى عدة خطوات:

### الخطوة 2.1: تحميل الصورة

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### الخطوة 2.2: حفظ الصورة

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // احفظ الصورة
    loadedImage.Save(outputPath);
}
```

كرر هذه الخطوات لكل تنسيق صورة تريد دعمه.

## خاتمة

تهانينا! لقد أتقنت فن تحميل الصور وحفظها باستخدام Aspose.Drawing لـ .NET. هذه المهارة لا تقدر بثمن بالنسبة للمطورين الذين يعملون مع تنسيقات الصور المتنوعة. قم بتجربة هذه المعرفة واستكشافها ودمجها في مشاريعك.

## الأسئلة الشائعة

### س1: هل Aspose.Drawing متوافق مع جميع تنسيقات الصور؟

A1: يدعم Aspose.Drawing نطاقًا واسعًا من التنسيقات، بما في ذلك BMP وGIF وJPG وPNG وTIFF.

### س2: أين يمكنني العثور على الوثائق التفصيلية الخاصة بـ Aspose.Drawing؟

ج2: راجع الوثائق الرسمية[هنا](https://reference.aspose.com/drawing/net/).

### س3: كيف يمكنني الحصول على ترخيص مؤقت لبرنامج Aspose.Drawing؟

 ج3: زيارة[هنا](https://purchase.aspose.com/temporary-license/) للحصول على تفاصيل الترخيص المؤقت.

### س 4: ماذا لو واجهت مشكلات أو كانت لدي أسئلة أثناء التنفيذ؟

 ج4: اطلب المساعدة من مجتمع Aspose.Drawing على[منتدى أسبوز](https://forum.aspose.com/c/diagram/17).

### س5: أين يمكنني شراء مكتبة Aspose.Drawing؟

 ج5: يمكنك شرائه[هنا](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
