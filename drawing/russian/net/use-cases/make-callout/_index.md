---
date: 2026-03-02
description: Улучшите иллюстрации в своих документах с помощью Aspose.Drawing для
  .NET! Узнайте пошагово, как добавлять выноски для более ясных и информативных визуальных
  материалов.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Как добавить выноски с помощью Aspose.Drawing для .NET
url: /ru/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создание выносов в Aspose.Drawing

## Introduction
Если вы задаётесь вопросом, **как добавить выноски** к вашим изображениям или диаграммам с помощью Aspose.Drawing для .NET, вы попали в нужное место. В этом руководстве мы пройдём весь процесс — от загрузки изображения до рисования красиво оформленных выносов — чтобы ваши иллюстрации стали более понятными и информативными.

## Quick Answers
- **Какая библиотека нужна?** Aspose.Drawing for .NET (downloadable from the official site).  
- **Какие версии .NET поддерживаются?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Нужна ли лицензия?** A free trial works for development; a commercial license is required for production.  
- **Сколько времени занимает реализация?** Typically under 10 minutes for a basic callout.  
- **Можно ли настроить цвета и шрифты?** Yes—everything is driven by standard GDI+ objects (Pen, Font, Brush).

## How to Add Callouts in Aspose.Drawing
Ниже представлено краткое пошаговое руководство, показывающее **как добавить выноски** к изображению. Смело копируйте код, экспериментируйте с позициями и адаптируйте стиль под ваш бренд.

## Prerequisites
Перед тем как начать, убедитесь, что у вас есть:

- Базовые знания языка программирования C#.  
- Aspose.Drawing library installed. You can download it [here](https://releases.aspose.com/drawing/net/).  
- A document or image where you want to add callouts.

## Import Namespaces
Убедитесь, что в проекте подключены необходимые пространства имён:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Step 1: Load the Image
Шаг 1: Загрузка изображения  
Start by loading the image where you want to add callouts. Replace `"Your Document Directory"` and `"gears.png"` with your actual directory and image filename.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Step 2: Create Graphics Object
Шаг 2: Создание объекта Graphics  
Create a `Graphics` object from the image to perform drawing operations.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Step 3: Define Callout Positions
Шаг 3: Определение позиций выноски  
Define the start and end points for each callout along with the callout value and unit.

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

## Step 4: Draw Callouts
Шаг 4: Рисование выноски  
Implement the `DrawCallOut` method to draw callouts on the image.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Step 5: Save the Image
Шаг 5: Сохранение изображения  
Save the image with callouts to your desired directory.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Draw Callout Source Code
Исходный код рисования выноски
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

## Common Issues & Tips
- **Неправильные координаты якоря** – make sure the start and end points are within the image bounds; otherwise the callout may be clipped.  
- **Перекрытие текста** – adjust `spaceSize` or the font size if the label collides with other graphics.  
- **Производительность** – for very large images, consider disposing of `Pen`, `Font`, and `Brush` objects after use to free resources.

## Conclusion
Поздравляем! Теперь вы знаете **как добавить выноски** к изображению с помощью Aspose.Drawing для .NET. Feel free to experiment with different positions, colors, and fonts to match your visual style.

## FAQs

### Can I use Aspose.Drawing for other types of illustrations?
Да, Aspose.Drawing supports a wide range of drawing operations for various types of illustrations.

### Is Aspose.Drawing compatible with different image formats?
Absolutely! Aspose.Drawing supports popular image formats like PNG, JPEG, GIF, and more.

### Where can I find more examples and documentation?
Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).

### How do I get support if I encounter issues?
Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) for community support.

### Can I try Aspose.Drawing before purchasing?
Certainly! Get started with a free trial [here](https://releases.aspose.com/).

**Additional Q&A**

**Q: Can I change the callout line style (dashed, dotted)?**  
A: Yes—simply configure the `Pen.DashStyle` property before drawing the line.

**Q: Is it possible to add a background color to the callout label?**  
A: Absolutely. Create a `SolidBrush` with your desired color and fill a rectangle behind the text before calling `DrawString`.

**Q: How do I ensure the callout looks the same on high‑DPI displays?**  
A: Set `graphics.PageUnit = GraphicsUnit.Pixel` (as shown) and use vector‑based measurements to keep scaling consistent.

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}