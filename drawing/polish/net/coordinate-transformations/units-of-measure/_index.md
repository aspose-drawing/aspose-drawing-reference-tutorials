---
title: Jednostki miary w Aspose.Drawing dla .NET
linktitle: Jednostki miary w Aspose.Drawing
second_title: Aspose.Drawing .NET API - alternatywa dla System.Drawing.Common
description: Odkryj wszechstronność Aspose.Drawing dla .NET w tym szczegółowym samouczku, opanowując jednostki miary dla precyzyjnej grafiki.
weight: 14
url: /pl/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jednostki miary w Aspose.Drawing dla .NET

## Wstęp

Witamy w świecie Aspose.Drawing dla .NET, gdzie precyzja i elastyczność spotykają się w manipulacji grafiką. W tym samouczku zagłębimy się w zawiłości jednostek miary w Aspose.Drawing, dostarczając przewodnik krok po kroku, jak wykorzystać moc tej niezwykłej biblioteki.

## Warunki wstępne

Zanim przejdziemy do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:

-  Aspose.Drawing dla .NET: Upewnij się, że masz zainstalowaną bibliotekę. Możesz go pobrać[Tutaj](https://releases.aspose.com/drawing/net/).

- Katalog dokumentów: Miej wyznaczony katalog, w którym chcesz zapisywać utworzone dokumenty.

- Podstawowa znajomość języka C#: Aby w pełni wykorzystać ten przewodnik, zaleca się podstawową znajomość języka C#.

## Importuj przestrzenie nazw

Zanim zaczniemy, zaimportujmy niezbędne przestrzenie nazw, aby efektywnie korzystać z Aspose.Drawing:

```csharp
using System.Drawing;
```

Teraz podzielmy każdy przykład na wiele kroków:

## Punkty jako jednostki miary

1. Utwórz mapę bitową: Zainicjuj mapę bitową o określonej szerokości i wysokości.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Utwórz grafikę: Wygeneruj obiekt graficzny z mapy bitowej, aby na niej rysować.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Ustaw jednostkę strony na punkty: Zdefiniuj punkty jako jednostkę miary (1 punkt = 1/72 cala).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Narysuj prostokąt: Narysuj prostokąt, używając punktów jako jednostki.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Milimetry jako jednostki miary

1. Ustaw jednostkę strony na milimetry: Zmień jednostkę miary na milimetry (1 mm = 1/25,4 cala).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Narysuj prostokąt w milimetrach: Narysuj kolejny prostokąt, używając milimetrów jako jednostki.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Cale jako jednostki miary

1. Ustaw jednostkę strony na cale: Zmień jednostkę miary na cale.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Narysuj prostokąt w calach: Narysuj prostokąt, używając cali jako jednostki.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Zapisz wynik

Po ukończeniu przykładów zapisz powstały obraz w katalogu dokumentów:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Udało Ci się teraz z powodzeniem poruszać po różnych jednostkach miary w Aspose.Drawing dla .NET, tworząc wizualną reprezentację prostokątów za pomocą punktów, milimetrów i cali.

## Wniosek

W tym samouczku sprawdziliśmy, jak Aspose.Drawing dla .NET obsługuje różne jednostki miary. Manipulując punktami, milimetrami i calami, możesz osiągnąć precyzję i elastyczność swoich kreacji graficznych. Eksperymentuj z tymi koncepcjami, aby odblokować pełny potencjał Aspose.Drawing.

## Często zadawane pytania

### P1: Czy mogę używać Aspose.Drawing dla .NET z innymi frameworkami .NET?

O1: Tak, Aspose.Drawing jest kompatybilny z różnymi frameworkami .NET, zapewniając elastyczność w Twoim środowisku programistycznym.

### P2: Czy dostępny jest bezpłatny okres próbny?

 Odpowiedź 2: Tak, możesz poznać Aspose.Drawing w ramach bezpłatnej wersji próbnej[Tutaj](https://releases.aspose.com/).

### P3: Jak uzyskać wsparcie dla Aspose.Drawing dla .NET?

 A3: Odwiedź[Forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17) za wsparcie społeczności i dyskusje.

### P4: Czy mogę kupić tymczasową licencję na projekty krótkoterminowe?

 Odpowiedź 4: Tak, możesz uzyskać licencję tymczasową[Tutaj](https://purchase.aspose.com/temporary-license/).

### P5: Gdzie mogę znaleźć szczegółową dokumentację Aspose.Drawing?

 Odpowiedź 5: Dostępna jest obszerna dokumentacja[Tutaj](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
