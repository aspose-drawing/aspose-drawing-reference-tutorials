---
date: 2026-08-01
description: Узнайте, как сохранить bitmap в PNG, используя solid brush в Aspose.Drawing
  для .NET. Используйте solid brush для заполнения фигур и создания яркой графики.
keywords:
- save bitmap as png
- export bitmap to png
- fill shape solid color
- bitmap to png conversion
lastmod: 2026-08-01
linktitle: Solid Brushes в Aspose.Drawing
og_description: Сохраните bitmap в PNG, используя solid brushes в Aspose.Drawing.
  Этот пошаговый учебник показывает, как создать bitmap, заполнить фигуры solid color
  и экспортировать результат в без потерь PNG‑файл для проектов .NET 6+.
og_image_alt: Guide showing how to save a bitmap as PNG using solid brushes in Aspose.Drawing
og_title: Сохранить bitmap в PNG с помощью Solid Brushes – руководство Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  headline: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  name: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image canvas. The `Bitmap` class
      is Aspose.Drawing's top‑level object that stores pixel data in a mutable buffer.
      You can specify width, height, and pixel format when constructing it.
  - name: Create Graphics Object
    text: A `Graphics` object provides drawing methods for the bitmap. The `Graphics`
      class acts as a drawing surface linked to a `Bitmap`. All subsequent drawing
      commands (lines, shapes, text) are routed through this object.
  - name: Choose a Solid Brush
    text: Select a colour for the brush; in this example we use a vivid blue. The
      `SolidBrush` class defines a brush that paints with a single, uniform colour.
      It is ideal for filling shapes where a flat colour is required.
  - name: Fill Shapes with Brush
    text: Use the brush to paint an ellipse (or any other shape) on the bitmap. `FillEllipse`
      draws an ellipse filled with the specified brush. The `FillEllipse` method of
      the `Graphics` object draws an ellipse filled with the supplied `SolidBrush`.
      You can replace it with `FillRectangle`, `FillPolygon`, etc.
  - name: Save the Result as PNG
    text: Export the bitmap to a PNG file on disk. `Save` writes the image to a file
      in the chosen format. The `Save` method writes the bitmap to the specified path
      using `ImageFormat.Png`. This operation preserves the alpha channel, ensuring
      transparent backgrounds remain intact. Repeat these steps, customiz
  type: HowTo
- questions:
  - answer: Absolutely—methods like `FillRectangle`, `FillPolygon`, or `DrawPath`
      work with the same solid brush.
    question: Can I use a different shape instead of an ellipse?
  - answer: Replace the file extension in `Save` and use `ImageFormat.Jpeg` (e.g.,
      `bitmap.Save("output.jpg", ImageFormat.Jpeg);`).
    question: How do I change the output format to JPEG?
  - answer: Yes—create separate `SolidBrush` instances for each colour and call the
      appropriate `Fill*` methods sequentially.
    question: Is it possible to draw multiple shapes with different brushes in one
      bitmap?
  - answer: It's best practice to wrap them in `using` statements or call `Dispose()`
      to free unmanaged resources.
    question: Do I need to dispose of the `Graphics` and `Bitmap` objects?
  - answer: Aspose.Drawing is cross‑platform; the same code runs on Linux and macOS
      when targeting .NET Core or .NET 5+.
    question: Will this work on Linux/macOS with .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- solid brush
title: Сохранить bitmap в PNG с помощью solid brushes в Aspose.Drawing
url: /ru/net/lines-curves-and-shapes/solid-brushes/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сохранить растровое изображение как PNG со сплошными кистями в Aspose.Drawing

## Введение

В этом руководстве вы узнаете **как сохранить растровое изображение как PNG** с помощью сплошных кистей в библиотеке Aspose.Drawing для .NET. Независимо от того, создаёте ли вы настольную утилиту, веб‑службу, генерирующую значки, или движок отчётности, которому нужны чёткие PNG‑ресурсы, нижеописанные шаги позволят вам от пустого холста перейти к готовому PNG‑файлу всего за несколько строк кода. Мы рассмотрим весь процесс, объясним, почему сплошные кисти — идеальный выбор для однородных заливок, и покажем, как поддерживать код чистым и кроссплатформенным.

## Быстрые ответы
- **Что означает «save bitmap as png»?** Это экспорт объекта `Bitmap` в без потерь PNG‑файл на диск.  
- **Какой класс создаёт сплошную кисть?** `SolidBrush` из пространства имён `Aspose.Drawing.Brushes`.  
- **Можно ли изменить цвет кисти?** Да — передайте любой `Color` (включая значения ARGB) в конструктор `SolidBrush`.  
- **Нужна ли лицензия для продакшна?** Пробная версия подходит для оценки; для продакшн‑развёртываний требуется коммерческая лицензия.  
- **Совместим ли этот подход с .NET 6+?** Абсолютно — Aspose.Drawing полностью поддерживает .NET 5, .NET 6 и более новые версии.

## Что такое «save bitmap as png»?

Сохранение растрового изображения как PNG преобразует массив пикселей в памяти в без потерь PNG‑файл, сохраняющий прозрачность и точные цветовые значения. **Save bitmap as PNG** — распространённая операция, когда нужен переносимый формат изображения, который браузеры и графические редакторы могут читать без потери качества.

## Почему использовать сплошные кисти для сохранения растрового изображения как PNG?

Сплошные кисти обеспечивают один единственный, однородный цвет, который мгновенно заполняет любую векторную форму, устраняя необходимость в сложных градиентах, когда нужен лишь плоский цвет. Использование сплошных кистей с Aspose.Drawing также задействует движок рендеринга, способный обрабатывать изображения размером до **10 000 × 10 000 пикселей**, при этом потребление памяти остаётся ниже **200 МБ**, что делает его подходящим для высокоразрешённых ресурсов.

## Предварительные требования

Прежде чем приступить к руководству, убедитесь, что у вас есть следующие предварительные требования:

- Aspose.Drawing для .NET: загрузите и установите библиотеку из [Aspose.Drawing for .NET Documentation](https://reference.aspose.com/drawing/net/).
- Интегрированная среда разработки (IDE): настройте рабочую .NET‑среду разработки, например Visual Studio, на вашем компьютере.

Теперь, когда всё готово, перейдём к реализации.

## Импорт пространств имён

Директивы `using` импортируют необходимые типы в область видимости.

`Aspose.Drawing` содержит основные графические классы, а `System.Drawing` предоставляет определения цветов и класс `SolidBrush`.

```csharp
using System.Drawing;
```

## Как сохранить растровое изображение как PNG со сплошными кистями

В этом разделе описан полный рабочий процесс: создание холста bitmap, получение графической поверхности, создание экземпляра `SolidBrush` с нужным цветом, заполнение одной или нескольких фигур и, наконец, вызов `Save` для записи изображения в PNG‑файл. Код работает кроссплатформенно на .NET 6 и более новых версиях.

### Шаг 1: Создать Bitmap

`Bitmap` представляет собой холст изображения в памяти.

`Bitmap` — объект верхнего уровня в Aspose.Drawing, который хранит данные пикселей в изменяемом буфере. При создании можно указать ширину, высоту и формат пикселей.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Шаг 2: Создать объект Graphics

Объект `Graphics` предоставляет методы рисования для bitmap.

Класс `Graphics` служит поверхностью рисования, связанной с `Bitmap`. Все последующие команды рисования (линии, фигуры, текст) проходят через этот объект.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Шаг 3: Выбрать сплошную кисть

Выберите цвет кисти; в этом примере используется ярко‑синий.

Класс `SolidBrush` определяет кисть, рисующую одним, однородным цветом. Он идеален для заполнения фигур, где требуется плоский цвет.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
```

### Шаг 4: Заполнить фигуры кистью

Используйте кисть для рисования эллипса (или любой другой фигуры) на bitmap.

`FillEllipse` рисует эллипс, заполненный указанной кистью. Метод `FillEllipse` объекта `Graphics` рисует эллипс, заполненный переданным `SolidBrush`. Вы можете заменить его на `FillRectangle`, `FillPolygon` и т.д., чтобы создавать разные геометрические формы.

```csharp
graphics.FillEllipse(brush, 100, 100, 800, 600);
```

### Шаг 5: Сохранить результат как PNG

Экспортируйте bitmap в PNG‑файл на диск.

`Save` записывает изображение в файл выбранного формата. Метод `Save` сохраняет bitmap по указанному пути, используя `ImageFormat.Png`. Эта операция сохраняет альфа‑канал, обеспечивая сохранность прозрачных фонов.

```csharp
bitmap.Save("Your Document Directory" + @"Brushes\Solid_out.png");
```

Повторите эти шаги, подбирая цвета и формы в соответствии с визуальным дизайном вашего приложения.

## Распространённые проблемы и решения

| Проблема | Почему происходит | Решение |
|----------|-------------------|---------|
| **Ошибка «File not found»** при сохранении | Целевая папка не существует | Убедитесь, что каталог (`Your Document Directory\Brushes`) создан перед вызовом `Save`. |
| **Неправильные цвета** | Используется `KnownColor`, который соответствует системной теме | Используйте `Color.FromArgb` для точных RGBA‑значений. |
| **Потеря прозрачности** | Используется формат пикселей без альфа‑канала | Сохраняйте `PixelFormat.Format32bppPArgb`, как показано, чтобы сохранить альфа‑канал. |

## Часто задаваемые вопросы

**В: Можно ли использовать другую форму вместо эллипса?**  
**О:** Абсолютно — методы `FillRectangle`, `FillPolygon` или `DrawPath` работают с той же сплошной кистью.

**В: Как изменить формат вывода на JPEG?**  
**О:** Замените расширение файла в `Save` и используйте `ImageFormat.Jpeg` (например, `bitmap.Save("output.jpg", ImageFormat.Jpeg);`).

**В: Можно ли нарисовать несколько фигур с разными кистями в одном bitmap?**  
**О:** Да — создайте отдельные экземпляры `SolidBrush` для каждого цвета и последовательно вызывайте соответствующие методы `Fill*`.

**В: Нужно ли освобождать объекты `Graphics` и `Bitmap`?**  
**О:** Рекомендуется оборачивать их в конструкции `using` или вызывать `Dispose()`, чтобы освободить неуправляемые ресурсы.

**В: Будет ли это работать на Linux/macOS с .NET Core?**  
**О:** Aspose.Drawing кроссплатформенен; тот же код работает на Linux и macOS при целевой платформе .NET Core или .NET 5+.

**Последнее обновление:** 2026-08-01  
**Тестировано с:** Aspose.Drawing 24.12 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Сохранить растровое изображение как PNG и нарисовать замкнутые кривые с Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Сохранить растровое изображение как PNG с использованием трансформаций в Aspose.Drawing](/drawing/net/coordinate-transformations/local-transformation/)
- [Как обрезать изображение до PNG с Aspose.Drawing для .NET](/drawing/net/image-editing/cropping/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}