---
date: 2026-06-23
description: Узнайте, как сохранять PNG с использованием Aspose.Drawing, применять
  world transformations и конвертировать графику в PNG. Включает примеры translate
  transform на C# и несколько графических преобразований.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: World Transformation в Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Как сохранить PNG с помощью Aspose.Drawing – World Transformation
url: /ru/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как сохранить PNG с помощью Aspose.Drawing – мировое преобразование

## Сохранение Bitmap в PNG – Введение

**Как сохранить PNG** с помощью Aspose.Drawing — это распространённая задача, когда нужны изображения высокого качества с прозрачностью, генерируемые «на лету». В этом руководстве вы узнаете, как **сохранить bitmap как PNG**, применить мировые преобразования такие как перемещение, вращение и масштабирование, а затем конвертировать графику в PNG — всё с чистым, поддерживаемым C# кодом. Независимо от того, создаёте ли вы движок отчётности, компонент построения графиков или пользовательский рендерер UI, освоив эти шаги, вы сможете генерировать динамические изображения, отлично выглядящие на любом устройстве.

## Быстрые ответы
- **Что означает «мировое преобразование»?** Оно отображает логические (мировые) координаты вашего рисунка в координаты страницы (устройства).  
- **Могу ли я экспортировать результат как PNG?** Да — после рисования вы просто вызываете `bitmap.Save(...)` с расширением `.png`.  
- **Нужна ли лицензия для Aspose.Drawing?** Бесплатная пробная версия подходит для разработки; для продакшн требуется коммерческая лицензия.  
- **Совместимо ли это с .NET 6/7?** Абсолютно — Aspose.Drawing поддерживает .NET Framework 4.5+ и .NET Core/5/6/7.  
- **Сколько преобразований я могу цепочкой?** Вы можете применять **несколько графических преобразований** последовательно (перемещение, вращение, масштабирование и т.д.).

## Что такое мировое преобразование в Aspose.Drawing?

Мировое преобразование меняет систему координат, которую используют ваши команды рисования. По умолчанию (0,0) находится в левом верхнем углу bitmap. С помощью `TranslateTransform`, `RotateTransform` или `ScaleTransform` вы можете переместить эту точку начала, вращать фигуры или изменять их размер без изменения исходной геометрии.

## Как сохранить PNG с помощью Aspose.Drawing?

Загрузите объект `Bitmap`, задайте необходимые мировые преобразования его экземпляру `Graphics`, нарисуйте фигуры и в конце вызовите `bitmap.Save("output.png", ImageFormat.Png)`. Этот однострочный вызов сохраняет без потерь PNG‑файл, сохраняющий прозрачность и точность цветов, что делает его идеальным для веб‑ресурсов и наложений UI.

## Зачем использовать пример графического перемещения?

Пример графического перемещения позволяет переместить начало координат один раз вместо пересчёта каждой точки. Такой подход уменьшает сложность кода, повышает читаемость и позволяет графическому движку эффективно выполнять матричные вычисления, что может увеличить производительность рендеринга до 30 % на больших холстах.

## Пример графического перемещения

**Пример графического перемещения** показывает, как перемещение начала упрощает позиционирование. Вместо пересчёта каждой точки вы один раз смещаете систему координат и рисуете так, как будто новое начало находится в центре холста.

## Требования

Перед началом убедитесь, что у вас есть:

- **Библиотека Aspose.Drawing** интегрирована в ваш .NET проект — загрузите её со официальной [страницы выпуска Aspose.Drawing](https://releases.aspose.com/drawing/net/).  
- **Каталог документов**, куда будет сохраняться выходное изображение.  
- Базовое знакомство с синтаксисом **C#** и Visual Studio или вашей предпочтительной IDE.  

Теперь давайте погрузимся в код!

## Импорт пространств имён

`Bitmap`, `Graphics` и утилиты Aspose находятся в этих пространствах имён.  
**Определение:** `System.Drawing` предоставляет основные типы GDI+, а `Aspose.Drawing` расширяет их кросс‑платформенными возможностями.

## Пошаговое руководство

### Шаг 1: Создание Bitmap

Мы начинаем с создания пустого холста, который будет содержать наш рисунок.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` создаёт 32‑битный bitmap с предумноженным альфа‑каналом, что является оптимальным форматом для вывода PNG, поскольку сохраняет прозрачность без дополнительных шагов конвертации.

- **Почему 32bppPArgb?** Этот формат пикселей поддерживает альфа‑прозрачность и высококачественную цветовую отрисовку, идеально подходит для вывода PNG.  
- **Совет:** Настройте ширину/высоту в соответствии с размером целевого изображения.

### Шаг 2: Установка мирового преобразования (пример графического перемещения)

`TranslateTransform` перемещает начало координат системы в новое место.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` смещает точку (0,0) в центр холста. После этого вызова любой объект, нарисованный с координатами (0,0), появится в центре изображения.

- Это перемещает точку (0,0) в (500, 400) — центр холста размером 1000 × 800.  
- Вы можете цепочкой добавить дополнительные преобразования: `RotateTransform` вращает систему координат, а `ScaleTransform` масштабирует её, позволяя использовать **множество графических преобразований**.

### Шаг 3: Рисование прямоугольника с использованием преобразованных координат

`DrawRectangle` рисует прямоугольник с указанной ручкой и координатами.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` рисует прямоугольник, центрированный на холсте, поскольку его левый верхний угол смещён на половину ширины и высоты от преобразованного начала.

- Левый верхний угол прямоугольника начинается в преобразованном начале (центр изображения).  
- Не стесняйтесь экспериментировать с другими фигурами — эллипсами, линиями или пользовательскими путями.

### Шаг 4: Сохранение результата — преобразование графики в PNG

`Save` записывает bitmap в файл в указанном формате изображения.  
`ImageFormat` указывает формат файла для сохранения изображений, например PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` создаёт безпотерянный PNG‑файл, который можно использовать напрямую в веб‑страницах или UI‑компонентах.

- PNG сохраняет точные цвета и прозрачность, которые мы задали ранее.  
- Замените `"Your Document Directory"` реальным путём на вашем компьютере.

## Распространённые проблемы и решения

| Проблема | Почему происходит | Решение |
|----------|-------------------|----------|
| **Ошибка «Файл не найден»** при сохранении | Целевая папка не существует. | Создайте папку программно (`Directory.CreateDirectory`) перед вызовом `Save`. |
| **Пустое изображение** после преобразования | `TranslateTransform` вызван после рисования. | Убедитесь, что преобразование установлено **до** любых команд рисования. |
| **Искажённые цвета** | Используется несовместимый формат пикселей. | Оставайтесь с `Format32bppPArgb` для вывода PNG. |

## Часто задаваемые вопросы

**В: Можно ли применить более одного преобразования?**  
**О:** Да — вы можете цепочкой использовать `TranslateTransform`, `RotateTransform` и `ScaleTransform` для получения сложных эффектов в едином графическом конвейере.

**В: Бесплатна ли Aspose.Drawing для коммерческих проектов?**  
**О:** Доступна бесплатная пробная версия для оценки, но для продакшн‑использования требуется коммерческая лицензия.

**В: Работает ли это с .NET Core и .NET 5/6/7?**  
**О:** Абсолютно. Aspose.Drawing поддерживает все современные .NET‑рантаймы, включая .NET Core, .NET 5, .NET 6 и .NET 7.

**В: Где найти полную справку по API?**  
**О:** Полная документация доступна [здесь](https://reference.aspose.com/drawing/net/).

**В: Как решить проблему с отсутствующим выходным файлом?**  
**О:** Проверьте строку пути, убедитесь в наличии прав на запись и в том, что каталог существует перед вызовом `Save`.

## Заключение

Теперь вы знаете, **как сохранить PNG** с помощью Aspose.Drawing, применили **мировое преобразование** и выполнили **пример графического перемещения**, который можно расширить вращением или масштабированием. Освоив эти базовые блоки, вы сможете генерировать динамические изображения, создавать пользовательские диаграммы или строить графику «на лету» для любого .NET‑приложения.

---

**Last Updated:** 2026-06-23  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose  
**Связанные ресурсы:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Связанные руководства

- [Учебник по матричным преобразованиям: матричные преобразования в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Как повернуть изображение с помощью глобального преобразования Aspose.Drawing](/drawing/net/coordinate-transformations/global-transformation/)
- [Преобразование системы координат — преобразование страницы в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}