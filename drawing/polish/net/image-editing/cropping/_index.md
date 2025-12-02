---
date: 2025-12-02
description: Dowiedz się, jak przycinać obrazy w .NET za pomocą Aspose.Drawing. Ten
  samouczek przycinania obrazów pokazuje krok po kroku, jak zapisać przycięty obraz,
  pracować z bitmapą i obsługiwać przycinanie obrazów w partiach.
language: pl
linktitle: How to Crop Image .NET Using Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak przyciąć obraz w .NET przy użyciu Aspose.Drawing
url: /net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak przycinać obrazy w .NET przy użyciu Aspose.Drawing

## Wstęp

Jeśli tworzysz aplikację .NET, która wymaga precyzyjnej manipulacji obrazami, nauka **jak przycinać obrazy** jest niezbędna. Aspose.Drawing udostępnia bogate, w pełni zarządzane API, które pozwala **przycinać obrazy w .NET** bez polegania na starszej bibliotece System.Drawing.Common. W tym samouczku zobaczysz kompletny, od‑a‑do‑końca przykład, który prowadzi Cię przez ładowanie bitmapy, definiowanie obszaru przycięcia, wykonanie operacji i w końcu **zapisanie przyciętego obrazu**. Po zakończeniu będziesz gotowy, aby zintegrować przycinanie obrazów z dowolnym rozwiązaniem .NET — niezależnie od tego, czy jest to pojedyncze zdjęcie, czy **przetwarzanie wsadowe przycinania obrazów**.

## Szybkie odpowiedzi
- **Jakiej biblioteki powinienem używać?** Aspose.Drawing dla .NET  
- **Czy mogę przycinać dowolny format obrazu?** Tak — obsługiwane są najpopularniejsze formaty (PNG, JPEG, BMP itp.).  
- **Czy potrzebna jest licencja?** Bezpłatna wersja próbna wystarcza do rozwoju; licencja jest wymagana w produkcji.  
- **Czy możliwe jest przetwarzanie wsadowe?** Oczywiście — można pętlić ten sam kod dla kolekcji plików.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Co to jest „crop image .net”?

Przycinanie obrazu oznacza wyodrębnienie prostokątnego fragmentu z większego zdjęcia. W .NET operacja ta jest zazwyczaj wykonywana na obiekcie `Bitmap`. Aspose.Drawing upraszcza proces, udostępniając wysokowydajne prymitywy graficzne działające spójnie na wszystkich platformach.

## Dlaczego warto używać Aspose.Drawing do przycinania obrazów?

- **Niezawodność wieloplatformowa** – Brak natywnych zależności, działa na Windows, Linux i macOS.  
- **Bogate wsparcie formatów pikseli** – Obsługuje 32‑bitowy ARGB, PArgb i wiele innych formatów.  
- **Wydajność** – Zoptymalizowane rysowanie i interpolacja dla dużych obrazów.  
- **Bezproblemowa integracja** – Działa ramię w ramię z innymi produktami Aspose, takimi jak PDF, Slides itp.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

- **Bibliotekę Aspose.Drawing** – Dodaj pakiet NuGet `Aspose.Drawing` do projektu lub pobierz go z [oficjalnej strony](https://releases.aspose.com/drawing/net/).  
- **Folder z obrazami** – Katalog zawierający obrazy źródłowe, które chcesz przyciąć. Zastąp w fragmentach kodu `"Your Document Directory"` rzeczywistą ścieżką na swoim komputerze.

## Importowanie przestrzeni nazw

Najpierw zaimportuj przestrzeń nazw zawierającą klasy rysunkowe:

```csharp
using System.Drawing;
```

Daje to dostęp do `Bitmap`, `Graphics`, `Rectangle` i innych niezbędnych typów.

## Przewodnik krok po kroku

### Krok 1: Utwórz płótno Bitmap (crop image bitmap)

Zaczynamy od utworzenia pustej bitmapy, która będzie przechowywać przycięty wynik. Dostosuj szerokość, wysokość i format pikseli, aby odpowiadały rozmiarowi wybranego obszaru.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Wskazówka:** Format `Format32bppPArgb` zachowuje przezroczystość alfa i zapewnia wysoką jakość renderowania.

### Krok 2: Utwórz obiekt Graphics

Obiekt `Graphics` pozwala rysować na płótnie bitmapy. Ustawienie `InterpolationMode` wpływa na sposób przeskalowywania obrazu podczas przycinania.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

> **Pro tip:** Dla płynniejszych wyników przy skalowanych obrazach rozważ `InterpolationMode.HighQualityBicubic`.

### Krok 3: Załaduj obraz źródłowy

Wczytaj obraz, który chcesz przyciąć. Ścieżka łączy katalog dokumentu z nazwą pliku.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

> **Uwaga:** Aspose.Drawing potrafi odczytywać PNG, JPEG, BMP, GIF, TIFF i wiele innych formatów bezpośrednio.

### Krok 4: Zdefiniuj prostokąty źródłowy i docelowy

`sourceRectangle` wybiera część oryginalnego obrazu, którą chcesz zachować. Tutaj wybieramy lewy górny obszar 50 × 40 pikseli. `destinationRectangle` określa, gdzie silnik graficzny umieści przycięty fragment na nowej bitmapie.

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

> **Dlaczego oba prostokąty?** Użycie identycznych prostokątów wykonuje prosty przycinanie. Możesz zmienić `destinationRectangle`, aby przemieścić lub przeskalować przycięty fragment.

### Krok 5: Wykonaj operację przycięcia

Metoda `DrawImage` kopiuje wybrany region ze źródłowego obrazu do docelowej bitmapy.

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

> **Typowy błąd:** Zapomnienie o zwolnieniu `Graphics` może zablokować plik bitmapy. Zajmiemy się zwolnieniem automatycznie po zakończeniu metody.

### Krok 6: Zapisz przycięty obraz (save cropped image)

Na koniec zapisz wynik na dysku. Zmien nazwę pliku i ścieżkę według potrzeb.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

> **Rezultat:** Masz teraz nowy plik PNG zawierający wyłącznie wybrany obszar 50 × 40 pikseli.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **Pusty plik wyjściowy** | Prostokąt źródłowy poza granicami obrazu | Sprawdź współrzędne i rozmiar `sourceRectangle`. |
| **Wyjątek Out‑of‑memory** | Bardzo duże obrazy źródłowe | Przetwarzaj obrazy w partiach lub używaj instrukcji `using`, aby szybko zwalniać zasoby. |
| **Nieprawidłowe kolory** | Niepasujący format pikseli | Dopasuj format pikseli bitmapy źródłowej lub skonwertuj przy użyciu `Bitmap.Clone`. |

## Najczęściej zadawane pytania

**P: Czy mogę przycinać obrazy w dowolnym formacie przy użyciu Aspose.Drawing?**  
O: Tak, Aspose.Drawing obsługuje PNG, JPEG, BMP, GIF, TIFF i wiele innych formatów, więc możesz **jak przycinać obrazy** niezależnie od ich pierwotnego typu.

**P: Czy dostępne są zaawansowane opcje przycinania?**  
O: Oczywiście. Możesz połączyć `GraphicsPath` dla przycinania nieregularnego, zastosować rotację lub użyć `ImageAttributes` do korekcji kolorów.

**P: Czy mogę wykonać wiele operacji przycinania na jednym obrazie?**  
O: Tak — po prostu powtórz wywołanie `DrawImage` z różnymi prostokątami źródłowymi lub łańcuchuj je w pętli dla skomplikowanych transformacji.

**P: Czy Aspose.Drawing nadaje się do wsadowego przycinania obrazów?**  
O: Zdecydowanie. Umieść powyższe kroki w pętli `foreach` przetwarzającej kolekcję ścieżek plików, aby automatycznie obsłużyć dziesiątki lub setki obrazów.

**P: Jak mogę uzyskać wsparcie w sprawach związanych z Aspose.Drawing?**  
O: Odwiedź [forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17), aby zadawać pytania, udostępniać kod i uzyskać pomoc od społeczności oraz inżynierów produktu.

## Podsumowanie

W tym samouczku przedstawiliśmy kompletny **workflow przycinania obrazu w .NET** przy użyciu Aspose.Drawing. Teraz wiesz, jak **jak przycinać obrazy**, definiować precyzyjne prostokąty źródłowe i **zapisywać przycięte obrazy**. Dzięki tej wiedzy możesz rozszerzyć kod o **wsadowe przycinanie obrazów**, stosować własne transformacje lub integrować logikę z większymi pipeline'ami przetwarzania obrazów.

---  

**Ostatnia aktualizacja:** 2025-12-02  
**Testowane z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}