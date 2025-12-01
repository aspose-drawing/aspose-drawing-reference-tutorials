---
date: 2025-12-01
description: Dowiedz się, jak odczytywać piksele i zapisywać dane pikseli, korzystając
  z bezpośredniego dostępu do danych Aspose.Drawing, aby efektywnie manipulować pikselami
  obrazu w .NET.
language: pl
linktitle: How to Read Pixels with Direct Data Access in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Direct Data Access for Image Pixel Manipulation
title: Jak odczytać piksele przy użyciu bezpośredniego dostępu do danych w Aspose.Drawing
url: /net/image-editing/direct-data-access/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak odczytywać piksele przy użyciu bezpośredniego dostępu do danych w Aspose.Drawing

## Wstęp

W tym samouczku dowiesz się **jak odczytywać piksele** z obrazu i zapisywać dane pikseli z powrotem przy użyciu funkcji **bezpośredniego dostępu do danych** w Aspose.Drawing. Bezpośredni dostęp do danych zapewnia kontrolę niskiego poziomu nad buforami pikseli, co sprawia, że manipulacja pikselami obrazu jest szybka i oszczędna pod względem pamięci — idealna w scenariuszach takich jak własne filtry, analiza obrazu lub masowe przekształcenia pikseli w aplikacjach .NET.

## Szybkie odpowiedzi
- **Jaka jest podstawowa metoda odczytu pikseli?** Użyj `ReadArgb32Pixels` na instancji `Bitmap`.  
- **Który format pikseli najlepiej nadaje się do bezpośredniego dostępu?** `PixelFormat.Format32bppPArgb` zapewnia 32‑bitowe wartości ARGB z wstępnie pomnożonym alfą.  
- **Czy potrzebna jest licencja na Aspose.Drawing?** Dostępna jest darmowa wersja próbna; licencja jest wymagana do użytku produkcyjnego.  
- **Czy mogę uruchomić ten kod na .NET 6+?** Tak, Aspose.Drawing obsługuje .NET 5, .NET 6 i nowsze wersje.  
- **Czy operacja jest bezpieczna wątkowo?** Odczyt/zapis na oddzielnych instancjach bitmap jest bezpieczny; unikaj udostępniania tej samej bitmapy między wątkami bez synchronizacji.

## Czym jest bezpośredni dostęp do danych w Aspose.Drawing?

Bezpośredni dostęp do danych pozwala pracować z leżącym u podstaw buforem pikseli bitmapy bez narzutu metod getter/setter dla pojedynczych pikseli. Czytając cały tablicę ARGB32, możesz przetworzyć tysiące pikseli w jednej operacji, a następnie zapisać zmodyfikowaną tablicę z powrotem jednym wywołaniem.

## Dlaczego warto używać bezpośredniego dostępu do danych przy manipulacji pikselami obrazu?

- **Wydajność:** Masowy odczyt/zapis zmniejsza liczbę wywołań interop i przyspiesza przetwarzanie dużych obrazów.  
- **Elastyczność:** Otrzymujesz surowe wartości całkowite (`0xAARRGGBB`), które możesz modyfikować dowolną logiką .NET.  
- **Prostota:** Jedno wywołanie metody do odczytu i jedno do zapisu — nie potrzebujesz zagnieżdżonych pętli, chyba że stosujesz własne algorytmy.

## Wymagania wstępne

- **Biblioteka Aspose.Drawing:** Pobierz i odwołaj się do najnowszej wersji Aspose.Drawing dla .NET ze strony oficjalnej.  
- **Środowisko programistyczne:** Dowolne IDE .NET (Visual Studio, Rider, VS Code) z zainstalowanym pakietem NuGet Aspose.Drawing.  

Możesz pobrać bibliotekę [tutaj](https://releases.aspose.com/drawing/net/).

## Importowanie przestrzeni nazw

Najpierw wprowadź wymaganą przestrzeń nazw, aby klasy bitmap były dostępne.

```csharp
using System.Drawing;
```

## Przewodnik krok po kroku

### Krok 1: Załaduj obraz źródłowy  

Zaczynamy od załadowania obrazu, który chcesz analizować. Zastąp ścieżkę zastępczą rzeczywistą lokalizacją pliku obrazu.

```csharp
Bitmap sourceBitmap = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

### Krok 2: Utwórz docelową bitmapę  

Utwórz nową bitmapę, której wymiary odpowiadają wymiarom źródła i używa 32‑bitowego formatu pikseli odpowiedniego do bezpośredniego dostępu.

```csharp
Bitmap targetBitmap = new Bitmap(sourceBitmap.Width, sourceBitmap.Height, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Krok 3: Odczytaj dane pikseli  

Odczytaj cały bufor pikseli ARGB32 z bitmapy źródłowej do tablicy całkowitej. To jest krok **jak odczytywać piksele**.

```csharp
int[] pixels = new int[sourceBitmap.Width * sourceBitmap.Height];
sourceBitmap.ReadArgb32Pixels(pixels);
```

### Krok 4: Zapisz dane pikseli  

Po dowolnej opcjonalnej manipulacji (np. zastosowaniu filtra) zapisz tablicę pikseli z powrotem do docelowej bitmapy. To pokazuje **jak efektywnie zapisywać piksele**.

```csharp
targetBitmap.WriteArgb32Pixels(pixels);
```

### Krok 5: Zapisz wynik  

Zachowaj zmodyfikowaną bitmapę na dysku. Dostosuj ścieżkę wyjściową w razie potrzeby.

```csharp
targetBitmap.Save("Your Document Directory" + @"Images\DirectDataAccess_out.png");
```

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **`ArgumentException` on `ReadArgb32Pixels`** | Upewnij się, że bitmapa źródłowa używa 32‑bitowego formatu pikseli; w przeciwnym razie najpierw skonwertuj ją przy użyciu `sourceBitmap.Clone(..., PixelFormat.Format32bppPArgb)`. |
| **Incorrect colors after write** | Sprawdź, czy nie modyfikujesz przypadkowo kanału alfa; zachowaj wartość `0xFF` (nieprzezroczysta), jeśli nie potrzebujesz przezroczystości. |
| **Performance lag on very large images** | Przetwarzaj tablicę pikseli w fragmentach lub użyj `Parallel.For`, aby wykorzystać wiele rdzeni. |

## Najczęściej zadawane pytania

**P:** Czy mogę używać Aspose.Drawing dla .NET z innymi frameworkami .NET?  
**O:** Tak, Aspose.Drawing działa z .NET Framework, .NET Core oraz .NET 5/6+.

**P:** Czy dostępna jest darmowa wersja próbna Aspose.Drawing?  
**O:** Oczywiście — pobierz wersję próbną [tutaj](https://releases.aspose.com/).

**P:** Jak mogę uzyskać wsparcie dla Aspose.Drawing?  
**O:** Odwiedź [forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17), aby uzyskać pomoc społeczności i oficjalne wsparcie.

**P:** Gdzie mogę znaleźć dokumentację Aspose.Drawing?  
**O:** Pełna referencja API jest dostępna na [stronie dokumentacji Aspose.Drawing](https://reference.aspose.com/drawing/net/).

**P:** Jak kupić licencję na Aspose.Drawing?  
**O:** Licencję możesz kupić bezpośrednio w sklepie Aspose [tutaj](https://purchase.aspose.com/buy).

**P:** Czy mogę manipulować danymi pikseli w środowisku wielowątkowym?  
**O:** Tak, pod warunkiem, że każdy wątek pracuje na własnej instancji bitmapy lub synchronizujesz dostęp do współdzielonych zasobów.

## Podsumowanie

Teraz nauczyłeś się **jak odczytywać piksele** z bitmapy, manipulować tablicą ARGB32 oraz **zapisywać dane pikseli** z powrotem przy użyciu bezpośredniego dostępu do danych w Aspose.Drawing. Ta technika otwiera drzwi do wysokowydajnych zadań przetwarzania obrazu, takich jak własne filtry, analiza na poziomie pikseli oraz masowe przekształcenia w Twoich aplikacjach .NET.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-01  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose  

---