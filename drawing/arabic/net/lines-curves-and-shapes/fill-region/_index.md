---
title: ملء المناطق في Aspose.Drawing
linktitle: ملء المناطق في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: تعرف على كيفية ملء المناطق في Aspose.Drawing لـ .NET باستخدام هذا البرنامج التعليمي خطوة بخطوة. عزز مهاراتك في التصميم الجرافيكي دون عناء.
weight: 20
url: /ar/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ملء المناطق في Aspose.Drawing

## مقدمة

غالبًا ما يتضمن إنشاء رسومات جذابة بصريًا ملء المناطق بالألوان أو الأنماط أو التدرجات اللونية. يوفر Aspose.Drawing for .NET أدوات قوية لتحقيق ذلك بكفاءة. في هذا البرنامج التعليمي، سوف نتعمق في عملية ملء المناطق باستخدام Aspose.Drawing، وهي مكتبة متعددة الاستخدامات تعمل على تبسيط العمليات الرسومية في تطبيقات .NET.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر المتطلبات الأساسية التالية:

1.  مكتبة Aspose.Drawing: قم بتنزيل وتثبيت مكتبة Aspose.Drawing. يمكنك العثور على المكتبة ووثائقها[هنا](https://reference.aspose.com/drawing/net/).

2. بيئة التطوير: قم بإعداد بيئة تطوير .NET، مثل Visual Studio، لدمج Aspose.Drawing في مشاريعك.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية إلى مشروعك. توفر مساحات الأسماء هذه إمكانية الوصول إلى الفئات والأساليب المطلوبة للعمل مع Aspose.Drawing.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


الآن، دعونا نقسم رمز المثال إلى خطوات متعددة للحصول على فهم واضح وشامل.

## الخطوة 1: إنشاء كائن نقطي ورسومات

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

في هذه الخطوة، نقوم بتهيئة صورة نقطية جديدة وكائن رسومي للرسم عليها.

## الخطوة 2: تحديد مسار الرسومات وإنشاء منطقة

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

حدد مسار الرسومات عن طريق تحديد مضلع بمجموعة من النقاط. قم بإنشاء منطقة باستخدام هذا المسار.

## الخطوة 3: استبعاد منطقة داخلية

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

قم بإنشاء مسار رسومات آخر يمثل مستطيلاً داخليًا وقم باستبعاده من المنطقة الرئيسية.

## الخطوة 4: اختر فرشاة واملأ المنطقة

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

حدد فرشاة (في هذه الحالة، لون أزرق خالص) واملأ المنطقة المحددة مسبقًا بالفرشاة المختارة.

## الخطوة 5: احفظ الصورة الناتجة

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

احفظ الصورة النهائية في الدليل الذي تريده.

## خاتمة

يعد ملء المناطق في Aspose.Drawing لـ .NET عملية مباشرة، مما يوفر لك المرونة اللازمة لإنشاء رسومات معقدة وجذابة بصريًا. قم بتجربة الأشكال والألوان والأنماط المختلفة لإطلاق العنان لإبداعك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.Drawing للمشاريع التجارية؟

 ج1: نعم، يمكن استخدام Aspose.Drawing لكل من المشاريع الشخصية والتجارية. للحصول على تفاصيل الترخيص، قم بزيارة[هنا](https://purchase.aspose.com/buy).

### س2: هل هناك نسخة تجريبية مجانية متاحة؟

 ج2: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية[هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.Drawing؟

 ج3: قم بزيارة[Aspose.منتدى الرسم](https://forum.aspose.com/c/drawing/44) للحصول على المساعدة من المجتمع والخبراء.

### س4: هل يمكنني إنشاء صور ديناميكية باستخدام Aspose.Drawing؟

ج4: بالتأكيد. يمكّنك Aspose.Drawing من إنشاء الصور ومعالجتها ديناميكيًا في تطبيقات .NET الخاصة بك.

### س5: هل التراخيص المؤقتة متاحة؟

 ج5: نعم، يمكن الحصول على تراخيص مؤقتة[هنا](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
