---
date: 2026-03-02
description: Улучшите иллюстрации в своих документах с помощью Aspose.Drawing для
  .NET! Узнайте пошагово, как добавлять выноски для более ясных и информативных визуальных
  материалов.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Как добавить выноски с помощью Aspose.Drawing для .NET
url: /ru/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Создание выносов в Aspose.Drawing

## Введение
Если вы задаетесь вопросом, **как добавить выноски** к вашим изображениям или диаграммам с помощью Aspose.Drawing для .NET, вы должны найти нужное место. В этом руководстве мы пройдём весь процесс — от загрузки изображений до рисования красиво оформленных выводов — чтобы ваши иллюстрации стали более понятными и информативными.

## Быстрые ответы
- **Какая библиотека нужна?** Aspose.Drawing для .NET (можно загрузить с официального сайта).
- **Какие версии .NET используются?** .NET Framework4.5+, .NETCore3.1+, .NET5/6+.
- **Нужна ли лицензия?** Бесплатная пробная версия предназначена для разработки; Для производства необходима коммерческая лицензия.
- **Сколько времени занимает производство?** Обычно для базового вызова требуется менее 10 минут.
- **Можно ли настроить цвета и шрифты?** Да — все управляется стандартными объектами GDI+ (Перо, Шрифт, Кисть).

## Как добавить выноски в Aspose.Drawing
Ниже представлено краткое пошаговое руководство, показывающее **как добавить выноски** к изображению. Смело копируйте, экспериментируйте с позициями и адаптируйте стиль под свой бренд.

## Предварительные условия
Перед тем как начать, убедитесь, что у вас есть:

- Базовые знания языка программирования C#.
- Установлена ​​библиотека Aspose.Drawing. Вы можете скачать его [здесь](https://releases.aspose.com/drawing/net/).
– Документ или изображение, к которому вы хотите добавить выноски.

## Импортировать пространства имен
Убедитесь, что в проекте подключены необходимые помещения:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Шаг 1: Загрузка изображения  
Начните с загрузки изображения в том месте, где вы хотите добавить выноски. Замените `"Ваш каталог документов"` и `"gears.png"` на фактическое имя вашего каталога и файла изображения.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Шаг 2: Создание объекта Graphics  
Создайте объект `Graphics` из изображения для выполнения операций рисования.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Шаг 3: Определение позиций выноски  
Определите начальную и конечную точки для каждой выноски, а также значение выноски и единицу измерения.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## Шаг 4: Рисование выноски  
Реализуйте метод `DrawCallOut` для рисования выносок на изображении.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Шаг 5: Сохранение изображения  
Сохраните изображение с выносками в нужном каталоге.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Исходный код функции отрисовки выноски

```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## Распространенные проблемы и советы
- **Неправильные координаты якоря** — убедитесь, что начальная и конечная точки находятся в пределах изображения; в противном случае выноска может быть обрезана.
- **Перекрытие текста** — отрегулируйте spaceSize или размер шрифта, если метка конфликтует с другой графикой.
- **Производительность** – для очень больших изображений рассмотрите возможность удаления объектов Pen, Font и Brush после использования, чтобы освободить ресурсы.

## Заключение
Поздравляем! Теперь вы знаете, **как добавить выноски** к изображению с помощью Aspose.Drawing для .NET. Не стесняйтесь экспериментировать с разными позициями, цветами и шрифтами, чтобы они соответствовали вашему визуальному стилю.

## Часто задаваемые вопросы

### Могу ли я использовать Aspose.Drawing для других типов иллюстраций?
Да, Aspose.Drawing поддерживает широкий спектр операций рисования для различных типов иллюстраций.

### Совместим ли Aspose.Drawing с различными форматами изображений?
Безусловно! Aspose.Drawing поддерживает популярные форматы изображений, такие как PNG, JPEG, GIF и другие.

### Где я могу найти больше примеров и документации?
Ознакомьтесь с подробной документацией [здесь](https://reference.aspose.com/drawing/net/).

### Как получить поддержку, если у меня возникнут проблемы?
Посетите [форум Aspose.Drawing](https://forum.aspose.com/c/drawing/44) для получения поддержки от сообщества.

### Могу ли я попробовать Aspose.Drawing перед покупкой?
Конечно! Начните с бесплатной пробной версии [здесь](https://releases.aspose.com/).

**Дополнительные вопросы и ответы**

**В: Можно ли изменить стиль линии выноски (пунктирная, точечная)?**
О: Да — просто настройте свойство `Pen.DashStyle` перед рисованием линии.

**В: Можно ли добавить цвет фона к метке выноски?**
О: Конечно. Создайте `SolidBrush` с желаемым цветом и залейте прямоугольник за текстом перед вызовом `DrawString`.

**В: Как обеспечить одинаковый внешний вид выноски на дисплеях с высоким разрешением?**
О: Установите `graphics.PageUnit = GraphicsUnit.Pixel` (как показано) и используйте векторные измерения для обеспечения согласованности масштабирования.

--

**Последнее обновление:** 02.03.2026
**Протестировано с:** Aspose.Drawing 24.11 для .NET
**Автор:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}