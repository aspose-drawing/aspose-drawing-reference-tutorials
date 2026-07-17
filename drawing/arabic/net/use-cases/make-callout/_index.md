---
date: 2026-03-02
description: عزز توضيحات مستنداتك باستخدام Aspose.Drawing لـ .NET! تعلّم خطوة بخطوة
  كيفية إضافة التعليقات التوضيحية للحصول على صور أوضح وأكثر إفادة.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: كيفية إضافة التعليقات التوضيحية باستخدام Aspose.Drawing لـ .NET
url: /ar/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء التعليقات التوضيحية في Aspose.Drawing

## المقدمة
إذا كنت تتساءل **كيف تضيف التعليقات التوضيحية** إلى صورك أو مخططاتك باستخدام Aspose.Drawing لـ .NET، فقد وصلت إلى المكان الصحيح. في هذا الدرس سنستعرض العملية بالكامل—من تحميل الصورة إلى رسم التعليقات التوضيحية ذات التصميم الجميل—حتى تتمكن من جعل توضيحاتك أكثر وضوحًا وإفادة.

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.Drawing لـ .NET (قابلة للتنزيل من الموقع الرسمي).  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6+.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **كم يستغرق التنفيذ؟** عادةً أقل من 10 دقيقة لإنشاء تعليق توضيحي أساسي.  
- **هل يمكنني تخصيص الألوان والخطوط؟** نعم—كل شيء يتم عبر كائنات GDI+ القياسية (Pen، Font، Brush).

## كيفية إضافة التعليقات التوضيحية في Aspose.Drawing
فيما يلي دليل مختصر خطوة بخطوة يوضح بالضبط **كيفية إضافة التعليقات التوضيحية** إلى صورة. لا تتردد في نسخ الشيفرة، تجربة المواضع، وتكييف التصميم ليتناسب مع علامتك التجارية.

## المتطلبات المسبقة
قبل البدء، تأكد من أن لديك:

- معرفة أساسية بلغة البرمجة C#.
- مكتبة Aspose.Drawing مثبتة. يمكنك تنزيلها [هنا](https://releases.aspose.com/drawing/net/).
- مستند أو صورة تريد إضافة التعليقات التوضيحية إليها.

## استيراد مساحات الأسماء
تأكد من تضمين مساحات الأسماء الضرورية في مشروعك:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## الخطوة 1: تحميل الصورة
ابدأ بتحميل الصورة التي تريد إضافة التعليقات التوضيحية إليها. استبدل `"Your Document Directory"` و `"gears.png"` بالدليل الفعلي واسم ملف الصورة الخاصين بك.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## الخطوة 2: إنشاء كائن Graphics
أنشئ كائن `Graphics` من الصورة لتنفيذ عمليات الرسم.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## الخطوة 3: تحديد مواضع التعليقات التوضيحية
حدد نقاط البداية والنهاية لكل تعليق توضيحي بالإضافة إلى قيمة التعليق ووحدتها.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## الخطوة 4: رسم التعليقات التوضيحية
نفّذ طريقة `DrawCallOut` لرسم التعليقات التوضيحية على الصورة.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## الخطوة 5: حفظ الصورة
احفظ الصورة التي تحتوي على التعليقات التوضيحية إلى الدليل الذي تختاره.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## شفرة مصدر رسم التعليق التوضيحي
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## المشكلات الشائعة والنصائح
- **إحداثيات التثبيت غير صحيحة** – تأكد من أن نقاط البداية والنهاية داخل حدود الصورة؛ وإلا قد يتم قطع التعليق التوضيحي.  
- **تداخل النص** – عدّل `spaceSize` أو حجم الخط إذا تصادم التسمية مع رسومات أخرى.  
- **الأداء** – بالنسبة للصور الكبيرة جدًا، فكر في تحرير كائنات `Pen` و `Font` و `Brush` بعد الاستخدام لتوفير الموارد.

## الخاتمة
تهانينا! الآن تعرف **كيفية إضافة التعليقات التوضيحية** إلى صورة باستخدام Aspose.Drawing لـ .NET. لا تتردد في تجربة مواضع وألوان وخطوط مختلفة لتتناسب مع نمطك البصري.

## الأسئلة المتكررة

### هل يمكنني استخدام Aspose.Drawing لأنواع أخرى من الرسوم التوضيحية؟
نعم، يدعم Aspose.Drawing مجموعة واسعة من عمليات الرسم لأنواع مختلفة من الرسوم التوضيحية.

### هل Aspose.Drawing متوافق مع صيغ صور مختلفة؟
بالطبع! يدعم Aspose.Drawing صيغ الصور الشائعة مثل PNG، JPEG، GIF، وغيرها.

### أين يمكنني العثور على المزيد من الأمثلة والوثائق؟
استكشف الوثائق الشاملة [هنا](https://reference.aspose.com/drawing/net/).

### كيف أحصل على الدعم إذا واجهت مشاكل؟
قم بزيارة [منتدى Aspose.Drawing](https://forum.aspose.com/c/drawing/44) للحصول على دعم المجتمع.

### هل يمكنني تجربة Aspose.Drawing قبل الشراء؟
بالتأكيد! ابدأ بتجربة مجانية [هنا](https://releases.aspose.com/).

**أسئلة إضافية وإجابات**

**س: هل يمكنني تغيير نمط خط التعليق التوضيحي (متقطع، منقط)؟**  
**ج: نعم—ما عليك سوى ضبط خاصية `Pen.DashStyle` قبل رسم الخط.**

**س: هل يمكن إضافة لون خلفية لتسمية التعليق التوضيحي؟**  
**ج: بالتأكيد. أنشئ `SolidBrush` باللون الذي تريده واملأ مستطيلًا خلف النص قبل استدعاء `DrawString`.**

**س: كيف أضمن أن يبدو التعليق التوضيحي بنفس الشكل على شاشات عالية الدقة؟**  
**ج: اضبط `graphics.PageUnit = GraphicsUnit.Pixel` (كما هو موضح) واستخدم قياسات قائمة على المتجهات للحفاظ على تناسق التحجيم.**

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}