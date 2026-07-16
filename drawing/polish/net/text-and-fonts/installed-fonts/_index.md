---
date: 2026-02-25
description: Dowiedz się, jak tworzyć grafikę bitmapową w C# i zapisywać obrazy PNG,
  jednocześnie wyświetlając zainstalowane czcionki, rysując tekst przy użyciu czcionek
  oraz dostosowując rozdzielczość bitmapy za pomocą Aspose.Drawing dla .NET.
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Tworzenie grafiki bitmapowej w C# – zapisywanie obrazu PNG i praca z zainstalowanymi
  czcionkami w Aspose.Drawing
url: /pl/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz obraz PNG i pracuj z wbudowanymi czcionkami w Aspose.Drawing

## Wstęp

Jeśli **zapisania plików PNG** oraz **tworzenie grafiki bitmapowej w C#**, Aspose.Drawing dla .NET zapewnia czysty, wieloplatformowy sposób na to. W tym samouczku przeprowadziliśmy Cię przez listowanie podłączonych czcionek, wyświetlanie rodzinne czcionek, tworzenie grafiki z bitmapy oraz rysowanie tekstu czcionkami — a na końcu zapisanie wyniku jako obrazu PNG. Po umieszczeniu fragmentu kodu, który może zostać wpisany do dowolnego projektu .NET.

## Szybkie odpowiedzi
- **Co tworzy ten samouczek?** Obraz PNG, który jest wymienialną rodziną rodziny czcionek.
- **Jakiej biblioteki wymaga?** Aspose.Drawing dla .NET (nie wymaga System.Drawing.Common).
- **Czy można zastosować urządzenie do ładowania?** Tak — wystarczy za użytkownika je do `InstalledFontCollection`.
- **Czy rozdzielczość wyjściowa jest regulowana?** Oczywiście — zmień rozmiar bitmapy lub format pikseli, aby **dostosuj rozdzielczość bitmapy C#**.
- **Czy jest to licencja do uruchomienia kodu?** Tymczasowa licencja działa w środowisku ewaluacyjnym; pełny licencjat jest wymagany w produkcji.

## Co to jest „zapisz obraz PNG” w kontekście Aspose.Drawing?
Zapisanie obrazu PNG oznacza wyrenderowanie powierzchni rysowania (obiektu `Bitmap`) do pliku z rozszerzeniam `.png`. Aspose.Drawing został wykorzystany do kodowania, więc wystarczy pobrać `bitmap.Save(...)` z dostępną.

## Po co wyświetlać listę zainstalowanych czcionek i wyświetlać rodziny czcionek?
udostępniane przez użytkownika, pozwala na utworzenie dynamicznej grafiki, która jest uruchamiana przez użytkownika końcowego. Jest to szczególne postanowienie przy generowaniu, certyfikatach lub odpowiednich treściach kontrolnych, które powodują poniesienie konsekwencji korporacyjnej bez konieczności dostarczania plików czcionek.

## Jak stworzyć grafikę bitmapową C# za pomocą Aspose.Drawing?
Poniżej znajduje się praktyczny przewodnik krok po kroku, który zawiera dokładne, jak **utwórz grafikę bitmapową C#**, rysować tekst czcionkami i w razie potrzeby wymagana rozdzielczość bitmapy.

## Warunki wstępne

- **Aspose.Drawing Library** – pobierz najnowszą wersję ze [strony pobrania Aspose Drawing](https://releases.aspose.com/drawing/net/).
- **IDE** — Visual Studio, Rider lub niezależny edytor z .NET.
- **Podstawowa przyjemność C#** — możliwość bycia zaznajomiony z klasami, obiektami i prostymi pętlami.

## Importuj przestrzenie nazw
Aby pracować z czcionkami i grafiką, zaimportuj te przestrzenie nazw na górze pliku C#:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Przewodnik krok po kroku

### Krok 1: Utwórz mapę bitową (płótno)
Najpierw tworzymy bitmapę, która będzie przechowywać końcowy obraz. Rozmiar bitmapy i format pikseli określają jakość zapisanego PNG i pozwalają **adjust bitmap resolution C#**.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Krok 2: Utwórz grafikę z mapy bitowej
Następnie uzyskujemy obiekt `Graphics` z bitmapy. Ten obiekt pozwala rysować kształty, tekst i obrazy na płótnie.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Krok 3: Skonfiguruj pędzel i czcionkę (rysuj tekst za pomocą czcionek)
Potrzebujemy pędzla (brush) do koloru tekstu oraz obiektu `Font`, który definiuje krój, rozmiar i styl. To tutaj **draw text with fonts**.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Krok 4: Wyświetl listę zainstalowanych czcionek i pokaż rodziny czcionek
Teraz wyświetlamy liczbę rodzin czcionek oraz kilka pierwszych nazw bezpośrednio na bitmapie. To demonstruje możliwości **list installed fonts** i **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Krok 5: Zapisz obraz PNG
Na koniec zapisujemy bitmapę na dysku jako plik PNG. To podstawowa operacja **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Wskazówka:** Używaj `Path.Combine` do budowania ścieżek plików, aby uniknąć problemów z separatorami katalogów w różnych systemach operacyjnych.

## Typowe problemy i rozwiązania
| Problem | Przyczyna | Rozwiązanie |
|--------|-----------|------------|
| **Brak określonych czcionek** | `InstalledFontCollection` nie jest wypełnione (np. uruchomienie na urządzeniu bez czcionek). | Wymagane podanie na wniosek lub wydanie własne w aplikacji. |
| **Zapisany plik jest dostępny** | Nieprawidłowy format pikseli lub brak uprawnień do zapisu. | następuje, że folder wyjściowy istnieje w aplikacji mającej uprawnienia do zapisu; zachowaj `Format32bppPArgb`. |
| **Tekst jest rozmyty** | Niskie ustawienia DPI. | Zwiększone wymiary bitmapy lub ustaw `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Często zadawane pytania

**P:** Czy można zainstalować urządzenia elektryczne, które nie są zainstalowane na komputerze?
**O:** Tak. Załaduj plik do `PrivateFontCollection` i utwórz `Font` z tej kolekcji.

**P:** Jak obsłużyć wyjątki z czcionkami?
**O:** powoduje utworzenie bloku w `try/catch` i sprawdzenie `ArgumentException` pod kątem hamulców rodzinnych.

**P:** Czy Aspose.Drawing nadaje się do aplikacji webowych?
**O:** Zdecydowanie. Biblioteka działa w ASP.NET Core, Azure Functions i innych środowiskach po stronie serwera.

**P:** Czy mogę zmienić kolor lub styl tekstu?
**O:** Tak. różne typy `Brush` (np. `LinearGradientBrush`) i zmodyfikuj enum `FontStyle`.

**P:** Gdzie mogę uzyskać tymczasową wydajność?
**O:** Pobierz dostępne próbną ze [strony tymczasowych licencji Aspose](https://purchase.aspose.com/temporary-license/).

## Wniosek

Postępując zgodnie z tymi krokami, nauczyłeś się, jak **save PNG image** tworzyć pliki, które dynamicznie **list installed fonts**, **show font families**, **create graphics from bitmap** i **draw text with fonts** przy użyciu Aspose.Drawing dla .NET. Teraz wiesz, jak **create bitmap graphics C#**, regulować rozdzielczość bitmapy i w razie potrzeby włączać własne czcionki. Śmiało eksperymentuj z innymi czcionkami, kolorami i rozmiarami bitmap, aby dopasować je do wymagań wizualnych Twojego projektu.

---

**Ostatnia aktualizacja:** 2026-02-25  
**Testowano z:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
