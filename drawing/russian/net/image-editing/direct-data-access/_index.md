---
date: 2026-07-22
description: Узнайте, как эффективно считывать пиксели, используя Direct Data Access
  от Aspose.Drawing для high performance image processing в .NET.
keywords:
- how to read pixels
- high performance image processing
- bulk image watermarking
lastmod: 2026-07-22
linktitle: Как считывать пиксели с помощью Direct Data Access в Aspose.Drawing
og_description: Как быстро считывать пиксели, используя Direct Data Access от Aspose.Drawing.
  Это руководство демонстрирует техники high performance image processing для разработчиков
  на .NET.
og_image_alt: 'Developer guide: Direct pixel access with Aspose.Drawing in .NET'
og_title: Как считывать пиксели – High Performance Image Processing с Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to read pixels efficiently using Aspose.Drawing's direct
    data access for high performance image processing in .NET.
  headline: How to Read Pixels with Direct Data Access in Aspose.Drawing
  type: TechArticle
- description: Learn how to read pixels efficiently using Aspose.Drawing's direct
    data access for high performance image processing in .NET.
  name: How to Read Pixels with Direct Data Access in Aspose.Drawing
  steps:
  - name: Load the Source Image
    text: We start by loading the image you want to analyze. Replace the placeholder
      path with the actual location of your image file.
  - name: Create a Target Bitmap
    text: Create a new bitmap that matches the source dimensions and uses a 32‑bit
      pixel format suitable for direct access.
  - name: Read Pixel Data
    text: Read the entire ARGB32 pixel buffer from the source bitmap into an integer
      array. This is the **how to read pixels** step.
  - name: Write Pixel Data
    text: After any optional manipulation (e.g., applying a filter), write the pixel
      array back to the target bitmap. This demonstrates **how to write pixels** efficiently.
  - name: Save the Result
    text: Persist the modified bitmap to disk. Adjust the output path as needed.
  type: HowTo
- questions:
  - answer: Yes, Aspose.Drawing works with .NET Framework, .NET Core, and .NET 5/6+.
    question: Can I use Aspose.Drawing for .NET with other .NET frameworks?
  - answer: Absolutely—download a trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official support.
    question: How can I get support for Aspose.Drawing?
  - answer: The full API reference is available at the [Aspose.Drawing documentation
      site](https://reference.aspose.com/drawing/net/).
    question: Where can I find the documentation for Aspose.Drawing?
  - answer: You can buy a license directly from the Aspose store [here](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Direct Data Access for Image Pixel Manipulation
tags:
- image processing
- Aspose.Drawing
- pixel manipulation
- .NET image editing
title: Как считывать пиксели с помощью Direct Data Access в Aspose.Drawing
url: /ru/net/image-editing/direct-data-access/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Как читать пиксели с прямым доступом к данным в Aspose.Drawing

## Введение

В этом руководстве вы узнаете **как читать пиксели** из изображения и записывать данные пикселей обратно, используя функции **прямого доступа к данным** Aspose.Drawing. Использование **высокопроизводительной обработки изображений** с прямым доступом к данным даёт низкоуровневый контроль над буферами пикселей, делая манипуляцию изображениями быстрой и экономичной по памяти — идеально для пользовательских фильтров, анализа изображений или массовых преобразований пикселей в приложениях .NET.

## Быстрые ответы
- **Какой основной метод для чтения пикселей?** Используйте `ReadArgb32Pixels` у экземпляра `Bitmap`.  
- **Какой формат пикселей лучше всего подходит для прямого доступа?** `PixelFormat.Format32bppPArgb` предоставляет 32‑битные ARGB‑значения с предварительно умноженным альфа‑каналом.  
- **Нужна ли лицензия для Aspose.Drawing?** Доступна бесплатная пробная версия; лицензия требуется для использования в продакшене.  
- **Можно ли запускать этот код на .NET 6+?** Да, Aspose.Drawing поддерживает .NET 5, .NET 6 и более новые версии.  
- **Является ли операция потокобезопасной?** Чтение/запись в разных экземплярах bitmap безопасны; избегайте совместного использования одного bitmap между потоками без синхронизации.

`ReadArgb32Pixels` считывает весь буфер пикселей ARGB32 из bitmap в массив целых чисел.  
`PixelFormat.Format32bppPArgb` — 32‑битный формат пикселей с предварительно умноженным альфа‑каналом.  
`Bitmap` представляет изображение, определяемое данными пикселей.

## Что такое прямой доступ к данным в Aspose.Drawing?

Прямой доступ к данным позволяет получить или заменить весь буфер пикселей bitmap одним вызовом, устраняя накладные расходы методов получения/установки пикселя. Этот подход считывает массив целых чисел ARGB32 (`0xAARRGGBB`), который можно обрабатывать любой логикой .NET, а затем записывает изменённый массив обратно одной операцией.

## Почему использовать прямой доступ к данным для высокопроизводительной обработки изображений?

Загрузите всё изображение в управляемый массив целых чисел, обработайте тысячи пикселей с помощью векторизованного или параллельного кода и запишите результат обратно всего двумя вызовами API. Это уменьшает количество переходов между управляемым и неуправляемым кодом до 90 % и позволяет обрабатывать изображения размером 10 000 × 10 000 пикселей без выделения дополнительных временных буферов, обеспечивая действительно высокопроизводительную обработку изображений.

## Распространённые случаи использования

- Создание пользовательских фильтров изображений (сепия, обнаружение границ, **применить сепию**)  
- Выполнение статистического анализа на уровне пикселей для задач компьютерного зрения  
- Преобразование цветовых пространств изображения или массовая коррекция цветов  
- Генерация миниатюр или **массовое наложение водяных знаков** для больших пакетов изображений  

## Требования

- **Библиотека Aspose.Drawing:** Скачайте и подключите последнюю версию Aspose.Drawing для .NET с официального сайта.  
- **Среда разработки:** Любая IDE .NET (Visual Studio, Rider, VS Code) с установленным пакетом Aspose.Drawing NuGet.  

Вы можете скачать библиотеку [здесь](https://releases.aspose.com/drawing/net/).

## Импорт пространств имён

Сначала импортируйте необходимое пространство имён, чтобы классы bitmap были доступны.

```csharp
using System.Drawing;
```

## Пошаговое руководство

### Шаг 1: Загрузить исходное изображение  

Мы начинаем с загрузки изображения, которое хотите проанализировать. Замените путь‑заполнитель реальным расположением вашего файла изображения.

```csharp
Bitmap sourceBitmap = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

### Шаг 2: Создать целевой Bitmap  

Создайте новый bitmap, соответствующий размерам источника и использующий 32‑битный формат пикселей, подходящий для прямого доступа.

```csharp
Bitmap targetBitmap = new Bitmap(sourceBitmap.Width, sourceBitmap.Height, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Шаг 3: Прочитать данные пикселей  

Считайте весь буфер пикселей ARGB32 из исходного bitmap в массив целых чисел. Это шаг **чтения пикселей**.

```csharp
int[] pixels = new int[sourceBitmap.Width * sourceBitmap.Height];
sourceBitmap.ReadArgb32Pixels(pixels);
```

### Шаг 4: Записать данные пикселей  

После любой необязательной обработки (например, применения фильтра) запишите массив пикселей обратно в целевой bitmap. Это демонстрирует **как записать пиксели** эффективно.

```csharp
targetBitmap.WriteArgb32Pixels(pixels);
```

### Шаг 5: Сохранить результат  

Сохраните изменённый bitmap на диск. При необходимости скорректируйте путь вывода.

```csharp
targetBitmap.Save("Your Document Directory" + @"Images\DirectDataAccess_out.png");
```

## Распространённые проблемы и решения

| Проблема | Решение |
|----------|---------|
| **`ArgumentException` при `ReadArgb32Pixels`** | Убедитесь, что исходный bitmap использует 32‑битный формат пикселей; иначе сначала сконвертируйте его с помощью `sourceBitmap.Clone(..., PixelFormat.Format32bppPArgb)`. |
| **Неправильные цвета после записи** | Убедитесь, что вы не изменяете альфа‑канал непреднамеренно; сохраняйте значение `0xFF` (непрозрачное), если прозрачность не нужна. |
| **Падение производительности при очень больших изображениях** | Обрабатывайте массив пикселей частями или используйте `Parallel.For` для задействования нескольких ядер. `Parallel.For` выполняет цикл параллельно в нескольких потоках. |

## Часто задаваемые вопросы

**В: Могу ли я использовать Aspose.Drawing для .NET с другими фреймворками .NET?**  
**О:** Да, Aspose.Drawing работает с .NET Framework, .NET Core и .NET 5/6+.

**В: Доступна ли бесплатная пробная версия Aspose.Drawing?**  
**О:** Конечно — скачайте пробную версию [здесь](https://releases.aspose.com/).

**В: Как получить поддержку Aspose.Drawing?**  
**О:** Посетите [форум Aspose.Drawing](https://forum.aspose.com/c/drawing/44) для получения помощи от сообщества и официальной поддержки.

**В: Где найти документацию Aspose.Drawing?**  
**О:** Полная ссылка на API доступна на сайте [документации Aspose.Drawing](https://reference.aspose.com/drawing/net/).

**В: Как приобрести лицензию на Aspose.Drawing?**  
**О:** Вы можете купить лицензию напрямую в магазине Aspose [здесь](https://purchase.aspose.com/buy).

**В: Можно ли манипулировать данными пикселей в многопоточном окружении?**  
**О:** Да, при условии, что каждый поток работает со своим экземпляром bitmap или вы синхронизируете доступ к общим ресурсам.

## Заключение

Теперь вы знаете **как читать пиксели** из bitmap, манипулировать массивом ARGB32 и **записывать данные пикселей** обратно с помощью прямого доступа к данным Aspose.Drawing. Этот подход обеспечивает **высокопроизводительную обработку изображений** для пользовательских фильтров, анализа на уровне пикселей и массовых преобразований в ваших .NET приложениях.

---

**Последнее обновление:** 2026-07-22  
**Тестировано с:** последняя версия Aspose.Drawing для .NET  
**Автор:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Связанные руководства

- [Как масштабировать изображение без потери — редактирование изображений с Aspose.Drawing](/drawing/net/image-editing/)
- [Как масштабировать изображения с Aspose.Drawing для .NET](/drawing/net/image-editing/scale/)
- [Как обрезать изображение до PNG с Aspose.Drawing для .NET](/drawing/net/image-editing/cropping/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}