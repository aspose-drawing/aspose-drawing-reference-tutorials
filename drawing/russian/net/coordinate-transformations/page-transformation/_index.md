---
date: 2026-11-04
description: Узнайте, как рисовать графику прямоугольника, выполняя преобразование
  системы координат в .NET с помощью API Aspose.Drawing. Это пошаговое руководство
  показывает, как преобразовать дюймы в пиксели и установить единицы страницы.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Преобразование системы координат в Aspose.Drawing
og_description: Узнайте, как рисовать графику прямоугольника, преобразуя дюймы в пиксели
  и устанавливая единицы страницы в Aspose.Drawing для .NET. Следуйте пошаговому руководству
  для точного преобразования страницы.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Как нарисовать прямоугольник с преобразованием страницы, используя Aspose.Drawing
  для .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Как нарисовать прямоугольник – преобразование системы координат (преобразование
  страницы) в Aspose.Drawing для .NET
url: /ru/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как нарисовать прямоугольник – преобразование системы координат (преобразование страницы) в Aspose.Drawing для .NET

## Введение

В этом руководстве вы узнаете **как нарисовать прямоугольник** графику, выполняя преобразование системы координат уровня страницы с помощью Aspose.Drawing для .NET. Независимо от того, создаёте ли вы движок отчётности, инструмент черчения в стиле CAD или любое приложение, требующее точных измерений реального мира, это руководство проведёт вас через каждый шаг — от создания bitmap до сохранения окончательного PNG. К концу вы будете уверенно конвертировать дюймы в пиксели, очищать фон холста и задавать единицы страницы для вывода, готового к печати.

## Быстрые ответы
- **Что такое преобразование системы координат?** Оно отображает единицы уровня страницы (например, дюймы) в пиксели уровня устройства, чтобы рисунки масштабировались корректно на любом выводном устройстве.  
- **Почему выбирают Aspose.Drawing?** Он предоставляет полностью управляемый, кросс‑платформенный графический API, заменяющий System.Drawing.Common и поддерживающий более 30 форматов изображений.  
- **Сколько времени занимает реализация примера?** Около 5‑10 минут для базового прямоугольника с преобразованием страницы.  
- **Нужна ли лицензия для разработки?** Бесплатная пробная версия подходит для разработки; коммерческая лицензия требуется для продакшн‑развертываний.  
- **Какие среды выполнения .NET поддерживаются?** .NET Framework 4.6+, .NET Core 3.1+, и .NET 5/6/7.

## Что такое Aspose.Drawing?

Aspose.Drawing — это .NET графическая библиотека, предоставляющая **device‑independent API** для создания и манипулирования растровыми изображениями, векторными объектами и рисунками уровня страницы без зависимости от GDI+. Она поддерживает **30+ форматов изображений** и может обрабатывать изображения размером до **10 000 × 10 000 пикселей**, при этом потребление памяти остаётся низким.

## Почему использовать преобразование системы координат с Aspose.Drawing?

Преобразование системы координат позволяет проектировать графику в реальных единицах измерения, в то время как библиотека автоматически обрабатывает масштабирование пикселей для любого выводного устройства. Этот подход гарантирует, что 5‑дюймовый прямоугольник будет печататься точно пять дюймов на принтере с 300 DPI и пропорционально отображаться на экране с 96 DPI, устраняя ошибки ручного преобразования.

- **Device‑independent design:** Пишите код один раз; Aspose.Drawing масштабирует его для экранов, принтеров или PDF.  
- **Precision drawing:** Идеально подходит для технических схем, инженерных чертежей или любых сценариев, где важны точные измерения.  
- **Cross‑platform reliability:** Работает последовательно на Windows, Linux и macOS без ограничений GDI+ в System.Drawing.  
- **Performance:** На типичном процессоре 2.5 GHz рисование 5‑дюймового прямоугольника при 300 DPI завершается менее чем за **15 мс**, а библиотека может отрисовывать **50 кадров в секунду** в сценариях реального времени.

## Предварительные требования

- **Aspose.Drawing library:** Скачайте последнюю версию с официального сайта [здесь](https://releases.aspose.com/drawing/net/).  
- **IDE:** Visual Studio, Rider или любой совместимый с .NET редактор.  
- **Output folder:** Замените `"Your Document Directory"` в примере кода на папку, куда вы хотите сохранить PNG.  
- **Optional ASP.NET support:** Вы можете добавить пакет NuGet в проект ASP.NET Core и использовать тот же API; шаблон следует типичному подходу **how to use aspnet** для .NET библиотек.

## Как нарисовать прямоугольник с преобразованием страницы?

Загрузите пустой bitmap, установите единицу страницы в дюймы и нарисуйте прямоугольник тонкой синей ручкой — это завершит рисование прямоугольника всего в несколько строк кода. Свойство `Graphics.PageUnit` указывает движку интерпретировать все координаты как дюймы, поэтому вы можете оперировать реальными измерениями вместо сырых пикселей, а библиотека автоматически **convert inches to pixels** на основе DPI bitmap.

### Шаг 1: импорт пространств имён

Операторы `using` предоставляют доступ к основным классам рисования.

```csharp
using System.Drawing;
```

### Шаг 2: создать bitmap

`Bitmap` — это контейнер изображения в памяти, на котором вы рисуете. Он хранит буфер пикселей и предоставляет методы для сохранения в файлы. Создание bitmap определяет размер холста и формат пикселей.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Шаг 3: создать объект Graphics

`Graphics` предоставляет поверхность рисования для bitmap. Он переводит высокоуровневые команды рисования (линии, фигуры, текст) в пиксельные операции над базовым bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Шаг 4: очистить фон холста

Очистка холста нейтральным цветом гарантирует, что ваши фигуры будут выделяться. В этом примере мы заполняем фон светло‑серым, что также демонстрирует технику **clear canvas background**.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Шаг 5: задать преобразование (как установить единицы измерения)

`Graphics.PageUnit` задаёт единицу измерения, используемую для координат страницы. Установка значения `GraphicsUnit.Inch` сообщает Aspose.Drawing автоматически **convert inches to pixels** на основе DPI bitmap (по умолчанию 96 DPI, 300 DPI для печати высокого разрешения). Вы также можете выбрать `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` или `GraphicsUnit.Pixel` в зависимости от требований к макету.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Шаг 6: нарисовать прямоугольник – рисование графики прямоугольника

`Pen` определяет цвет, ширину и стиль линий, рисуемых на поверхности Graphics. Используя тонкую синюю ручку, мы рисуем прямоугольник, размеры которого заданы в дюймах, делая код более читаемым для печатных макетов.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Шаг 7: сохранить bitmap как png

Наконец, запишите bitmap в файл PNG в папку, указанную ранее. Сохранение в PNG сохраняет без потерь качество и широко поддерживается на разных платформах.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Как масштабировать графику для принтера?

Установите DPI bitmap в целевое разрешение принтера (например, 300 DPI) перед рисованием. Это автоматически **scale graphics printer** вывод, так что один дюйм в вашем коде соответствует одному дюйму на печатной странице, при этом логический размер прямоугольника остаётся неизменным. После вызова `bitmap.SetResolution(300, 300)` тот же прямоугольник будет выглядеть больше на бумаге, но сохранит свои точные размеры.

## Распространённые проблемы и решения

| Проблема | Почему происходит | Решение |
|----------|-------------------|---------|
| **Файл вывода не создан** | Неправильный путь или отсутствующая папка | Убедитесь, что целевая директория существует, или вызовите `Directory.CreateDirectory` перед сохранением. |
| **Прямоугольник выглядит искажённым** | Несоответствие `PageUnit` или DPI | Проверьте, что `graphics.PageUnit` соответствует требуемой единице, и что DPI bitmap установлен корректно (по умолчанию 96 DPI, 300 DPI для печати). |
| **Исключение лицензии** | Запуск без действующей лицензии в продакшн | Примените временную или постоянную лицензию Aspose.Drawing перед созданием объектов Graphics. |

## Часто задаваемые вопросы

**Q: Можно ли использовать Aspose.Drawing бесплатно?**  
A: Да, бесплатная пробная версия доступна [здесь](https://releases.aspose.com/).

**Q: Где можно найти подробную документацию по Aspose.Drawing?**  
A: Полная справка по API находится [здесь](https://reference.aspose.com/drawing/net/).

**Q: Как получить поддержку для Aspose.Drawing?**  
A: Посетите [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) для помощи сообщества и официальной поддержки.

**Q: Доступна ли временная лицензия для Aspose.Drawing?**  
A: Конечно — получите её [здесь](https://purchase.aspose.com/temporary-license/).

**Q: Где можно приобрести полную лицензию Aspose.Drawing?**  
A: Вы можете купить её [здесь](https://purchase.aspose.com/buy).

## Заключение

Теперь вы знаете **как нарисовать прямоугольник** графику с преобразованием уровня страницы, используя Aspose.Drawing для .NET. Установив единицу страницы в дюймы, очистив фон холста и сохранив результат в PNG, вы получаете точный, независимый от устройства вывод, подходящий как для отображения на экране, так и для печати высокого разрешения. Экспериментируйте с другими единицами, вращением или пользовательскими началами координат, чтобы раскрыть ещё более мощные сценарии рисования.

---

**Последнее обновление:** 2026-11-04  
**Тестировано с:** Aspose.Drawing 24.12 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Как установить единицу измерения в Aspose.Drawing для .NET – Единицы измерения](/drawing/net/coordinate-transformations/units-of-measure/)
- [Глобальное преобразование](/drawing/net/coordinate-transformations/global-transformation/)
- [Пошаговое преобразование – Преобразования координат](/drawing/net/coordinate-transformations/step-by-step-transformation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}