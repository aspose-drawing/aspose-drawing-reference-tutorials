---
date: 2026-02-17
description: Dowiedz się, jak rysować prostokąt w .NET przy użyciu Aspose.Drawing.
  Ten przewodnik krok po kroku pokazuje, jak utworzyć obraz bitmapowy, narysować prostokąt
  na bitmapie i zapisać narysowany obraz.
linktitle: Drawing Rectangles in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak narysować prostokąt za pomocą Aspose.Drawing dla .NET
url: /pl/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować prostokąt przy użyciu Aspose.Drawing dla .NET

## Wprowadzenie

W tym samouczku dowiesz się **jak narysować prostokąt** w swoich aplikacjach .NET przy użyciu biblioteki Aspose.Drawing. Niezależnie od tego, czy potrzebujesz wygenerować prosty prostokąt jako element UI, czy stworzyć złożoną grafikę do raportu, poniższe kroki poprowadzą Cię przez tworzenie obrazu bitmapowego, konfigurację obiektu graficznego, rysowanie prostokąta na bitmapie oraz zapisanie narysowanego obrazu na dysku.

## Szybkie odpowiedzi
- **Jakiej biblioteki wymaga?** Aspose.Drawing for .NET  
- **Która metoda rysuje kształt?** `Graphics.DrawRectangle`  
- **Czy potrzebna jest licencja?** Wersja próbna jest darmowa; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę zmienić rozmiar prostokąta?** Tak – dostosuj parametry szerokości, wysokości i pozycji.  
- **Czy kod jest kompatybilny z .NET 6+?** Absolutnie, Aspose.Drawing obsługuje nowoczesne wersje .NET.

## Co oznacza „jak narysować prostokąt” w kontekście Aspose.Drawing?

Rysowanie prostokąta przy użyciu Aspose.Drawing oznacza użycie klasy `Graphics` do renderowania prostokątnego obrysu (lub wypełnionego kształtu) na płótnie bitmapy. Takie podejście daje pełną kontrolę nad rozmiarem, kolorem, grubością linii i formatem obrazu, co czyni je idealnym do generowania grafik w locie.

## Dlaczego warto używać Aspose.Drawing do tworzenia prostokątów?
- **Wsparcie wieloplatformowe** – działa na Windows, Linux i macOS.  
- **Brak zależności od GDI+** – unika ograniczeń `System.Drawing.Common`.  
- **Bogaty zestaw funkcji** – zaawansowane rysowanie, antyaliasing i wysokiej jakości formaty wyjściowe.  
- **Łatwa licencjonowanie** – dostępna wersja próbna, z płynnym przejściem na licencję komercyjną.

## Wymagania wstępne

Zanim przejdziemy do kodu, upewnij się, że masz następujące elementy:

- Biblioteka Aspose.Drawing: Upewnij się, że masz zainstalowaną bibliotekę Aspose.Drawing dla .NET. Możesz ją pobrać [tutaj](https://releases.aspose.com/drawing/net/).
- Środowisko programistyczne: Miej skonfigurowane działające środowisko .NET, takie jak Visual Studio, na swoim komputerze.
- Podstawowa znajomość .NET: Zapoznaj się z podstawami programowania w .NET.

## Importowanie przestrzeni nazw

Zacznij od zaimportowania niezbędnych przestrzeni nazw do swojego projektu. Te przestrzenie nazw są niezbędne do pracy z grafiką i operacjami rysowania:

```csharp
using System.Drawing;
```

## Krok 1: Utwórz obraz bitmapowy

Najpierw utwórz obiekt `Bitmap`, który będzie służył jako powierzchnia rysowania. Ta bitmapa jest miejscem, w którym **wygenerujemy zawartość obrazu prostokąta**.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Krok 2: Utwórz obiekt Graphics

Następnie uzyskaj obiekt `Graphics` z bitmapy. Obiekt graficzny jest silnikiem, który pozwala na **tworzenie operacji obiektu graficznego** takich jak rysowanie kształtów, linii i tekstu.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Krok 3: Zdefiniuj pióro (Pen) dla prostokąta

Zdefiniuj obiekt `Pen`, aby określić kolor i grubość obrysu prostokąta.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## Krok 4: Narysuj prostokąt na bitmapie

Teraz użyj obiektu `Graphics`, aby **narysować prostokąt na bitmapie**. Dostosuj wartości X, Y, szerokości i wysokości do swojego projektu.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## Krok 5: Zapisz narysowany obraz

Na koniec zapisz bitmapę do pliku, aby móc zobaczyć rezultat. Ten krok demonstruje możliwość **zapisania narysowanego obrazu**.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

Gratulacje! Pomyślnie ukończyłeś **jak narysować prostokąt** przy użyciu Aspose.Drawing dla .NET.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|----------|
| Pusty obraz wyjściowy | Bitmapa nie została zwolniona lub grafika nie została wypłukana | Wywołaj `graphics.Dispose();` przed zapisem lub użyj bloku `using`. |
| Krawędzie niskiej jakości | Domyślny tryb wygładzania | Ustaw `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`. |
| Błędy ścieżki pliku | Nieprawidłowy katalog | Upewnij się, że folder docelowy istnieje lub użyj `Path.Combine`, aby zbudować bezpieczną ścieżkę. |

## Najczęściej zadawane pytania

**Q: Czy mogę wypełnić prostokąt jednolitym kolorem?**  
A: Tak, utwórz `SolidBrush` i wywołaj `graphics.FillRectangle(brush, …)` przed lub po narysowaniu obrysu.

**Q: Jak narysować wiele prostokątów?**  
A: Iteruj po kolekcji struktur `Rectangle` i wywołuj `DrawRectangle` dla każdej iteracji.

**Q: Czy istnieje sposób na obrócenie prostokąta?**  
A: Użyj `graphics.RotateTransform(angle)` przed rysowaniem, a następnie zresetuj transformację po.

**Q: Jakie formaty obrazu są obsługiwane przy zapisie?**  
A: PNG, JPEG, BMP, GIF i TIFF są obsługiwane poprzez odpowiedni parametr `ImageFormat`.

**Q: Czy Aspose.Drawing działa na .NET Core?**  
A: Tak, biblioteka jest w pełni kompatybilna z .NET Core, .NET 5, .NET 6 i nowszymi.

## Dodatkowe zasoby

Jeśli napotkasz jakiekolwiek problemy lub masz pytania, śmiało szukaj pomocy na [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44).

### FAQ

#### P1: Czy mogę używać Aspose.Drawing za darmo?

A1: Aspose.Drawing jest biblioteką komercyjną, ale możesz przetestować jej funkcje za pomocą [bezpłatnej wersji próbnej](https://releases.aspose.com/).

#### P2: Gdzie mogę znaleźć szczegółową dokumentację?

A2: Odwołaj się do [dokumentacji](https://reference.aspose.com/drawing/net/) po szczegółowe informacje.

#### P3: Jak mogę uzyskać tymczasową licencję?

A3: Uzyskaj [tymczasową licencję](https://purchase.aspose.com/temporary-license/) do celów testowych.

#### P4: Czy Aspose.Drawing jest odpowiedni do złożonych zadań graficznych?

A4: Absolutnie! Aspose.Drawing zapewnia zaawansowane funkcje obsługi skomplikowanych operacji graficznych.

#### P5: Gdzie mogę kupić Aspose.Drawing?

A5: Odwiedź [tutaj](https://purchase.aspose.com/buy), aby zakupić licencję.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2026-02-17  
**Testowano z:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose