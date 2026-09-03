---
date: 2026-09-03
description: Узнайте, как создать text overlay на images, используя Aspose.Drawing
  для .NET. Это пошаговое руководство покажет, как добавить text к image, draw text
  on image и измерять string size эффективно.
keywords:
- create text overlay
- add text to image
- draw text on image
- measure string size
- calculate text dimensions
lastmod: 2026-09-03
linktitle: Добавление text на images в Aspose.Drawing
og_description: Узнайте, как создать text overlay на images, используя Aspose.Drawing
  для .NET. Это руководство охватывает добавление text к image, draw text on image
  и измерение string size в несколько простых шагов.
og_image_alt: Tutorial showing how to create text overlay on images using Aspose.Drawing
  in .NET
og_title: Как создать text overlay на images с помощью Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create text overlay on images using Aspose.Drawing for
    .NET. This step‑by‑step guide shows you how to add text to image, draw text on
    image, and measure string size efficiently.
  headline: How to create text overlay on images with Aspose.Drawing
  type: TechArticle
- description: Learn how to create text overlay on images using Aspose.Drawing for
    .NET. This step‑by‑step guide shows you how to add text to image, draw text on
    image, and measure string size efficiently.
  name: How to create text overlay on images with Aspose.Drawing
  steps:
  - name: import namespaces
    text: 'Begin by importing the necessary namespaces into your C# project:'
  - name: load the image
    text: Here, we load the image from the specified file path and initialize the
      graphics object for further processing.
  - name: set text properties
    text: Define the text properties such as color, font, and padding. Adjust these
      parameters according to your preferences.
  - name: measure text size
    text: Calculate the required size for the text by measuring each word individually.
      This ensures proper placement and avoids text overlap.
  - name: draw text on image
    text: Now, position the text on the image based on the calculated size and draw
      it using the specified font and color.
  - name: save the image
    text: Save the modified image to your desired directory. This step‑by‑step guide
      demonstrates a straightforward process of adding text to images using Aspose.Drawing
      for .NET. Experiment with different fonts, colors, and text content to achieve
      the desired visual effect.
  type: HowTo
- questions:
  - answer: Measure the string width with `Graphics.MeasureString`, subtract it from
      the image width, divide by two, and use that X coordinate when calling `DrawString`.
    question: How do I center text horizontally on the image?
  - answer: Yes—use `StringFormat` with `FormatFlags.LineLimit` and pass a string
      containing `\n` to `DrawString`.
    question: Can I add multi‑line text with line breaks?
  - answer: Absolutely. Set the brush color using `Color.FromArgb(alpha, r, g, b)`
      where `alpha` controls opacity.
    question: Does Aspose.Drawing support transparent text?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- image processing
- Aspose.Drawing
- .NET graphics
title: Как создать text overlay на images с помощью Aspose.Drawing
url: /ru/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как создать текстовое наложение на изображениях с Aspose.Drawing

## Введение
Aspose.Drawing — это .NET API, предоставляющий расширенные возможности обработки изображений без зависимости от System.Drawing.Common. В динамичном мире разработки на .NET создание текстового наложения на изображения часто требуется — будь то добавление водяных знаков к фотографиям, подписи или генерация пользовательской графики. Этот учебник проведёт вас через весь процесс добавления текста к изображениям с использованием C# и Aspose.Drawing, чтобы вы могли реализовать решение за считанные минуты.

## Быстрые ответы
- **Какой основной класс для рисования?** `Graphics` из Aspose.Drawing обрабатывает все операции рисования.  
- **Нужна ли лицензия для разработки?** Бесплатная временная лицензия подходит для тестирования; полная лицензия требуется для продакшн.  
- **Какие форматы изображений поддерживаются?** Более 30 форматов, включая JPEG, PNG, BMP и GIF.  
- **Можно ли измерить размер текста перед рисованием?** Да — используйте `Graphics.MeasureString` для расчёта точных размеров.  
- **Совместим ли API с .NET 6?** Абсолютно, Aspose.Drawing нацелен на .NET Framework 4.5+ и .NET 5/6+.

## Что такое создание текстового наложения?
Создание текстового наложения относится к процессу отрисовки текстового содержимого поверх существующего растрового изображения, создавая единый комбинированный визуальный ресурс, который можно сохранить или отобразить. На практике текст становится частью пиксельных данных, позволяя использовать полученное изображение везде, где принимаются стандартные изображения, например на веб‑страницах, в отчётах или печатных материалах. Наложение может включать стилизацию, позиционирование и прозрачность для достижения желаемого визуального эффекта.

## Почему использовать Aspose.Drawing для этой задачи?
Aspose.Drawing поддерживает более 30 форматов изображений и может обрабатывать файлы размером более 500 МБ без загрузки всего изображения в память, обеспечивая до 2× более быструю отрисовку по сравнению с System.Drawing при работе с большими партиями. Его API полностью управляемый, что исключает зависимости от нативного кода и упрощает развертывание на Windows, Linux и macOS.

## Предварительные требования
Перед тем как приступить к учебнику, убедитесь, что у вас есть следующее:
1. **Библиотека Aspose.Drawing** – загрузите и установите её из [документации Aspose.Drawing для .NET](https://reference.aspose.com/drawing/net/).  
2. **Среда разработки** – Visual Studio 2022, Rider или любой IDE, поддерживающий .NET 6+.  
3. **Пример изображения** – любой файл JPEG/PNG, который вы хотите аннотировать.

Теперь давайте пошагово пройдём реализацию.

## Как создать текстовое наложение на изображении?
Вы начнёте с загрузки исходного битмапа в объект `Graphics`, затем определите шрифт, кисть и отступы. После измерения размеров текста, чтобы избежать обрезки, вы позиционируете прямоугольник и отрисовываете строку. Наконец, сохраняете изменённое изображение на диск. Ниже приведено краткое описание полной последовательности, которой вы будете следовать в детальных шагах ниже.

### Шаг 1: импорт пространств имён
Begin by importing the necessary namespaces into your C# project:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

### Шаг 2: загрузить изображение
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Here, we load the image from the specified file path and initialize the graphics object for further processing.

### Шаг 3: установить свойства текста
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Define the text properties such as color, font, and padding. Adjust these parameters according to your preferences.

### Шаг 4: измерить размер текста
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Calculate the required size for the text by measuring each word individually. This ensures proper placement and avoids text overlap.

### Шаг 5: нарисовать текст на изображении
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Now, position the text on the image based on the calculated size and draw it using the specified font and color.

### Шаг 6: сохранить изображение
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Save the modified image to your desired directory.

This step‑by‑step guide demonstrates a straightforward process of adding text to images using Aspose.Drawing for .NET. Experiment with different fonts, colors, and text content to achieve the desired visual effect.

## Распространённые проблемы и решения
- **Текст выглядит размытым** — убедитесь, что разрешение изображения (DPI) соответствует размеру шрифта; используйте `Graphics.SmoothingMode = SmoothingMode.AntiAlias`.  
- **Неожиданное обрезание** — проверьте, что измеренная ширина строки не превышает границы изображения; при необходимости добавьте отступ или уменьшите размер шрифта.  
- **Лицензия не найдена** — разместите файл лицензии в каталоге исполняемого файла или задайте её программно с помощью `new License().SetLicense("Aspose.Drawing.lic")`.

## Часто задаваемые вопросы
### Совместим ли Aspose.Drawing со всеми форматами изображений?
Aspose.Drawing поддерживает широкий спектр форматов изображений, включая популярные JPEG, PNG и GIF. Смотрите полный список в [документации](https://reference.aspose.com/drawing/net/).

### Могу ли я использовать Aspose.Drawing в коммерческих проектах?
Да, Aspose.Drawing подходит как для личных, так и для коммерческих проектов. Подробнее о лицензировании на [странице покупки](https://purchase.aspose.com/buy).

### Доступны ли временные лицензии для тестирования?
Да, временную лицензию для тестирования можно получить, перейдя по ссылке [Temporary License](https://purchase.aspose.com/temporary-license/).

### Где я могу найти поддержку сообщества для Aspose.Drawing?
Общайтесь с сообществом и получайте поддержку на [форуме Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

### Как начать работу с Aspose.Drawing?
Скачайте библиотеку со [страницы загрузки Aspose.Drawing](https://releases.aspose.com/drawing/net/) и изучите обширную [документацию](https://reference.aspose.com/drawing/net/).

**Additional Q&A**

**Вопрос: Как центрировать текст по горизонтали на изображении?**  
**Ответ:** Измерьте ширину строки с помощью `Graphics.MeasureString`, вычтите её из ширины изображения, разделите на два и используйте полученную координату X при вызове `DrawString`.

**Вопрос: Можно ли добавить многострочный текст с разрывами строк?**  
**Ответ:** Да — используйте `StringFormat` с `FormatFlags.LineLimit` и передайте строку, содержащую `\n`, в `DrawString`.

**Вопрос: Поддерживает ли Aspose.Drawing прозрачный текст?**  
**Ответ:** Абсолютно. Установите цвет кисти с помощью `Color.FromArgb(alpha, r, g, b)`, где `alpha` управляет непрозрачностью.

## Заключение
Aspose.Drawing упрощает задачи манипуляции изображениями в .NET, предлагая надёжный набор инструментов, который может **обрабатывать более 30 форматов изображений** и **работать с файлами размером более 500 МБ** без полной загрузки в память. Добавление текстового наложения — лишь один из примеров его универсальности, позволяющий эффективно создавать водяные знаки, подписи и пользовательскую графику.

---

**Последнее обновление:** 2026-09-03  
**Тестировано с:** Aspose.Drawing 24.12 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Как рисовать текст и шрифты с Aspose.Drawing для .NET](/drawing/net/text-and-fonts/)
- [Как рисовать текст с Aspose.Drawing для .NET](/drawing/net/text-and-fonts/draw-text/)
- [Как рисовать прямоугольник – трансформация системы координат (трансформация страницы) с использованием Aspose.Drawing API для .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}