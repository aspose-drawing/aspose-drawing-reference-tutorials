---
date: 2026-02-12
description: Dowiedz się, jak rysować łuk w aplikacjach .NET przy użyciu Aspose.Drawing.
  Ten przewodnik krok po kroku pokazuje, jak utworzyć bitmapę w C#, ustawić kolor
  pióra, narysować łuk na bitmapie i zapisać bitmapę w formacie PNG.
linktitle: Drawing Arcs in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak narysować łuk przy użyciu Aspose.Drawing
url: /pl/net/lines-curves-and-shapes/draw-arc/
weight: 11
---

 all shortcodes exactly.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować łuk przy użyciu Aspose.Drawing

## Wprowadzenie

Jeśli potrzebujesz **jak narysować łuk** w projekcie .NET, Aspose.Drawing sprawia, że proces jest prosty i wydajny. W tym samouczku przeprowadzimy Cię przez tworzenie bitmapy w C#, ustawianie koloru pióra, generowanie obrazu łuku oraz ostateczne zapisanie bitmapy jako pliku PNG. Niezależnie od tego, czy tworzysz narzędzie raportujące, własny komponent UI, czy po prostu eksperymentujesz z grafiką, te kroki zapewnią solidne podstawy.

## Szybkie odpowiedzi
- **Jaka biblioteka jest najlepsza do rysowania łuków w .NET?** Aspose.Drawing for .NET  
- **Która metoda tworzy łuk?** `Graphics.DrawArc`  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna działa do testów; licencja jest wymagana w produkcji.  
- **Czy mogę zapisać wynik jako PNG?** Tak, użyj `Bitmap.Save` z rozszerzeniem `.png`.  
- **Jakie wersje .NET są wspierane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Co to jest „jak narysować łuk” w Aspose.Drawing?

Rysowanie łuku oznacza renderowanie zakrzywionego odcinka elipsy lub koła na powierzchni graficznej. Aspose.Drawing udostępnia znaną metodę `Graphics.DrawArc`, pozwalającą zdefiniować prostokąt ograniczający, kąt początkowy i kąt przebycia z precyzją pikselową.

## Dlaczego używać Aspose.Drawing do łuków?

- **Spójność międzyplatformowa** – Działa tak samo na Windows, Linux i macOS.  
- **Brak zależności System.Drawing.Common** – Idealne dla nowoczesnych aplikacji .NET Core/5+.  
- **Bogate API** – Pełna kontrola nad kolorami, szerokością linii i formatami obrazów.  

## Wymagania wstępne

- Visual Studio (dowolna aktualna edycja).  
- Aspose.Drawing for .NET – pobierz go ze [strony internetowej](https://releases.aspose.com/drawing/net/).  
- Podstawowa znajomość C# (zmienne, obiekty i wywołania metod).  

## Importowanie przestrzeni nazw

Aby rozpocząć, wprowadź wymaganą przestrzeń nazw do zasięgu:

```csharp
using System.Drawing;
```

## Przewodnik krok po kroku

### Krok 1: Utwórz obiekt bitmapy C# 

Najpierw tworzymy `Bitmap`, który będzie służył jako płótno do naszego rysunku.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

*Wyjaśnienie*: Rozmiar bitmapy (1000 × 800) zapewnia dużo miejsca, a format pikseli gwarantuje wysokiej jakości mieszanie alfa.

### Krok 2: Skonfiguruj pióro i ustaw kolor pióra

Teraz definiujemy `Pen`, który określa wygląd linii. Tutaj **ustawiamy kolor pióra** na niebieski i wybieramy szerokość 2 piksele.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

Możesz zamienić `KnownColor.Blue` na dowolny inny znany kolor lub własną wartość `Color.FromArgb`.

### Krok 3: Narysuj łuk na bitmapie

Gdy powierzchnia graficzna i pióro są gotowe, możemy **narysować łuk na bitmapie**.

```csharp
graphics.DrawArc(pen, 0, 0, 700, 700, 0, 180);
```

Parametry są:

- `pen` – styl, który zdefiniowaliśmy.  
- `0, 0` – lewy górny róg prostokąta ograniczającego.  
- `700, 700` – szerokość i wysokość prostokąta (tworzy idealne koło).  
- `0` – kąt początkowy w stopniach.  
- `180` – kąt przebycia, tworzący półokrąg.

### Krok 4: Zapisz bitmapę PNG

Na koniec **zapisujemy bitmapę PNG** na dysku. Dostosuj ścieżkę do folderu wyjściowego projektu.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawArc_out.png");
```

Zapisany plik (`DrawArc_out.png`) zawiera wygenerowany obraz łuku, gotowy do użycia w interfejsie, raportach lub dalszym przetwarzaniu.

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|---------|-------------|
| **Łuk jest zniekształcony** | Upewnij się, że wartości szerokości i wysokości są równe, aby uzyskać prawdziwe koło; w przeciwnym razie otrzymasz eliptyczny łuk. |
| **Wyjątek: plik nie znaleziony** | Sprawdź, czy docelowy katalog istnieje lub utwórz go programowo przed wywołaniem `Save`. |
| **Kolory wyglądają inaczej na Linuxie** | Użyj `Color.FromArgb` z explicite określonymi wartościami RGBA, aby zapewnić spójne renderowanie na wszystkich platformach. |

## FAQ

### P1: Czy mogę dostosować kolor łuku?

Odp1: Tak, możesz. Po prostu zmodyfikuj parametr koloru przy tworzeniu obiektu `Pen`.

### P2: Co zrobić, jeśli chcę inny kąt początkowy łuku?

Odp2: Dostosuj parametr kąta początkowego w metodzie `DrawArc` zgodnie z wymaganiami.

### P3: Czy Aspose.Drawing nadaje się do innych elementów graficznych?

Odp3: Zdecydowanie. Aspose.Drawing obsługuje szeroki zakres elementów graficznych, w tym linie, krzywe i kształty.

### P4: Czy mogę zintegrować Aspose.Drawing z innymi bibliotekami .NET?

Odp4: Tak, Aspose.Drawing płynnie integruje się z innymi bibliotekami .NET, zapewniając elastyczność w rozwoju.

### P5: Gdzie mogę znaleźć dodatkowe wsparcie lub dyskusje społecznościowe?

Odp5: Odwiedź [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) aby uzyskać wsparcie społeczności i dyskusje.

## Często zadawane pytania

**P: Czy to działa z .NET 6 i nowszymi?**  
O: Tak, Aspose.Drawing w pełni wspiera środowiska .NET 6, .NET 7 i .NET 8.

**P: Jak duża może być bitmapa?**  
O: Rozmiar jest ograniczony jedynie dostępną pamięcią; dla bardzo dużych obrazów rozważ techniki strumieniowania lub kafelkowania.

**P: Czy mogę narysować wiele łuków na tej samej bitmapie?**  
O: Oczywiście — po prostu wywołaj `graphics.DrawArc` wielokrotnie z różnymi współrzędnymi lub kątami.

**P: Czy anti‑aliasing jest stosowany automatycznie?**  
O: Możesz go włączyć, ustawiając `graphics.SmoothingMode = SmoothingMode.AntiAlias;` przed rysowaniem.

**P: Jak zwolnić zasoby po zapisaniu?**  
O: Wywołaj `graphics.Dispose();` i `bitmap.Dispose();` po zakończeniu, aby zwolnić zasoby natywne.

## Podsumowanie

Teraz wiesz **jak narysować łuk** przy użyciu Aspose.Drawing, od tworzenia obiektu bitmapy C# po ustawienie koloru pióra, wygenerowanie obrazu łuku i zapisanie wyniku jako PNG. Eksperymentuj z różnymi kątami, kolorami i szerokościami linii, aby tworzyć własne grafiki wzbogacające Twoje aplikacje.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}