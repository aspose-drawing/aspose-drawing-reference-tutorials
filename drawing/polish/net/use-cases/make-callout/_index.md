---
date: 2026-03-02
description: Ulepsz ilustracje w swoich dokumentach, korzystając z Aspose.Drawing
  dla .NET! Dowiedz się krok po kroku, jak dodać dymki, aby uzyskać jaśniejsze i bardziej
  informacyjne wizualizacje.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak dodać dymki za pomocą Aspose.Drawing dla .NET
url: /pl/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie dymków w Aspose.Drawing

## Wprowadzenie
Jeśli zastanawiasz się **jak dodać dymki** do swoich obrazów lub diagramów przy użyciu Aspose.Drawing dla .NET, trafiłeś we właściwe miejsce. W tym samouczku przeprowadzimy Cię przez cały proces — od wczytania obrazu po narysowanie pięknie stylizowanych dymków — aby Twoje ilustracje były jaśniejsze i bardziej informacyjne.

## Szybkie odpowiedzi
- **Jakiej biblioteki potrzebuję?** Aspose.Drawing dla .NET (do pobrania z oficjalnej strony).  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Czy potrzebna jest licencja?** Bezpłatna wersja próbna działa w trakcie rozwoju; licencja komercyjna jest wymagana w produkcji.  
- **Jak długo trwa implementacja?** Zazwyczaj mniej niż 10 minut dla podstawowego dymka.  
- **Czy mogę dostosować kolory i czcionki?** Tak — wszystko jest sterowane przez standardowe obiekty GDI+ (Pen, Font, Brush).

## Jak dodać dymki w Aspose.Drawing
Poniżej znajduje się zwięzły przewodnik krok po kroku, który dokładnie pokazuje **jak dodać dymki** do obrazu. Śmiało kopiuj kod, eksperymentuj z pozycjami i dostosuj stylizację, aby pasowała do Twojej marki.

## Wymagania wstępne
- Podstawowa znajomość języka programowania C#.  
- Zainstalowana biblioteka Aspose.Drawing. Możesz ją pobrać [tutaj](https://releases.aspose.com/drawing/net/).  
- Dokument lub obraz, do którego chcesz dodać dymki.

## Importowanie przestrzeni nazw
Upewnij się, że w projekcie uwzględniono niezbędne przestrzenie nazw:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Krok 1: Wczytaj obraz
Rozpocznij od wczytania obrazu, do którego chcesz dodać dymki. Zastąp `"Your Document Directory"` i `"gears.png"` rzeczywistą ścieżką katalogu i nazwą pliku obrazu.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Krok 2: Utwórz obiekt Graphics
Utwórz obiekt `Graphics` z obrazu, aby wykonywać operacje rysowania.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Krok 3: Zdefiniuj pozycje dymków
Zdefiniuj punkty początkowe i końcowe dla każdego dymka wraz z wartością i jednostką dymka.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## Krok 4: Narysuj dymki
Zaimplementuj metodę `DrawCallOut`, aby narysować dymki na obrazie.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Krok 5: Zapisz obraz
Zapisz obraz z dymkami w wybranym katalogu.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Kod źródłowy rysowania dymka
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## Typowe problemy i wskazówki
- **Nieprawidłowe współrzędne kotwicy** — upewnij się, że punkty początkowy i końcowy znajdują się w granicach obrazu; w przeciwnym razie dymek może zostać przycięty.  
- **Nakładanie się tekstu** — dostosuj `spaceSize` lub rozmiar czcionki, jeśli etykieta koliduje z innymi elementami graficznymi.  
- **Wydajność** — przy bardzo dużych obrazach rozważ zwolnienie obiektów `Pen`, `Font` i `Brush` po użyciu, aby zwolnić zasoby.

## Zakończenie
Gratulacje! Teraz wiesz **jak dodać dymki** do obrazu przy użyciu Aspose.Drawing dla .NET. Śmiało eksperymentuj z różnymi pozycjami, kolorami i czcionkami, aby dopasować je do swojego stylu wizualnego.

## FAQ

### Czy mogę używać Aspose.Drawing do innych typów ilustracji?
Tak, Aspose.Drawing obsługuje szeroki zakres operacji rysunkowych dla różnych typów ilustracji.

### Czy Aspose.Drawing jest kompatybilny z różnymi formatami obrazów?
Zdecydowanie! Aspose.Drawing obsługuje popularne formaty obrazów, takie jak PNG, JPEG, GIF i inne.

### Gdzie mogę znaleźć więcej przykładów i dokumentacji?
Zapoznaj się ze szczegółową dokumentacją [tutaj](https://reference.aspose.com/drawing/net/).

### Jak uzyskać wsparcie, jeśli napotkam problemy?
Odwiedź [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44), aby uzyskać wsparcie społeczności.

### Czy mogę wypróbować Aspose.Drawing przed zakupem?
Oczywiście! Rozpocznij darmowy okres próbny [tutaj](https://releases.aspose.com/).

**Dodatkowe Pytania i Odpowiedzi**

**Q: Czy mogę zmienić styl linii dymka (przerywana, kropkowana)?**  
A: Tak — po prostu skonfiguruj właściwość `Pen.DashStyle` przed narysowaniem linii.

**Q: Czy można dodać kolor tła do etykiety dymka?**  
A: Zdecydowanie. Utwórz `SolidBrush` z wybranym kolorem i wypełnij prostokąt za tekstem przed wywołaniem `DrawString`.

**Q: Jak zapewnić, że dymek wygląda tak samo na wyświetlaczach o wysokiej rozdzielczości DPI?**  
A: Ustaw `graphics.PageUnit = GraphicsUnit.Pixel` (jak pokazano) i używaj pomiarów wektorowych, aby zachować spójne skalowanie.

---

**Ostatnia aktualizacja:** 2026-03-02  
**Testowano z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}