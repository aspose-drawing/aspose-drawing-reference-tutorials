---
title: Dodawanie tekstu do obrazów w Aspose.Drawing
linktitle: Dodawanie tekstu do obrazów w Aspose.Drawing
second_title: Aspose.Drawing .NET API - alternatywa dla System.Drawing.Common
description: Odkryj płynną integrację tekstu z obrazami dzięki Aspose.Drawing dla .NET. Postępuj zgodnie z naszym przewodnikiem krok po kroku, aby łatwo manipulować obrazami. Pobierz teraz!
weight: 12
url: /pl/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dodawanie tekstu do obrazów w Aspose.Drawing

## Wstęp
dynamicznym świecie rozwoju .NET Aspose.Drawing wyróżnia się jako potężne narzędzie do łatwego manipulowania obrazami. Dodawanie tekstu do obrazów jest powszechnym wymogiem, niezależnie od tego, czy chodzi o znak wodny, adnotacje, czy tworzenie spersonalizowanej grafiki. W tym samouczku omówimy, jak wykorzystać Aspose.Drawing do płynnej integracji tekstu z obrazami za pomocą języka C#.
## Warunki wstępne
Zanim zagłębisz się w samouczek, upewnij się, że masz następujące elementy:
1.  Biblioteka Aspose.Drawing: Pobierz i zainstaluj bibliotekę Aspose.Drawing z[Aspose.Drawing dla dokumentacji .NET](https://reference.aspose.com/drawing/net/).
2. Środowisko programistyczne: Posiadaj działające środowisko programistyczne .NET, w tym Visual Studio lub dowolne inne kompatybilne IDE.
Zacznijmy teraz od przewodnika krok po kroku.
## Importuj przestrzenie nazw
Rozpocznij od zaimportowania niezbędnych przestrzeni nazw do projektu C#:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## Krok 1: Załaduj obraz
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Tutaj ładujemy obraz z określonej ścieżki pliku i inicjujemy obiekt graficzny do dalszego przetwarzania.
## Krok 2: Ustaw właściwości tekstu
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Zdefiniuj właściwości tekstu, takie jak kolor, czcionka i wypełnienie. Dostosuj te parametry zgodnie ze swoimi preferencjami.
## Krok 3: Zmierz rozmiar tekstu
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Oblicz wymagany rozmiar tekstu, mierząc każde słowo indywidualnie. Zapewnia to właściwe rozmieszczenie i pozwala uniknąć nakładania się tekstu.
## Krok 4: Narysuj tekst na obrazie
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Teraz umieść tekst na obrazie w oparciu o obliczony rozmiar i narysuj go, używając określonej czcionki i koloru.
## Krok 5: Zapisz obraz
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Zapisz zmodyfikowany obraz w wybranym katalogu.
Ten przewodnik krok po kroku demonstruje prosty proces dodawania tekstu do obrazów przy użyciu Aspose.Drawing dla .NET. Eksperymentuj z różnymi czcionkami, kolorami i zawartością tekstu, aby osiągnąć pożądany efekt wizualny.
## Wniosek
Aspose.Drawing upraszcza zadania manipulacji obrazami w .NET, zapewniając programistom solidny zestaw narzędzi. Dodawanie tekstu do obrazów to tylko jeden z przykładów jego możliwości, ukazujący wszechstronność biblioteki w obsłudze elementów graficznych.
## Często Zadawane Pytania
### Czy Aspose.Drawing jest kompatybilny ze wszystkimi formatami obrazów?
 Aspose.Drawing obsługuje szeroką gamę formatów obrazów, w tym popularne, takie jak JPEG, PNG i GIF. Patrz[dokumentacja](https://reference.aspose.com/drawing/net/) aby uzyskać pełną listę.
### Czy mogę używać Aspose.Drawing do projektów komercyjnych?
Tak, Aspose.Drawing nadaje się zarówno do projektów osobistych, jak i komercyjnych. Aby uzyskać szczegółowe informacje na temat licencji, odwiedź stronę[strona zakupu](https://purchase.aspose.com/buy).
### Czy dostępne są licencje tymczasowe do celów testowych?
 Tak, możesz uzyskać tymczasową licencję na testowanie odwiedzając[Licencja tymczasowa](https://purchase.aspose.com/temporary-license/).
### Gdzie mogę znaleźć wsparcie społeczności dla Aspose.Drawing?
 Nawiąż kontakt ze społecznością i uzyskaj wsparcie na stronie[Forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44).
### Jak rozpocząć pracę z Aspose.Drawing?
 Rozpocznij od pobrania biblioteki z[Tutaj](https://releases.aspose.com/drawing/net/) i odkrywaj kompleksowo[dokumentacja](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
