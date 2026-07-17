---
date: 2026-07-17
description: Узнайте, как предотвратить переполнение текста, задав выравнивание текста
  в Aspose.Drawing для .NET, и добавить текст к изображениям. Пошаговое руководство
  с примерами.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Установка выравнивания текста с помощью Aspose.Drawing для .NET
og_description: Предотвратите переполнение текста, задав выравнивание текста в Aspose.Drawing
  для .NET. Узнайте, как нарисовать строку на изображении, центрировать текст в прямоугольнике
  и заменить System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Предотвращение переполнения текста – Установка выравнивания текста с помощью
  Aspose.Drawing для .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Предотвращение переполнения текста – Установка выравнивания текста с помощью
  Aspose.Drawing для .NET
url: /ru/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Предотвращение переполнения текста – Установка выравнивания текста с помощью Aspose.Drawing

## Введение

Когда вам нужно **предотвратить переполнение текста** при рендеринге графики в .NET, Aspose.Drawing предоставляет тонкий контроль над размещением текста, выравниванием и переносом. Будь то генератор бейджей, динамический отчет или любой вывод в виде изображения, умение управлять выравниванием текста гарантирует, что текст останется внутри заданного прямоугольника и будет выглядеть аккуратно. В этом руководстве мы пройдемся по созданию bitmap‑холста, настройке `StringFormat`, рисованию прямоугольника с центрированным текстом, обработке переполнения и, наконец, сохранению изображения.

## Быстрые ответы
- **Что означает «установка выравнивания текста»?** Это определяет, как текст позиционируется по горизонтали и вертикали внутри прямоугольника рисования.  
- **Какой класс управляет выравниванием?** `StringFormat` позволяет задать `Alignment` и `LineAlignment`.  
- **Можно ли нарисовать строку и прямоугольник одновременно?** Да — используйте `Graphics.DrawRectangle`, а затем `Graphics.DrawString`.  
- **Как предотвратить переполнение текста?** Отрегулируйте размер прямоугольника или вручную разбейте текст на несколько строк.  
- **Нужна ли лицензия для продакшн?** Для коммерческого использования Aspose.Drawing требуется платная лицензия, а не оценочная версия.

## Что такое **установка выравнивания текста** в Aspose.Drawing?

`set text alignment` настраивает горизонтальное (`StringAlignment`) и вертикальное (`LineAlignment`) размещение текста внутри `Rectangle` или области рисования. Регулируя эти свойства, вы контролируете, будет ли текст выровнен по левому краю, по центру, по правому краю, сверху, по середине или снизу, что обеспечивает точную компоновку в графике, бейджах и отчетах, генерируемых с помощью Aspose.Drawing.

## Почему стоит использовать Aspose.Drawing для выравнивания текста?

Aspose.Drawing устраняет ограничения GDI+, характерные для `System.Drawing.Common`. Он поддерживает **5 основных .NET рантаймов** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 и .NET 7 – и может рендерить изображения до **4000 × 4000 px** (≈ 100 MB), не исчерпывая память. Анти‑алиасинг, масштабирование под высокие DPI и полная совместимость с Linux‑контейнерами позволяют генерировать пиксельно‑точную графику в любой среде развертывания.

## Предварительные требования

1. **Библиотека Aspose.Drawing** – скачайте её [здесь](https://releases.aspose.com/drawing/net/).  
2. **Среда разработки** – Visual Studio 2022 (или любой другой IDE для C#).  
3. **Базовые знания .NET** – вы должны быть уверены в работе с проектами C# и пакетами NuGet.

## Импорт пространств имён

Для начала подключите необходимые пространства имён. Они дают доступ к графике, рендерингу текста и примитивам рисования.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Как предотвратить переполнение текста с помощью Aspose.Drawing?

`Bitmap` — класс, представляющий изображение, хранящееся в памяти, а `RectangleF` определяет область прямоугольника с плавающей точкой для рисования. Используя `StringFormat` с `Trimming`, установленным в `StringTrimming.EllipsisCharacter`, лишние символы автоматически заменяются многоточием, гарантируя, что текст не выйдет за пределы прямоугольника. Предварительное измерение строки позволяет решить, уменьшать ли прямоугольник или разбивать текст на несколько строк, обеспечивая чистую компоновку без выхода за границы.

Загрузите ваш bitmap, задайте подходящий `RectangleF` и используйте `StringFormat` с `Trimming = StringTrimming.EllipsisCharacter`, чтобы автоматически отрезать лишние символы. Для полного контроля измерьте строку с помощью `Graphics.MeasureString` и уменьшите прямоугольник или разбейте текст на строки перед рисованием. Такой подход гарантирует, что ни один символ не выйдет за визуальные границы.

## Шаг 1: Создание объектов Bitmap и Graphics  

`Bitmap` представляет изображение в памяти, а `Graphics` предоставляет методы рисования для этого bitmap. Создание bitmap дает вам холст, на котором можно рисовать. Объект `Graphics` — это поверхность рисования, и мы включаем высококачественный рендеринг текста с помощью `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Шаг 2: Определение **StringFormat** и стилей  

`StringFormat` задаёт параметры компоновки текста, такие как выравнивание, межстрочный интервал и обрезка. Здесь мы **устанавливаем выравнивание текста**, конфигурируя экземпляр `StringFormat`. Мы также подготавливаем кисти, пера и шрифт, которые будут использоваться при рисовании строки.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Шаг 3: Создание и форматирование текста – **как нарисовать строку** и **нарисовать прямоугольник с текстом**

`Graphics.DrawString` выводит текст на холст, а `Graphics.DrawRectangle` рисует форму прямоугольника. Мы формируем текст, определяем прямоугольник, который его будет содержать, а затем рисуем как границу прямоугольника, так и саму строку.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Как обрабатывать переполнение текста

Если предоставленный `text` превышает границы прямоугольника, у вас есть два распространённых варианта:

1. **Изменить размер прямоугольника** – увеличить `rectangle.Width` или `rectangle.Height`.  
2. **Разбить текст** – разделить строку на строки, которые помещаются, затем вызвать `DrawString` для каждой строки с скорректированными координатами Y.

## Как нарисовать строку на изображении с помощью Aspose.Drawing?

`Graphics.DrawString` рисует указанный текст, используя шрифт и параметры форматирования. Создайте объект `Graphics` из вашего bitmap, затем вызовите `DrawString` с подготовленным `StringFormat`. Этот один вызов отрисовывает текст точно там, где вам нужно, учитывая выравнивание, обрезку и любые трансформационные матрицы, которые вы применили. Добавление высококачественного режима рендеринга гарантирует чёткость вывода на дисплеях с высоким DPI.

## Как центрировать текст в прямоугольнике?

`StringAlignment` определяет горизонтальное выравнивание текста внутри прямоугольника компоновки. Установите `stringFormat.Alignment = StringAlignment.Center` и `stringFormat.LineAlignment = StringAlignment.Center`. Это центрирует текст по горизонтали и вертикали внутри прямоугольника, что идеально подходит для бейджей, кнопок или наложения меток. Центрированное размещение работает последовательно при разных размерах изображений и настройках DPI, обеспечивая сбалансированный визуальный вид.

## Как достичь вертикального выравнивания текста?

`LineAlignment` управляет вертикальным размещением текста внутри прямоугольника. Используйте `stringFormat.LineAlignment` со значениями `StringAlignment.Near`, `Center` или `Far`, чтобы разместить текст вверху, посередине или внизу прямоугольника. При необходимости комбинируйте это с `Graphics.TranslateTransform`, если нужно вращать текст, сохраняя вертикальное выравнивание. Регулировка вертикального выравнивания гарантирует, что многострочные блоки располагаются точно там, где вы ожидаете, даже после трансформаций.

## Шаг 4: Сохранение результата – **добавление текста к изображению**

Наконец, запишите bitmap на диск. Этот шаг демонстрирует **добавление текста к изображению** одним вызовом.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Распространённые проблемы и их решения

| Проблема | Решение |
|----------|---------|
| **Текст выглядит размытым** | Убедитесь, что установлено `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`. |
| **Текст обрезается** | Увеличьте размер прямоугольника или включите логику переноса слов, измерив размер строки (`Graphics.MeasureString`). |
| **Шрифт не найден** | Проверьте, установлен ли шрифт на хост‑машине, или внедрите приватный шрифт с помощью `PrivateFontCollection`. |
| **Неожиданные цвета** | Перепроверьте цвета кистей и перьев; помните, что `Color.FromKnownColor` использует системные предопределённые цвета. |

## Часто задаваемые вопросы

**В1: Совместим ли Aspose.Drawing со всеми версиями .NET?**  
О1: Да, Aspose.Drawing разработан так, чтобы быть совместимым с широким спектром версий .NET, обеспечивая гибкость для разработчиков.

**В2: Можно ли дополнительно настроить стиль шрифта?**  
О2: Абсолютно! Регулируйте параметры объекта `Font`, чтобы получить нужный размер, стиль и семейство шрифта.

**В3: Как обработать переполнение текста внутри заданного прямоугольника?**  
О3: Вы можете управлять переполнением, изменяя размер прямоугольника или реализуя собственную логику обработки длинного текста.

**В4: Есть ли другие параметры форматирования в Aspose.Drawing?**  
О4: Да, Aspose.Drawing предоставляет обширный набор инструментов для работы с графикой, включая различные варианты форматирования текста, фигур и многое другое.

**В5: Где можно получить дополнительную поддержку по Aspose.Drawing?**  
О5: Изучите форум Aspose.Drawing [здесь](https://forum.aspose.com/c/drawing/44) для получения помощи от сообщества и обсуждений.

**Дополнительные вопросы и ответы**

**В: Как нарисовать строку без окружающего прямоугольника?**  
О: Просто опустите вызов `DrawRectangle` и передайте желаемую позицию `PointF` в `Graphics.DrawString`.

**В: Можно ли вращать текст, сохраняя выравнивание?**  
О: Да — примените трансформацию `Matrix` к объекту `Graphics` перед рисованием, а затем сбросьте её.

**В: Можно ли экспортировать изображение как JPEG вместо PNG?**  
О: Достаточно изменить расширение файла в `bitmap.Save` и, при необходимости, указать `ImageFormat.Jpeg`.

---

**Последнее обновление:** 2026-07-17  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Похожие руководства

- [Как рисовать текст с Aspose.Drawing для .NET](/drawing/net/text-and-fonts/draw-text/)
- [Добавление текста к изображениям в Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [Как рисовать текст и шрифты с Aspose.Drawing для .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}