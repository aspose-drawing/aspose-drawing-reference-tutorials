---
date: 2026-02-19
description: Dowiedz się, jak rysować ścieżki i łączyć je piórami w Aspose.Drawing,
  a następnie zapisać obraz jako PNG przy użyciu prostego kodu C#.
linktitle: Joining Paths with Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak rysować ścieżkę i łączyć ścieżki przy użyciu piór w Aspose.Drawing
url: /pl/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak rysować ścieżki i łączyć ścieżki piórami w Aspose.Drawing

## Wprowadzenie

Witamy w świecie **Aspose.Drawing for .NET**! W tym samouczku odkryjesz **jak rysować ścieżkę** obiektów, połączysz je różnymi stylami łączenia linii i ostatecznie **zapiszesz obraz jako PNG**. Niezależnie od tego, czy tworzysz narzędzie raportujące, edytor projektów, czy po prostu potrzebujesz wyraźnej grafiki wektorowej, opanowanie rysowania ścieżek piórami daje Ci precyzyjną kontrolę nad wynikiem wizualnym.

## Szybkie odpowiedzi
- **Co oznacza „draw path”?** Tworzy definicje linii lub kształtów opartych na wektorach, które obiekt `Graphics` może renderować.  
- **Jakie łączenia linii są dostępne?** `Bevel`, `Miter`, `Round` i `BevelClipped`.  
- **Czy mogę wyeksportować wynik jako PNG?** Tak — użyj `Bitmap.Save` z rozszerzeniem `.png`.  
- **Czy potrzebna jest licencja?** Wersja próbna działa w celach oceny; licencja komercyjna jest wymagana w produkcji.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.6+, .NET Core 3.1+ i .NET 6+.

## Czym jest „how to draw path” w Aspose.Drawing?

Rysowanie ścieżki oznacza tworzenie obiektu `GraphicsPath`, który zawiera serię linii, krzywych lub kształtów. Po zbudowaniu ścieżki malujesz ją na powierzchni `Graphics` przy użyciu `Pen`. To podejście jest bardziej elastyczne niż rysowanie pojedynczych linii, ponieważ możesz zastosować transformacje, przycinanie i różne style łączenia do całego kształtu.

## Dlaczego warto używać Aspose.Drawing do łączenia ścieżek?

- **Pełna kompatybilność z .NET** – działa na Windows, Linux i macOS.  
- **Bogate opcje łączenia linii** – twórz ścięte, zaokrąglone lub ścięte (miter) rogi za pomocą jednej właściwości.  
- **Wysokiej jakości wyjście rastrowe** – zapisuj bezpośrednio do PNG, JPEG, BMP itp., bez dodatkowych kroków konwersji.  
- **Brak ograniczeń GDI+** – idealne do renderowania po stronie serwera, gdzie `System.Drawing.Common` może być ograniczony.

## Wymagania wstępne

Zanim przejdziemy do kodu, upewnij się, że masz:

1. **Bibliotekę Aspose.Drawing** – pobierz ją **[tutaj](https://releases.aspose.com/drawing/net/)**.  
2. **Środowisko programistyczne .NET** – Visual Studio, VS Code lub dowolne IDE obsługujące C#.

Teraz, gdy wszystko jest gotowe, przejdźmy przez każdy krok.

## Importowanie przestrzeni nazw

Dodaj wymagane przestrzenie nazw na początku pliku, aby kompilator wiedział, gdzie znaleźć klasy graficzne:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Krok 1: Utwórz obiekt Bitmap i Graphics

Zaczynamy od pustego płótna (`Bitmap`) o rozmiarze 1000 × 800 pikseli i uzyskujemy obiekt `Graphics`, który będzie renderował nasze polecenia rysowania.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Krok 2: Zdefiniuj metodę DrawPath

Ta metoda pomocnicza kapsułkuje logikę rysowania:

- **Pen** – ustawia kolor i grubość (30 px).  
- **GraphicsPath** – definiuje dwie połączone linie tworzące kształt „L”.  
- **LineJoin** – kontroluje, jak renderowany jest narożnik pomiędzy dwiema liniami (`Bevel`, `Round` itp.).  

Możesz wywołać tę metodę z dowolną wartością `LineJoin`, aby zobaczyć różnicę wizualną.

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

## Krok 3: Łączenie ścieżek przy użyciu Bevel LineJoin

Użycie `LineJoin.Bevel` tworzy spłaszczony narożnik w miejscu, gdzie dwie linie się spotykają.

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

## Krok 4: Łączenie ścieżek przy użyciu Round LineJoin

`LineJoin.Round` tworzy gładki, zaokrąglony narożnik — idealny dla bardziej wyrafinowanego wyglądu.

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

## Krok 5: Zapisz wynik jako PNG

Wywołanie `Save` zapisuje bitmapę do pliku w formacie PNG. Dostosuj ścieżkę do swojego środowiska.

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Obraz jest pusty** | Obiekt `Graphics` nie został wyczyszczony lub rozmiar bitmapy jest zbyt mały. | Wywołaj `graphics.Clear(Color.White);` przed rysowaniem lub zwiększ wymiary bitmapy. |
| **Róg wygląda ząbkowanie** | Używanie bitmapy o niskiej rozdzielczości z grubym piórem. | Zwiększ DPI bitmapy (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) lub zmniejsz szerokość pióra. |
| **Błąd: plik nie znaleziony** | Nieprawidłowa ścieżka zapisu. | Użyj `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## Najczęściej zadawane pytania

### P1: Czy mogę używać Aspose.Drawing za darmo?

A1: Aspose.Drawing jest produktem komercyjnym, ale możesz zapoznać się z jego możliwościami korzystając z **[bezpłatnej wersji próbnej](https://releases.aspose.com/)**.

### P2: Gdzie mogę znaleźć dokumentację Aspose.Drawing?

A2: Odwołaj się do **[dokumentacji](https://reference.aspose.com/drawing/net/)**, aby uzyskać kompleksowe wskazówki.

### P3: Jak mogę uzyskać wsparcie dla Aspose.Drawing?

A3: Odwiedź **[forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44)**, aby uzyskać pomoc społeczności i oficjalne wsparcie.

### P4: Czy dostępne są tymczasowe licencje dla Aspose.Drawing?

A4: Tak, możesz uzyskać **[tymczasową licencję](https://purchase.aspose.com/temporary-license/)** na krótkotrwałe użycie.

### P5: Gdzie mogę kupić Aspose.Drawing?

A5: Kup Aspose.Drawing **[tutaj](https://purchase.aspose.com/buy)**.

## Podsumowanie

W tym przewodniku omówiliśmy **jak rysować ścieżki** (path) obiekty, zastosowaliśmy różne style `LineJoin` i zapisaliśmy końcową grafikę jako plik PNG przy użyciu Aspose.Drawing dla .NET. Opanowując te kroki, możesz tworzyć zaawansowaną grafikę wektorową, niestandardowe ikony lub dynamiczne wykresy bezpośrednio z kodu po stronie serwera.

---

**Ostatnia aktualizacja:** 2026-02-19  
**Testowano z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}