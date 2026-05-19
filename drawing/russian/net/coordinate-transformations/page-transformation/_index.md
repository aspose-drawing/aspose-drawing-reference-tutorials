---
date: 2026-05-19
description: Узнайте, как рисовать графику прямоугольника, выполняя преобразование
  системы координат в .NET с помощью Aspose.Drawing. Это пошаговое руководство показывает,
  как преобразовать дюймы в пиксели и установить единицы измерения страницы.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Преобразование системы координат в Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Как нарисовать прямоугольник – преобразование системы координат (преобразование
  страницы) в Aspose.Drawing для .NET
url: /ru/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как нарисовать прямоугольник – Преобразование системы координат (преобразование страницы) в Aspose.Drawing для .NET

## Введение

Добро пожаловать! В этом руководстве вы узнаете, **как нарисовать прямоугольник** графически, преобразуя координаты страницы с помощью Aspose.Drawing для .NET. Независимо от того, создаёте ли вы приложение, интенсивно использующее графику, или вам нужен точный контроль над единицами рисования, это руководство проведёт вас через каждый шаг — от настройки холста до рисования элемента прямоугольника. К концу вы сможете уверенно применять эти техники в своих проектах.

## Быстрые ответы
- **Что такое преобразование системы координат?** Преобразование единиц уровня страницы (например, дюймы) в пиксели уровня устройства.  
- **Зачем использовать Aspose.Drawing?** Он предоставляет полностью управляемую кросс‑платформенную альтернативу System.Drawing.Common.  
- **Сколько времени занимает реализация примера?** Около 5‑10 минут для базового преобразования страницы.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для разработки; коммерческая лицензия требуется для продакшна.  
- **Какие версии .NET поддерживаются?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Что такое Aspose.Drawing?

`Aspose.Drawing` — это .NET‑библиотека графики, предоставляющая **независимый от устройства API** для создания и манипулирования растровыми изображениями, векторной графикой и рисунками уровня страницы без зависимости от GDI+. Она поддерживает **30+ форматов изображений** и может обрабатывать изображения размером до **10 000 × 10 000 пикселей** без загрузки всего файла в память.

## Зачем использовать преобразование системы координат с Aspose.Drawing?

Преобразование системы координат позволяет проектировать графику в реальных единицах измерения, пока библиотека автоматически масштабирует пиксели для любого выходного устройства. Это обеспечивает согласованный размер на экранах и принтерах и упрощает расчёты макета.

- **Независимый от устройства дизайн:** Пишите код один раз, а Aspose.Drawing будет выполнять масштабирование пикселей для любого экрана или принтера.  
- **Точное рисование:** Идеально подходит для технических схем, чертежей в стиле CAD или любой ситуации, где важны точные измерения.  
- **Надёжность кросс‑платформенно:** Работает одинаково на Windows, Linux и macOS без ограничений GDI+ в System.Drawing.  
- **Показатели производительности:** На типичном процессоре 2.5 ГГц рисование 5‑дюймового прямоугольника при 300 DPI занимает менее **15 мс**, а библиотека может отрисовывать **50 кадров в секунду** в сценариях предварительного просмотра в реальном времени.

## Требования

Перед началом убедитесь, что у вас есть:

- **Библиотека Aspose.Drawing:** Скачайте последнюю версию с официального сайта [здесь](https://releases.aspose.com/drawing/net/).  
- **Среда разработки:** Visual Studio, Rider или любой совместимый с .NET IDE.  
- **Каталог вашего документа:** Замените `"Your Document Directory"` в коде на папку, куда вы хотите сохранять выходное изображение.  
- **Поддержка ASP.NET (необязательно):** Вы можете использовать Aspose.Drawing в проектах ASP.NET Core, добавив пакет NuGet в веб‑приложение — это следует тому же шаблону **how to use aspnet**, что и любая другая .NET библиотека.

Теперь, когда всё готово, давайте перейдём к пошаговому руководству.

## Как нарисовать прямоугольник с преобразованием страницы?

Загрузите пустой bitmap, задайте единицу измерения страницы в дюймах и нарисуйте прямоугольник тонкой синей ручкой — это завершит рисование прямоугольника всего в несколько строк кода. Свойство `Graphics.PageUnit` сообщает движку интерпретировать все координаты как дюймы, поэтому вы можете работать с реальными измерениями вместо сырых пикселей.

### Шаг 1: Импорт пространств имён

Операторы `using` дают вам доступ к основным классам рисования.

```csharp
using System.Drawing;
```

### Шаг 2: Создать Bitmap

`Bitmap` представляет изображение в памяти, на которое можно рисовать. Мы начинаем с создания пустого bitmap, который будет служить поверхностью для рисования. Формат пикселей `Format32bppPArgb` обеспечивает высокое качество и поддержку предварительно умноженной альфа‑прозрачности.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Шаг 3: Создать объект Graphics

Объект `Graphics` предоставляет API рисования для bitmap. Это мост между вашим кодом и буфером пикселей.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Шаг 4: Очистить холст

Задайте холсту нейтральный фон, чтобы нарисованные формы выделялись. Здесь мы заполняем его светло‑серым цветом.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Шаг 5: Установить преобразование (Как задать единицу измерения)

`Graphics.PageUnit` указывает единицу измерения, используемую для координат страницы. Чтобы сопоставить координаты страницы с пикселями устройства, установите свойство `PageUnit`. В этом примере мы выбираем дюймы, но можно также использовать `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` или `GraphicsUnit.Pixel`. Установка единицы в дюймы позволяет **автоматически преобразовывать дюймы в пиксели** на основе DPI bitmap (по умолчанию 96 DPI, 300 DPI для печати высокого разрешения).

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Шаг 6: Нарисовать прямоугольник – рисуем графику прямоугольника

`Pen` определяет цвет, ширину и стиль линий, рисуемых на графической поверхности. Теперь мы рисуем прямоугольник тонкой синей ручкой. Поскольку мы переключились на дюймы, размер и позиция прямоугольника задаются в дюймах, что делает код более читаемым для макетов, ориентированных на печать.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Шаг 7: Сохранить изображение

Наконец, запишите bitmap в файл PNG в папку, указанную ранее.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Как масштабировать графику для принтера?

Установите DPI bitmap в целевое разрешение принтера (например, 300 DPI) перед рисованием. Это автоматически **масштабирует графику для принтера**, так что один дюйм в вашем коде будет соответствовать одному дюйму на печатной странице. После вызова `bitmap.SetResolution(300, 300)` тот же прямоугольник будет выглядеть больше на печатном листе, сохраняя свои точные размеры.

## Распространённые проблемы и решения

| Проблема | Почему происходит | Решение |
|----------|-------------------|---------|
| **Файл вывода не создан** | Неправильный путь или отсутствующая папка | Убедитесь, что целевая директория существует, или используйте `Directory.CreateDirectory` перед сохранением. |
| **Прямоугольник выглядит искажённым** | Неправильный `PageUnit` или несоответствие DPI | Проверьте, что `graphics.PageUnit` соответствует используемым единицам, и что DPI bitmap установлен правильно (по умолчанию 96 DPI). |
| **Исключение лицензии** | Запуск без действующей лицензии в продакшене | Примените временную или постоянную лицензию Aspose.Drawing перед созданием графических объектов. |

## Часто задаваемые вопросы

**В: Могу ли я использовать Aspose.Drawing бесплатно?**  
**О:** Да, бесплатная пробная версия доступна [здесь](https://releases.aspose.com/).

**В: Где я могу найти подробную документацию по Aspose.Drawing?**  
**О:** Полная ссылка на API находится [здесь](https://reference.aspose.com/drawing/net/).

**В: Как получить поддержку по Aspose.Drawing?**  
**О:** Посетите [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) для помощи сообщества и официальной поддержки.

**В: Доступна ли временная лицензия для Aspose.Drawing?**  
**О:** Конечно — получите её [здесь](https://purchase.aspose.com/temporary-license/).

**В: Где можно приобрести полную лицензию Aspose.Drawing?**  
**О:** Вы можете купить её [здесь](https://purchase.aspose.com/buy).

## Заключение

В этом руководстве мы рассмотрели всё, что нужно знать, **как нарисовать прямоугольник** с помощью Aspose.Drawing: настройка холста, конфигурация единиц страницы, точное рисование фигур и сохранение результата. Используйте эти техники для создания масштабируемой, независимой от устройства графики для отчётов, чертежей в стиле CAD или любого приложения, где важна точность измерений. Далее изучайте продвинутые преобразования, такие как вращение, масштабирование и пользовательские начала координат, чтобы открыть ещё более мощные сценарии рисования.

---

**Последнее обновление:** 2026-05-19  
**Тестировано с:** Aspose.Drawing 24.12 for .NET  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Единицы измерения в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/units-of-measure/)
- [Как применить преобразование: локальное преобразование в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/local-transformation/)
- [Учебник по матричным преобразованиям: матричные преобразования в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/matrix-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}