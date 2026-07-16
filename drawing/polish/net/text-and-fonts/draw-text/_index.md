---
date: 2026-02-25
description: Dowiedz się, jak rysować tekst i tworzyć dynamiczne obrazy tekstowe przy
  użyciu Aspose.Drawing dla .NET. Ten przewodnik krok po kroku pokazuje, jak dodać
  tekst do bitmapy, narysować ciąg znaków na obrazie i zapisać bitmapę jako PNG.
linktitle: How to Draw Text with Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak rysować tekst przy użyciu Aspose.Drawing dla .NET
url: /pl/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak rysować tekst przy użyciu Aspose.Drawing dla .NET

## Wstęp

W tym przewodniku krok po kroku nauczyćsz się **jak rysować tekst** na obrazach przy użyciu Aspose.Drawing dla .NET. Oprogramowanie od tego, czy pochodzi z *dynamiczny obraz tekstowy*, przesłany tekst do bitmapy, czy wygenerowany grafikę z znanych czcionkami, dziesięć samouczków przeprowadzonych przez każdy szczegółowy, może być zapisany do rysowania tekstu w kilku minutach.

## Szybkie odpowiedzi
- **Jakiej biblioteki użyto?** Aspose.Drawing dla .NET
- **Główne zadanie?** Rysowanie tekstu na obrazie (tworzenie obrazu z tekstem)
- **Kluczowa metoda?** `Graphics.DrawString` (rysowanie ciągu znaków na obrazie)
- **Format wyjściowy?** PNG (zapis bitmapy jako PNG)
- **Wymagania wstępne?** Środowisko programistyczne .NET oraz biblioteka Aspose.Drawing

## Co to jest rysowanie tekstu za pomocą Aspose.Drawing?
Rysunki udostępniające w pełni zarządzane API, które wyznaczają klasyczny model GDI+, jednocześnie dodając obsługę wieloplatformową. Umożliwia renderowanie tekstu, kształtowanie i obrazy o wysokiej jakości bez konieczności stosowania systemu.Drawing.Common.

## Dlaczego warto używać Aspose.Drawing do dodawania tekstu do obrazów?
- **Niezawodność wieloplatformowa** – działa na Windows, Linux i macOS.
- **Zaawansowane renderowanie** – antyaliasing i wygładzanie tekstu subpikselowego dla zaawansowanego wyniku.
- **Brak zewnętrznych zależności** – biblioteka zawiera wszystko, co potrzebne, aby *stwórz obraz z tekstem*.

## Warunki wstępne

Przed nurkowaniem upewnij się, że masz:

- **Aspose.Drawing dla .NET** – pobierz go z [dokumentacji Aspose.Drawing](https://reference.aspose.com/drawing/net/).
- **IDE .NET** takie jak Visual Studio lub VS Code.

## Importuj przestrzenie nazw

Rozpocznij od zaimportowania wymaganych przestrzeni nazw:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Krok 1: Utwórz obiekty Bitmap i Graphics

Tutaj tworzymy `Bitmap`, który będzie przechowywał ostateczny obraz, oraz obiekt `Graphics`, który pozwala rysować na nim. Wskazówka antyaliasingu zapewnia płynny wygląd tekstu.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Krok 2: Skonfiguruj Brush, Pen i Font

- **Brush** określa kolor tekstu.  
- **Pen** jest używany później do rysowania prostokąta wokół tekstu (opcjonalnie).  
- **Font** określa krój, rozmiar i styl dla operacji *rysowania ciągu znaków na obrazie*.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Krok 3: Zdefiniuj tekst i prostokąt

`Rectangle` określa, gdzie zostanie umieszczony tekst. Dostosuj współrzędne i rozmiar do swojego układu.

```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

## Krok 4: Narysuj prostokąt i tekst

Najpierw obrysowujemy obszar niebieskim prostokątem, a następnie **dodajemy tekst do bitmapy** wywołując `DrawString`. To jest sedno *rysowania tekstu* na obrazie.

```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

## Krok 5: Zapisz wynik

Obraz jest zapisywany jako plik PNG, spełniając wymaganie *zapis bitmapy jako PNG*. Zastąp ścieżkę zastępczą rzeczywistym folderem, w którym chcesz przechowywać plik.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Typowe przypadki użycia

- **Generowanie certyfikatów** z spersonalizowanymi nazwiskami.  
- **Tworzenie miniatur z znakami wodnymi** dla galerii internetowych.  
- **Budowanie dynamicznych wykresów** zawierających etykiety lub adnotacje.  

## Rozwiązywanie problemów i wskazówki

- **Czcionka nie znaleziona?** Upewnij się, że czcionka jest zainstalowana na maszynie hosta lub użyj prywatnej kolekcji czcionek.  
- **Tekst obcięty?** Zwiększ rozmiar prostokąta lub zmniejsz rozmiar czcionki.  
- **Obawy o wydajność?** Ponownie używaj tego samego obiektu `Graphics` dla wielu operacji rysowania, gdy to możliwe.  

## Często zadawane pytania

**P: Jak zmienić format wyjściowy na JPEG?**
O: Zastąp definicji `.png` rozszerzeniam `.jpg` w metodzie `Save` i opcji definicji `ImageCodecInfo` dla jakości JPEG.

**P: Czy mogę rysować tekst wielowierszowy?**
O: Tak, wstaw znaki nowej linii (`\n`) w ciągu znaków lub `StringFormat` z `FormatFlags.LineLimit`.

**P: Czy istnieje sposób zmierzenia rozmiaru tekstu przed rysowaniem?**
O: wykorzystanie `Graphics.MeasureString`, aby uzyskać szczegółowe dane renderowanego tekstu.

**P: Czy Aspose.Drawing obsługuje znaki Unicode?**
O: Zdecydowanie tak. Dostarcz czcionkę zawiera wymaganą glify, a biblioteka wyrenderuje je poprawnie.

**P: Jaka wersja Aspose.Drawing została użyta do testów?**
O: Przykłady opracowane z Aspose.Drawing 24.11 dla .NET.

---

**Aktualizacja Ostatnia:** 2026-02-25
**Testowano z:** Aspose.Drawing 24.11 dla .NET
**Autor:** Asponuj  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}