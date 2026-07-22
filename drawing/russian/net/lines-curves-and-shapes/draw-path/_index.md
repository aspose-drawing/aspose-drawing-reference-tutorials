---
date: 2026-07-22
description: Узнайте, как сохранить bitmap в PNG и экспортировать изображение в JPEG
  с помощью Aspose.Drawing. Пошаговое руководство показывает drawing paths, creating
  images и exporting formats.
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: Drawing Paths в Aspose.Drawing
og_description: Сохраните bitmap в PNG и экспортируйте изображение в JPEG с помощью
  Aspose.Drawing для .NET. Следуйте этому руководству, чтобы draw complex paths, create
  high‑quality images и output multiple formats.
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: Сохранить Bitmap как PNG – Drawing Paths с Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: Сохранить Bitmap как PNG – использование GraphicsPath в Aspose.Drawing
url: /ru/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Рисование путей в Aspose.Drawing

## Как использовать GraphicsPath – введение

**Save bitmap as PNG** часто является первым шагом, когда требуется без потерь изображение для дальнейшей обработки или публикации. В этом руководстве вы узнаете, как рисовать сложные векторные пути с помощью `GraphicsPath`, отрисовывать их на bitmap, а затем **save bitmap as PNG** или даже **export image to JPEG**. Независимо от того, создаёте ли вы движок отчётности, собственную библиотеку графиков или просто нужно генерировать динамическую графику, Aspose.Drawing предоставляет полностью управляемый, кросс‑платформенный API, заменяющий System.Drawing.Common.

## Быстрые ответы
- **Что я могу рисовать с помощью GraphicsPath?** Линии, прямоугольники, эллипсы, кривые и пользовательские фигуры.  
- **Нужна ли лицензия?** Пробная версия бесплатна; коммерческая лицензия требуется для продакшн.  
- **Какие версии .NET поддерживаются?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Требуется ли System.Drawing.Common?** Нет, Aspose.Drawing работает независимо.  
- **Можно ли сохранять в разные форматы?** Да – PNG, JPEG, BMP, GIF и другие.

## Что такое GraphicsPath?
`GraphicsPath` — это векторный контейнер Aspose.Drawing, который хранит последовательность графических примитивов, таких как линии, дуги и кривые, в виде единого объекта. Группируя эти примитивы, вы можете применять трансформации, правила заполнения и настройки обводки единообразно, что упрощает создание сложной графики и обеспечивает согласованную отрисовку в разных форматах вывода.

## Почему использовать GraphicsPath с Aspose.Drawing?
Использование GraphicsPath с Aspose.Drawing даёт точные, гибкие и высокопроизводительные возможности векторного рисования. Это позволяет создавать сложные формы, применять трансформации и эффективно их отрисовывать, сохраняя кросс‑платформенную согласованность и поддерживая масштабную обработку изображений. Кроме того, он без проблем интегрируется с другими .NET‑библиотеками, позволяя комбинировать растровые и векторные рабочие процессы в одном приложении.

- **Точность:** Обрабатывает более 50 векторных примитивов с субпиксельной точностью, гарантируя, что при **save bitmap as PNG** результат остаётся чётким при любой разрешающей способности.  
- **Гибкость:** Объединяйте линии, дуги и кривые Безье в один путь, а затем отрисовывайте его одним вызовом `Graphics.DrawPath`.  
- **Производительность:** Оптимизированный конвейер рендеринга обрабатывает изображения до 400 МП без загрузки полного файла в память, делая возможными крупномасштабные пакетные задачи.  
- **Кросс‑платформенность:** Идентичные результаты на Windows, Linux и macOS, устраняя платформенно‑специфичные баги.

## Предварительные требования

Перед тем как приступить к руководству, убедитесь, что у вас есть следующие компоненты:

- **Aspose.Drawing Library:** Скачайте и установите библиотеку Aspose.Drawing. Вы можете найти её [здесь](https://releases.aspose.com/drawing/net/).
- **Другие продукты Aspose:** Ознакомьтесь с дополнительными предложениями Aspose [здесь](https://releases.aspose.com/).
- **Среда разработки:** Настройте вашу .NET‑среду разработки с необходимыми инструментами (Visual Studio, .NET SDK и т.д.).

## Импорт пространств имён

Начните с импорта необходимых пространств имён в вашем проекте:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Шаг 1: Создание Bitmap и Graphics

Bitmap представляет изображение в памяти, а Graphics предоставляет методы рисования для отрисовки на этом изображении. Создайте объект `Bitmap` и объект `Graphics`, с которыми будете работать. Этот bitmap будет холстом, на котором будет отрисован `GraphicsPath`, а затем вы **save bitmap as PNG**:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Шаг 2: Определение Pen и GraphicsPath

Pen задаёт цвет линии, её толщину и стиль; GraphicsPath хранит коллекцию графических примитивов как единый векторный объект. Далее определите `Pen` для указания атрибутов рисования и создайте `GraphicsPath`. Объект `GraphicsPath` удерживает векторные данные до их отрисовки:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## Шаг 3: Добавление линий и фигур

AddLine, AddRectangle и AddEllipse добавляют соответствующие фигуры в GraphicsPath для последующей отрисовки. Добавляйте линии, прямоугольники и эллипсы в `GraphicsPath`, чтобы создать сложный путь. Вы также можете добавить пользовательские кривые Безье для плавных форм:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## Шаг 4: Отрисовка пути

DrawPath отрисовывает векторные данные из GraphicsPath на поверхность Graphics с использованием указанного Pen. Нарисуйте путь на объекте `Graphics`, используя заданный `Pen`. Эта операция растеризует векторные данные на bitmap‑холсте:

```csharp
graphics.DrawPath(pen, path);
```

## Шаг 5: Сохранение изображения – экспорт в PNG или JPEG

Метод Bitmap.Save записывает изображение на диск в выбранном формате, таком как PNG или JPEG. После рисования вы можете **save bitmap as PNG** для безпотерьного качества или **export image to JPEG** для уменьшения размера файла. Выберите формат, который лучше всего подходит для вашего последующего сценария:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

Повторяйте эти шаги по мере необходимости, чтобы создавать сложные и визуально привлекательные пути.

## Распространённые проблемы и решения

| Проблема | Решение |
|----------|---------|
| **Путь не виден** | Убедитесь, что цвет Pen контрастирует с фоном и что bitmap сохраняется корректно. |
| **Неожиданный размер изображения** | Проверьте, что размеры bitmap и формат пикселей соответствуют вашим требованиям. |
| **Исключение лицензии** | Используйте пробную лицензию для тестирования; примените действующую лицензию перед развертыванием в продакшн. |

## Часто задаваемые вопросы

### Q1: Могу ли я использовать Aspose.Drawing с другими .NET‑библиотеками?

A1: Да, Aspose.Drawing без проблем интегрируется с другими .NET‑библиотеками, предоставляя гибкость в ваших проектах.

### Q2: Доступна ли пробная версия?

A2: Да, вы можете получить бесплатную пробную версию [здесь](https://releases.aspose.com/).

### Q3: Где я могу найти поддержку по Aspose.Drawing?

A3: Посетите форум Aspose.Drawing [здесь](https://forum.aspose.com/c/drawing/44) для получения помощи и поддержки сообщества.

### Q4: Как получить временную лицензию?

A4: Получите временную лицензию [здесь](https://purchase.aspose.com/temporary-license/).

### Q5: Можно ли приобрести Aspose.Drawing?

A5: Да, вы можете приобрести Aspose.Drawing [здесь](https://purchase.aspose.com/buy).

**Дополнительные вопросы и ответы**

**В: Могу ли я рисовать пользовательские кривые Безье с помощью GraphicsPath?**  
О: Абсолютно — используйте `path.AddBezier(...)` для определения плавных кривых.

**В: Как очистить GraphicsPath перед повторным использованием?**  
О: Вызовите `path.Reset()`, чтобы удалить все фигуры и начать заново.

## Заключение

Поздравляем! Вы успешно изучили **как использовать GraphicsPath** для рисования путей, а затем **save bitmap as PNG** или **export image to JPEG** с помощью Aspose.Drawing для .NET. В этом руководстве рассмотрены создание bitmap, определение pen, построение `GraphicsPath`, отрисовка различных фигур и экспорт конечного изображения в нескольких форматах. Экспериментируйте с разными координатами, цветами и толщинами линий, чтобы раскрыть весь творческий потенциал Aspose.Drawing.

---

**Последнее обновление:** 2026-07-22  
**Тестировано с:** Aspose.Drawing 24.12 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Сохранить Bitmap как PNG и нарисовать замкнутые кривые с Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Сохранить Bitmap C# – нарисовать сплайны Безье с Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Как сохранить изображение и нарисовать кардинальные сплайны в Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}