---
date: 2026-09-23
description: Узнайте, как добавить текст на изображение с использованием Aspose.Drawing
  for .NET. Создавайте изображения с текстом, добавляйте текст в bitmap и сохраняйте
  bitmap как PNG с custom fonts.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Как добавить текст с Aspose.Drawing
og_description: Узнайте, как добавить текст на изображение с помощью Aspose.Drawing
  for .NET. Этот учебник показывает, как создавать изображения с текстом, добавлять
  текст в bitmap и сохранять bitmap как PNG с custom fonts.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Добавление текста на изображение с Aspose.Drawing for .NET – Краткое руководство
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Как добавить текст на изображение с помощью Aspose.Drawing for .NET
url: /ru/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как рисовать текст на изображении с помощью Aspose.Drawing для .NET

## Введение

В этом пошаговом руководстве вы узнаете **как рисовать текст на изображении** с помощью Aspose.Drawing для .NET. Независимо от того, нужно ли вам создать *динамичное изображение с текстом*, добавить текст к существующему битмапу или сгенерировать графику с пользовательскими шрифтами, это руководство проведёт вас через каждый шаг, чтобы вы могли начать рисовать текст за считанные минуты. Библиотека поддерживает более 30 методов GDI+, работает на Windows, Linux и macOS и имеет **ноль внешних зависимостей**, что делает её надёжным выбором для серверной генерации изображений.

## Быстрые ответы
- **Какая библиотека используется?** Aspose.Drawing for .NET  
- **Основная задача?** Нарисовать текст на изображении (создать изображение с текстом)  
- **Ключевой метод?** `Graphics.DrawString` (нарисовать строку на изображении)  
- **Формат вывода?** PNG (сохранить битмап как PNG)  
- **Требования?** .NET среда разработки и библиотека Aspose.Drawing  

## Что такое рисование текста с помощью Aspose.Drawing?

Рисование текста с помощью Aspose.Drawing означает использование совместимого с GDI+ API библиотеки для отрисовки Unicode‑строк на растровом холсте. Метод `Graphics.DrawString` записывает текст в битмап, позволяя управлять шрифтом, цветом, выравниванием и сглаживанием. Такой подход позволяет генерировать изображения высокого качества без установки System.Drawing.Common.

## Почему стоит использовать Aspose.Drawing для добавления текста к изображениям?

Aspose.Drawing предлагает надёжный, кросс‑платформенный способ отрисовки текста на изображениях без необходимости в нативных библиотеках GDI+, обеспечивая одинаковое качество и производительность на любой операционной системе. Он поддерживает продвинутое сглаживание, Unicode‑символы и пользовательские шрифты, а также бесшовно интегрируется с .NET‑приложениями, что делает его идеальным как для серверной генерации изображений, так и для настольных инструментов.

- **Надёжность кросс‑платформенности** – работает на Windows, Linux и macOS.  
- **Продвинутая отрисовка** – сглаживание и субпиксельное сглаживание текста для чёткого вывода.  
- **Отсутствие внешних зависимостей** – библиотека включает всё необходимое для *создания изображения с текстом*.

## Предварительные требования

Перед тем как приступить, убедитесь, что у вас есть:

- **Aspose.Drawing for .NET** – скачайте её из [документации Aspose.Drawing](https://reference.aspose.com/drawing/net/).  
- **IDE для .NET** такой как Visual Studio или VS Code.

## Импорт пространств имён

Начните с импорта необходимых пространств имён:

Эти пространства имён предоставляют основные типы GDI+, такие как `Bitmap`, `Graphics` и утилиты для отрисовки текста.  
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Шаг 1: создание объектов bitmap и graphics

`Bitmap` — это контейнер растрового изображения Aspose.Drawing для пиксельных данных, а `Graphics` предоставляет методы рисования для отрисовки фигур и текста на нём.

`Bitmap` представляет изображение в памяти, тогда как `Graphics` предоставляет методы рисования для отрисовки на этом bitmap.  
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Здесь мы создаём `Bitmap`, который будет хранить окончательное изображение, и объект `Graphics`, позволяющий рисовать на нём. Подсказка по сглаживанию обеспечивает плавный вид текста.

## Шаг 2: настройка brush, pen и font

`Brush` определяет цвет заливки, `Pen` — контур фигур, а `Font` задаёт тип шрифта, размер и стиль для отрисовки текста.

`Brush` заполняет фигуры цветом, `Pen` обводит их, а `Font` определяет тип шрифта и размер для отрисовки текста.  
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** определяет цвет текста.  
- **Pen** используется позже для рисования прямоугольника вокруг текста (необязательно).  
- **Font** задает тип шрифта, размер и стиль для операции *draw string on image*.

## Шаг 3: определение текста и прямоугольника

`Rectangle` определяет ограничивающий прямоугольник, в котором будет размещён текст, задавая координаты X/Y и ширину/высоту.

`Rectangle` указывает позицию и размер прямоугольной области, используемой здесь для ограничения отрисованного текста.  
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` определяет, где будет размещён текст. Отрегулируйте координаты и размеры в соответствии с вашим макетом.

## Шаг 4: рисование прямоугольника и текста

`Graphics.DrawString` отображает указанный текст внутри заданного прямоугольника, используя предоставленные шрифт и кисть.

`Graphics.DrawString` выводит строку текста внутри указанного прямоугольника, используя заданные шрифт и кисть.  
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Сначала мы обводим область синим прямоугольником, затем **добавляем текст в bitmap** вызовом `DrawString`. Это ядро *drawing text* на изображении.

## Шаг 5: сохранение результата

Изображение сохраняется как файл PNG, удовлетворяя требование *save bitmap as PNG*.  
Замените путь‑заполнитель реальным каталогом, где вы хотите хранить файл.

`bitmap.Save` записывает изображение в файл в выбранном формате, например PNG.  
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Распространённые сценарии использования

- **Создание сертификатов** с персонализированными именами.  
- **Создание миниатюр с водяным знаком** для веб‑галерей.  
- **Построение динамических диаграмм** с метками или аннотациями.  

## Устранение неполадок и советы

- **Шрифт не найден?** Убедитесь, что шрифт установлен на хост‑машине, или используйте частную коллекцию шрифтов.  
- **Текст обрезан?** Увеличьте размер прямоугольника или уменьшите размер шрифта.  
- **Проблемы с производительностью?** По возможности переиспользуйте один и тот же объект `Graphics` для нескольких операций рисования.

## Часто задаваемые вопросы

**Q: Как изменить формат вывода на JPEG?**  
A: Замените расширение `.png` на `.jpg` в методе `Save` и при желании укажите `ImageCodecInfo` для качества JPEG.

**Q: Можно ли рисовать многострочный текст?**  
A: Да, включите символы переноса строки (`\n`) в строку или используйте `StringFormat` с `FormatFlags.LineLimit`.

**Q: Есть ли способ измерить размер текста перед отрисовкой?**  
A: Используйте `Graphics.MeasureString`, чтобы получить точные размеры отрисованного текста.

**Q: Поддерживает ли Aspose.Drawing Unicode‑символы?**  
A: Абсолютно. Предоставьте шрифт, содержащий необходимые глифы, и библиотека отрисует их корректно.

**Q: Какая версия Aspose.Drawing использовалась для тестирования?**  
A: Примеры тестировались с Aspose.Drawing 24.11 для .NET.

---

**Последнее обновление:** 2026-09-23  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Создание графики Bitmap C# – Сохранение PNG‑изображения и работа с установленными шрифтами в Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Как сохранить bitmap как PNG с помощью API Aspose.Drawing для .NET](/drawing/net/image-editing/display/)
- [Текст на изображении](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}