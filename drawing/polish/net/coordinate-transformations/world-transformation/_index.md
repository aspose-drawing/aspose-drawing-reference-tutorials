---
date: 2026-06-23
description: Dowiedz się, jak zapisać PNG przy użyciu Aspose.Drawing, zastosować world
  transformations i konwertować grafikę do formatu PNG. Zawiera przykłady translate
  transform C# oraz wiele transformacji graficznych.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: World Transformation w Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak zapisać PNG przy użyciu Aspose.Drawing – World Transformation
url: /pl/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zapisać PNG przy użyciu Aspose.Drawing – Transformacja świata

## Zapis bitmapy jako PNG – Wprowadzenie

**Jak zapisać PNG** przy użyciu Aspose.Drawing jest powszechnym wymaganiem, gdy potrzebujesz wysokiej jakości, przezroczystych obrazów generowanych w locie. W tym samouczku nauczysz się **zapisywać bitmapę jako PNG**, stosować transformacje świata takie jak przesunięcie, obrót i skalowanie oraz ostatecznie konwertować grafikę na PNG — wszystko przy użyciu czystego, łatwego do utrzymania kodu C#. Niezależnie od tego, czy tworzysz silnik raportowania, komponent wykresów, czy własny renderer UI, opanowanie tych kroków pozwoli Ci tworzyć dynamiczne obrazy, które świetnie wyglądają na każdym urządzeniu.

## Szybkie odpowiedzi
- **Co oznacza „transformacja świata”?** Mapuje logiczne (światowe) współrzędne twojego rysunku na współrzędne strony (urządzenia).  
- **Czy mogę wyeksportować wynik jako PNG?** Tak – po narysowaniu po prostu wywołujesz `bitmap.Save(...)` z rozszerzeniem `.png`.  
- **Czy potrzebuję licencji na Aspose.Drawing?** Darmowa wersja próbna działa w fazie rozwoju; licencja komercyjna jest wymagana w produkcji.  
- **Czy jest to kompatybilne z .NET 6/7?** Absolutnie – Aspose.Drawing obsługuje .NET Framework 4.5+ oraz .NET Core/5/6/7.  
- **Ile transformacji mogę łączyć?** Możesz zastosować **wiele transformacji graficznych** kolejno (przesunięcie, obrót, skalowanie itp.).

## Czym jest transformacja świata w Aspose.Drawing?

Transformacja świata zmienia układ współrzędnych używany przez polecenia rysowania. Domyślnie (0,0) znajduje się w lewym górnym rogu bitmapy. Dzięki `TranslateTransform`, `RotateTransform` lub `ScaleTransform` możesz przemieścić ten punkt początkowy, obrócić kształty lub zmienić ich rozmiar bez modyfikacji oryginalnej geometrii.

## Jak zapisać PNG przy użyciu Aspose.Drawing?

Załaduj obiekt `Bitmap`, ustaw dowolne wymagane transformacje świata na jego instancji `Graphics`, narysuj kształty, a na końcu wywołaj `bitmap.Save("output.png", ImageFormat.Png)`. To jednowierszowe wywołanie zapisu tworzy bezstratny plik PNG, który zachowuje przezroczystość i wierność kolorów, co czyni go idealnym dla zasobów internetowych i nakładek UI.

## Dlaczego używać przykładu translacji grafiki?

Przykład translacji grafiki pozwala przenieść początek rysowania jednorazowo zamiast przeliczać każdy punkt. Takie podejście zmniejsza złożoność kodu, poprawia czytelność i pozwala silnikowi graficznemu efektywnie obsługiwać obliczenia macierzy, co może zwiększyć wydajność renderowania nawet o 30 % na dużych płótnach.

## Przykład translacji grafiki

**Przykład translacji grafiki** pokazuje, jak przeniesienie początku upraszcza pozycjonowanie. Zamiast przeliczać każdy punkt, przesuwasz układ współrzędnych jednorazowo i rysujesz, jakby nowy początek znajdował się w centrum płótna.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz:

- **Bibliotekę Aspose.Drawing** zintegrowaną w swoim projekcie .NET – pobierz ją z oficjalnej [strony wydania Aspose.Drawing](https://releases.aspose.com/drawing/net/).  
- **Katalog dokumentów**, w którym zostanie zapisany obraz wyjściowy.  
- Podstawową znajomość składni **C#** oraz Visual Studio lub wybranego IDE.  

Teraz zanurzmy się w kod!

## Importowanie przestrzeni nazw

`Bitmap`, `Graphics` oraz narzędzia rysunkowe Aspose znajdują się w tych przestrzeniach nazw.  
**Definicja:** `System.Drawing` dostarcza podstawowe typy GDI+, natomiast `Aspose.Drawing` rozszerza je o możliwości wieloplatformowe.

## Przewodnik krok po kroku

### Krok 1: Utwórz bitmapę

Zaczynamy od utworzenia pustego płótna, które będzie zawierało nasz rysunek.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` tworzy bitmapę 32‑bitową na piksel z wstępnie pomnożonym alfą, co jest optymalnym formatem dla wyjścia PNG, ponieważ zachowuje przezroczystość bez dodatkowych kroków konwersji.

- **Dlaczego 32bppPArgb?** Ten format pikseli obsługuje przezroczystość alfa i renderowanie kolorów wysokiej jakości, idealny dla wyjścia PNG.  
- **Wskazówka:** Dostosuj szerokość/wysokość, aby odpowiadały docelowemu rozmiarowi obrazu.

### Krok 2: Ustaw transformację świata (Przykład translacji grafiki)

`TranslateTransform` przesuwa początek układu współrzędnych do nowej lokalizacji.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` przesuwa punkt (0,0) do środka płótna. Po tym wywołaniu każdy kształt narysowany przy użyciu współrzędnych (0,0) pojawi się w środku obrazu.

- To przesuwa punkt (0,0) do (500, 400) – środka płótna o wymiarach 1000 × 800.  
- Możesz łączyć dodatkowe transformacje: `RotateTransform` obraca układ współrzędnych, a `ScaleTransform` go skalowuje, umożliwiając **wiele transformacji graficznych**.

### Krok 3: Narysuj prostokąt używając przekształconych współrzędnych

`DrawRectangle` rysuje prostokąt przy użyciu określonego pióra i współrzędnych.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` rysuje prostokąt wyśrodkowany na płótnie, ponieważ jego lewy górny róg jest przesunięty o połowę szerokości i wysokości od przekształconego początku.

- Lewy górny róg prostokąta zaczyna się w przekształconym początku (środku obrazu).  
- Śmiało eksperymentuj z innymi kształtami — elipsami, liniami lub własnymi ścieżkami.

### Krok 4: Zapisz wynik – Konwertuj grafikę do PNG

`Save` zapisuje bitmapę do pliku w określonym formacie obrazu.  
`ImageFormat` określa format pliku przy zapisywaniu obrazów, np. PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` zapisuje bezstratny plik PNG, który może być używany bezpośrednio w stronach internetowych lub komponentach UI.

- PNG zachowuje dokładne kolory i przezroczystość ustawioną wcześniej.  
- Zastąp `"Your Document Directory"` rzeczywistą ścieżką na swoim komputerze.

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| **Błąd „plik nie znaleziony”** przy zapisywaniu | Folder docelowy nie istnieje. | Utwórz folder programowo (`Directory.CreateDirectory`) przed wywołaniem `Save`. |
| **Pusty obraz** po transformacji | `TranslateTransform` wywołany po rysowaniu. | Upewnij się, że transformacja jest ustawiona **przed** jakimikolwiek poleceniami rysowania. |
| **Zniekształcone kolory** | Użycie niekompatybilnego formatu pikseli. | Trzymaj się `Format32bppPArgb` dla wyjścia PNG. |

## Najczęściej zadawane pytania

**P: Czy mogę zastosować więcej niż jedną transformację?**  
O: Tak – możesz łączyć `TranslateTransform`, `RotateTransform` i `ScaleTransform`, aby uzyskać złożone efekty w jednym potoku graficznym.

**P: Czy Aspose.Drawing jest darmowy dla projektów komercyjnych?**  
O: Dostępna jest darmowa wersja próbna do oceny, ale do użytku produkcyjnego wymagana jest licencja komercyjna.

**P: Czy to działa z .NET Core i .NET 5/6/7?**  
O: Absolutnie. Aspose.Drawing obsługuje wszystkie nowoczesne środowiska .NET, w tym .NET Core, .NET 5, .NET 6 i .NET 7.

**P: Gdzie mogę znaleźć pełną dokumentację API?**  
O: Pełna dokumentacja jest dostępna [tutaj](https://reference.aspose.com/drawing/net/).

**P: Jak rozwiązać problem brakującego pliku wyjściowego?**  
O: Zweryfikuj ciąg ścieżki, upewnij się, że masz uprawnienia do zapisu i potwierdź, że katalog istnieje przed wywołaniem `Save`.

## Zakończenie

Nauczyłeś się teraz **jak zapisać PNG** przy użyciu Aspose.Drawing, zastosowałeś **transformację świata** i wykonałeś **przykład translacji grafiki**, który można rozszerzyć o obrót lub skalowanie. Opanowując te elementy, możesz generować dynamiczne obrazy, tworzyć własne wykresy lub budować grafiki w locie dla dowolnej aplikacji .NET.

---

**Ostatnia aktualizacja:** 2026-06-23  
**Testowano z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose  
**Powiązane zasoby:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Powiązane samouczki

- [Samouczek transformacji macierzy: Transformacje macierzy w Aspose.Drawing dla .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Jak obrócić obraz przy użyciu globalnej transformacji Aspose.Drawing](/drawing/net/coordinate-transformations/global-transformation/)
- [Transformacja układu współrzędnych – Transformacja strony w Aspose.Drawing dla .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}