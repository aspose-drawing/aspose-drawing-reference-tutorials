---
date: 2025-12-01
description: Dowiedz się, jak przeprowadzić transformację układu współrzędnych i rysować
  grafiki prostokątne w .NET przy użyciu Aspose.Drawing. Przewodnik krok po kroku,
  jak przekształcać współrzędne strony.
language: pl
linktitle: Coordinate System Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Transformacja układu współrzędnych – Transformacja strony w Aspose.Drawing
  dla .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Transformacja układu współrzędnych – Transformacja strony w Aspose.Drawing dla .NET

## Wprowadzenie

Witamy! W tym samouczku odkryjesz **jak przekształcić współrzędne strony** przy użyciu Aspose.Drawing dla .NET i poznasz podstawy **transformacji układu współrzędnych**. Niezależnie od tego, czy tworzysz aplikację intensywnie korzystającą z grafiki, czy potrzebujesz precyzyjnej kontroli nad jednostkami rysowania, ten przewodnik przeprowadzi Cię przez każdy krok — od konfiguracji płótna po narysowanie elementu graficznego w kształcie prostokąta. Po zakończeniu będziesz mógł zastosować te techniki w własnych projektach z pewnością.

## Szybkie odpowiedzi
- **Czym jest transformacja układu współrzędnych?** Mapowanie jednostek na poziomie strony (takich jak cale) na piksele na poziomie urządzenia.  
- **Dlaczego używać Aspose.Drawing?** Oferuje w pełni zarządzaną alternatywę dla System.Drawing.Common z obsługą wieloplatformową.  
- **Jak długo trwa implementacja przykładu?** Około 5‑10 minut dla podstawowej transformacji strony.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w fazie rozwoju; licencja komercyjna jest wymagana w produkcji.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Czym jest transformacja układu współrzędnych?

**Transformacja układu współrzędnych** określa, w jaki sposób logiczne jednostki strony (takie jak cale, centymetry lub punkty) są przeliczane na piksele urządzenia podczas renderowania grafiki. Konfigurując właściwość `Graphics.PageUnit`, informujesz silnik rysujący, jak interpretować podane współrzędne, co daje Ci precyzyjną kontrolę nad rozmiarem i układem.

## Dlaczego używać transformacji układu współrzędnych z Aspose.Drawing?

- **Projekt niezależny od urządzenia:** Napisz kod raz i pozwól Aspose.Drawing obsłużyć skalowanie pikseli dla dowolnego ekranu lub drukarki.  
- **Precyzyjne rysowanie:** Idealne do diagramów technicznych, szkiców w stylu CAD lub wszelkich sytuacji, w których liczy się dokładny pomiar.  
- **Niezawodność wieloplatformowa:** Działa konsekwentnie na Windows, Linux i macOS bez ograniczeń GDI+ znanych z System.Drawing.

## Wymagania wstępne

- **Biblioteka Aspose.Drawing:** Pobierz najnowszą wersję ze strony oficjalnej [here](https://releases.aspose.com/drawing/net/).  
- **Środowisko programistyczne:** Visual Studio, Rider lub dowolne IDE zgodne z .NET.  
- **Katalog dokumentów:** Zastąp `"Your Document Directory"` w kodzie folderem, w którym chcesz zapisać obraz wyjściowy.

Teraz, gdy wszystko jest gotowe, przejdźmy do przewodnika krok po kroku.

## Importowanie przestrzeni nazw

Najpierw dodaj wymaganą przestrzeń nazw do swojego projektu:

```csharp
using System.Drawing;
```

## Krok 1: Utwórz bitmapę

Zaczynamy od utworzenia pustej bitmapy, która będzie służyć jako powierzchnia rysowania. Format pikseli `Format32bppPArgb` zapewnia wysoką jakość oraz wsparcie dla wstępnie pomnożonej alfa.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Krok 2: Utwórz obiekt Graphics

Obiekt `Graphics` udostępnia API rysowania dla bitmapy. Jest mostem między Twoim kodem a buforem pikseli.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Krok 3: Wyczyść płótno

Nadaj płótnu neutralne tło, aby narysowane kształty się wyróżniały. Tutaj wypełniamy je jasnoszarym kolorem.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Krok 4: Ustaw transformację (Jak przekształcić stronę)

Aby zamapować współrzędne strony na piksele urządzenia, ustaw właściwość `PageUnit`. W tym przykładzie wybieramy cale, ale możesz również użyć `GraphicsUnit.Millimeter`, `Point` itp.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

## Krok 5: Narysuj prostokąt – rysowanie grafiki prostokąta

Teraz rysujemy prostokąt przy użyciu cienkiego niebieskiego pióra. Ponieważ przeszliśmy na cale, rozmiar i pozycja prostokąta są wyrażone w calach, co sprawia, że kod jest bardziej czytelny w układach przeznaczonych do druku.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

## Krok 6: Zapisz obraz

Na koniec zapisz bitmapę do pliku PNG w folderze, który określiłeś wcześniej.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

Gratulacje! Właśnie wykonałeś **transformację układu współrzędnych**, ustawiłeś jednostkę strony na cale i **narysowałeś grafikę prostokąta** na bitmapie przy użyciu Aspose.Drawing.

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Plik wyjściowy nie został utworzony** | Nieprawidłowa ścieżka lub brak folderu | Upewnij się, że docelowy katalog istnieje lub użyj `Directory.CreateDirectory` przed zapisem. |
| **Prostokąt jest zniekształcony** | Nieprawidłowy `PageUnit` lub niezgodny DPI | Sprawdź, czy `graphics.PageUnit` odpowiada jednostkom, które zamierzasz używać oraz czy DPI bitmapy jest ustawione prawidłowo (domyślnie 96 DPI). |
| **Wyjątek licencyjny** | Uruchamianie bez ważnej licencji w produkcji | Zastosuj tymczasową lub stałą licencję Aspose.Drawing przed tworzeniem obiektów graficznych. |

## Najczęściej zadawane pytania

**P: Czy mogę używać Aspose.Drawing za darmo?**  
O: Tak, dostępna jest darmowa wersja próbna [here](https://releases.aspose.com/).

**P: Gdzie mogę znaleźć szczegółową dokumentację Aspose.Drawing?**  
O: Pełna referencja API znajduje się [here](https://reference.aspose.com/drawing/net/).

**P: Jak uzyskać wsparcie dla Aspose.Drawing?**  
O: Odwiedź [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17) aby uzyskać pomoc społeczności i oficjalną pomoc.

**P: Czy dostępna jest tymczasowa licencja dla Aspose.Drawing?**  
O: Oczywiście — uzyskaj ją [here](https://purchase.aspose.com/temporary-license/).

**P: Gdzie mogę kupić pełną licencję Aspose.Drawing?**  
O: Możesz ją kupić [here](https://purchase.aspose.com/buy).

## Podsumowanie

W tym przewodniku omówiliśmy wszystko, co musisz wiedzieć o **transformacji układu współrzędnych** w Aspose.Drawing: konfiguracji płótna, ustawianiu jednostek strony, rysowaniu precyzyjnych grafik prostokątnych oraz zapisywaniu wyniku. Wykorzystaj te techniki do tworzenia skalowalnej, niezależnej od urządzenia grafiki dla raportów, rysunków w stylu CAD lub dowolnej aplikacji, w której dokładność pomiarów ma znaczenie.

---

**Ostatnia aktualizacja:** 2025-12-01  
**Testowano z:** Aspose.Drawing 24.12 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}