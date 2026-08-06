---
date: 2026-05-29
description: Узнайте, как сохранять PNG и рисовать кардинальные сплайны в .NET с Aspose.Drawing.
  Сохраняйте кривую как PNG, создавайте плавную графику и без усилий генерируйте bitmap
  в файл.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Рисование кардинальных сплайнов в Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Как сохранить PNG и нарисовать кардинальные сплайны с помощью Aspose.Drawing
url: /ru/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как сохранить PNG и нарисовать кардинальные сплайны с помощью Aspose.Drawing

## Введение

В этом руководстве вы узнаете **как сохранить PNG** файлы, рисуя плавные кардинальные сплайны с помощью Aspose.Drawing для .NET. Независимо от того, создаёте ли вы компонент построения графиков, редактор диаграмм или просто хотите экспортировать пользовательскую кривую в PNG, нижеописанные шаги проведут вас через создание битмап‑холста, рисование сплайна пером и сохранение результата на диск. Вы также увидите, почему Aspose.Drawing является надёжной кросс‑платформенной альтернативой System.Drawing.Common.

## Быстрые ответы
- **Что делает основной метод?** `Graphics.DrawCurve` интерполирует серию точек в плавный кардинальный сплайн.  
- **Какой формат используется для сохранения изображения?** PNG через `Bitmap.Save`.  
- **Нужна ли лицензия для сохранения изображений?** Пробная версия подходит для разработки; для продакшна требуется коммерческая лицензия.  
- **Можно ли изменить натяжение кривой?** Да, перегрузки `DrawCurve` позволяют задать натяжение.  
- **Совместим ли Aspose.Drawing с .NET 6+?** Абсолютно — поддерживает .NET Framework и .NET Core/5/6.

## Что означает «как сохранить PNG» в контексте Aspose.Drawing?

Сохранение PNG означает преобразование находящегося в памяти битмапа, на котором вы рисуете, в физический PNG‑файл на диске. Процесс записывает пиксельные данные с использованием без потерь сжатия, сохраняет точные цвета и любую информацию альфа‑канала. Метод `Bitmap.Save` библиотеки Aspose.Drawing автоматически обрабатывает PNG‑кодирование, поэтому вам не нужно управлять деталями формата вручную.

## Почему рисовать кардинальный сплайн с Aspose.Drawing?

Кардинальный сплайн создаёт плавную, текучую кривую, точно следуя набору контрольных точек, что делает его идеальным для визуализации данных, графики пользовательского интерфейса и пользовательских фигур. Aspose.Drawing поддерживает **30+ image formats** и может рендерить графику сотен страниц без загрузки всего файла в память, обеспечивая как скорость, так и гибкость.

## Требования

Перед тем как начать, убедитесь, что у вас есть:

- Установленная Visual Studio (любая современная версия).  
- Библиотека Aspose.Drawing для .NET. Вы можете скачать её [здесь](https://releases.aspose.com/drawing/net/).  
- Базовые знания программирования на C#.

## Импорт пространств имён

В вашем C#‑файле начните с импорта необходимого пространства имён:

Пространство имён `Aspose.Drawing` содержит все основные типы, такие как `Bitmap`, `Graphics` и `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Шаг 1: Создание Bitmap (Холста)

Сначала создайте битмап, который будет служить холстом для вашего рисунка. Этот битмап — место, где сплайн будет отрисован перед тем, как вы **сохраните изображение**.

Bitmap представляет собой изображение в памяти с определённым форматом пикселей и размерами.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Шаг 2: Создание объекта Graphics

Затем получите объект `Graphics` из битмапа. Этот объект предоставляет поверхность для рисования.

Graphics предоставляет поверхность для рендеринга фигур, текста и изображений на битмапе.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Шаг 3: Определение Pen и рисование кривой

Определите `Pen` с нужным цветом и шириной, затем нарисуйте кардинальный сплайн с помощью `DrawCurve`. Это демонстрирует технику **рисовать кривую с помощью пера** и служит **примером кардинального сплайна**.

Pen инкапсулирует цвет, ширину и стиль линии, используемые для рисования линий и кривых.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Шаг 4: Сохранение изображения (Сохранить кривую как PNG)

Наконец, сохраните битмап в PNG‑файл. Это суть **как сохранить PNG** в данном руководстве.

`Bitmap.Save` записывает изображение в файл в указанном формате, например PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Полезный совет:** Используйте `Path.Combine` для безопасного построения путей к файлам на разных платформах.

Поздравляем! Вы успешно нарисовали кардинальный сплайн и сохранили результат в виде PNG‑изображения с помощью Aspose.Drawing для .NET. Не стесняйтесь экспериментировать с различными массивами точек, цветами пера или толщиной линий, чтобы настроить свои кривые.

## Распространённые сценарии использования

- **Визуализация данных** — плавные линейные графики, требующие точного управления точками.  
- **Пользовательские UI‑компоненты** — рисование регуляторов, слайдеров или декоративных рамок.  
- **Экспортируемая графика** — генерация PNG‑ресурсов «на лету» для отчётов или веб‑контента.

## Устранение неполадок и советы

- **Изображение пустое?** Убедитесь, что формат пикселей битмапа поддерживает альфа‑канал (`Format32bppPArgb`) и при необходимости вызовите `graphics.Clear(Color.Transparent)`.  
- **Неожиданная форма кривой?** Отрегулируйте параметр натяжения, используя перегрузку `DrawCurve(pen, points, tension)`.  
- **Ошибки доступа к файлу?** Проверьте, существует ли целевая директория, и что у вашего приложения есть права на запись.

## Часто задаваемые вопросы

**Q1: Можно ли использовать Aspose.Drawing в коммерческих проектах?**  
A1: Да, Aspose.Drawing подходит как для личных, так и для коммерческих проектов. Ознакомьтесь с деталями лицензирования на [странице покупки](https://purchase.aspose.com/buy).

**Q2: Как получить временную лицензию для тестирования?**  
A2: Получите временную лицензию для тестовых целей [здесь](https://purchase.aspose.com/temporary-license/).

**Q3: Где найти дополнительную поддержку?**  
A3: Посетите [форум Aspose.Drawing](https://forum.aspose.com/c/drawing/44) для получения поддержки от сообщества и обсуждений.

**Q4: Доступна ли бесплатная пробная версия?**  
A4: Да, изучите возможности с помощью [бесплатной пробной версии](https://releases.aspose.com/) перед покупкой.

**Q5: Как получить доступ к документации?**  
A5: Обратитесь к полной [документации](https://reference.aspose.com/drawing/net/) для получения подробной информации и примеров.

---

**Последнее обновление:** 2026-05-29  
**Тестировано с:** Aspose.Drawing 24.11 для .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
