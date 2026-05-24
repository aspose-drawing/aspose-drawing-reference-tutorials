---
date: 2026-05-24
description: Узнайте, как установить единицу измерения в Aspose.Drawing для .NET,
  легко конвертировать графические единицы и освоить точные измерения при рендеринге
  графики.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Единицы измерения в Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Как установить единицу измерения в Aspose.Drawing для .NET – Единицы измерения
url: /ru/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как установить единицу измерения в Aspose.Drawing для .NET – Единицы измерения

## Введение

Добро пожаловать в мир Aspose.Drawing для .NET, где точность и гибкость встречаются в графическом манипулировании. В этом руководстве вы узнаете **как установить единицу измерения** для ваших рисунков, научитесь **конвертировать графические единицы** между пунктами, миллиметрами и дюймами, а также увидите практические примеры, которые делают ваши изображения пиксель‑идеальными. Независимо от того, создаёте ли вы отчёты, миниатюры или пользовательские диаграммы, владение единицами измерения необходимо для согласованного рендеринга на разных устройствах.

## Быстрые ответы
- **Какой основной способ изменить единицы измерения?** Вызовите `graphics.PageUnit = PageUnit.Point` (или `.Millimeter`, `.Inch`) у объекта `Graphics`.  
- **Какая единица равна 1/72 дюйма?** Points.  
- **Сколько миллиметров в дюйме?** 25.4 mm = 1 inch.  
- **Нужны ли дополнительные библиотеки для использования единиц?** Нет, основная библиотека Aspose.Drawing предоставляет все константы единиц.  
- **Можно ли смешивать единицы в одном изображении?** Установите единицу один раз для экземпляра `Graphics`; рисуйте всё, используя эту единицу, для согласованности.

## Предварительные требования

Прежде чем погрузиться в руководство, убедитесь, что у вас есть следующие предварительные требования:

- Aspose.Drawing for .NET: Убедитесь, что библиотека установлена. Вы можете скачать её [здесь](https://releases.aspose.com/drawing/net/).
- Каталог документов: Иметь назначенный каталог, куда вы хотите сохранять созданные документы.
- Базовые знания C#: Рекомендуется фундаментальное понимание C#, чтобы максимально эффективно использовать это руководство.

## Импорт пространств имён

Прежде чем начать, импортируем необходимые пространства имён для эффективного использования Aspose.Drawing:

```csharp
using System.Drawing;
```

Теперь разберём каждый пример на несколько шагов:

## Как установить единицу измерения в пункты?

`Bitmap` класс представляет изображение в памяти, которое служит холстом для рисования. Загрузите ваш bitmap, создайте объект `Graphics` и установите единицу страницы в пункты — это сообщает Aspose.Drawing интерпретировать все координаты как значения 1/72 дюйма. Использование пунктов даёт тонкий контроль для графики, готовой к печати, и позволяет задавать толщину линий с высокой точностью.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Шаг 1: Создать Bitmap  
`Bitmap` класс представляет изображение в памяти, которое служит холстом для рисования.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Шаг 2: Создать объект Graphics  
`Graphics` предоставляет методы рисования для отрисовки фигур и текста на `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Шаг 3: Установить единицу страницы в пункты  
`PageUnit` — это перечисление, которое задаёт единицу измерения координат страницы. `PageUnit.Point` определяет пункты как единицу измерения (1 пункт = 1/72 дюйма). Эта настройка применяется ко всем последующим вызовам рисования.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Шаг 4: Нарисовать прямоугольник в пунктах  
Когда вы рисуете прямоугольник после установки единицы, указанные размеры интерпретируются как пункты, обеспечивая точный размер.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Как установить единицу измерения в миллиметры?

`PageUnit` — это перечисление, которое задаёт единицу измерения координат страницы. Переход на миллиметры полезен, когда нужны метрические размеры, например при создании инженерных схем. Aspose.Drawing рассматривает 1 мм как 1/25.4 дюйма, позволяя согласовать графику с физическими измерениями, используемыми в производстве и технической документации.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Шаг 1: Установить единицу страницы в миллиметры  
Назначьте `PageUnit.Millimeter` объекту `Graphics`; все координаты теперь соответствуют метрической системе.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Шаг 2: Нарисовать прямоугольник в миллиметрах  
Ширина и высота прямоугольника теперь выражаются в миллиметрах, что упрощает согласование с физическими измерениями и гарантирует, что печатный результат соответствует реальным размерам.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Как установить единицу измерения в дюймы?

`Graphics` предоставляет методы рисования для отрисовки фигур и текста на `Bitmap`. Дюймы являются единицей по умолчанию для многих американских инструментов дизайна. Установка единицы в дюймы позволяет мыслить в привычных терминах при размещении элементов UI и упрощает переход от экранного дизайна к печати, где часто используют дюймы.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Шаг 1: Установить единицу страницы в дюймы  
`PageUnit.Inch` меняет систему координат так, что 1 единица равна 1 дюйму, предоставляя простой способ задавать размеры элементов для печатных макетов.

CODE_BLOCK_PLACEHOLDER_10_END

### Шаг 2: Нарисовать прямоугольник в дюймах  
Теперь любая фигура, которую вы рисуете, использует дюймы в качестве базовой единицы измерения, что идеально подходит для печатных макетов и для передачи размеров заинтересованным сторонам, привыкшим к имперской системе.

CODE_BLOCK_PLACEHOLDER_11_END

## Сохранить результат

После завершения примеров сохраните полученное изображение в ваш каталог документов. Метод `Bitmap.Save` записывает файл в указанном вами формате (PNG, JPEG и т.д.).

CODE_BLOCK_PLACEHOLDER_12_END

Теперь вы успешно освоили различные единицы измерения в Aspose.Drawing для .NET, создав визуальное представление прямоугольников с использованием пунктов, миллиметров и дюймов.

## Почему стоит использовать систему единиц Aspose.Drawing?

Aspose.Drawing поддерживает **более 30 форматов изображений** и может обрабатывать изображения размером до **5000 × 5000 пикселей** без загрузки всего файла в память, обеспечивая высокую производительность при генерации графики большого масштаба. Явно задавая единицу измерения, вы исключаете догадки, снижаете ошибки конвертации и гарантируете, что ваш вывод соответствует точным физическим размерам на всех платформах.

## Распространённые проблемы и решения

- **Неожиданный размер после сохранения** – Убедитесь, что вы установили `graphics.PageUnit` **до** любых вызовов рисования; изменение единицы позже не изменит размер уже созданных фигур.  
- **Размытие на экранах с высоким DPI** – Увеличьте разрешение bitmap (например, `new Bitmap(width, height, 300)`) чтобы соответствовать целевому DPI.  
- **Смешивание единиц в одном изображении** – Создайте отдельные экземпляры `Graphics` для каждой единицы или выполните ручную конвертацию перед рисованием.

## Часто задаваемые вопросы

### Q1: Могу ли я использовать Aspose.Drawing для .NET с другими .NET фреймворками?
A1: Да, Aspose.Drawing совместим с различными .NET фреймворками, обеспечивая гибкость в вашей среде разработки.

### Q2: Доступна ли бесплатная пробная версия?
A2: Да, вы можете ознакомиться с Aspose.Drawing с помощью бесплатной пробной версии [здесь](https://releases.aspose.com/).

### Q3: Как получить поддержку для Aspose.Drawing для .NET?
A3: Посетите [форум Aspose.Drawing](https://forum.aspose.com/c/drawing/44) для получения поддержки от сообщества и обсуждений.

### Q4: Можно ли приобрести временную лицензию для краткосрочных проектов?
A4: Да, вы можете получить временную лицензию [здесь](https://purchase.aspose.com/temporary-license/).

### Q5: Где можно найти подробную документацию по Aspose.Drawing?
A5: Полная документация доступна [здесь](https://reference.aspose.com/drawing/net/).

---

**Последнее обновление:** 2026-05-24  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Преобразование системы координат – Преобразование страницы в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Учебник по матричным преобразованиям: Матричные преобразования в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Как применить преобразование: Локальное преобразование в Aspose.Drawing для .NET](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}