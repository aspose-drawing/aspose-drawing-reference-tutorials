---
date: 2026-02-07
description: Мастер загрузки изображений, пакетного преобразования изображений и изменения
  форматов в .NET с использованием Aspose.Drawing. Узнайте, как конвертировать BMP
  в PNG, как преобразовать изображение и эффективно менять формат изображения.
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Преобразовать BMP в PNG и другие форматы с Aspose.Drawing
url: /ru/net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Конвертирование BMP в PNG и другие форматы с Aspose.Drawing

## Введение

Добро пожаловать в наше пошаговое руководство о том, как **конвертировать BMP в PNG** (и многие другие форматы изображений) с помощью Aspose.Drawing для .NET. Независимо от того, нужно ли вам **изменить формат изображения** для одного файла или выполнить **пакетную конвертацию изображений** для десятков картинок, это руководство покажет, как точно загрузить, преобразовать и сохранить изображения с чистым, поддерживаемым кодом. Мы также рассмотрим типичный шаблон **c# load image file** и продемонстрируем переиспользуемый метод **load and save image**.

## Краткие ответы
- **Может ли Aspose.Drawing конвертировать BMP в PNG?** Да — просто загрузите BMP и вызовите `Save` с расширением .png.  
- **Поддерживается ли пакетная конвертация?** Абсолютно; пройдитесь по файлам в цикле и повторно используйте тот же метод `LoadAndSave`.  
- **Нужна ли лицензия для продакшна?** Для использования в продакшене требуется лицензия; временная лицензия доступна для оценки.  
- **Какие версии .NET совместимы?** Работает с .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Где можно скачать библиотеку?** Получите последнюю версию пакета Aspose.Drawing со страницы официального скачивания.

## Что такое конвертация форматов изображений c# с Aspose.Drawing?

Aspose.Drawing — это высокопроизводительная, полностью управляемая .NET библиотека, заменяющая устаревший `System.Drawing.Common`. Она предоставляет полный контроль над сценариями **load image ASP.NET**, поддерживает более 100 форматов изображений и устраняет ограничения, зависящие от платформы. Короче говоря, это **how to convert image** файлы надёжно на разных платформах.

## Почему стоит использовать Aspose.Drawing для пакетной конвертации изображений?

- **Cross‑platform reliability** — отсутствие зависимостей от GDI+.  
- **Rich format support** — BMP, GIF, JPG, PNG, TIFF и многие другие.  
- **Consistent API** — один и тот же код работает в Windows, Linux и macOS.  
- **Performance** — оптимизировано для конвейеров обработки изображений большого масштаба.

## Требования

Прежде чем приступить, убедитесь, что у вас есть:

- **Aspose.Drawing for .NET** — скачайте его [здесь](https://releases.aspose.com/drawing/net/).  
- Рабочая **.NET development environment** (Visual Studio, VS Code или Rider).  

Теперь, когда всё готово, импортируем необходимые пространства имён и начнём кодировать.

## Импорт пространств имён

В вашем .NET проекте начните с импорта необходимого пространства имён:

```csharp
using System.Drawing;
```

Эти классы предоставляют базовый функционал для загрузки и сохранения изображений.

## Шаг 1: Загрузка изображения

Первый шаг — загрузить файл изображения. Пример ниже демонстрирует загрузку изображений различных форматов, включая BMP, который мы позже конвертируем в PNG. Это иллюстрирует типичный сценарий **c# load image file**.

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

Метод `LoadAndSave` обрабатывает как загрузку исходного файла, так и сохранение его в нужном формате вывода. Передавая `"bmp"` в качестве аргумента, метод автоматически создаст PNG‑файл, когда вы измените расширение в `outputPath`.

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

Тот же метод демонстрирует классический рабочий процесс **load and save image**. Изменяя расширение `outputPath`, вы можете **convert BMP to PNG**, **change image format** на GIF, JPG и т.д., используя один и тот же переиспользуемый код.

## Распространённые подводные камни и советы

- **File path separators** — используйте `Path.Combine` для кроссплатформенной надёжности вместо ручного склеивания строк.  
- **Disposing Bitmaps** — оберните `Bitmap` в блок `using`, чтобы своевременно освобождать нативные ресурсы.  
- **Quality settings** — при сохранении JPEG учитывайте указание объекта `EncoderParameters` для контроля качества сжатия.  
- **Batch processing** — разместите файлы изображений в папке и перебирайте их с помощью `Directory.GetFiles` для автоматизации массовых конвертаций.  
- **Parallel execution** — для более быстрой пакетной конвертации можно выполнять вызовы `LoadAndSave` внутри цикла `Parallel.ForEach`, но не забудьте правильно освобождать каждый `Bitmap`.

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

A5: Вы можете купить её [здесь](https://purchase.aspose.com/buy).

**Дополнительные вопросы и ответы**

**Q: Можно ли использовать этот код в веб‑приложении ASP.NET?**  
A: Да — та же логика `LoadAndSave` работает в ASP.NET, MVC или Razor Pages; просто убедитесь, что пути к файлам доступны веб‑процессу.

**Q: Можно ли обрабатывать изображения параллельно для ускорения пакетной конвертации?**  
A: Абсолютно. Оберните вызовы `LoadAndSave` в цикл `Parallel.ForEach`, но не забудьте обеспечить потокобезопасное освобождение объектов `Bitmap`.

## Заключение

Теперь вы знаете, как **convert BMP to PNG**, выполнять **batch image conversion** и **change image format** с помощью Aspose.Drawing для .NET. Применяйте эти шаблоны для автоматизации конвейеров обработки изображений, создания миниатюр или подготовки ресурсов для веб‑доставки. Экспериментируйте с различными форматами, интегрируйте код в свои сервисы и наслаждайтесь надёжностью полностью управляемой библиотеки рисования.

---

**Последнее обновление:** 2026-02-07  
**Тестировано с:** Aspose.Drawing 24.12 for .NET  
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}