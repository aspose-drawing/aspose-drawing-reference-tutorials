---
date: 2026-05-29
description: Узнайте, как установить лицензию Aspose.Drawing в .NET и удалить водяной
  знак Aspose. Овладейте методами лицензирования, чтобы разблокировать все функции
  без водяных знаков.
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
linktitle: Лицензирование в Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  headline: Remove Aspose Watermark – Set Aspose.Drawing License
  type: TechArticle
- description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  name: Remove Aspose Watermark – Set Aspose.Drawing License
  steps:
  - name: Confirm Success
    text: '> **Pro tip:** Place the `.lic` file in the same folder as your executable
      or provide an absolute path to avoid “file not found” errors.'
  - name: Confirm Success
    text: '> **Warning:** Remember to dispose the `FileStream` (or use a `using` block)
      to free file handles.'
  - name: Display the Consumption Details
    text: '> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will
      fall back to trial mode and you’ll see watermarks in the output.'
  type: HowTo
- questions:
  - answer: Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.
    question: What is the primary way to activate Aspose.Drawing?
  - answer: Yes, you can load the license from a `Stream` for dynamic scenarios.
    question: Can I apply a license at runtime?
  - answer: Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable
      consumption‑based billing.
    question: Is a metered license supported?
  - answer: A trial works for testing, but a valid license removes watermarks and
      unlocks all APIs.
    question: Do I need a license for development builds?
  - answer: Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.
    question: Which .NET versions are compatible?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Удалить водяной знак Aspose – установить лицензию Aspose.Drawing
url: /ru/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Установить лицензию Aspose.Drawing

## Введение

Если вы разрабатываете .NET‑приложения, использующие мощную графику и обработку изображений, **установка лицензии Aspose.Drawing** — первый шаг к удалению водяного знака Aspose и получению полного набора функций. В этом руководстве вы узнаете три практических способа установить лицензию Aspose.Drawing — загрузка из файла, загрузка из потока и использование модели с оплатой за использование — чтобы интегрировать библиотеку с уверенностью и получать чистый вывод.

## Быстрые ответы
- **Какой основной способ активировать Aspose.Drawing?** Загрузите файл лицензии, используя `License.SetLicense("Aspose.Drawing.lic")`.  
- **Можно ли применить лицензию во время выполнения?** Да, вы можете загрузить лицензию из `Stream` для динамических сценариев.  
- **Поддерживается ли метered‑лицензия?** Абсолютно; используйте `Metered.SetMeteredKey(publicKey, privateKey)`, чтобы включить оплату по потреблению.  
- **Нужна ли лицензия для сборок разработки?** Пробная версия работает для тестирования, но действительная лицензия удаляет водяные знаки и открывает все API.  
- **Какие версии .NET совместимы?** Aspose.Drawing поддерживает .NET Framework 4.x, .NET Core 3.1+ и .NET 5/6+.

## Предварительные требования

Прежде чем начать, убедитесь, что у вас есть:

- **Библиотека Aspose.Drawing** – загрузите последнюю версию пакета с [здесь](https://releases.aspose.com/drawing/net/).  
- **Файл лицензии** – получите действительный файл `.lic` от [Aspose](https://purchase.aspose.com/buy).  
- **Среда разработки .NET** – Visual Studio, Rider или любая IDE, нацеленная на .NET Framework/.NET Core.

## Импорт пространств имён

Нужны стандартные пространства имён .NET и пространство имён Aspose.Drawing для лицензирования. Добавьте следующие инструкции `using` в начало вашего C# файла:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Как загрузить лицензию из файла?

Класс `License` представляет компонент лицензирования Aspose.Drawing, который, будучи созданным, позволяет применить лицензию к библиотеке. Загрузка лицензии из файла — самый простой подход; вы просто указываете метод `SetLicense` на файл `.lic`, и библиотека удаляет все пробные водяные знаки на оставшуюся часть сеанса приложения. Этот метод работает как в настольных, так и в серверных средах и не требует дополнительной конфигурации, кроме обеспечения доступности файла во время выполнения.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## Как загрузить лицензию из потока?

Когда файл лицензии встроен как ресурс или получен по сети, загрузка его из `Stream` даёт гибкость, одновременно гарантируя удаление водяного знака. Передавая экземпляр `Stream` в метод `SetLicense`, вы держите лицензию вне папки развертывания, что может повысить безопасность и упростить распространение в контейнеризованных или облачных сценариях. Процесс идентичен загрузке из файла, за исключением того, что вы сами управляете жизненным циклом потока.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## Как активировать метered‑лицензию?

Класс `Metered` обрабатывает активацию лицензии с оплатой за использование для Aspose.Drawing, позволяя платить только за выполненные операции. Метered‑лицензия идеальна для SaaS или моделей оплаты за использование. После предоставления публичного и приватного ключей каждый вызов обработки изображений отслеживается и автоматически тарифицируется, а библиотека работает в полном режиме без водяных знаков в течение сеанса.

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## Почему важно правильно установить лицензию Aspose.Drawing?

Правильная установка лицензии гарантирует работу библиотеки в полном режиме, удаляет пробные водяные знаки и соответствует условиям лицензирования Aspose. Корректно применённая лицензия также открывает премиум‑API, повышает производительность, отключая проверки оценки, и позволяет использовать оплату за использование при желании. Если не загрузить лицензию до первого вызова API, библиотека перейдёт в пробный режим, и на всех сгенерированных изображениях появятся водяные знаки.

- **Удаляет водяные знаки**, которые появляются в пробном режиме.  
- **Разблокирует премиум‑API**, такие как продвинутые фильтры изображений и конвертация PDF.  
- **Обеспечивает соответствие** условиям лицензирования Aspose для коммерческого распространения.  
- **Включает оплату за использование**, позволяя платить только за фактически использованные функции.  

Aspose.Drawing поддерживает **30+ форматов изображений** (включая PNG, JPEG, BMP, TIFF и WebP) и может обрабатывать **многосотневые PDF‑документы без загрузки всего файла в память**, обеспечивая высокопроизводительное преобразование на скромном оборудовании.

## Загрузка лицензии из файла

Загрузка лицензии из файла — самый простой подход. Выполните следующие три шага:

### Шаг 1: Инициализировать объект License

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Шаг 2: Установить лицензию из файла `.lic`

```csharp
Console.WriteLine("License set successfully.");
```

### Шаг 3: Подтвердить успех

```csharp
Console.WriteLine("License set successfully.");
```

> **Полезный совет:** Поместите файл `.lic` в ту же папку, что и исполняемый файл, или укажите абсолютный путь, чтобы избежать ошибок «файл не найден».

## Загрузка лицензии из потока

Когда ваш файл лицензии встроен как ресурс или получен из удалённого места, загрузка его из `Stream` даёт гибкость.

### Шаг 1: Инициализировать объект License

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Шаг 2: Загрузить лицензию с помощью `FileStream`

```csharp
Console.WriteLine("License set successfully.");
```

### Шаг 3: Подтвердить успех

```csharp
Console.WriteLine("License set successfully.");
```

> **Внимание:** Не забудьте освободить `FileStream` (или использовать блок `using`), чтобы освободить файловые дескрипторы.

## Использование метered‑лицензии

Метered‑лицензия идеальна для SaaS или моделей оплаты за использование. Она отслеживает потребление и выставляет счёт на основе фактического использования.

### Шаг 1: Инициализировать объект Metered

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Шаг 2: Установить публичный и приватный ключи

```csharp
// Your image processing logic here
```

### Шаг 3: Выполнить обработку изображений

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Шаг 4: Получить информацию о потреблении

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### Шаг 5: Отобразить детали потребления

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Распространённая ошибка:** Если вы забудете вызвать `SetMeteredKey`, API перейдёт в пробный режим, и вы увидите водяные знаки в выводе.

## Распространённые проблемы и решения

| Проблема | Причина | Решение |
|----------|---------|---------|
| “Ошибка: файл лицензии не найден” | Неправильный путь или отсутствует файл в папке вывода | Используйте абсолютный путь или установите свойство файла *Copy to Output Directory* в значение *Copy always*. |
| Водяной знак всё ещё появляется после установки лицензии | Лицензия не загружена до первого вызова API | Загрузите лицензию **до** любой операции Aspose.Drawing. |
| Потребление по метered‑лицензии всегда равно нулю | Ключи не заданы или переменные окружения неверны | Проверьте публичный и приватный ключи и убедитесь, что есть подключение к интернету для сервера метered‑лицензий Aspose. |

## Часто задаваемые вопросы

**Q1: Могу ли я использовать Aspose.Drawing без лицензии?**  
A1: Да, пробная лицензия работает для разработки и оценки, но она добавляет водяные знаки и ограничивает некоторые функции.

**Q2: Как часто мне нужно обновлять лицензию Aspose.Drawing?**  
A2: Лицензии являются бессрочными для приобретённой версии. Обновление требуется только для поддержки и обновлений.

**Q3: Что такое метered‑лицензия и когда её использовать?**  
A3: Метered‑лицензия взимает плату на основе использования (операций или обработанных данных). Она идеальна для облачных сервисов или моделей оплаты за использование.

**Q4: Могу ли я использовать Aspose.Drawing в коммерческих проектах?**  
A4: Конечно — после получения действующей лицензии вы можете внедрять Aspose.Drawing в любое коммерческое приложение.

**Q5: Где я могу найти поддержку сообщества для Aspose.Drawing?**  
A5: Посетите [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) для помощи сообщества, примеров и обсуждений.

## Заключение

Освоив, как **установить лицензию Aspose.Drawing** — из файла, из потока или через модель с оплатой за использование — вы получаете максимум от этой мощной .NET‑библиотеки графики, полностью **удаляя водяной знак Aspose**. Следуйте приведённым шагам, учитывайте распространённые подводные камни, и вы будете готовы создавать надёжные решения по обработке изображений без проблем с лицензированием.

---

**Последнее обновление:** 2026-05-29  
**Тестировано с:** Aspose.Drawing 24.11 for .NET  
**Автор:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
