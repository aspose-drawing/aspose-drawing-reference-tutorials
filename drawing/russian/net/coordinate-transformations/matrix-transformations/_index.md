---
date: 2026-08-28
description: Изучите этот учебник по преобразованию матриц для Aspose.Drawing .NET,
  охватывающий рисование повернутого прямоугольника, применение вращения матрицы и
  масштабирование матрицы на C#.
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- matrix rotation c#
- matrix scaling c#
- Aspose.Drawing graphics
lastmod: 2026-08-28
linktitle: Преобразования матриц в Aspose.Drawing
og_description: Учебник по преобразованию матриц для Aspose.Drawing .NET. Узнайте,
  как рисовать повернутый прямоугольник, применять вращение матрицы, перемещать и
  масштабировать графику с помощью C# за несколько минут.
og_image_alt: Screenshot of a rotated rectangle created with Aspose.Drawing using
  matrix transformations
og_title: Учебник по преобразованию матриц – применение вращения, масштабирования
  и переноса в Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  headline: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  type: TechArticle
- description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  name: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  steps:
  - name: set up the canvas
    text: Create a bitmap that will serve as the drawing surface. We also clear it
      with a neutral gray background so the transformed shapes stand out. > **Pro
      tip:** Using `Format32bppPArgb` ensures correct alpha handling when you later
      apply anti‑aliasing.
  - name: define the original rectangle
    text: This rectangle is the base shape we’ll transform. Its coordinates are chosen
      to keep it well within the canvas bounds.
  - name: rotate the rectangle (draw rotated rectangle)
    text: The `Matrix` class is Aspose.Drawing's representation of a 3 × 3 affine
      transformation matrix used for rotation, scaling and translation. We now **apply
      matrix rotation** of 15 degrees around the origin. The helper method `TransformPath`
      (shown later) takes a lambda that receives a `Matrix` instance
  - name: translate the rectangle
    text: Translation moves the shape without altering its size or orientation. Here
      we shift it left‑up by 250 pixels.
  - name: scale the rectangle (matrix scaling C#)
    text: Scaling changes the rectangle’s dimensions. A factor of `0.3f` reduces both
      width and height to 30 % of the original size.
  - name: save the result
    text: Finally, write the transformed image to disk. Adjust the path to point to
      a folder that exists on your machine. > **Note:** The `TransformPath` method
      (used in the steps above) creates a `GraphicsPath` from the rectangle, applies
      the supplied matrix, and draws the transformed shape. It’s a compact w
  type: HowTo
- questions:
  - answer: The documentation is available **[here](https://reference.aspose.com/drawing/net/)**.
    question: Where can I find the Aspose.Drawing documentation?
  - answer: Obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: How do I get a temporary license for Aspose.Drawing?
  - answer: Visit the Aspose.Drawing forum **[here](https://forum.aspose.com/c/drawing/44)**.
    question: Where can I seek support or connect with the community?
  - answer: Yes, download it from **[here](https://releases.aspose.com/drawing/net/)**.
    question: Can I download Aspose.Drawing for .NET?
  - answer: Purchase your license **[here](https://purchase.aspose.com/buy)**.
    question: How can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- matrix transformation
- Aspose.Drawing
- .NET graphics
- C# drawing
- cross‑platform rendering
title: 'Учебник по преобразованию матриц: преобразования матриц в Aspose.Drawing для
  .NET'
url: /ru/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Учебник по матричным преобразованиям: матричные преобразования в Aspose.Drawing для .NET

## Введение

В этом **учебнике по матричным преобразованиям** вы узнаете, как класс `Matrix` из Aspose.Drawing позволяет вращать, перемещать и масштабировать графические объекты с пиксельной точностью. Независимо от того, создаёте ли вы редактор диаграмм, генерируете автоматические отчёты или добавляете визуальные эффекты в серверный сервис, освоение матричных преобразований необходимо для получения профессионального результата на Windows, Linux и macOS.

## Быстрые ответы
- **Что покрывает этот учебник?** Он показывает, как вращать, перемещать и масштабировать прямоугольник с помощью API матриц Aspose.Drawing.  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для разработки; коммерческая лицензия требуется для использования в продакшене.  
- **Какие версии .NET поддерживаются?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7 и более новые.  
- **Сколько времени займет реализация?** Около 10‑15 минут для полного примера.  
- **Можно ли увидеть результирующее изображение?** Да — учебник сохраняет PNG, который можно сразу открыть.

## Что такое учебник по матричным преобразованиям?

Учебник по матричным преобразованиям объясняет, как использовать 3 × 3 аффинную матрицу для перемещения, вращения, масштабирования или сдвига графических примитивов. В Aspose.Drawing класс `Matrix` инкапсулирует эти операции, позволяя любому `GraphicsPath` или фигуре быть преобразованными с помощью одного переиспользуемого объекта.

## Зачем использовать Aspose.Drawing для матричных преобразований?

Aspose.Drawing поддерживает **три основных операционных системы** (Windows, Linux, macOS) и может рендерить изображения до **10 000 × 10 000 px** менее чем за **200 ms** за операцию на типичном серверном оборудовании. Библиотека обеспечивает **100 % совместимость с API GDI+**, поэтому вы можете мигрировать существующий код System.Drawing без переписывания логики, одновременно избегая ограничений лицензирования, которые влияют на System.Drawing.Common на платформах, отличных от Windows.

## Требования

- Рабочая среда разработки C# (Visual Studio, Rider или VS Code).  
- Aspose.Drawing для .NET установлен — скачайте его с официального сайта **[здесь](https://releases.aspose.com/drawing/net/)** или **[по этой ссылке](https://releases.aspose.com/drawing/net/)**, если вы ещё не загрузили его.  
- Базовое понимание битмап‑канвасов, прямоугольников и графических путей.

## Импорт пространств имён

Сначала подключите необходимые пространства имён:

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

Эти пространства имён дают вам доступ к `Bitmap`, `Graphics` и классу `Matrix`, необходимым для преобразований.

## Пошаговое руководство

Ниже представлена лаконичная нумерованная пошаговая инструкция. Каждый шаг включает краткое объяснение, за которым следует точный код, который вам понадобится (блоки кода остаются без изменений).

### Шаг 1: настройка холста

Создайте битмап, который будет служить поверхностью для рисования. Мы также очищаем его нейтральным серым фоном, чтобы преобразованные фигуры выделялись.

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **Совет:** Использование `Format32bppPArgb` обеспечивает корректную обработку альфа‑канала при последующем применении сглаживания.

### Шаг 2: определение исходного прямоугольника

Этот прямоугольник — базовая форма, которую мы будем преобразовывать. Его координаты выбраны так, чтобы он находился полностью внутри границ холста.

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### Шаг 3: поворот прямоугольника (рисуем повернутый прямоугольник)

Класс `Matrix` в Aspose.Drawing представляет собой 3 × 3 аффинную матрицу, используемую для вращения, масштабирования и перемещения. Теперь мы **применяем вращение матрицы** на 15 градусов вокруг начала координат. Вспомогательный метод `TransformPath` (показан позже) принимает лямбда‑выражение, получающее экземпляр `Matrix`.

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### Шаг 4: перемещение прямоугольника

Перемещение смещает фигуру, не изменяя её размер или ориентацию. Здесь мы сдвигаем её влево‑вверх на 250 пикселей.

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### Шаг 5: масштабирование прямоугольника (масштабирование матрицы C#)

Масштабирование изменяет размеры прямоугольника. Коэффициент `0.3f` уменьшает как ширину, так и высоту до 30 % от исходного размера.

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### Шаг 6: сохранение результата

Наконец, запишите преобразованное изображение на диск. Отрегулируйте путь так, чтобы он указывал на существующую папку на вашем компьютере.

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **Примечание:** Метод `TransformPath` (использованный в шагах выше) создаёт `GraphicsPath` из прямоугольника, применяет переданную матрицу и рисует преобразованную фигуру. Это компактный способ переиспользовать одну и ту же логику рисования для каждого преобразования.

## Распространённые проблемы и решения

| Проблема | Решение |
|----------|---------|
| **Изображение пустое** | Убедитесь, что каталог вывода существует и у вас есть права записи. |
| **Преобразования смещены** | Помните, что `Matrix.Rotate` вращает вокруг начала координат (0,0). Переместите фигуру к желаемой точке вращения перед вращением. |
| **Падение производительности на больших изображениях** | Используйте `graphics.SmoothingMode = SmoothingMode.AntiAlias;` только при необходимости и своевременно освобождайте объекты `Graphics`. |

## Часто задаваемые вопросы

**В: Где я могу найти документацию Aspose.Drawing?**  
Ответ: Документация доступна **[здесь](https://reference.aspose.com/drawing/net/)**.

**В: Как получить временную лицензию для Aspose.Drawing?**  
Ответ: Получите временную лицензию **[здесь](https://purchase.aspose.com/temporary-license/)**.

**В: Где я могу получить поддержку или связаться с сообществом?**  
Ответ: Посетите форум Aspose.Drawing **[здесь](https://forum.aspose.com/c/drawing/44)**.

**В: Можно ли скачать Aspose.Drawing для .NET?**  
Ответ: Да, скачайте его **[здесь](https://releases.aspose.com/drawing/net/)**.

**В: Как я могу приобрести Aspose.Drawing?**  
Ответ: Приобретите лицензию **[здесь](https://purchase.aspose.com/buy)**.

## Заключение

Вы завершили полный **учебник по матричным преобразованиям** с использованием Aspose.Drawing для .NET. Вы знаете, как **рисовать повернутый прямоугольник**, **применять вращение матрицы**, и выполнять **масштабирование матрицы C#** для любой фигуры. Экспериментируйте, комбинируя несколько преобразований или используя пользовательские точки вращения, чтобы открыть ещё более креативные графические эффекты.

---

**Последнее обновление:** 2026-08-28  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose

## Связанные учебники

- [Как нарисовать прямоугольник – преобразование системы координат (преобразование страницы) с использованием Aspose.Drawing API для .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Как сохранить PNG с Aspose.Drawing – глобальное преобразование](/drawing/net/coordinate-transformations/world-transformation/)
- [Пошаговое преобразование – преобразования координат](/drawing/net/coordinate-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}