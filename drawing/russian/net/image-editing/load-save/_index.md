---
date: 2025-12-04
description: Освойте загрузку изображений, пакетное преобразование изображений и изменение
  форматов в .NET с использованием Aspose.Drawing. Узнайте, как конвертировать BMP
  в PNG и многое другое.
language: ru
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Конвертировать BMP в PNG и другие форматы с помощью Aspose.Drawing
url: /net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Конвертировать BMP в PNG и другие форматы с Aspose.Drawing

## Introduction

Добро пожаловать в наше пошаговое руководство по тому, как **конвертировать BMP в PNG** (и многие другие форматы изображений) с помощью Aspose.Drawing для .NET. Независимо от того, нужно ли вам **изменить формат изображения** для одного файла или выполнить **пакетную конвертацию изображений** для десятков картинок, это руководство покажет, как загрузить, преобразовать и сохранить изображения с чистым, поддерживаемым кодом.

## Quick Answers
- **Может ли Aspose.Drawing конвертировать BMP в PNG?** Да – просто загрузите BMP и вызовите `Save` с расширением .png.  
- **Поддерживается ли пакетная конвертация?** Абсолютно; перебирайте файлы и повторно используйте тот же метод `LoadAndSave`.  
- **Нужна ли лицензия для продакшн?** Лицензия требуется для использования в продакшн; временная лицензия доступна для оценки.  
- **Какие версии .NET совместимы?** Работает с .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Где можно скачать библиотеку?** Получите последнюю версию пакета Aspose.Drawing со страницы официального скачивания.

## Что такое конвертация форматов изображений c# с Aspose.Drawing?

Aspose.Drawing — это высокопроизводительная полностью управляемая .NET‑библиотека, заменяющая устаревший `System.Drawing.Common`. Она предоставляет полный контроль над сценариями **load image ASP.NET**, поддерживает более 100 форматов изображений и устраняет ограничения, зависящие от платформы.

## Почему стоит использовать Aspose.Drawing для пакетной конвертации изображений?

- **Кроссплатформенная надёжность** – отсутствие зависимостей от GDI+.  
- **Широкая поддержка форматов** – BMP, GIF, JPG, PNG, TIFF и многие другие.  
- **Последовательный API** – один и тот же код работает на Windows, Linux и macOS.  
- **Производительность** – оптимизировано для масштабных конвейеров обработки изображений.

## Предварительные требования

Before we dive in, make sure you have:

- **Aspose.Drawing for .NET** – скачайте его [здесь](https://releases.aspose.com/drawing/net/).  
- Рабочее **.NET development environment** (Visual Studio, VS Code или Rider).  

Теперь, когда всё готово, импортируем необходимые пространства имён и начнём писать код.

## Импорт пространств имён

In your .NET project, begin by importing the necessary namespace:

```csharp
using System.Drawing;
```

These classes provide the core functionality for loading and saving images.

## Шаг 1: Загрузка изображения

The first step is to load an image file. The sample below demonstrates loading images of various formats, including BMP, which we’ll later convert to PNG.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## Как конвертировать BMP в PNG с помощью Aspose.Drawing

The `LoadAndSave` method handles both loading the source file and saving it in the desired output format. By passing `"bmp"` as the argument, the method will automatically produce a PNG file when you change the extension in the `outputPath`.

### Шаг 2.1: Загрузка изображения

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Шаг 2.2: Сохранение изображения (изменение формата изображения)

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

Repeat the `LoadAndSave` call for each image format you wish to process. By adjusting the `outputPath` extension, you can **конвертировать BMP в PNG**, **изменять формат изображения** на GIF, JPG и т.д., используя один и тот же метод.

## Распространённые подводные камни и советы

- **Разделители путей файлов** – используйте `Path.Combine` для кроссплатформенной надёжности вместо ручного конкатенирования строк.  
- **Освобождение Bitmap** – оберните `Bitmap` в блок `using`, чтобы своевременно освобождать нативные ресурсы.  
- **Настройки качества** – при сохранении JPEG рассмотрите возможность указания объекта `EncoderParameters` для управления качеством сжатия.  
- **Пакетная обработка** – разместите файлы изображений в папке и перебирайте их с помощью `Directory.GetFiles` для автоматизации масштабных конвертаций.

## Часто задаваемые вопросы

### Q1: Совместим ли Aspose.Drawing со всеми форматами изображений?

A1: Aspose.Drawing поддерживает широкий спектр форматов, включая BMP, GIF, JPG, PNG и TIFF.

### Q2: Где можно найти подробную документацию по Aspose.Drawing?

A2: Ознакомьтесь с официальной документацией [здесь](https://reference.aspose.com/drawing/net/).

### Q3: Как получить временную лицензию для Aspose.Drawing?

A3: Перейдите [сюда](https://purchase.aspose.com/temporary-license/) для получения информации о временной лицензии.

### Q4: Что делать, если возникнут проблемы или вопросы во время реализации?

A4: Обратитесь за помощью к сообществу Aspose.Drawing на [форуме Aspose](https://forum.aspose.com/c/drawing/44).

### Q5: Где можно приобрести библиотеку Aspose.Drawing?

A5: Вы можете приобрести её [здесь](https://purchase.aspose.com/buy).

**Дополнительные вопросы и ответы**

**Q: Можно ли использовать этот код в веб‑приложении ASP.NET?**  
A: Да – та же логика `LoadAndSave` работает в ASP.NET, MVC или Razor Pages; просто убедитесь, что пути к файлам доступны веб‑процессу.

**Q: Возможно ли обрабатывать изображения параллельно для более быстрой пакетной конвертации?**  
A: Абсолютно. Оберните вызовы `LoadAndSave` в цикл `Parallel.ForEach`, но не забудьте обеспечить потокобезопасное освобождение объектов `Bitmap`.

## Заключение

Теперь вы знаете, как **конвертировать BMP в PNG**, выполнять **пакетную конвертацию изображений** и **изменять формат изображения** с помощью Aspose.Drawing для .NET. Применяйте эти шаблоны для автоматизации конвейеров обработки изображений, создания миниатюр или подготовки ресурсов для веб‑доставки. Экспериментируйте с различными форматами, интегрируйте код в свои сервисы и наслаждайтесь надёжностью полностью управляемой библиотеки рисования.

---

**Последнее обновление:** 2025-12-04  
**Тестировано с:** Aspose.Drawing 24.12 for .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}