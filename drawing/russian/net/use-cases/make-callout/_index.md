---
date: 2026-08-01
description: Узнайте, как добавить callouts к изображениям с помощью Aspose.Drawing
  для .NET – пошаговое руководство с шаблонами кода, tips и FAQs.
keywords:
- how to add callouts
- Aspose.Drawing callout tutorial
- .NET image annotation
lastmod: 2026-08-01
linktitle: Создание callouts в Aspose.Drawing
og_description: Узнайте, как добавить callouts в Aspose.Drawing для .NET. Этот учебник
  охватывает prerequisites, пошаговую implementation, tips и FAQs для разработчиков.
og_image_alt: Screenshot showing callout annotation on an image using Aspose.Drawing
og_title: Как добавить callouts с помощью Aspose.Drawing для .NET – Быстрое руководство
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to add callouts to images using Aspose.Drawing for .NET –
    step‑by‑step guide with code placeholders, tips, and FAQs.
  headline: How to Add Callouts with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of drawing operations for diagrams,
      charts, and custom graphics beyond simple callouts.
    question: Can I use Aspose.Drawing for other types of illustrations?
  - answer: Absolutely! Aspose.Drawing handles PNG, JPEG, GIF, BMP, TIFF, and many
      more formats.
    question: Is Aspose.Drawing compatible with different image formats?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find more examples and documentation?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      for community assistance and official support.
    question: How do I get support if I encounter issues?
  - answer: Certainly! Get started with a free trial [here](https://releases.aspose.com/).
    question: Can I try Aspose.Drawing before purchasing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- callout
- Aspose.Drawing
- .NET graphics
- image annotation
title: Как добавить callouts с помощью Aspose.Drawing для .NET
url: /ru/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как добавить выноски с помощью Aspose.Drawing для .NET

## Введение
Если вы ищете **как добавить выноски** к вашим изображениям или диаграммам с помощью Aspose.Drawing для .NET, вы попали в нужное место. В этом руководстве мы пройдем каждый шаг — от загрузки растрового изображения, создания холста `Graphics`, определения геометрии выноски до отрисовки стилизованных выносок — чтобы ваши визуальные материалы стали более понятными и информативными.

## Быстрые ответы
- **Какую библиотеку мне нужно?** Aspose.Drawing for .NET (доступна для загрузки с официального сайта).  
- **Какие версии .NET поддерживаются?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для разработки; коммерческая лицензия требуется для продакшна.  
- **Сколько времени занимает реализация?** Обычно менее 10 минут для базовой выноски.  
- **Можно ли настроить цвета и шрифты?** Да — всё управляется стандартными объектами GDI+ (Pen, Font, Brush).

## Что такое выноска?
Выноска — это графическая аннотация, сочетающая линию (или стрелку) с текстовой меткой для выделения определённой части изображения. Она обычно используется в технических диаграммах, скриншотах и презентациях, чтобы привлечь внимание к конкретному элементу, объяснить функцию или предоставить измерительные данные, делая визуальную коммуникацию более ясной и эффективной.

## Почему использовать Aspose.Drawing для выносок?
Aspose.Drawing разработан для высокопроизводительной обработки изображений и поддерживает широкий спектр форматов, что делает его идеальным для добавления выносок к большим или сложным графикам. Его память‑эффективная архитектура может обрабатывать файлы размером до **500 МБ** без загрузки всего растрового изображения в ОЗУ, а также предоставляет детальный контроль над графическими примитивами, цветами и отрисовкой текста, обеспечивая чёткие, профессионального вида аннотации.

## Предварительные требования
- Базовые знания языка программирования C#.  
- Библиотека Aspose.Drawing установлена. Вы можете скачать её [здесь](https://releases.aspose.com/drawing/net/).  
- Документ или изображение, к которому вы хотите добавить выноски.

## Импорт пространств имён
Следующие пространства имён предоставляют доступ к основным классам рисования:

`System.Drawing` предоставляет типы GDI+, такие как `Bitmap`, `Graphics`, `Pen`, `Font` и `Brush`. Импортируйте их перед началом кодирования.

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Как добавить выноски в Aspose.Drawing
Загрузите исходное изображение, создайте холст `Graphics`, определите начальные/конечные точки и вызовите вспомогательный метод, который рисует линию, стрелку и метку — всё в нескольких лаконичных инструкциях. Этот подход работает с файлами PNG, JPEG, BMP и GIF и позволяет полностью настраивать цвета, шрифты и стили линий.

## Шаг 1: Загрузка изображения
`Image` представляет растровое изображение и предоставляет методы для загрузки, сохранения и манипуляции данными битмапа. Начните с загрузки изображения, к которому вы хотите добавить выноски. Замените `"Your Document Directory"` и `"gears.png"` на ваш реальный каталог и имя файла изображения.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Шаг 2: Создание объекта Graphics
`Graphics` предоставляет методы рисования на поверхности для отрисовки фигур, текста и изображений на битмапе. Объект `Graphics`, полученный из изображения, позволяет выполнять операции рисования.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Шаг 3: Определение позиций выноски
`PointF` определяет точку в двумерном пространстве с использованием координат с плавающей запятой. Укажите начальную (якорную) и конечную (метка) точки для каждой выноски. Эти координаты должны находиться внутри границ изображения; иначе выноска будет обрезана.

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

## Шаг 4: Рисование выносок
Реализуйте метод `DrawCallOut` для отрисовки линии, необязательной стрелки и текстовой метки. Метод использует `Pen` для линии, `Font` для метки и `SolidBrush` для цветов заливки.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Шаг 5: Сохранение изображения
Сохраните аннотированный битмап на диск. Вы можете выбрать любой поддерживаемый формат, например PNG или JPEG.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Исходный код рисования выноски
Полный исходный код, объединяющий все шаги, находится в заполнителе ниже. Вставьте свои детали реализации там, где указано.

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

## Распространённые проблемы и советы
- **Неправильные координаты якоря** — убедитесь, что начальная и конечная точки находятся внутри границ изображения; иначе выноска может быть обрезана.  
- **Перекрытие текста** — отрегулируйте `spaceSize` или размер шрифта, если метка сталкивается с другими графическими элементами.  
- **Производительность** — для очень больших изображений рассмотрите возможность освобождения объектов `Pen`, `Font` и `Brush` после использования, чтобы освободить ресурсы.

## Заключение
Теперь у вас есть полный, готовый к продакшену шаблон для **как добавить выноски** к любому изображению с помощью Aspose.Drawing для .NET. Не стесняйтесь экспериментировать с разными цветами, стилями линий и семействами шрифтов, чтобы соответствовать вашему бренду.

## Часто задаваемые вопросы

**В: Можно ли использовать Aspose.Drawing для других типов иллюстраций?**  
О: Да, Aspose.Drawing поддерживает широкий спектр операций рисования для диаграмм, графиков и пользовательской графики, выходящей за рамки простых выносок.

**В: Совместим ли Aspose.Drawing с различными форматами изображений?**  
О: Абсолютно! Aspose.Drawing работает с PNG, JPEG, GIF, BMP, TIFF и многими другими форматами.

**В: Где можно найти больше примеров и документацию?**  
О: Изучите полную документацию [здесь](https://reference.aspose.com/drawing/net/).

**В: Как получить поддержку, если возникнут проблемы?**  
О: Посетите [форум Aspose.Drawing](https://forum.aspose.com/c/drawing/44) для получения помощи от сообщества и официальной поддержки.

**В: Можно ли попробовать Aspose.Drawing перед покупкой?**  
О: Конечно! Начните с бесплатной пробной версии [здесь](https://releases.aspose.com/).

---

**Последнее обновление:** 2026-08-01  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Как рисовать дуги и другие формы с помощью Aspose.Drawing для .NET](/drawing/net/lines-curves-and-shapes/)
- [Учебник по матричным преобразованиям: Матричные преобразования в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Как соединять пути с помощью Pen в Aspose.Drawing .NET](/drawing/net/pens/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}