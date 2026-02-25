---
date: 2026-02-25
description: Узнайте, как установить выравнивание текста в Aspose.Drawing для .NET
  и добавить текст к изображениям. Пошаговое руководство с примерами.
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Установить выравнивание текста с помощью Aspose.Drawing для .NET
url: /ru/net/text-and-fonts/format-text/
weight: 11
---

 the file extension in `bitmap.Save` and optionally specify `ImageFormat.Jpeg`.

Translate.

Then footer:

**Last Updated:** 2026-02-25 => keep date.

**Tested With:** Aspose.Drawing 24.11 for .NET

**Author:** Aspose

Then closing shortcodes.

Make sure to keep markdown formatting.

Now produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установка выравнивания текста в Aspose.Drawing

## Введение

Когда речь идет о **set text alignment** и форматировании текста в ваших .NET‑приложениях, Aspose.Drawing является основной библиотекой для разработчиков, которым нужна точность, производительность и богатый набор API. Независимо от того, создаёте ли вы движок отчетности, динамический генератор бейджей или любое графически‑интенсивное решение, возможность контролировать расположение текста внутри фигур делает ваш вывод аккуратным и профессиональным. В этом руководстве мы пройдем весь процесс — от создания bitmap‑холста до рисования прямоугольника с текстом, обработки переполнения и окончательного сохранения изображения.

## Быстрые ответы
- **Что означает “set text alignment”?** Это определяет, как текст позиционируется горизонтально и вертикально внутри прямоугольника рисования.  
- **Какой класс управляет выравниванием?** `StringFormat` позволяет задать `Alignment` и `LineAlignment`.  
- **Можно ли одновременно нарисовать строку и прямоугольник?** Да — используйте `Graphics.DrawRectangle`, а затем `Graphics.DrawString`.  
- **Как предотвратить переполнение текста?** Отрегулируйте размер прямоугольника или вручную разбейте текст на несколько строк.  
- **Нужна ли лицензия для продакшн?** Для использования не в оценочных целях требуется коммерческая лицензия Aspose.Drawing.

## Что такое **set text alignment** в Aspose.Drawing?

`set text alignment` относится к конфигурации горизонтального (`StringAlignment`) и вертикального (`LineAlignment`) позиционирования текста внутри `Rectangle` или любой области рисования. Настраивая эти параметры, вы контролируете, будет ли текст выровнен по левому краю, по центру, по правому краю, сверху, по середине или снизу.

## Почему стоит использовать Aspose.Drawing для выравнивания текста?

- **Полная совместимость с .NET** — работает с .NET Framework, .NET Core и .NET 5/6+.  
- **Пиксель‑идеальная отрисовка** — антиалиасинг и поддержка high‑DPI из коробки.  
- **Отсутствие ограничений GDI+** — в отличие от `System.Drawing.Common`, Aspose.Drawing работает в Linux‑контейнерах без нативных зависимостей.  
- **Богатое стилизование** — комбинируйте шрифты, кисти, пера и пользовательские объекты `StringFormat` для сложных макетов.

## Предварительные требования

1. **Библиотека Aspose.Drawing** — скачайте её [здесь](https://releases.aspose.com/drawing/net/).  
2. **Среда разработки** — Visual Studio 2022 (или любой IDE для C#).  
3. **Базовые знания .NET** — вы должны быть уверены в работе с проектами C# и пакетами NuGet.

## Импорт пространств имён

Чтобы начать, подключите необходимые пространства имён. Они дают доступ к графике, рендерингу текста и базовым примитивам рисования.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Шаг 1: Создание объектов Bitmap и Graphics  

Создание bitmap предоставляет холст, на котором можно рисовать. Объект `Graphics` является поверхностью рисования, и мы включаем высококачественный рендеринг текста с помощью `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Шаг 2: Определение **StringFormat** и стилей  

Здесь мы **set text alignment** путем настройки экземпляра `StringFormat`. Мы также подготавливаем кисти, пера и шрифт, которые будут использоваться при рисовании строки.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Шаг 3: Создание и форматирование текста — **how to draw string** и **draw rectangle with text**

Мы формируем текст, определяем прямоугольник, который будет его содержать, а затем рисуем как границу прямоугольника, так и саму строку.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Как обработать переполнение текста

Если предоставленный `text` превышает границы прямоугольника, у вас есть два распространённых варианта:

1. **Изменить размер прямоугольника** — увеличить `rectangle.Width` или `rectangle.Height`.  
2. **Разбить текст** — разделить строку на подходящие строки, затем вызвать `DrawString` для каждой строки с скорректированными координатами Y.

## Шаг 4: Сохранение результата — **add text to image**

Наконец, сохраняем bitmap на диск. Этот шаг демонстрирует **add text to image** в одном вызове.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Распространённые проблемы и решения

| Проблема | Решение |
|----------|----------|
| **Текст выглядит размытым** | Убедитесь, что установлено `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`. |
| **Текст обрезается** | Увеличьте размер прямоугольника или включите перенос слов, измерив размер строки (`Graphics.MeasureString`). |
| **Шрифт не найден** | Проверьте, установлен ли шрифт на хост‑машине, или внедрите частный шрифт с помощью `PrivateFontCollection`. |
| **Неожиданные цвета** | Проверьте цвета кисти и пера; помните, что `Color.FromKnownColor` использует системные цвета. |

## Часто задаваемые вопросы

### Q1: Совместим ли Aspose.Drawing со всеми версиями .NET?

A1: Да, Aspose.Drawing разработан так, чтобы быть совместимым с широким спектром версий .NET, обеспечивая гибкость для разработчиков.

### Q2: Можно ли дальше настроить стиль шрифта?

A2: Абсолютно! Настройте параметры объекта `Font`, чтобы получить нужный размер, стиль и семейство шрифта.

### Q3: Как обработать переполнение текста внутри заданного прямоугольника?

A3: Вы можете управлять переполнением, изменяя размер прямоугольника или реализуя собственную логику для обработки длинного текста.

### Q4: Есть ли другие варианты форматирования в Aspose.Drawing?

A4: Да, Aspose.Drawing предоставляет обширный набор инструментов для работы с графикой, включая различные варианты форматирования текста, фигур и многое другое.

### Q5: Где можно найти дополнительную поддержку по Aspose.Drawing?

A5: Изучите форум Aspose.Drawing [здесь](https://forum.aspose.com/c/drawing/44) для получения поддержки от сообщества и обсуждений.

**Additional Q&A**

**Q: Как нарисовать строку без окружающего прямоугольника?**  
A: Опустите вызов `DrawRectangle` и передайте желаемое расположение `PointF` в `Graphics.DrawString`.

**Q: Можно ли повернуть текст, сохранив выравнивание?**  
A: Да — примените трансформацию `Matrix` к объекту `Graphics` перед рисованием, затем сбросьте её после.

**Q: Можно ли экспортировать изображение как JPEG вместо PNG?**  
A: Просто измените расширение файла в `bitmap.Save` и, при необходимости, укажите `ImageFormat.Jpeg`.

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}