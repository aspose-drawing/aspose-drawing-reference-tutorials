---
date: 2026-09-23
description: Узнайте, как сохранить PNG‑изображение в C# с помощью Aspose.Drawing,
  вывести список установленных шрифтов, отрисовать текст пользовательскими шрифтами
  и настроить разрешение bitmap для графики высокого качества.
keywords:
- save png image c#
- installed fonts aspnet
- aspose.drawing bitmap graphics
- c# font collection
- png export .net
lastmod: 2026-09-23
linktitle: Сохранить PNG‑изображение в C# с Aspose.Drawing и установленными шрифтами
og_description: Сохраните PNG‑изображение в C# с Aspose.Drawing. В этом руководстве
  показано, как вывести список установленных шрифтов, отрисовать текст и управлять
  разрешением bitmap для профессиональной графики.
og_image_alt: Developer guide showing C# code that creates a bitmap, lists system
  fonts, and saves a PNG file with Aspose.Drawing
og_title: Сохранить PNG‑изображение в C# с Aspose.Drawing и установленными шрифтами
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  headline: Save PNG image in C# with Aspose.Drawing and installed fonts
  type: TechArticle
- description: Learn how to save PNG image in C# using Aspose.Drawing, list installed
    fonts, draw text with custom fonts, and adjust bitmap resolution for high‑quality
    graphics.
  name: Save PNG image in C# with Aspose.Drawing and installed fonts
  steps:
  - name: Create a bitmap (the canvas)
    text: '`Bitmap` is the raster image object that holds pixel data for the canvas.'
  - name: Create graphics from bitmap
    text: '`Graphics` is the object that supplies drawing functions such as drawing
      shapes and text onto a bitmap.'
  - name: Set up brush and font (draw text with fonts)
    text: '`Brush` defines how shapes and text are filled with colour, while `Font`
      specifies the typeface, size, and style for text rendering.'
  - name: List installed fonts and show font families
    text: '`InstalledFontCollection` provides access to all font families installed
      on the host system.'
  - name: Save PNG image
    text: '`bitmap.Save` writes the bitmap to a file in the chosen image format, such
      as PNG. > **Pro tip:** Use `Path.Combine` for building file paths to avoid issues
      with directory separators on different operating systems.'
  type: HowTo
- questions:
  - answer: Yes. Load the font file into a `PrivateFontCollection` and create a `Font`
      from that collection, then draw it the same way as system fonts.
    question: Can I use custom fonts that are not installed on the machine?
  - answer: Wrap font creation in a `try/catch` block and inspect `ArgumentException`
      for missing families; provide a fallback font such as `Arial`.
    question: How do I handle font‑related exceptions?
  - answer: Absolutely. The library works in ASP.NET Core, Azure Functions, and other
      server‑side .NET environments without needing GDI+.
    question: Is Aspose.Drawing suitable for web applications?
  - answer: Yes. Use different `Brush` types (e.g., `LinearGradientBrush`) and modify
      the `FontStyle` enum to apply bold, italic, or underline.
    question: Can I change the text colour or style?
  - answer: Download a trial license from the [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – bitmap graphics and font handling
tags:
- save png
- aspose.drawing
- c# graphics
- installed fonts
- bitmap
title: Сохранить PNG‑изображение в C# с Aspose.Drawing и установленными шрифтами
url: /ru/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сохранить PNG‑изображение в C# с Aspose.Drawing и установленными шрифтами

## Введение

Если вам нужно **сохранить PNG‑изображение в C#** и одновременно **создавать bitmap‑графику**, Aspose.Drawing для .NET предоставляет чистый, кроссплатформенный способ сделать это. В этом руководстве мы пройдемся по перечислению установленных шрифтов, отображению семейств шрифтов, созданию графики из bitmap и рисованию текста со шрифтами — и, в конце, сохраним результат как PNG‑изображение. К концу вы получите переиспользуемый фрагмент кода, который можно вставить в любой проект .NET, будь то Windows, Linux или macOS.

## Быстрые ответы
- **Что создает это руководство?** PNG‑изображение, перечисляющее установленные семейства шрифтов на хост‑машине.  
- **Какая библиотека требуется?** Aspose.Drawing для .NET (без зависимости от System.Drawing.Common).  
- **Могу ли я использовать пользовательские шрифты?** Да — загрузите их в `InstalledFontCollection` или `PrivateFontCollection`.  
- **Можно ли регулировать разрешение вывода?** Конечно — измените размер bitmap или формат пикселей, чтобы контролировать разрешение.  
- **Нужна ли лицензия для выполнения кода?** Временная лицензия подходит для оценки; полная лицензия требуется для продакшн.  

## Что означает «сохранить PNG‑изображение» в контексте Aspose.Drawing?

`Bitmap` — это растровый контейнер изображений Aspose.Drawing, который хранит данные пикселей.  
Сохранение PNG‑изображения означает отрисовку вашей поверхности рисования — `Bitmap` — в файл с расширением `.png`. Aspose.Drawing выполняет безпотерьную PNG‑компрессию и может обрабатывать изображения размером до **10 000 × 10 000 pixels**, не исчерпывая память, что делает его подходящим для графики высокого разрешения. Полученный файл можно использовать в веб‑страницах, отчетах или дальнейших конвейерах обработки изображений.

## Зачем перечислять установленные шрифты и показывать семейства шрифтов?

Перечисление установленных шрифтов позволяет вашему приложению адаптироваться к окружению конечного пользователя, гарантируя, что сгенерированная графика соответствует корпоративному брендингу или предпочтениям пользователя без необходимости поставлять дополнительные файлы шрифтов. `InstalledFontCollection` перечисляет шрифты, установленные в операционной системе. Это особенно полезно для автоматической генерации отчетов, сертификатов или любого визуального контента, который должен учитывать системную типографику.

## Как создать bitmap‑графику в C# с помощью Aspose.Drawing?

`Bitmap` представляет собой холст изображения; `Graphics` предоставляет методы рисования для этого холста; `Font` описывает типографику, используемую для рендеринга текста. Вы можете создать полноценный PNG всего за несколько строк: создать `Bitmap`, получить объект `Graphics`, нарисовать текст, используя `Font` из установленной коллекции, и, наконец, вызвать `bitmap.Save`. Следующее пошаговое руководство раскрывает каждую часть и добавляет практические советы.

## Требования

- **Библиотека Aspose.Drawing** – загрузите последнюю версию со [страницы загрузки Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider или любой совместимый с .NET редактор.  
- **Базовые знания C#** – вы должны быть уверены в работе с классами, объектами и простыми циклами.  
- **.NET runtime** – рекомендуется .NET 6+ или .NET Core 3.1+ для полной кроссплатформенной поддержки.  

## Импорт пространств имён

Add the following `using` statements at the top of your C# file so the compiler can locate the graphics and font types:

```csharp
using Aspose.Drawing;
using Aspose.Drawing.Imaging;
using Aspose.Drawing.Text;
using System.IO;
```

## Пошаговое руководство

### Шаг 1: Создать bitmap (полотно)

`Bitmap` — это растровый объект изображения, который хранит данные пикселей для полотна.  

```csharp
using System.Drawing;
using System.Drawing.Text;
```

### Шаг 2: Создать graphics из bitmap

`Graphics` — объект, предоставляющий функции рисования, такие как отрисовка фигур и текста на bitmap.  

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Шаг 3: Настроить кисть и шрифт (рисовать текст со шрифтами)

`Brush` определяет, как фигуры и текст заполняются цветом, а `Font` указывает типографику, размер и стиль для рендеринга текста.  

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Шаг 4: Перечислить установленные шрифты и показать семейства шрифтов

`InstalledFontCollection` предоставляет доступ ко всем семействам шрифтов, установленным в системе.  

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Шаг 5: Сохранить PNG‑изображение

`bitmap.Save` записывает bitmap в файл в выбранном формате изображения, например PNG.  

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

> **Совет:** Используйте `Path.Combine` для построения путей к файлам, чтобы избежать проблем с разделителями каталогов в разных операционных системах.

## Распространённые проблемы и решения
| Проблема | Причина | Решение |
|-------|-------|-----|
| **Шрифты не отображаются** | `InstalledFontCollection` не заполнен (например, запуск на безголовом сервере без шрифтов). | Установите необходимые шрифты на сервере или внедрите пользовательские шрифты в приложение. |
| **Сохранённый файл повреждён** | Неправильный формат пикселей или отсутствие прав на запись. | Убедитесь, что целевая папка существует и приложение имеет права записи; оставьте `PixelFormat.Format32bppPArgb`. |
| **Текст выглядит размытым** | Низкие настройки DPI или небольшие размеры bitmap. | Увеличьте размеры bitmap или установите `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Часто задаваемые вопросы

**В: Могу ли я использовать пользовательские шрифты, которые не установлены на машине?**  
О: Да. Загрузите файл шрифта в `PrivateFontCollection` и создайте `Font` из этой коллекции, затем рисуйте его так же, как системные шрифты.

**В: Как обрабатывать исключения, связанные со шрифтами?**  
О: Оберните создание шрифта в блок `try/catch` и проверьте `ArgumentException` на отсутствие семейств; предоставьте запасной шрифт, например `Arial`.

**В: Подходит ли Aspose.Drawing для веб‑приложений?**  
О: Безусловно. Библиотека работает в ASP.NET Core, Azure Functions и других серверных средах .NET без необходимости GDI+.

**В: Можно ли изменить цвет или стиль текста?**  
О: Да. Используйте разные типы `Brush` (например, `LinearGradientBrush`) и измените перечисление `FontStyle`, чтобы применить полужирный, курсив или подчеркивание.

**В: Где можно получить временную лицензию для тестирования?**  
О: Скачайте пробную лицензию со [страницы временной лицензии Aspose](https://purchase.aspose.com/temporary-license/).

## Заключение

Следуя этим шагам, вы узнали, как **сохранить PNG‑изображение в C#**, которое динамически **перечисляет установленные шрифты**, **показывает семейства шрифтов**, **создаёт графику из bitmap** и **рисует текст со шрифтами** с помощью Aspose.Drawing для .NET. Теперь вы знаете, как **создавать bitmap‑графику в C#**, регулировать разрешение bitmap и при необходимости включать пользовательские шрифты. Экспериментируйте с разными цветами, размерами шрифтов и размерами bitmap, чтобы соответствовать визуальным требованиям вашего проекта, и изучайте другие возможности Aspose.Drawing, такие как рисование фигур и обработка изображений для более богатой графики.

---

**Последнее обновление:** 2026-09-23  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

## Связанные руководства

- [Как рисовать текст с Aspose.Drawing для .NET](/drawing/net/text-and-fonts/draw-text/)
- [Улучшить качество изображения с антиалиасингом в Aspose.Drawing](/drawing/net/rendering/antialiasing/)
- [Как сохранить PNG с Aspose.Drawing – мировое преобразование](/drawing/net/coordinate-transformations/world-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}