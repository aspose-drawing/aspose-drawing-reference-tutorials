---
date: 2025-11-29
description: Dowiedz się, jak tworzyć bitmapy przy użyciu Aspose.Drawing, stosować
  transformacje świata i konwertować grafikę na PNG. Przewodnik krok po kroku dla
  programistów .NET.
linktitle: World Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Utwórz bitmapę przy użyciu Aspose.Drawing – przewodnik po transformacji świata
url: /pl/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Utwórz bitmapę z Aspose.Drawing – Transformacja świata

## Wprowadzenie

Witamy! W tym samouczku **utworzysz bitmapę z Aspose.Drawing** i poznasz transformacje świata, które pozwalają przesuwać, obracać lub skalować grafikę z łatwością. Niezależnie od tego, czy potrzebujesz **przykładu translacji grafiki**, chcesz **konwertować grafikę do PNG**, czy planujesz **wiele transformacji grafiki**, ten przewodnik przeprowadzi Cię krok po kroku w jasnym, konwersacyjnym stylu.

## Szybkie odpowiedzi
- **Co oznacza „transformacja świata”?** Mapuje logiczne (światowe) współrzędne Twojego rysunku na współrzędne strony (urządzenia).  
- **Czy mogę wyeksportować wynik jako PNG?** Tak – po rysowaniu po prostu wywołujesz `bitmap.Save(...)` z rozszerzeniem `.png`.  
- **Czy potrzebuję licencji na Aspose.Drawing?** Darmowa wersja próbna działa w trakcie rozwoju; licencja komercyjna jest wymagana w produkcji.  
- **Czy jest to kompatybilne z .NET 6/7?** Absolutnie – Aspose.Drawing obsługuje .NET Framework 4.5+ oraz .NET Core/5/6/7.  
- **Ile transformacji mogę łączyć?** Możesz zastosować **wiele transformacji grafiki** kolejno (przesunięcie, obrót, skalowanie itp.).

## Czym jest transformacja świata w Aspose.Drawing?

Transformacja świata zmienia układ współrzędnych używany przez polecenia rysowania. Domyślnie (0,0) znajduje się w lewym górnym rogu bitmapy. Dzięki `TranslateTransform`, `RotateTransform` lub `ScaleTransform` możesz przemieścić ten punkt początkowy, obracać kształty lub zmieniać ich rozmiar bez modyfikacji pierwotnej geometrii.

## Dlaczego używać przykładu translacji grafiki?

- **Upraszcza pozycjonowanie** – przenoszenie obiektów bez przeliczania każdego punktu.  
- **Utrzymuje kod czystym** – jedno wywołanie transformacji zastępuje wiele ręcznych korekt współrzędnych.  
- **Zwiększa wydajność** – silnik graficzny obsługuje obliczenia wewnętrznie.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz:

- **Bibliotekę Aspose.Drawing** zintegrowaną z projektem .NET (pobierz z oficjalnej [strony wydania Aspose.Drawing](https://releases.aspose.com/drawing/net/)).  
- **Katalog dokumentów**, w którym zostanie zapisana wygenerowana grafika.  
- Podstawową znajomość składni **C#** oraz Visual Studio lub wybranego IDE.  

Teraz zanurzmy się w kod!

## Importowanie przestrzeni nazw

Najpierw wprowadź wymagane przestrzenie nazw:

```csharp
using System.Drawing;
using Aspose.Drawing;
```

## Przewodnik krok po kroku

### Krok 1: Utwórz bitmapę

Zaczynamy od utworzenia pustego płótna, które będzie zawierało nasz rysunek.

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

- **Dlaczego 32bppPArgb?** Ten format pikseli obsługuje przezroczystość alfa i renderowanie kolorów wysokiej jakości, idealny do wyjścia PNG.  
- **Wskazówka:** Dostosuj szerokość/wysokość, aby pasowały do docelowego rozmiaru obrazu.

### Krok 2: Ustaw transformację świata (przykład translacji grafiki)

Tutaj przesuwamy początek układu współrzędnych do środka bitmapy, tak aby polecenia rysowania były względem tego punktu.

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

- To przesuwa punkt (0,0) do (500, 400) – środka płótna o wymiarach 1000 × 800.  
- Możesz łączyć dodatkowe transformacje (np. `RotateTransform`, `ScaleTransform`) w celu **wielu transformacji grafiki**.

### Krok 3: Narysuj prostokąt używając przetransformowanych współrzędnych

Teraz każdy kształt, który narysujemy, będzie pozycjonowany względem nowego początku układu.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

- Górny lewy róg prostokąta zaczyna się w przetransformowanym początku (środek obrazu).  
- Śmiało eksperymentuj z innymi kształtami — elipsami, liniami lub własnymi ścieżkami.

### Krok 4: Zapisz wynik – konwertuj grafikę do PNG

Na koniec zapisz bitmapę jako plik PNG.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

- PNG zachowuje dokładne kolory i przezroczystość ustawioną wcześniej.  
- Zastąp `"Your Document Directory"` rzeczywistą ścieżką na swoim komputerze.

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|-------|----------------|-----|
| **Błąd: plik nie znaleziony** przy zapisywaniu | Folder docelowy nie istnieje. | Utwórz folder programowo (`Directory.CreateDirectory`) przed wywołaniem `Save`. |
| **Pusty obraz** po transformacji | `TranslateTransform` wywołano po rysowaniu. | Upewnij się, że transformacja jest ustawiona **przed** jakimikolwiek poleceniami rysowania. |
| **Zniekształcone kolory** | Użycie niekompatybilnego formatu pikseli. | Trzymaj się `Format32bppPArgb` przy wyjściu PNG. |

## Najczęściej zadawane pytania

**P: Czy mogę zastosować więcej niż jedną transformację?**  
O: Tak – możesz łączyć `TranslateTransform`, `RotateTransform` i `ScaleTransform`, aby uzyskać złożone efekty.

**P: Czy Aspose.Drawing jest darmowy dla projektów komercyjnych?**  
O: Dostępna jest darmowa wersja próbna do oceny, ale licencja komercyjna jest wymagana w produkcji.

**P: Czy to działa z .NET Core i .NET 5/6/7?**  
O: Absolutnie. Aspose.Drawing obsługuje wszystkie nowoczesne środowiska .NET.

**P: Gdzie mogę znaleźć pełną referencję API?**  
O: Pełna dokumentacja jest dostępna [tutaj](https://reference.aspose.com/drawing/net/).

**P: Jak rozwiązać problem brakującego pliku wyjściowego?**  
O: Sprawdź ciąg ścieżki, upewnij się, że masz uprawnienia do zapisu i potwierdź, że katalog istnieje przed wywołaniem `Save`.

## Podsumowanie

Teraz wiesz, jak **utworzyć bitmapę z Aspose.Drawing**, zastosować **transformację świata** i **konwertować grafikę do PNG**. Opanowując te podstawy, możesz tworzyć bardziej zaawansowane grafiki, generować dynamiczne obrazy i integrować wyrafinowane efekty wizualne w dowolnej aplikacji .NET.

---

**Ostatnia aktualizacja:** 2025-11-29  
**Testowano z:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  
**Powiązane zasoby:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}