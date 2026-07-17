---
date: 2026-07-17
description: Dowiedz się, jak zapobiegać text overflow poprzez ustawianie text alignment
  w Aspose.Drawing for .NET i dodawać tekst do images. Przewodnik krok po kroku z
  przykładami.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Ustaw text alignment przy użyciu Aspose.Drawing for .NET
og_description: Zapobiegaj text overflow poprzez ustawianie text alignment w Aspose.Drawing
  for .NET. Dowiedz się, jak draw string na image, wyśrodkować text w rectangle oraz
  zastąpić System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Zapobiegaj text overflow – ustaw text alignment przy użyciu Aspose.Drawing
  for .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Zapobiegaj text overflow – ustaw text alignment przy użyciu Aspose.Drawing
  for .NET
url: /pl/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapobieganie przepełnieniu tekstu – Ustawianie wyrównania tekstu w Aspose.Drawing

## Wprowadzenie

Gdy potrzebujesz **zapobiec przepełnieniu tekstu** podczas renderowania grafiki w .NET, Aspose.Drawing zapewnia precyzyjną kontrolę nad rozmieszczeniem tekstu, jego wyrównaniem i zawijaniem. Niezależnie od tego, czy tworzysz generator odznak, dynamiczny raport, czy jakikolwiek wynik oparty na obrazie, opanowanie wyrównania tekstu zapewnia, że tekst pozostaje wewnątrz zamierzonego prostokąta i wygląda profesjonalnie. W tym przewodniku przeprowadzimy Cię przez tworzenie płótna bitmapowego, konfigurowanie `StringFormat`, rysowanie prostokąta z wyśrodkowanym tekstem, obsługę przepełnienia oraz ostateczne zapisanie obrazu.

## Szybkie odpowiedzi
- **Co oznacza „ustawianie wyrównania tekstu”?** Definiuje, jak tekst jest pozycjonowany poziomo i pionowo w obrębie prostokąta rysowania.  
- **Która klasa kontroluje wyrównanie?** `StringFormat` pozwala ustawić `Alignment` i `LineAlignment`.  
- **Czy mogę narysować ciąg znaków i prostokąt razem?** Tak — użyj `Graphics.DrawRectangle`, a następnie `Graphics.DrawString`.  
- **Jak zapobiec przepełnieniu tekstu?** Dostosuj rozmiar prostokąta lub ręcznie podziel tekst na wiele linii.  
- **Czy potrzebna jest licencja do produkcji?** Wymagana jest komercyjna licencja Aspose.Drawing do użytku nie‑ewaluacyjnego.

## Czym jest **ustawianie wyrównania tekstu** w Aspose.Drawing?

`set text alignment` konfiguruje poziome (`StringAlignment`) i pionowe (`LineAlignment`) rozmieszczenie tekstu w `Rectangle` lub obszarze rysowania. Poprzez dostosowanie tych właściwości kontrolujesz, czy tekst jest wyrównany do lewej, wyśrodkowany, wyrównany do prawej, do góry, do środka lub do dołu, co umożliwia precyzyjne układanie w grafice, odznakach i raportach generowanych przy użyciu Aspose.Drawing.

## Dlaczego używać Aspose.Drawing do wyrównania tekstu?

Aspose.Drawing eliminuje ograniczenia GDI+, które utrudniają `System.Drawing.Common`. Obsługuje **5 głównych środowisk .NET** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 i .NET 7 – i może renderować obrazy do **4000 × 4000 px** (≈ 100 MB) bez wyczerpywania pamięci. Anti‑aliasing, skalowanie wysokiego DPI oraz pełna kompatybilność z kontenerami Linux pozwalają generować grafiki o perfekcyjnej jakości pikselowej w dowolnym scenariuszu wdrożeniowym.

## Wymagania wstępne

1. **Biblioteka Aspose.Drawing** – pobierz ją [tutaj](https://releases.aspose.com/drawing/net/).  
2. **Środowisko programistyczne** – Visual Studio 2022 (lub dowolne IDE C#).  
3. **Podstawowa znajomość .NET** – powinieneś być zaznajomiony z projektami C# i pakietami NuGet.

## Importowanie przestrzeni nazw

Na początek wprowadź wymagane przestrzenie nazw do zakresu. Dają one dostęp do grafiki, renderowania tekstu i prymitywów rysowania.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Jak zapobiec przepełnieniu tekstu w Aspose.Drawing?

Bitmap to klasa reprezentująca obraz przechowywany w pamięci, natomiast `RectangleF` definiuje obszar prostokąta zmiennoprzecinkowego do rysowania. Używając `StringFormat` z właściwością `Trimming` ustawioną na `StringTrimming.EllipsisCharacter`, nadmiarowe znaki są automatycznie zastępowane elipsą, zapewniając, że tekst nigdy nie wykracza poza granice prostokąta. Pomiar ciągu znaków najpierw pozwala zdecydować, czy zmniejszyć prostokąt, czy podzielić tekst na wiele linii, gwarantując czysty układ bez wycieków.

Wczytaj swoją bitmapę, zdefiniuj odpowiednio wielki `RectangleF` i użyj `StringFormat` z `Trimming` ustawionym na `StringTrimming.EllipsisCharacter`, aby automatycznie odciąć nadmiarowe znaki. Dla pełnej kontroli zmierz ciąg za pomocą `Graphics.MeasureString` i zmniejsz prostokąt lub podziel tekst na linie przed rysowaniem. Takie podejście zapewnia, że żadne znaki nie wyjdą poza widoczne granice.

## Krok 1: Utwórz obiekty Bitmap i Graphics  

Bitmap reprezentuje obraz w pamięci, natomiast Graphics udostępnia metody rysowania dla tej bitmapy. Utworzenie bitmapy zapewnia płótno, na którym można rysować. Obiekt `Graphics` jest powierzchnią rysowania, a my włączamy wysokiej jakości renderowanie tekstu przy użyciu `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Krok 2: Zdefiniuj **StringFormat** i stylizację  

`StringFormat` określa opcje układu tekstu, takie jak wyrównanie, odstępy między wierszami i przycinanie. Tutaj **ustawiamy wyrównanie tekstu** konfigurować instancję `StringFormat`. Przygotowujemy również pędzle, pióra i czcionkę, które będą użyte przy rysowaniu ciągu znaków.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Krok 3: Utwórz i sformatuj tekst – **jak rysować ciąg znaków** i **rysować prostokąt z tekstem**

`Graphics.DrawString` renderuje tekst na płótnie, a `Graphics.DrawRectangle` rysuje kształt prostokąta. Składamy tekst, definiujemy prostokąt, który go będzie zawierał, a następnie rysujemy zarówno obramowanie prostokąta, jak i sam ciąg znaków.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Jak obsłużyć przepełnienie tekstu

Jeśli podany `text` przekracza granice prostokąta, masz dwie typowe opcje:

1. **Zmień rozmiar prostokąta** – zwiększ `rectangle.Width` lub `rectangle.Height`.  
2. **Podziel tekst** – podziel ciąg na linie, które pasują, a następnie wywołaj `DrawString` dla każdej linii z dostosowanymi współrzędnymi Y.

## Jak narysować ciąg znaków na obrazie przy użyciu Aspose.Drawing?

`Graphics.DrawString` rysuje określony tekst przy użyciu czcionki i opcji formatowania. Utwórz obiekt `Graphics` ze swojej bitmapy, a następnie wywołaj `DrawString` z przygotowanym `StringFormat`. To pojedyncze wywołanie renderuje tekst dokładnie tam, gdzie chcesz, respektując wyrównanie, przycinanie i wszelkie zastosowane macierze przekształceń. Dodanie wskazówki wysokiej jakości renderowania zapewnia, że wynik pozostaje ostry na wyświetlaczach o wysokim DPI.

## Jak wyśrodkować tekst w prostokącie?

`StringAlignment` określa poziome wyrównanie tekstu w prostokącie układu. Ustaw `stringFormat.Alignment = StringAlignment.Center` oraz `stringFormat.LineAlignment = StringAlignment.Center`. To wyśrodkowuje tekst poziomo i pionowo wewnątrz prostokąta, co czyni go idealnym dla odznak, przycisków lub nakładek etykiet. Wyśrodkowane położenie działa konsekwentnie w różnych rozmiarach obrazu i ustawieniach DPI, zapewniając zrównoważony wygląd.

## Jak uzyskać pionowe wyrównanie tekstu?

`LineAlignment` kontroluje pionowe położenie tekstu wewnątrz prostokąta. Użyj `stringFormat.LineAlignment` z wartościami `StringAlignment.Near`, `Center` lub `Far`, aby umieścić tekst odpowiednio u góry, w środku lub na dole prostokąta. Połącz to z `Graphics.TranslateTransform`, jeśli musisz obrócić tekst, zachowując pionowe wyrównanie. Dostosowanie wyrównania wierszy zapewnia, że wieloliniowe bloki są dokładnie tam, gdzie ich oczekujesz, nawet po przekształceniach.

## Krok 4: Zapisz wynik – **dodaj tekst do obrazu**

Na koniec zapisz bitmapę na dysk. Ten krok demonstruje **dodawanie tekstu do obrazu** w jednym wywołaniu.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Typowe problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Tekst jest rozmyty** | Upewnij się, że `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` jest ustawione. |
| **Tekst jest obcięty** | Zwiększ rozmiar prostokąta lub włącz logikę zawijania słów, mierząc rozmiar ciągu (`Graphics.MeasureString`). |
| **Czcionka nie znaleziona** | Sprawdź, czy czcionka jest zainstalowana na maszynie hosta lub osadź prywatną czcionkę używając `PrivateFontCollection`. |
| **Nieoczekiwane kolory** | Sprawdź ponownie kolory pędzla i pióra; pamiętaj, że `Color.FromKnownColor` używa kolorów zdefiniowanych przez system. |

## Najczęściej zadawane pytania

**Q1: Czy Aspose.Drawing jest kompatybilny ze wszystkimi wersjami .NET?**  
A1: Tak, Aspose.Drawing jest zaprojektowany tak, aby być kompatybilnym z szerokim zakresem wersji .NET, zapewniając elastyczność programistom.

**Q2: Czy mogę dalej dostosować styl czcionki?**  
A2: Oczywiście! Dostosuj parametry obiektu `Font`, aby uzyskać żądany rozmiar, styl i rodzinę czcionki.

**Q3: Jak mogę obsłużyć przepełnienie tekstu w określonym prostokącie?**  
A3: Możesz zarządzać przepełnieniem tekstu, dostosowując rozmiar prostokąta lub implementując własną logikę obsługi długiego tekstu.

**Q4: Czy w Aspose.Drawing dostępne są inne opcje formatowania?**  
A4: Tak, Aspose.Drawing oferuje kompleksowy zestaw narzędzi do manipulacji grafiką, w tym różne opcje formatowania tekstu, kształtów i nie tylko.

**Q5: Gdzie mogę znaleźć dodatkowe wsparcie dla Aspose.Drawing?**  
A5: Przeglądaj forum Aspose.Drawing [tutaj](https://forum.aspose.com/c/drawing/44) w celu uzyskania wsparcia społeczności i dyskusji.

**Dodatkowe Q&A**

**Q: Jak narysować ciąg znaków bez otaczającego prostokąta?**  
A: Pomiń wywołanie `DrawRectangle` i przekaż żądaną lokalizację `PointF` do `Graphics.DrawString`.

**Q: Czy mogę obrócić tekst, zachowując wyrównanie?**  
A: Tak — zastosuj transformację `Matrix` na obiekcie `Graphics` przed rysowaniem, a następnie przywróć go po zakończeniu.

**Q: Czy można wyeksportować obraz jako JPEG zamiast PNG?**  
A: Po prostu zmień rozszerzenie pliku w `bitmap.Save` i opcjonalnie określ `ImageFormat.Jpeg`.

---

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Powiązane samouczki

- [Jak rysować tekst przy użyciu Aspose.Drawing dla .NET](/drawing/net/text-and-fonts/draw-text/)
- [Dodawanie tekstu na obrazach w Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [Jak rysować tekst i czcionki przy użyciu Aspose.Drawing dla .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}