---
date: 2026-05-29
description: Dowiedz się, jak zapisać PNG i rysować krzywe kardynalne w .NET z Aspose.Drawing.
  Zapisz krzywą jako PNG, twórz płynne grafiki i generuj bitmapę do pliku bez wysiłku.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Rysowanie krzywych kardynalnych w Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak zapisać PNG i rysować krzywe kardynalne przy użyciu Aspose.Drawing
url: /pl/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zapisać PNG i rysować splajny kardynalne przy użyciu Aspose.Drawing

## Wprowadzenie

W tym samouczku odkryjesz **how to save PNG** pliki, rysując jednocześnie płynne splajny kardynalne przy użyciu Aspose.Drawing dla .NET. Niezależnie od tego, czy tworzysz komponent wykresów, edytor diagramów, czy po prostu potrzebujesz wyeksportować niestandardową krzywą jako PNG, poniższe kroki przeprowadzą Cię przez tworzenie bitmapowego płótna, rysowanie splajnu piórem i zapisywanie wyniku na dysku. Zobaczysz także, dlaczego Aspose.Drawing jest niezawodną, wieloplatformową alternatywą dla System.Drawing.Common.

## Szybkie odpowiedzi
- **Co robi główna metoda?** `Graphics.DrawCurve` interpoluje serię punktów w płynny splajn kardynalny.  
- **Jaki format jest używany do zapisu obrazu?** PNG za pomocą `Bitmap.Save`.  
- **Czy potrzebuję licencji do zapisywania obrazów?** Wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę zmienić napięcie krzywej?** Tak, przeciążenia `DrawCurve` pozwalają określić napięcie.  
- **Czy Aspose.Drawing jest kompatybilny z .NET 6+?** Zdecydowanie – obsługuje .NET Framework oraz .NET Core/5/6.

## Co oznacza „how to save PNG” w kontekście Aspose.Drawing?

Zapisanie PNG oznacza konwersję bitmapy w pamięci, na której rysujesz, do fizycznego pliku PNG na dysku. Proces zapisuje dane pikseli przy użyciu bezstratnej kompresji, zachowując dokładne kolory oraz informacje o kanale alfa. Metoda `Bitmap.Save` z Aspose.Drawing obsługuje kodowanie PNG automatycznie, więc nie musisz samodzielnie zarządzać szczegółami formatu.

## Dlaczego rysować splajn kardynalny przy użyciu Aspose.Drawing?

Splajn kardynalny tworzy płynną, płynącą krzywą, która ściśle podąża za zestawem punktów kontrolnych, co czyni go idealnym do wizualizacji danych, grafiki interfejsu użytkownika i kształtów niestandardowych. Aspose.Drawing obsługuje **ponad 30 formatów obrazu** i może renderować grafiki wielostronicowe bez ładowania całego pliku do pamięci, zapewniając zarówno szybkość, jak i elastyczność.

## Wymagania wstępne

- Visual Studio (dowolna aktualna wersja) zainstalowane.  
- Biblioteka Aspose.Drawing dla .NET. Możesz ją pobrać [tutaj](https://releases.aspose.com/drawing/net/).  
- Podstawowa znajomość programowania w C#.

## Importowanie przestrzeni nazw

W swoim pliku C# rozpocznij od zaimportowania niezbędnej przestrzeni nazw:

Przestrzeń nazw `Aspose.Drawing` zawiera wszystkie podstawowe typy, takie jak `Bitmap`, `Graphics` i `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Krok 1: Utwórz Bitmapę (Płótno)

Najpierw utwórz bitmapę, która będzie pełnić rolę płótna dla twojego rysunku. Ta bitmapa jest miejscem, w którym splajn zostanie wyrenderowany przed **zapisaniem obrazu**.

Bitmapa reprezentuje obraz w pamięci z określonym formatem pikseli i wymiarami.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Krok 2: Utwórz obiekt Graphics

Następnie uzyskaj obiekt `Graphics` z bitmapy. Obiekt ten zapewnia powierzchnię do rysowania.

`Graphics` zapewnia powierzchnię do rysowania kształtów, tekstu i obrazów na bitmapie.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Krok 3: Zdefiniuj Pen i narysuj krzywą

Zdefiniuj `Pen` o żądanym kolorze i szerokości, a następnie narysuj splajn kardynalny przy użyciu `DrawCurve`. To demonstruje technikę **draw curve with pen** i służy jako **przykład splajnu kardynalnego**.

`Pen` kapsułkuje kolor, szerokość i styl linii używany do rysowania linii i krzywych.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Krok 4: Zapisz obraz (Zapisz krzywą jako PNG)

Na koniec zapisz bitmapę do pliku PNG. To jest sedno **how to save PNG** w tym samouczku.

`Bitmap.Save` zapisuje obraz do pliku w określonym formacie, takim jak PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Pro tip:** Użyj `Path.Combine`, aby bezpiecznie budować ścieżki plików na różnych platformach.

Gratulacje! Pomyślnie narysowałeś splajn kardynalny i zapisałeś wynik jako obraz PNG przy użyciu Aspose.Drawing dla .NET. Śmiało eksperymentuj z różnymi tablicami punktów, kolorami pióra lub szerokościami linii, aby dostosować swoje krzywe.

## Typowe przypadki użycia

- **Wizualizacje danych** – płynne wykresy liniowe, które wymagają precyzyjnych punktów kontrolnych.  
- **Niestandardowe komponenty UI** – rysowanie pokręteł, suwaków lub dekoracyjnych obramowań.  
- **Grafika do eksportu** – generowanie zasobów PNG w locie dla raportów lub treści internetowych.

## Rozwiązywanie problemów i wskazówki

- **Obraz jest pusty?** Upewnij się, że format pikseli bitmapy obsługuje alfa (`Format32bppPArgb`) i że wywołujesz `graphics.Clear(Color.Transparent)`, jeśli to konieczne.  
- **Nieoczekiwany kształt krzywej?** Dostosuj parametr napięcia, używając przeciążenia `DrawCurve(pen, points, tension)`.  
- **Błędy dostępu do pliku?** Sprawdź, czy docelowy katalog istnieje i czy aplikacja ma uprawnienia do zapisu.

## Najczęściej zadawane pytania

**Q1: Czy mogę używać Aspose.Drawing w projektach komercyjnych?**  
A1: Tak, Aspose.Drawing jest odpowiedni zarówno dla projektów prywatnych, jak i komercyjnych. Sprawdź szczegóły licencjonowania na [stronie zakupu](https://purchase.aspose.com/buy).

**Q2: Jak mogę uzyskać tymczasową licencję do testów?**  
A2: Uzyskaj tymczasową licencję do celów testowych [tutaj](https://purchase.aspose.com/temporary-license/).

**Q3: Gdzie mogę znaleźć dodatkowe wsparcie?**  
A3: Odwiedź [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) w celu uzyskania wsparcia społeczności i dyskusji.

**Q4: Czy dostępna jest darmowa wersja próbna?**  
A4: Tak, wypróbuj funkcje w wersji [darmowej próby](https://releases.aspose.com/) przed zakupem.

**Q5: Jak uzyskać dostęp do dokumentacji?**  
A5: Odwołaj się do obszernej [dokumentacji](https://reference.aspose.com/drawing/net/) w celu uzyskania szczegółowych informacji i przykładów.

---

**Ostatnia aktualizacja:** 2026-05-29  
**Testowano z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Zapisz bitmapę jako PNG i rysuj zamknięte krzywe przy użyciu Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Zapisz bitmapę C# – rysuj splajny Beziera przy użyciu Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Zapisz bitmapę jako PNG z użyciem stałych pędzli w Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}