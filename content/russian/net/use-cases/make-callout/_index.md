---
title: Создание выносок в Aspose.Drawing
linktitle: Создание выносок в Aspose.Drawing
second_title: Aspose.Drawing .NET API — альтернатива System.Drawing.Common
description: Улучшите иллюстрации в своих документах с помощью Aspose.Drawing для .NET! Узнайте шаг за шагом, как добавлять выноски для более четких и информативных визуальных эффектов.
type: docs
weight: 10
url: /ru/net/use-cases/make-callout/
---
## Введение
Добро пожаловать в наше пошаговое руководство по созданию выносок в Aspose.Drawing для .NET! Если вы хотите улучшить иллюстрации своих документов с помощью выносок, вы попали по адресу. В этом уроке мы разобьем процесс на управляемые шаги, используя библиотеку Aspose.Drawing.
## Предварительные условия
Прежде чем приступить к изучению руководства, убедитесь, что у вас есть следующие предварительные условия:
- Базовые знания языка программирования C#.
-  Установлена библиотека Aspose.Drawing. Вы можете скачать его[здесь](https://releases.aspose.com/drawing/net/).
- Документ или изображение, в которое вы хотите добавить выноски.
## Импортировать пространства имен
Убедитесь, что в ваш проект включены необходимые пространства имен:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Шаг 1. Загрузите изображение
 Начните с загрузки изображения, куда вы хотите добавить выноски. Заменять`"Your Document Directory"` и`"gears.png"` с вашим фактическим каталогом и именем файла изображения.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Ваш код здесь
}
```
## Шаг 2. Создайте графический объект
 Создать`Graphics` объект из изображения для выполнения операций рисования.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Шаг 3. Определите позиции выносок
Определите начальную и конечную точки для каждой выноски, а также значение выноски и единицу измерения.
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
## Шаг 4: Нарисуйте выноски
 Внедрить`DrawCallOut` метод рисования выносок на изображении.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Шаг 5: Сохраните изображение
Сохраните изображение с выносками в нужную директорию.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Рисовать исходный код выноски
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
## Заключение

Поздравляем! Вы успешно добавили выноски к своему изображению с помощью Aspose.Drawing для .NET. Не стесняйтесь экспериментировать с различными позициями и значениями, чтобы дополнительно настроить выноски.

## Часто задаваемые вопросы

### Могу ли я использовать Aspose.Drawing для других типов иллюстраций?

Да, Aspose.Drawing поддерживает широкий спектр операций рисования для различных типов иллюстраций.

### Совместим ли Aspose.Drawing с различными форматами изображений?

Абсолютно! Aspose.Drawing поддерживает популярные форматы изображений, такие как PNG, JPEG, GIF и другие.

### Где я могу найти больше примеров и документации?

 Изучите полную документацию[здесь](https://reference.aspose.com/drawing/net/).

### Как мне получить поддержку, если у меня возникнут проблемы?

 Посетить[Форум Aspose.Рисование](https://forum.aspose.com/c/diagram/17) для поддержки сообщества.

### Могу ли я попробовать Aspose.Drawing перед покупкой?

 Конечно! Начните работу с бесплатной пробной версии[здесь](https://releases.aspose.com/).