---
date: 2026-02-25
description: Узнайте, как создавать растровую графику в C#, сохранять изображения
  в формате PNG, выводить список установленных шрифтов, рисовать текст шрифтами и
  регулировать разрешение битмапа с помощью Aspose.Drawing для .NET.
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Создание растровой графики C# – Сохранение PNG‑изображения и работа с установленными
  шрифтами в Aspose.Drawing
url: /ru/net/text-and-fonts/installed-fonts/
weight: 13
---

ет:**". Let's do that.

Thus blockquote: "> **Совет:** Используйте `Path.Combine`..." Keep.

Now produce final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Сохранить PNG‑изображение и работать с установленными шрифтами в Aspose.Drawing

## Введение

Если вам нужно **save PNG image** файлы, а также **create bitmap graphics C#**, Aspose.Drawing для .NET предоставляет чистый, кросс‑платформенный способ сделать это. В этом руководстве мы пройдёмся по перечислению установленных шрифтов, отображению семейств шрифтов, созданию графики из bitmap и рисованию текста шрифтами — и в конце сохраним результат как PNG‑изображение. К концу у вас будет переиспользуемый фрагмент кода, который можно вставить в любой проект .NET.

## Быстрые ответы
- **Что создаёт это руководство?** PNG‑изображение, в котором перечислены установленные семейства шрифтов.  
- **Какая библиотека требуется?** Aspose.Drawing для .NET (System.Drawing.Common не нужен).  
- **Могу ли я использовать пользовательские шрифты?** Да — просто загрузите их в `InstalledFontCollection`.  
- **Можно ли регулировать разрешение вывода?** Абсолютно — измените размер bitmap или формат пикселей, чтобы **adjust bitmap resolution C#** стиль.  
- **Нужна ли лицензия для выполнения кода?** Временная лицензия подходит для оценки; полная лицензия требуется для продакшн.

## Что означает «save PNG image» в контексте Aspose.Drawing?

Сохранение PNG‑изображения означает отрисовку вашей поверхности рисования ( `Bitmap` ) в файл с расширением `.png`. Aspose.Drawing выполняет кодирование за вас, поэтому достаточно вызвать `bitmap.Save(...)` с нужным путём.

## Зачем перечислять установленные шрифты и показывать семейства шрифтов?

Знание доступных шрифтов позволяет создавать динамическую графику, адаптирующуюся к окружению конечного пользователя. Это особенно удобно для генерации отчётов, сертификатов или любого визуального контента, который должен соответствовать фирменному стилю без необходимости поставлять файлы шрифтов.

## Как создать bitmap graphics C# с помощью Aspose.Drawing?

Ниже представлена практическая пошаговая инструкция, показывающая, как именно **create bitmap graphics C#**, рисовать текст шрифтами и при необходимости регулировать разрешение bitmap.

## Требования

- **Aspose.Drawing Library** – загрузите последнюю версию со страницы [Aspose Drawing download page](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider или любой совместимый с .NET редактор.  
- **Basic C# knowledge** – вы должны быть уверены в работе с классами, объектами и простыми циклами.

## Импорт пространств имён

Чтобы работать с шрифтами и графикой, импортируйте следующие пространства имён в начале вашего C#‑файла:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Пошаговое руководство

### Шаг 1: Создать bitmap (полотно)

Сначала мы создаём bitmap, который будет содержать окончательное изображение. Размер bitmap и формат пикселей определяют качество сохраняемого PNG и позволяют вам **adjust bitmap resolution C#** стиль.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Шаг 2: Создать graphics из bitmap

Затем мы получаем объект `Graphics` из bitmap. Этот объект позволяет рисовать фигуры, текст и изображения на холсте.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Шаг 3: Настроить кисть и шрифт (draw text with fonts)

Нужна кисть для цвета текста и объект `Font`, определяющий тип шрифта, размер и стиль. Здесь мы **draw text with fonts**.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Шаг 4: Перечислить установленные шрифты и показать семейства шрифтов

Теперь мы выводим количество семейств шрифтов и первые несколько названий непосредственно на bitmap. Это демонстрирует возможности **list installed fonts** и **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Шаг 5: Сохранить PNG‑изображение

Наконец, мы записываем bitmap на диск как PNG‑файл. Это основная операция **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Совет:** Используйте `Path.Combine` для построения путей к файлам, чтобы избежать проблем с разделителями каталогов в разных операционных системах.

## Распространённые проблемы и решения
| Проблема | Причина | Решение |
|----------|---------|---------|
| **Шрифты не отображаются** | `InstalledFontCollection` не заполнен (например, запуск на безголовом сервере без шрифтов). | Установите необходимые шрифты на сервере или внедрите пользовательские шрифты в приложение. |
| **Сохранённый файл повреждён** | Неправильный формат пикселей или отсутствие прав на запись. | Убедитесь, что целевая папка существует и приложение имеет права записи; оставьте `Format32bppPArgb`. |
| **Текст выглядит размытым** | Низкие настройки DPI. | Увеличьте размеры bitmap или установите `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Часто задаваемые вопросы

**Q: Могу ли я использовать пользовательские шрифты, которые не установлены на машине?**  
A: Да. Загрузите файл шрифта в `PrivateFontCollection` и создайте `Font` из этой коллекции.

**Q: Как обрабатывать исключения, связанные со шрифтами?**  
A: Оберните создание шрифта в блок `try/catch` и проверьте `ArgumentException` на отсутствие семейств.

**Q: Подходит ли Aspose.Drawing для веб‑приложений?**  
A: Абсолютно. Библиотека работает в ASP.NET Core, Azure Functions и других серверных средах.

**Q: Можно ли изменить цвет или стиль текста?**  
A: Да. Используйте разные типы `Brush` (например, `LinearGradientBrush`) и измените перечисление `FontStyle`.

**Q: Где можно получить временную лицензию для тестирования?**  
A: Скачайте пробную лицензию со страницы [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).

## Заключение

Следуя этим шагам, вы узнали, как **save PNG image** файлы, которые динамически **list installed fonts**, **show font families**, **create graphics from bitmap** и **draw text with fonts** с помощью Aspose.Drawing для .NET. Теперь вы знаете, как **create bitmap graphics C#**, регулировать разрешение bitmap и при необходимости использовать пользовательские шрифты. Не стесняйтесь экспериментировать с другими шрифтами, цветами и размерами bitmap, чтобы соответствовать визуальным требованиям вашего проекта.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Последнее обновление:** 2026-02-25  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose