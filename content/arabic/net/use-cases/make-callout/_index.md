---
title: إجراء وسائل الشرح في Aspose.Drawing
linktitle: إجراء وسائل الشرح في Aspose.Drawing
second_title: Aspose.Drawing .NET API - بديل لـ System.Drawing.Common
description: قم بتحسين الرسوم التوضيحية للمستند الخاص بك باستخدام Aspose.Drawing لـ .NET! تعرف على كيفية إضافة وسائل الشرح خطوة بخطوة للحصول على صور أكثر وضوحًا وغنية بالمعلومات.
type: docs
weight: 10
url: /ar/net/use-cases/make-callout/
---
## مقدمة
مرحبًا بك في دليلنا خطوة بخطوة حول إجراء وسائل الشرح في Aspose.Drawing لـ .NET! إذا كنت تتطلع إلى تحسين الرسوم التوضيحية للمستند باستخدام وسائل الشرح، فأنت في المكان الصحيح. في هذا البرنامج التعليمي، سنقوم بتقسيم العملية إلى خطوات يمكن التحكم فيها باستخدام مكتبة Aspose.Drawing.
## المتطلبات الأساسية
قبل الغوص في البرنامج التعليمي، تأكد من أن لديك المتطلبات الأساسية التالية:
- المعرفة الأساسية بلغة البرمجة C#.
-  تم تثبيت مكتبة Aspose.Drawing. يمكنك تنزيله[هنا](https://releases.aspose.com/drawing/net/).
- مستند أو صورة تريد إضافة وسائل شرح إليها.
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
 ابدأ بتحميل الصورة حيث تريد إضافة وسائل الشرح. يستبدل`"Your Document Directory"` و`"gears.png"` مع الدليل الفعلي واسم ملف الصورة.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // الرمز الخاص بك هنا
}
```
## الخطوة 2: إنشاء كائن رسومي
 إنشاء`Graphics` كائن من الصورة لإجراء عمليات الرسم.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## الخطوة 3: تحديد مواضع وسائل الشرح
حدد نقطتي البداية والنهاية لكل وسيلة شرح بالإضافة إلى قيمة وسيلة الشرح والوحدة.
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
## الخطوة 4: ارسم وسائل الشرح
 تنفيذ`DrawCallOut` طريقة رسم وسائل الشرح على الصورة.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## الخطوة 5: احفظ الصورة
احفظ الصورة مع وسائل الشرح في الدليل الذي تريده.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## رسم كود مصدر وسيلة الشرح
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
## خاتمة

تهانينا! لقد نجحت في إضافة وسائل شرح إلى صورتك باستخدام Aspose.Drawing لـ .NET. لا تتردد في تجربة مواضع وقيم مختلفة لتخصيص وسائل الشرح بشكل أكبر.

## الأسئلة الشائعة

### هل يمكنني استخدام Aspose.Drawing لأنواع أخرى من الرسوم التوضيحية؟

نعم، يدعم Aspose.Drawing مجموعة واسعة من عمليات الرسم لأنواع مختلفة من الرسوم التوضيحية.

### هل Aspose.Drawing متوافق مع تنسيقات الصور المختلفة؟

قطعاً! يدعم Aspose.Drawing تنسيقات الصور الشائعة مثل PNG وJPEG وGIF والمزيد.

### أين يمكنني العثور على المزيد من الأمثلة والوثائق؟

 استكشاف الوثائق الشاملة[هنا](https://reference.aspose.com/drawing/net/).

### كيف يمكنني الحصول على الدعم إذا واجهت مشاكل؟

 قم بزيارة[Aspose.منتدى الرسم](https://forum.aspose.com/c/diagram/17) لدعم المجتمع.

### هل يمكنني تجربة Aspose.Drawing قبل الشراء؟

 بالتأكيد! ابدأ بالتجربة المجانية[هنا](https://releases.aspose.com/).