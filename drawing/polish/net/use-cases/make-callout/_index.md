---
title: Tworzenie objaśnień w Aspose.Drawing
linktitle: Tworzenie objaśnień w Aspose.Drawing
second_title: Aspose.Drawing .NET API - alternatywa dla System.Drawing.Common
description: Ulepsz ilustracje w swoich dokumentach za pomocą Aspose.Drawing dla .NET! Dowiedz się krok po kroku, jak dodawać objaśnienia, aby uzyskać wyraźniejsze i bardziej informacyjne obrazy.
weight: 10
url: /pl/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tworzenie objaśnień w Aspose.Drawing

## Wstęp
Witamy w naszym przewodniku krok po kroku dotyczącym tworzenia objaśnień w Aspose.Drawing dla .NET! Jeśli chcesz ulepszyć ilustracje dokumentów za pomocą objaśnień, jesteś we właściwym miejscu. W tym samouczku podzielimy proces na łatwe do wykonania kroki, korzystając z biblioteki Aspose.Drawing.
## Warunki wstępne
Zanim przejdziesz do samouczka, upewnij się, że spełniasz następujące wymagania wstępne:
- Podstawowa znajomość języka programowania C#.
-  Zainstalowana biblioteka Aspose.Drawing. Możesz go pobrać[Tutaj](https://releases.aspose.com/drawing/net/).
- Dokument lub obraz, do którego chcesz dodać objaśnienia.
## Importuj przestrzenie nazw
Upewnij się, że w projekcie znajdują się niezbędne przestrzenie nazw:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Krok 1: Załaduj obraz
 Zacznij od załadowania obrazu, do którego chcesz dodać objaśnienia. Zastępować`"Your Document Directory"` I`"gears.png"` z rzeczywistym katalogiem i nazwą pliku obrazu.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Twój kod tutaj
}
```
## Krok 2: Utwórz obiekt graficzny
 Stwórz`Graphics` obiekt z obrazu, aby wykonać operacje rysowania.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Krok 3: Zdefiniuj pozycje objaśnień
Zdefiniuj punkty początkowe i końcowe każdego objaśnienia wraz z wartością objaśnienia i jednostką.
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
## Krok 4: Narysuj objaśnienia
 Wdrażaj`DrawCallOut` metoda rysowania objaśnień na obrazie.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Krok 5: Zapisz obraz
Zapisz obraz z objaśnieniami w wybranym katalogu.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Narysuj kod źródłowy objaśnienia
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
## Wniosek

Gratulacje! Pomyślnie dodałeś objaśnienia do swojego obrazu za pomocą Aspose.Drawing dla .NET. Możesz eksperymentować z różnymi pozycjami i wartościami, aby jeszcze bardziej dostosować objaśnienia.

## Często zadawane pytania

### Czy mogę używać Aspose.Drawing do innych typów ilustracji?

Tak, Aspose.Drawing obsługuje szeroki zakres operacji rysowania dla różnych typów ilustracji.

### Czy Aspose.Drawing jest kompatybilny z różnymi formatami obrazów?

Absolutnie! Aspose.Drawing obsługuje popularne formaty obrazów, takie jak PNG, JPEG, GIF i inne.

### Gdzie mogę znaleźć więcej przykładów i dokumentacji?

 Zapoznaj się z obszerną dokumentacją[Tutaj](https://reference.aspose.com/drawing/net/).

### Jak uzyskać pomoc, jeśli napotkam problemy?

 Odwiedzić[Forum Aspose.Drawing](https://forum.aspose.com/c/diagram/17) za wsparcie społeczności.

### Czy mogę wypróbować Aspose.Drawing przed zakupem?

 Z pewnością! Zacznij od bezpłatnego okresu próbnego[Tutaj](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
