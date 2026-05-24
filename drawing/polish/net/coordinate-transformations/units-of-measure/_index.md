---
date: 2026-05-24
description: Dowiedz się, jak ustawić jednostkę w Aspose.Drawing dla .NET, łatwo konwertować
  jednostki graficzne i opanować precyzyjne pomiary przy renderowaniu grafiki.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Jednostki miary w Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak ustawić jednostkę w Aspose.Drawing dla .NET – Jednostki miary
url: /pl/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak ustawić jednostkę w Aspose.Drawing dla .NET – Jednostki miary

## Wprowadzenie

Witamy w świecie Aspose.Drawing dla .NET, gdzie precyzja i elastyczność spotykają się w manipulacji grafiką. W tym samouczku odkryjesz **jak ustawić jednostkę** dla swoich rysunków, nauczysz się **konwertować jednostki graficzne** między punktami, milimetrami i calami oraz zobaczysz przykłady z rzeczywistego świata, które sprawiają, że Twoje obrazy są idealnie dopasowane pikselowo. Niezależnie od tego, czy tworzysz raporty, miniatury, czy niestandardowe wykresy, opanowanie jednostek miary jest niezbędne do spójnego renderowania na różnych urządzeniach.

## Szybkie odpowiedzi
- **Jaki jest podstawowy sposób zmiany jednostek?** Wywołaj `graphics.PageUnit = PageUnit.Point` (lub `.Millimeter`, `.Inch`) na obiekcie `Graphics`.  
- **Która jednostka równa się 1/72 cala?** Punkty.  
- **Ile milimetrów mieści się w calu?** 25.4 mm = 1 inch.  
- **Czy potrzebuję dodatkowych bibliotek do używania jednostek?** Nie, podstawowa biblioteka Aspose.Drawing dostarcza wszystkie stałe jednostek.  
- **Czy mogę mieszać jednostki w jednym obrazie?** Ustaw jednostkę raz na instancję `Graphics`; rysuj wszystko używając tej jednostki dla spójności.

## Wymagania wstępne

Zanim zanurkujemy w samouczek, upewnij się, że masz spełnione następujące wymagania:

- Aspose.Drawing dla .NET: Upewnij się, że masz zainstalowaną bibliotekę. Możesz ją pobrać [tutaj](https://releases.aspose.com/drawing/net/).
- Katalog dokumentów: Miej wyznaczony katalog, w którym chcesz zapisywać utworzone dokumenty.
- Podstawowa znajomość C#: Zalecane jest podstawowe zrozumienie C#, aby w pełni wykorzystać ten przewodnik.

## Importowanie przestrzeni nazw

Zanim zaczniemy, zaimportujmy niezbędne przestrzenie nazw, aby skutecznie korzystać z Aspose.Drawing:

```csharp
using System.Drawing;
```

Teraz rozbijmy każdy przykład na kilka kroków:

## Jak ustawić jednostkę na punkty?

Klasa `Bitmap` reprezentuje obraz w pamięci, który służy jako płótno do rysowania. Załaduj swój bitmap, utwórz obiekt `Graphics` i ustaw jednostkę strony na punkty — to informuje Aspose.Drawing, aby interpretował wszystkie współrzędne jako wartości 1/72 cala. Używanie punktów daje precyzyjną kontrolę nad grafiką gotową do druku i pozwala określać szerokość linii z wysoką dokładnością.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Krok 1: Utwórz bitmapę  
Klasa `Bitmap` reprezentuje obraz w pamięci, który służy jako płótno do rysowania.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Krok 2: Utwórz obiekt Graphics  
`Graphics` udostępnia metody rysowania do renderowania kształtów i tekstu na `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Krok 3: Ustaw jednostkę strony na punkty  
`PageUnit` jest wyliczeniem określającym jednostkę miary dla współrzędnych strony. `PageUnit.Point` definiuje punkty jako jednostkę miary (1 punkt = 1/72 cala). To ustawienie ma zastosowanie do wszystkich kolejnych wywołań rysujących.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Krok 4: Narysuj prostokąt w punktach  
Gdy narysujesz prostokąt po ustawieniu jednostki, podane wymiary są interpretowane jako punkty, zapewniając precyzyjne rozmiary.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Jak ustawić jednostkę na milimetry?

`PageUnit` jest wyliczeniem określającym jednostkę miary dla współrzędnych strony. Przejście na milimetry jest przydatne, gdy potrzebujesz wymiarów metrycznych, na przykład przy generowaniu diagramów inżynieryjnych. Aspose.Drawing traktuje 1 mm jako 1/25.4 cala, co pozwala dopasować grafikę do fizycznych pomiarów używanych w produkcji i dokumentacji technicznej.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Krok 1: Ustaw jednostkę strony na milimetry  
Przypisz `PageUnit.Millimeter` do obiektu `Graphics`; wszystkie współrzędne są teraz mapowane na system metryczny.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Krok 2: Narysuj prostokąt w milimetrach  
Szerokość i wysokość prostokąta są teraz wyrażone w milimetrach, co ułatwia dopasowanie do fizycznych pomiarów i zapewnia, że wydrukowane wyjście odpowiada rzeczywistym rozmiarom.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Jak ustawić jednostkę na cale?

`Graphics` udostępnia metody rysowania do renderowania kształtów i tekstu na `Bitmap`. Cale są domyślną jednostką w wielu amerykańskich narzędziach projektowych. Ustawienie jednostki na cale pozwala myśleć w znanych jednostkach przy układaniu elementów UI i upraszcza przejście od projektowania ekranowego do druku, gdzie cale są powszechnie używane.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Krok 1: Ustaw jednostkę strony na cale  
`PageUnit.Inch` zmienia system współrzędnych tak, że 1 jednostka równa się 1 cala, zapewniając prosty sposób na określanie rozmiarów elementów w układach przeznaczonych do druku.

CODE_BLOCK_PLACEHOLDER_10_END

### Krok 2: Narysuj prostokąt w calach  
Teraz każdy kształt, który narysujesz, używa cali jako podstawy pomiarowej, co jest idealne dla układów drukowanych i do komunikowania wymiarów interesariuszom przyzwyczajonym do jednostek imperialnych.

CODE_BLOCK_PLACEHOLDER_11_END

## Zapisz wynik

Po zakończeniu przykładów zapisz powstały obraz w swoim katalogu dokumentów. Metoda `Bitmap.Save` zapisuje plik w formacie, który określisz (PNG, JPEG itp.).

CODE_BLOCK_PLACEHOLDER_12_END

Teraz pomyślnie opanowałeś różnorodne jednostki miary w Aspose.Drawing dla .NET, tworząc wizualną reprezentację prostokątów przy użyciu punktów, milimetrów i cali.

## Dlaczego warto używać systemu jednostek Aspose.Drawing?

Aspose.Drawing obsługuje **ponad 30 formatów obrazu** i może przetwarzać obrazy do **5000 × 5000 pikseli** bez ładowania całego pliku do pamięci, zapewniając wysoką wydajność przy generowaniu grafiki na dużą skalę. Poprzez explicite ustawienie jednostki eliminujesz zgadywanie, zmniejszasz liczbę błędów konwersji i zapewniasz, że Twoje wyjście odpowiada dokładnym wymiarom fizycznym na wszystkich platformach.

## Typowe problemy i rozwiązania

- **Nieoczekiwany rozmiar po zapisaniu** – Zweryfikuj, że ustawiłeś `graphics.PageUnit` **przed** jakimikolwiek wywołaniami rysującymi; zmiana jednostki później nie zmieni retroaktywnie istniejących kształtów.  
- **Rozmyte wyjście na ekranach o wysokiej rozdzielczości DPI** – Zwiększ rozdzielczość bitmapy (np. `new Bitmap(width, height, 300)`) aby dopasować się do docelowego DPI.  
- **Mieszane jednostki w jednym obrazie** – Utwórz osobne instancje `Graphics` dla każdej jednostki lub wykonaj ręczną konwersję przed rysowaniem.

## Najczęściej zadawane pytania

### Q1: Czy mogę używać Aspose.Drawing dla .NET z innymi frameworkami .NET?
A1: Tak, Aspose.Drawing jest kompatybilny z różnymi frameworkami .NET, zapewniając elastyczność w środowisku programistycznym.

### Q2: Czy dostępna jest bezpłatna wersja próbna?
A2: Tak, możesz wypróbować Aspose.Drawing w wersji próbnej [tutaj](https://releases.aspose.com/).

### Q3: Jak uzyskać wsparcie dla Aspose.Drawing dla .NET?
A3: Odwiedź [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) w celu uzyskania wsparcia społeczności i dyskusji.

### Q4: Czy mogę kupić tymczasową licencję na krótkoterminowe projekty?
A4: Tak, możesz uzyskać tymczasową licencję [tutaj](https://purchase.aspose.com/temporary-license/).

### Q5: Gdzie mogę znaleźć szczegółową dokumentację Aspose.Drawing?
A5: Kompleksowa dokumentacja jest dostępna [tutaj](https://reference.aspose.com/drawing/net/).

**Ostatnia aktualizacja:** 2026-05-24  
**Testowano z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Transformacja układu współrzędnych – Transformacja strony w Aspose.Drawing dla .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Samouczek transformacji macierzy: Transformacje macierzy w Aspose.Drawing dla .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Jak zastosować transformację: Transformacja lokalna w Aspose.Drawing dla .NET](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}