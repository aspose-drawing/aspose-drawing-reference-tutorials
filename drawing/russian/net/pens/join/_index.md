---
date: 2026-09-18
description: Узнайте, как рисовать путь и соединять пути с помощью перьев в Aspose.Drawing,
  а затем сохранять изображение в формате PNG с помощью простого кода на C#.
keywords:
- save image as png
- server side image rendering
- raster image from vector
- export graphics to png
- alternative to system drawing
lastmod: 2026-09-18
linktitle: Соединение путей с помощью перьев в Aspose.Drawing
og_description: Сохраните изображение в формате PNG с помощью Aspose.Drawing. Узнайте,
  как рисовать пути, применять стили соединения линий и экспортировать растровую графику
  высокого качества из векторных данных на сервере.
og_image_alt: Developer guide showing how to draw and join paths with pens, then save
  the result as a PNG file using Aspose.Drawing
og_title: Как нарисовать путь, соединить пути с помощью перьев и сохранить изображение
  в формате PNG
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to draw path and join paths with pens in Aspose.Drawing,
    then save the image as PNG using simple C# code.
  headline: How to draw path, join paths with pens and save image as PNG
  type: TechArticle
- questions:
  - answer: Aspose.Drawing is a commercial product, but you can explore its capabilities
      with a **[free trial](https://releases.aspose.com/)**.
    question: Can I use Aspose.Drawing for free?
  - answer: Refer to the **[documentation](https://reference.aspose.com/drawing/net/)**
      for comprehensive guidance.
    question: Where can I find Aspose.Drawing documentation?
  - answer: Visit the **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)**
      for community help and official assistance.
    question: How can I get support for Aspose.Drawing?
  - answer: Yes, you can obtain a **[temporary license](https://purchase.aspose.com/temporary-license/)**
      for short‑term usage.
    question: Are temporary licenses available for Aspose.Drawing?
  - answer: Purchase Aspose.Drawing **[Aspose.Drawing purchase page](https://purchase.aspose.com/buy)**.
    question: Where can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- C# graphics
- save PNG
- vector to raster
- server side rendering
title: Как нарисовать путь, соединить пути с помощью перьев и сохранить изображение
  в формате PNG
url: /ru/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как рисовать путь, соединять пути с помощью перьев и сохранять изображение в PNG

## Введение

В этом руководстве вы узнаете, как создавать объекты **draw path**, соединять их с различными стилями соединения линий и **сохранять изображение в PNG**, используя Aspose.Drawing для .NET. Независимо от того, создаёте ли вы движок отчетности, редактор дизайна или вам требуется серверный рендеринг изображений для веб‑сервиса, освоение рисования путей с помощью перьев дает точный контроль над преобразованием векторного изображения в растровое.

## Быстрые ответы
- **Что означает “draw path”?** Он создает векторные определения линий или фигур, которые объект `Graphics` может отрисовать.  
- **Какие типы соединения линий доступны?** `Bevel`, `Miter`, `Round` и `BevelClipped`.  
- **Могу ли я экспортировать результат в PNG?** Да — используйте `Bitmap.Save` с расширением `.png`.  
- **Нужна ли лицензия?** Пробная версия подходит для оценки; для продакшна требуется коммерческая лицензия.  
- **Какие версии .NET поддерживаются?** .NET Framework 4.6+, .NET Core 3.1+ и .NET 6+.

## Что такое “draw path” в Aspose.Drawing?

**Draw path** означает создание `GraphicsPath`, содержащего последовательность линий, кривых или фигур.  
`GraphicsPath` — это контейнер Aspose.Drawing для векторной геометрии; позже вы можете отрисовать его с помощью `Pen` или заполнить кистью. Такой подход позволяет применять трансформации, обрезку и единые стили соединения линий ко всей фигуре, а не рисовать каждый сегмент отдельно.

## Почему стоит использовать Aspose.Drawing для серверного рендеринга изображений?

Aspose.Drawing предоставляет надёжный движок серверного рендеринга, который работает на любой операционной системе без зависимости от GDI+, что делает его идеальным для облачных сервисов, контейнеризованных приложений и высокопроизводительных веб‑API, где требуется кроссплатформенная совместимость и безголовый режим, обеспечивая масштабируемую производительность.

- **Полная совместимость с .NET** — поддерживает .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Богатые варианты соединения линий** — `Bevel`, `Miter`, `Round`, `BevelClipped`.  
- **Высококачественный растровый вывод** — может экспортировать в **более 10 растровых форматов** (PNG, JPEG, BMP, GIF, TIFF и др.) напрямую из векторных данных.  
- **Отсутствие ограничений GDI+** — идеально для облачных сервисов, контейнеров и безголовых сред.

## Предварительные требования

Прежде чем перейти к коду, убедитесь, что у вас есть:

1. **Библиотека Aspose.Drawing** — скачайте её со **[страницы загрузки Aspose.Drawing](https://releases.aspose.com/drawing/net/)**.  
2. **Среда разработки .NET** — Visual Studio, VS Code или любой IDE, поддерживающий C#.

Теперь, когда всё готово, пройдём каждый шаг.

## Импорт пространств имён

Пространства имён `System.Drawing` и `System.Drawing.Drawing2D` содержат основные типы графики, используемые Aspose.Drawing.  

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Шаг 1: Создание bitmap и объекта graphics

`Bitmap` — это растровый холст Aspose.Drawing в памяти. Он представляет растровое изображение, на котором можно рисовать с помощью поверхности `Graphics`.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Мы начинаем с пустого холста (`Bitmap`) размером 1000 × 800 пикселей и получаем объект `Graphics`, который будет выполнять наши команды рисования.

## Шаг 2: Определение метода drawPath

`Pen` — инструмент Aspose.Drawing для обводки векторных контуров; он задаёт цвет, толщину и стиль соединения линий.  

`LineJoin` управляет тем, как два отрезка соединяются в углу.  

`GraphicsPath` — векторный контейнер, содержащий последовательность линий, которые мы будем соединять.

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

Этот вспомогательный метод инкапсулирует логику рисования:

- **Pen** — задаёт цвет и толщину (30 px).  
- **GraphicsPath** — определяет две соединённые линии, образующие форму «L».  
- **LineJoin** — управляет тем, как отображается угол между двумя линиями (`Bevel`, `Round` и др.).

Вы можете вызвать этот метод с любым значением `LineJoin`, чтобы увидеть визуальную разницу.

## Шаг 3: Соединение путей с помощью bevel line join

`LineJoin.Bevel` создаёт плоский угол там, где встречаются две линии, что полезно, когда нужен чёткий, не перекрывающийся стык.

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

## Шаг 4: Соединение путей с помощью round line join

`LineJoin.Round` создаёт плавный, закруглённый угол — идеально для более изысканного вида.

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

## Шаг 5: Сохранение результата в PNG

Вызов `Save` записывает bitmap в файл в формате PNG, завершая процесс **save image as PNG**. Скорректируйте путь в соответствии с вашей средой.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

## Распространённые проблемы и решения

| Проблема | Почему происходит | Решение |
|----------|-------------------|---------|
| **Изображение пустое** | `Graphics` объект не был очищен или размер bitmap слишком мал. | Вызовите `graphics.Clear(Color.White);` перед рисованием или увеличьте размеры bitmap. |
| **Угол выглядит зазубренным** | Используется bitmap низкого разрешения с толстым пером. | Увеличьте DPI bitmap (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) или уменьшите толщину пера. |
| **Ошибка: файл не найден** | Неверный путь сохранения. | Используйте `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), \"Pens\", \"Join_out.png\")`. |

## Часто задаваемые вопросы

**Q: Могу ли я использовать Aspose.Drawing бесплатно?**  
A: Aspose.Drawing — коммерческий продукт, но вы можете изучить его возможности с помощью **[бесплатной пробной версии](https://releases.aspose.com/)**.

**Q: Где я могу найти документацию Aspose.Drawing?**  
A: Обратитесь к **[документации](https://reference.aspose.com/drawing/net/)** для полного руководства.

**Q: Как получить поддержку Aspose.Drawing?**  
A: Посетите **[форум Aspose.Drawing](https://forum.aspose.com/c/drawing/44)** для помощи от сообщества и официальной поддержки.

**Q: Доступны ли временные лицензии для Aspose.Drawing?**  
A: Да, вы можете получить **[временную лицензию](https://purchase.aspose.com/temporary-license/)** для краткосрочного использования.

**Q: Где можно приобрести Aspose.Drawing?**  
A: Приобретите Aspose.Drawing на **[странице покупки Aspose.Drawing](https://purchase.aspose.com/buy)**.

## Заключение

В этом руководстве мы рассмотрели, как создавать объекты **draw path**, применять различные стили `LineJoin` и **сохранять изображение в PNG** с помощью Aspose.Drawing для .NET. Овладев этими шагами, вы сможете генерировать сложную векторную графику, пользовательские иконки или динамические диаграммы непосредственно из серверного кода, предоставляя надёжное решение **export graphics to PNG**, работающее на любой платформе.

**Последнее обновление:** 2026-09-18  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose

## Связанные руководства

- [Как нарисовать дугу и сохранить изображение PNG с Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-arc/)
- [Как сохранить bitmap в PNG при рисовании нескольких линий с Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [Как сохранить bitmap в PNG, используя Aspose.Drawing API для .NET](/drawing/net/image-editing/display/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}