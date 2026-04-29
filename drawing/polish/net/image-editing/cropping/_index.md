---
date: 2026-02-07
description: Krok po kroku tutorial przycinania obrazu do formatu PNG przy użyciu
  Aspose.Drawing, alternatywy dla System.Drawing dla programistów .NET. Zawiera przycinanie
  wsadowe i niezbędne techniki.
linktitle: Image Cropping Tutorial – Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Jak przyciąć obraz do PNG przy użyciu Aspose.Drawing dla .NET
url: /pl/net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak przyciąć obraz do PNG przy użyciu Aspose.Drawing dla .NET

Jeśli potrzebujesz szybko i niezawodnie **przyciąć obraz do PNG** w środowisku .NET, jesteś we właściwym miejscu. W tym samouczku przeprowadzimy Cię przez dokładne kroki ładowania obrazu, określenia obszaru przycięcia i zapisania wyniku jako plik PNG — wszystko przy użyciu Aspose.Drawing, nowoczesnej **alternatywy dla System.Drawing**, która działa wieloplatformowo.

## Szybkie odpowiedzi
- **Jakiej biblioteki powinienem używać?** Aspose.Drawing for .NET (pełnoprawna alternatywa dla System.Drawing.Common)  
- **Jak długo trwa podstawowe przycięcie?** Zazwyczaj poniżej sekundy dla pojedynczego obrazu na nowoczesnym procesorze  
- **Czy mogę przyciąć do PNG?** Tak – zapisz przycięty bitmap jako plik PNG (zobacz Krok 6)  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji  
- **Czy przetwarzanie wsadowe jest możliwe?** Absolutnie – otocz te same kroki pętlą, aby przetworzyć wiele plików  

## Co to jest „przycięcie obrazu do PNG”?

Przycięcie obrazu oznacza wyodrębnienie prostokątnego obszaru z oryginalnego bitmapu. Gdy zapiszesz ten obszar jako PNG, zachowujesz przezroczystość i korzystasz z bezstratnej kompresji — idealne do miniatur, ikon lub dowolnych zasobów UI.

## Dlaczego Aspose.Drawing jest alternatywą dla System.Drawing?

- **Wsparcie wieloplatformowe** – działa na Windows, Linux i macOS bez natywnych zależności GDI+.  
- **Bogata obsługa formatów pikseli** – 32‑bit, 24‑bit, indeksowane i inne.  
- **API skoncentrowane na wydajności** – idealne zarówno do edycji pojedynczych obrazów, jak i dużych zadań wsadowych.  

## Wymagania wstępne

Zanim zanurkujemy, upewnij się, że masz:

- **Biblioteka Aspose.Drawing** zintegrowana z Twoim projektem .NET. Możesz ją pobrać [tutaj](https://releases.aspose.com/drawing/net/).  
- Folder zawierający obrazy źródłowe, które chcesz przyciąć. Zastąp `"Your Document Directory"` w fragmentach kodu rzeczywistą ścieżką na swoim komputerze.

## Importowanie przestrzeni nazw

```csharp
using System.Drawing;
```

Przestrzeń nazw `System.Drawing` zapewnia dostęp do `Bitmap`, `Graphics` i powiązanych typów, które rozszerza Aspose.Drawing.

## Przewodnik krok po kroku

### Krok 1: Utwórz płótno Bitmap

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

Zaczynamy od pustego płótna o rozmiarze, który pomieści przycięty wynik. Dostosuj szerokość i wysokość, aby odpowiadały wymiarom obszaru, który zamierzasz wyodrębnić.

### Krok 2: Utwórz obiekt Graphics

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

Obiekt `Graphics` pozwala rysować na płótnie. `InterpolationMode` kontroluje, jak obliczane są wartości pikseli podczas skalowania lub transformacji — `NearestNeighbor` sprawdza się dobrze przy ostrych krawędziach.

### Krok 3: Załaduj obraz do przycięcia

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

Załaduj obraz źródłowy. Upewnij się, że ścieżka wskazuje istniejący plik; w przeciwnym razie zostanie zgłoszony wyjątek.

### Krok 4: Zdefiniuj prostokąty źródłowy i docelowy

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

`sourceRectangle` informuje API, którą część oryginalnego obrazu zachować. Tutaj wybieramy obszar 50 × 40 pikseli w lewym górnym rogu. Przypisując ten sam prostokąt do `destinationRectangle`, zachowujemy przycięty region w jego oryginalnym rozmiarze.

### Krok 5: Wykonaj operację przycięcia

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

`Graphics.DrawImage` kopiuje zdefiniowaną część `image` na nasze puste `bitmap`. To jest podstawowa operacja **przycięcia obrazu do PNG**.

### Krok 6: Zapisz przycięty obraz (przycięcie obrazu do PNG)

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

Na koniec zapisz płótno na dysku jako plik PNG. PNG zachowuje kanał alfa i zapewnia bezstratną jakość — idealne dla zasobów UI.

## Jak przycinać obrazy w scenariuszu wsadowym

Gdy masz dziesiątki lub setki zdjęć, po prostu umieść cały fragment kodu wewnątrz pętli `foreach`, która iteruje po kolekcji ścieżek do plików. Ta sama logika `Graphics.DrawImage` ma zastosowanie, co sprawia, że **wsadowe przycinanie obrazów** jest trywialnym rozszerzeniem tego samouczka.

## Częste pułapki i wskazówki

- **Niezgodności formatu pikseli** – upewnij się, że obraz źródłowy i bitmapa płótna mają kompatybilny format pikseli, aby uniknąć przesunięć kolorów.  
- **Zwalnianie obiektów GDI** – otocz `Bitmap` i `Graphics` instrukcjami `using` lub wywołaj `Dispose()` ręcznie; w przeciwnym razie możesz wyciekać niezarządzane zasoby.  
- **Błędy współrzędnych** – współrzędne prostokąta są zerowe. Wybranie prostokąta wykraczającego poza granice obrazu źródłowego spowoduje wyjątek.  

## Najczęściej zadawane pytania

**Q: Czy mogę przycinać obrazy w dowolnym formacie przy użyciu Aspose.Drawing?**  
A: Tak, Aspose.Drawing obsługuje szeroką gamę formatów (PNG, JPEG, BMP, GIF, TIFF itp.), więc możesz przycinać praktycznie każdy typ obrazu.

**Q: Czy dostępne są zaawansowane opcje przycinania?**  
A: Absolutnie. Możesz łączyć `GraphicsPath`, transformacje `Matrix` lub używać klasy `ImageProcessor` do bardziej złożonych wyborów, takich jak przycinanie kołowe.

**Q: Czy mogę zastosować wiele operacji przycinania do jednego obrazu?**  
A: Tak. Po pierwszym przycięciu możesz ponownie użyć uzyskanego bitmapu jako nowego źródła i powtórzyć proces, aby łańcuchowo wykonać kolejne przycięcia.

**Q: Czy Aspose.Drawing nadaje się do wsadowego przetwarzania obrazów?**  
A: Zdecydowanie. Jego lekka API i brak natywnych zależności czynią go idealnym do przetwarzania dużych kolekcji obrazów na serwerach.

**Q: Jak mogę uzyskać wsparcie w kwestiach związanych z Aspose.Drawing?**  
A: Odwiedź [Forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44), aby uzyskać pomoc i połączyć się ze społecznością.

---

**Ostatnia aktualizacja:** 2026-02-07  
**Testowano z:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}