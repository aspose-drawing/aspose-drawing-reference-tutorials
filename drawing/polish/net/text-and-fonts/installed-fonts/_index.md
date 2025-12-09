---
date: 2025-12-06
description: Dowiedz się, jak zapisywać pliki PNG, jednocześnie wypisując zainstalowane
  czcionki, wyświetlając rodziny czcionek, tworząc grafikę z bitmapy oraz rysując
  tekst przy użyciu czcionek w Aspose.Drawing dla .NET.
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Zapisz obraz PNG i pracuj z zainstalowanymi czcionkami w Aspose.Drawing
url: /pl/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz obraz PNG i pracuj z zainstalowanymi czcionkami w Aspose.Drawing

## Wprowadzenie

Jeśli potrzebujesz **zapisz obraz PNG** pliki, które dodatkowo wyświetlają informacje o czcionkach zainstalowanych na maszynie, Aspose.Drawing dla .NET zapewnia czysty, wieloplatformowy sposób ich tworzenia. W tym tutorialu przeprowadzimy Cię przez wymienianie zainstalowanych czcionek, wyświetlanie rodzin czcionek, tworzenie grafiki z bitmapy oraz rysowanie tekstu czcionkami — a na końcu zapisanie wyniku jako plik PNG. Po zakończeniu będziesz mieć gotowy fragment kodu, który możesz wstawić do dowolnego projektu .NET.

## Szybkie odpowiedzi
- **Co tworzy ten tutorial?** Obraz PNG, który wymienia zainstalowane rodziny czcionek.  
- **Jakiej biblioteki wymaga?** Aspose.Drawing dla .NET (nie wymaga System.Drawing.Common).  
- **Czy mogę używać własnych czcionek?** Tak – wystarczy załadować je do `InstalledFontCollection`.  
- **Czy rozdzielczość wyjściowa jest regulowana?** Oczywiście – zmień rozmiar bitmapy lub format pikseli.  
- **Czy potrzebna jest licencja do uruchomienia kodu?** Licencja tymczasowa wystarczy do oceny; pełna licencja jest wymagana w produkcji.

## Co oznacza „zapisz obraz PNG” w kontekście Aspose.Drawing?
Zapisanie obrazu PNG oznacza wyrenderowanie powierzchni rysunkowej (obiektu `Bitmap`) do pliku z rozszerzeniem `.png`. Aspose.Drawing zajmuje się kodowaniem, więc wystarczy wywołać `bitmap.Save(...)` z żądaną ścieżką.

## Dlaczego wymieniać zainstalowane czcionki i pokazywać rodziny czcionek?
Znajomość dostępnych czcionek pozwala tworzyć dynamiczną grafikę, która dostosowuje się do środowiska użytkownika końcowego. Jest to szczególnie przydatne przy generowaniu raportów, certyfikatów lub dowolnych treści wizualnych, które muszą odpowiadać identyfikacji wizualnej firmy bez konieczności dołączania plików czcionek.

## Wymagania wstępne

- **Biblioteka Aspose.Drawing** – pobierz najnowszą wersję ze [strony pobierania Aspose Drawing](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider lub dowolny edytor kompatybilny z .NET.  
- **Podstawowa znajomość C#** – powinieneś być pewny w pracy z klasami, obiektami i prostymi pętlami.

## Importuj przestrzenie nazw
Aby pracować z czcionkami i grafiką, zaimportuj następujące przestrzenie nazw na początku pliku C#:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Przewodnik krok po kroku

### Krok 1: Utwórz bitmapę (płótno)
Najpierw tworzymy bitmapę, która będzie przechowywać końcowy obraz. Rozmiar bitmapy i format pikseli określają jakość zapisanego PNG.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Krok 2: Utwórz grafikę z bitmapy
Następnie uzyskujemy obiekt `Graphics` z bitmapy. Ten obiekt pozwala rysować kształty, tekst i obrazy na płótnie.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Krok 3: Skonfiguruj pędzel i czcionkę (rysuj tekst przy użyciu czcionek)
Potrzebujemy pędzla dla koloru tekstu oraz obiektu `Font`, który definiuje krój, rozmiar i styl.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Krok 4: Wymień zainstalowane czcionki i pokaż rodziny czcionek
Teraz wyświetlamy liczbę rodzin czcionek oraz kilka pierwszych nazw bezpośrednio na bitmapie. Demonstracja **list installed fonts** i **show font families**.

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

> **Pro tip:** Używaj `Path.Combine` do budowania ścieżek plików, aby uniknąć problemów z separatorami katalogów na różnych systemach operacyjnych.

## Typowe problemy i rozwiązania
| Problem | Przyczyna | Rozwiązanie |
|---------|-----------|-------------|
| **Brak wyświetlonych czcionek** | `InstalledFontCollection` nie został wypełniony (np. uruchamianie na serwerze bez czcionek). | Zainstaluj wymagane czcionki na serwerze lub osadź własne czcionki w aplikacji. |
| **Zapisany plik jest uszkodzony** | Nieprawidłowy format pikseli lub brak uprawnień do zapisu. | Upewnij się, że docelowy folder istnieje i aplikacja ma prawo zapisu; zachowaj `Format32bppPArgb`. |
| **Tekst jest rozmyty** | Niskie ustawienia DPI. | Zwiększ wymiary bitmapy lub ustaw `graphics.SmoothingMode SmoothingMode.AntiAlias`. |

## Najczęściej zadawane pytania

**P: Czy mogę używać własnych czcionek, które nie są zainstalowane na maszynie?**  
O: Tak. Załaduj plik czcionki do `PrivateFontCollection` i utwórz `Font` z tej kolekcji.

**P: Jak obsłużyć wyjątki związane z czcionkami?**  
O: Otocz tworzenie czcionki blokiem `try/catch` i sprawdzaj `ArgumentException` pod kątem brakujących rodzin.

**P: Czy Aspose.Drawing nadaje się do aplikacji webowych?**  
O: Absolutnie. Biblioteka działa w ASP.NET Core, Azure Functions i innych środowiskach po stronie serwera.

**P: Czy mogę zmienić kolor lub styl tekstu?**  
O: Tak. Użyj różnych typów `Brush` (np. `LinearGradientBrush`) i zmodyfikuj enum `FontStyle`.

**P: Gdzie mogę uzyskać tymczasową licencję do testów?**  
O: Pobierz licencję próbną ze [strony tymczasowej licencji Aspose](https://purchase.aspose.com/temporary-license/).

## Podsumowanie

Postępując zgodnie z tymi krokami, nauczyłeś się **zapisz obraz PNG** pliki, które dynamicznie **list installed fonts**, **show font families**, **create graphics from bitmap** oraz **draw text with fonts** przy użyciu Aspose.Drawing dla .NET. Śmiało eksperymentuj z innymi czcionkami, kolorami i rozmiarami bitmapy, aby dopasować je do wymagań Twojego projektu.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Ostatnia aktualizacja:** 2025-12-06  
**Testowano z:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose