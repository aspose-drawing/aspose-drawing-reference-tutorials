---
date: 2025-11-30
description: Dowiedz się, jak zastosować transformację układu współrzędnych, rysować
  bitmapę prostokąta i przekształcać strony przy użyciu Aspose.Drawing dla .NET.
language: pl
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Transformacja układu współrzędnych (transformacja strony) w Aspose.Drawing
  dla .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Transformacja Systemu Współrzędnych (Transformacja Strony) w Aspose.Drawing dla .NET

## Wstęp

Witamy! W tym samouczku dowiesz się **jak wykonać transformację systemu współrzędnych** na stronie przy użyciu Aspose.Drawing dla .NET. Niezależnie od tego, czy musisz **rysować prostokąt bitmapowy**, skalować rysunki, czy po prostu mapować jednostki strony na jednostki urządzenia, poniższe kroki poprowadzą Cię przez cały proces — jasno, zwięźle i gotowe do skopiowania‑wklejenia do Twojego projektu.

## Szybkie odpowiedzi
- **Jaka jest podstawowa klasa do rysowania?** `Graphics` z Aspose.Drawing.
- **Jak ustawić jednostki strony?** Użyj `graphics.PageUnit = GraphicsUnit.Inch;`.
- **Czy mogę narysować prostokąt na przekształconej stronie?** Tak — utwórz `Pen` i wywołaj `DrawRectangle`.
- **Gdzie zapisywany jest wynik?** W folderze, który określisz w `bitmap.Save`.
- **Czy potrzebna jest licencja do produkcji?** Do użytku komercyjnego wymagana jest ważna licencja Aspose.Drawing.

## Co to jest transformacja systemu współrzędnych?

**Transformacja systemu współrzędnych** zmienia sposób, w jaki logiczne współrzędne strony (np. cale lub milimetry) mapowane są na fizyczne współrzędne urządzenia (piksele). Poprzez dostosowanie transformacji kontrolujesz skalowanie, obrót i translację wszystkich operacji rysunkowych, co ułatwia projektowanie grafiki niezależnej od rozdzielczości.

## Dlaczego warto używać Aspose.Drawing do transformacji stron?

- **Pełna kompatybilność z .NET** – działa z .NET Framework, .NET Core oraz .NET 5/6.  
- **Bogate API graficzne** – oferuje tę samą funkcjonalność co System.Drawing.Common bez ograniczeń platformowych.  
- **Proste zarządzanie jednostkami** – przełączaj się między calami, milimetrami, punktami itp. za pomocą jednej właściwości.  
- **Wysokiej jakości wyjście** – generuj PNG, JPEG, BMP i inne formaty z precyzyjną kontrolą.

## Wymagania wstępne

Zanim przejdziemy dalej, upewnij się, że masz:

- **Bibliotekę Aspose.Drawing** – pobierz najnowszą wersję z oficjalnej strony [here](https://releases.aspose.com/drawing/net/).  
- **Środowisko programistyczne** – Visual Studio (dowolna edycja) lub inne IDE .NET.  
- **Uprawnienia zapisu** – folder na Twoim komputerze, w którym zostanie zapisana przekształcona grafika (zastąp `"Your Document Directory"` w kodzie rzeczywistą ścieżką).

Teraz, gdy wszystko jest gotowe, przejdźmy przez poszczególne kroki.

## Importowanie przestrzeni nazw

Najpierw wprowadź wymaganą przestrzeń nazw do zasięgu:

```csharp
using System.Drawing;
```

> *Dlaczego to ważne*: `System.Drawing` zawiera `Bitmap`, `Graphics`, `Pen` oraz struktury kolorów, które będziemy wykorzystywać w całym samouczku.

## Krok 1: Utworzenie bitmapy

Utwórz pustą płaszczyznę, która będzie hostować przekształcone rysowanie. Określamy rozmiar **1000 × 800 pikseli** oraz format pikseli obsługujący przezroczystość alfa.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> Ta bitmapa pełni rolę powierzchni rysunkowej. Wybrany format pikseli (`Format32bppPArgb`) zapewnia wysoką jakość renderowania z premultypowaną alfą.

## Krok 2: Utworzenie obiektu Graphics

Obiekt `Graphics` udostępnia metody rysowania (linie, kształty, tekst). Uzyskujemy go z bitmapy, którą właśnie stworzyliśmy.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> Obiekt `Graphics` jest sercem wszystkich operacji renderowania; respektuje ustawienia transformacji, które zastosujemy w następnym kroku.

## Krok 3: Wyczyść płótno

Zanim narysujesz cokolwiek, wyczyść płótno do neutralnego koloru tła (szary w tym przykładzie). Ten krok demonstruje także, jak wypełnić całą bitmapę jednolitym kolorem.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Krok 4: Ustaw transformację (Zastosuj transformację strony)

Tutaj **zastosowujemy transformację strony** ustawiając `PageUnit` na cale. To mówi silnikowi graficznemu, aby interpretował wszystkie kolejne współrzędne jako cale, a nie piksele.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *Wskazówka*: Zmiana `PageUnit` to prosty sposób na **jak przekształcić współrzędne strony** bez ręcznego obliczania wartości w pikselach.

## Krok 5: Narysuj prostokąt (Draw rectangle bitmap)

Teraz rysujemy prostokąt o wymiarach **1 cal × 1 cal** w pozycji (1, 1) cali. Szerokość `Pen` ustawiona jest na `0.1f` cala, co daje cienką, ale widoczną linię.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> To pokazuje **draw rectangle bitmap** po zastosowaniu transformacji — zauważ, że rozmiar prostokąta jest definiowany w calach, a nie w pikselach.

## Krok 6: Zapisz obraz

Na koniec zapisz przekształconą bitmapę na dysku. Zastąp `"Your Document Directory"` rzeczywistą ścieżką folderu na swoim komputerze.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> Plik wyjściowy (`PageTransformation_out.png`) będzie zawierał prostokąt narysowany przy użyciu wcześniej ustawionej transformacji systemu współrzędnych.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|----------|
| **Obraz jest pusty** | Płótno nie zostało wyczyszczone lub rysowanie odbyło się poza widocznym obszarem. | Sprawdź `graphics.PageUnit` i wartości współrzędnych; upewnij się, że prostokąt mieści się w granicach bitmapy. |
| **Nieprawidłowe skalowanie** | Użyto niewłaściwego `GraphicsUnit`. | Zweryfikuj, czy `graphics.PageUnit` odpowiada jednostce, której chcesz używać (np. `GraphicsUnit.Inch`). |
| **Błędy ścieżki pliku** | Brakujący katalog lub nieprawidłowe znaki. | Utwórz docelowy folder wcześniej lub użyj `Path.Combine`, aby bezpiecznie zbudować ścieżkę. |

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.Drawing za darmo?**  
A: Aspose.Drawing oferuje bezpłatną wersję próbną, którą możesz uzyskać [here](https://releases.aspose.com/).

**Q: Gdzie znajdę szczegółową dokumentację Aspose.Drawing?**  
A: Dokumentacja jest dostępna [here](https://reference.aspose.com/drawing/net/).

**Q: Jak mogę uzyskać wsparcie dla Aspose.Drawing?**  
A: Wsparcie znajdziesz na [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17).

**Q: Czy dostępna jest tymczasowa licencja dla Aspose.Drawing?**  
A: Tak, tymczasową licencję możesz uzyskać [here](https://purchase.aspose.com/temporary-license/).

**Q: Gdzie mogę kupić Aspose.Drawing?**  
A: Zakup Aspose.Drawing możliwy jest [here](https://purchase.aspose.com/buy).

## Zakończenie

Teraz wiesz, jak **zastosować transformację systemu współrzędnych**, **narysować prostokąt bitmapowy** oraz **zapisać wynik** przy użyciu Aspose.Drawing dla .NET. Te elementy budulcowe pozwalają tworzyć grafikę niezależną od rozdzielczości, idealną do raportów, elementów UI lub wszelkich scenariuszy, w których precyzyjne wymiary mają znaczenie. Eksperymentuj z innymi wartościami `GraphicsUnit` (takimi jak `Millimeter` czy `Point`), aby zobaczyć, jak wpływają na Twoje rysunki.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2025-11-30  
**Testowane z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose