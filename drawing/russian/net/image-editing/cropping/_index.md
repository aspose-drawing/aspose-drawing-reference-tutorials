---
date: 2026-10-13
description: Узнайте, как пакетно обрезать изображения до PNG с использованием Aspose.Drawing
  API, кросс‑платформенной альтернативы System.Drawing для разработчиков .NET.
keywords:
- how to batch crop
- crop images to png
- batch image cropping
- convert images to png
- batch crop images
lastmod: 2026-10-13
linktitle: Учебник по обрезке изображений – Aspose.Drawing
og_description: Узнайте, как быстро пакетно обрезать изображения до PNG с помощью
  Aspose.Drawing, кросс‑платформенной альтернативы System.Drawing для разработчиков
  .NET. Следуйте пошаговым инструкциям, чтобы эффективно обрабатывать несколько файлов.
og_image_alt: 'Developer guide: batch crop images to PNG using Aspose.Drawing .NET
  API'
og_title: Как пакетно обрезать изображения до PNG с Aspose.Drawing для .NET
schemas:
- author: Aspose
  dateModified: '2026-10-13'
  description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  headline: How to batch crop images to PNG using Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to batch crop images to PNG using the Aspose.Drawing API,
    the cross‑platform alternative to System.Drawing for .NET developers.
  name: How to batch crop images to PNG using Aspose.Drawing for .NET
  steps:
  - name: Create a bitmap canvas
    text: '`Bitmap` is Aspose.Drawing''s in‑memory representation of an image, providing
      pixel‑level access and format control. We start with a blank canvas sized to
      hold the cropped result. Adjust the width and height to match the dimensions
      of the area you plan to extract.'
  - name: Create a graphics object
    text: '`Graphics` is the drawing surface that lets you render shapes, text, or
      other images onto a Bitmap. A `Graphics` object lets us draw onto the canvas.
      The `InterpolationMode` controls how pixel values are calculated during scaling
      or transformation—`NearestNeighbor` works well for sharp edges.'
  - name: Load the image to crop
    text: '`Image` (or `Bitmap`) loads the source file into memory, ready for manipulation.
      Load the source image. Make sure the path points to an existing file; otherwise
      an exception will be thrown.'
  - name: Define source and destination rectangles
    text: '`Rectangle` objects describe the region of the source image to keep and
      where it should be placed on the destination canvas. The `sourceRectangle` tells
      the API which part of the original image to keep. Here we pick the top‑left
      50 × 40 pixel area. By assigning the same rectangle to `destinationRect'
  - name: Perform the crop operation
    text: '`Graphics.DrawImage` copies the defined portion of `image` onto our blank
      `bitmap`. This is the core **crop image to PNG** operation. The method respects
      the source rectangle and writes only the selected pixels to the destination
      bitmap.'
  - name: Save the cropped image (crop image to PNG)
    text: '`Bitmap.Save` writes the in‑memory bitmap to a file using the specified
      format. Finally, write the canvas to disk as a PNG file. PNG preserves any alpha
      channel and provides lossless quality—ideal for UI assets.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of formats (PNG, JPEG, BMP,
      GIF, TIFF, etc.), so you can crop virtually any image type.
    question: Can I crop images of any format using Aspose.Drawing?
  - answer: Absolutely. You can combine `GraphicsPath`, `Matrix` transformations,
      or use the `ImageProcessor` class for more complex selections like circular
      crops.
    question: Are there advanced cropping options available?
  - answer: Yes. After the first crop, you can reuse the resulting bitmap as the new
      source and repeat the process to chain multiple crops.
    question: Can I apply multiple crop operations to a single image?
  - answer: Indeed. Its lightweight API and lack of native dependencies make it perfect
      for processing large image collections on servers.
    question: Is Aspose.Drawing suitable for batch image processing?
  - answer: Head over to the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      to seek assistance and connect with the community.
    question: How can I get support for Aspose.Drawing‑related queries?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
tags:
- batch image cropping
- Aspose.Drawing
- .NET image processing
- PNG conversion
title: Как пакетно обрезать изображения до PNG с помощью Aspose.Drawing для .NET
url: /ru/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как пакетно обрезать изображения до PNG с помощью Aspose.Drawing для .NET

Если вам нужно **crop image to PNG** быстро, надёжно и в масштабах в среде .NET, вы попали по адресу. В этом руководстве мы пройдём по точным шагам загрузки изображения, определения области обрезки и сохранения результата в файл PNG — все с использованием Aspose.Drawing, современного **alternative to System.Drawing**, работающего кросс‑платформенно. Вы также увидите, как расширить процесс обработки одного изображения до полноценного **batch crop** конвейера.

## Быстрые ответы
- **Какую библиотеку следует использовать?** Aspose.Drawing for .NET (полнофункциональная альтернатива System.Drawing.Common)  
- **Сколько времени занимает базовое обрезание?** Обычно менее секунды для одного изображения на современном процессоре  
- **Можно ли обрезать до PNG?** Да – сохраните обрезанный битмап как PNG‑файл (см. Шаг 6)  
- **Нужна ли лицензия?** Бесплатная пробная версия подходит для разработки; для продакшна требуется коммерческая лицензия  
- **Возможна ли пакетная обработка?** Абсолютно – оберните те же шаги в цикл, чтобы обрабатывать несколько файлов за секунды  

## Как пакетно обрезать изображения до PNG?

Загружайте каждый исходный файл с помощью `new Bitmap(path)`, создавайте соответствующий пустой `Bitmap` для области обрезки, рисуйте выбранный прямоугольник с помощью `Graphics.DrawImage` и, наконец, вызывайте `Save("output.png", ImageFormat.Png)`. Оберните эти шесть строк в цикл `foreach`, который перебирает файлы в каталоге, и вы получите полное решение для пакетного обрезания, обрабатывающее десятки изображений за секунды.

## Почему использовать Aspose.Drawing для пакетного обрезания?

Aspose.Drawing работает на **Windows, Linux и macOS**, обрабатывает **изображения более 500 пикселей менее чем за 0,5 секунды** на типичном серверном процессоре и поддерживает **более 50 форматов изображений** с полной сохранностью альфа‑канала. Поскольку он устраняет зависимости от нативных библиотек GDI+, вы можете развёртывать тот же код в контейнерах, Azure App Service или AWS Lambda без дополнительных библиотек, что делает его идеальным для масштабных конвейеров обработки изображений.

## Что такое «crop image to PNG»?

Операция `crop image to PNG` извлекает прямоугольный регион из исходного битмапа и записывает его в файл PNG. PNG сохраняет любой альфа‑канал, обеспечивая без потерь сжатие, что делает полученное изображение идеальным для миниатюр, иконок, UI‑активов или любой ситуации, где требуется качество и прозрачность.

## Почему Aspose.Drawing является альтернативой System.Drawing?

Aspose.Drawing служит заменой System.Drawing, предоставляя полную кросс‑платформенную совместимость и устраняя необходимость в нативных библиотеках GDI+. Он поддерживает широкий спектр пиксельных форматов, обеспечивает высокопроизводительные операции с изображениями и включает продвинутые функции, такие как работа с альфа‑каналом и обширная поддержка форматов, что делает его подходящим как для простых правок, так и для крупномасштабной пакетной обработки.

## Предварительные требования

Прежде чем приступить, убедитесь, что у вас есть:

- **Aspose.Drawing library** интегрированная в ваш .NET‑проект. Вы можете скачать её со [страницы загрузки Aspose.Drawing](https://releases.aspose.com/drawing/net/).  
- Папка, содержащая исходные изображения, которые нужно обрезать. Замените `"Your Document Directory"` в примерах кода фактическим путём на вашем компьютере.

## Импорт пространств имён

Пространство имён `System.Drawing` даёт доступ к `Bitmap`, `Graphics` и связанным типам, которые расширяет Aspose.Drawing.

```csharp
using System.Drawing;
```

## Пошаговое руководство

### Шаг 1: Создать bitmap‑холст

`Bitmap` — это in‑memory представление изображения в Aspose.Drawing, предоставляющее доступ к пикселям и контроль над форматом.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Мы начинаем с пустого холста нужного размера, чтобы разместить обрезанный результат. Отрегулируйте ширину и высоту, чтобы они соответствовали размерам области, которую планируете извлечь.

### Шаг 2: Создать объект graphics

`Graphics` — поверхность рисования, позволяющая рендерить формы, текст или другие изображения на `Bitmap`.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Объект `Graphics` позволяет рисовать на холсте. `InterpolationMode` управляет тем, как вычисляются значения пикселей при масштабировании или трансформации — `NearestNeighbor` хорошо подходит для резких краёв.

### Шаг 3: Загрузить изображение для обрезки

`Image` (или `Bitmap`) загружает исходный файл в память, готовый к манипуляциям.  

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Загрузите исходное изображение. Убедитесь, что путь указывает на существующий файл; иначе будет выброшено исключение.

### Шаг 4: Определить исходные и целевые прямоугольники

Объекты `Rectangle` описывают регион исходного изображения, который нужно сохранить, и место его размещения на целевом холсте.  

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` указывает API, какую часть оригинального изображения оставить. Здесь мы выбираем область 50 × 40 пикселей в левом верхнем углу. Присвоив тот же прямоугольник `destinationRectangle`, мы сохраняем обрезанный регион в его исходном размере.

### Шаг 5: Выполнить операцию обрезки

`Graphics.DrawImage` копирует определённую часть `image` на наш пустой `bitmap`.  

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

Это основная операция **crop image to PNG**. Метод учитывает исходный прямоугольник и записывает только выбранные пиксели в целевой битмап.

### Шаг 6: Сохранить обрезанное изображение (crop image to PNG)

`Bitmap.Save` записывает битмап из памяти в файл в указанном формате.  

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Наконец, сохраняем холст на диск как PNG‑файл. PNG сохраняет любой альфа‑канал и обеспечивает без потерь качество — идеально для UI‑активов.

## Как пакетно обрезать изображения в цикле?

Итерируйте каждый путь к файлу с помощью `foreach (var file in Directory.GetFiles(sourceFolder, "*.png"))`, повторяйте Шаги 1‑6 внутри цикла и сохраняйте каждый результат в целевую папку. Этот шаблон масштабируется линейно, может быть параллелен с `Parallel.ForEach` для ещё более высокой пропускной способности и эффективно обрабатывает изображения быстро.

## Распространённые подводные камни и советы

- **Несоответствия форматов пикселей** – убедитесь, что исходное изображение и битмап‑холст используют совместимый пиксельный формат, чтобы избежать смещения цветов.  
- **Освобождение GDI‑объектов** – оборачивайте `Bitmap` и `Graphics` в конструкции `using` или вызывайте `Dispose()` вручную; иначе может произойти утечка неуправляемых ресурсов.  
- **Ошибки координат** – координаты прямоугольника начинаются с нуля. Выбор прямоугольника, выходящего за границы исходного изображения, вызовет исключение.  

## Часто задаваемые вопросы

**Q: Можно ли обрезать изображения любого формата с помощью Aspose.Drawing?**  
A: Да, Aspose.Drawing поддерживает широкий спектр форматов (PNG, JPEG, BMP, GIF, TIFF и др.), поэтому вы можете обрезать практически любой тип изображения.

**Q: Доступны ли продвинутые варианты обрезки?**  
A: Абсолютно. Вы можете комбинировать `GraphicsPath`, трансформации `Matrix` или использовать класс `ImageProcessor` для более сложных выделений, например, круглой обрезки.

**Q: Можно ли применить несколько операций обрезки к одному изображению?**  
A: Да. После первой обрезки вы можете использовать полученный битмап как новый источник и повторять процесс, цепляя несколько обрезок.

**Q: Подходит ли Aspose.Drawing для пакетной обработки изображений?**  
A: Безусловно. Его лёгкий API и отсутствие нативных зависимостей делают его идеальным для обработки больших коллекций изображений на серверах.

**Q: Как получить поддержку по вопросам, связанным с Aspose.Drawing?**  
A: Перейдите на [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44), чтобы задать вопрос и связаться с сообществом.

---

**Last Updated:** 2026-10-13  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose

## Связанные руководства

- [Load, Convert BMP to PNG and Other Formats with Aspose.Drawing](/drawing/net/image-editing/load-save/)
- [How to License Aspose.Drawing for .NET – how to license aspose.drawing](/drawing/net/licensing/)
- [How to Draw Rectangle – Coordinate System Transformation (Page Transformation) using Aspose.Drawing API for .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}