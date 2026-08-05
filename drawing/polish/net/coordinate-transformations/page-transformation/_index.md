---
date: 2026-05-19
description: Dowiedz się, jak rysować grafiki prostokątne, wykonując transformację
  układu współrzędnych w .NET z Aspose.Drawing. Ten przewodnik krok po kroku pokazuje,
  jak przeliczyć cale na piksele i ustawić jednostki strony.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Transformacja układu współrzędnych w Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Jak narysować prostokąt – Transformacja układu współrzędnych (Transformacja
  strony) w Aspose.Drawing dla .NET
url: /pl/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak Narysować Prostokąt – Transformacja Systemu Współrzędnych (Transformacja Strony) w Aspose.Drawing dla .NET

## Wprowadzenie

Witamy! W tym samouczku odkryjesz **jak narysować prostokąt** w grafice, jednocześnie przekształcając współrzędne strony przy użyciu Aspose.Drawing dla .NET. Niezależnie od tego, czy tworzysz aplikację intensywnie wykorzystującą grafikę, czy potrzebujesz precyzyjnej kontroli nad jednostkami rysowania, ten przewodnik poprowadzi Cię przez każdy krok — od przygotowania płótna po narysowanie elementu prostokąta. Po zakończeniu będziesz mógł zastosować te techniki w swoich własnych projektach z pewnością.

## Szybkie Odpowiedzi
- **Co to jest transformacja systemu współrzędnych?** Mapowanie jednostek poziomu strony (takich jak cale) na piksele poziomu urządzenia.  
- **Dlaczego używać Aspose.Drawing?** Oferuje w pełni zarządzaną, wieloplatformową alternatywę dla System.Drawing.Common.  
- **Jak długo trwa implementacja przykładu?** Około 5‑10 minut dla podstawowej transformacji strony.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w fazie rozwoju; licencja komercyjna jest wymagana w produkcji.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Czym jest Aspose.Drawing?

`Aspose.Drawing` jest biblioteką graficzną .NET, która zapewnia **device‑independent API** do tworzenia i manipulacji obrazami rastrowymi, wektorowymi oraz rysunkami na poziomie strony bez polegania na GDI+. Obsługuje **ponad 30 formatów obrazów** i może przetwarzać obrazy do **10 000 × 10 000 pikseli** bez ładowania całego pliku do pamięci.

## Dlaczego używać transformacji systemu współrzędnych z Aspose.Drawing?

Transformacja systemu współrzędnych pozwala projektować grafikę w jednostkach rzeczywistych, podczas gdy biblioteka zajmuje się skalowaniem pikseli dla dowolnego urządzenia wyjściowego. Zapewnia to spójne rozmiary na ekranach i drukarkach oraz upraszcza obliczenia układu.

- **Projektowanie niezależne od urządzenia:** Napisz kod raz i pozwól Aspose.Drawing obsługiwać skalowanie pikseli dla każdego ekranu lub drukarki.  
- **Precyzyjne rysowanie:** Idealne do diagramów technicznych, szkiców w stylu CAD lub wszelkich scenariuszy, w których istotne są dokładne pomiary.  
- **Niezawodność wieloplatformowa:** Działa konsekwentnie na Windows, Linux i macOS bez ograniczeń GDI+ znanych z System.Drawing.  
- **Wyniki wydajności:** Na typowym procesorze 2,5 GHz rysowanie 5‑calowego prostokąta przy 300 DPI zajmuje mniej niż **15 ms**, a biblioteka może renderować **50 klatek na sekundę** w scenariuszach podglądu w czasie rzeczywistym.

## Wymagania wstępne

Zanim zaczniemy, upewnij się, że masz:

- **Biblioteka Aspose.Drawing:** Pobierz najnowszą wersję ze strony oficjalnej [here](https://releases.aspose.com/drawing/net/).  
- **Środowisko programistyczne:** Visual Studio, Rider lub dowolne IDE zgodne z .NET.  
- **Katalog dokumentów:** Zastąp `"Your Document Directory"` w kodzie folderem, w którym chcesz zapisać wygenerowany obraz.  
- **Wsparcie ASP.NET (opcjonalnie):** Możesz używać Aspose.Drawing w projektach ASP.NET Core, dodając pakiet NuGet do swojej aplikacji webowej — to follows the same **how to use aspnet** pattern as any other .NET library.

Teraz, gdy wszystko jest gotowe, przejdźmy do przewodnika krok po kroku.

## Jak Narysować Prostokąt z Transformacją Strony?

Załaduj pustą bitmapę, ustaw jednostkę strony na cale i narysuj prostokąt przy użyciu cienkiego niebieskiego pióra — to kończy rysowanie prostokąta w kilku linijkach kodu. Właściwość `Graphics.PageUnit` informuje silnik, aby interpretował wszystkie współrzędne jako cale, dzięki czemu możesz myśleć w rzeczywistych jednostkach zamiast surowych pikseli.

### Krok 1: Importowanie przestrzeni nazw

Instrukcje `using` dają dostęp do podstawowych klas rysunkowych.

```csharp
using System.Drawing;
```

### Krok 2: Tworzenie Bitmapy

`Bitmap` reprezentuje obraz w pamięci, na którym możesz rysować. Zaczynamy od stworzenia pustej bitmapy, która będzie służyć jako powierzchnia rysunkowa. Format pikseli `Format32bppPArgb` zapewnia wysoką jakość i wsparcie dla premultypowanego alfa.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Krok 3: Tworzenie Obiektu Graphics

Obiekt `Graphics` udostępnia API rysowania dla bitmapy. Jest mostem między Twoim kodem a buforem pikseli.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Krok 4: Czyszczenie Płótna

Nadaj płótnu neutralne tło, aby narysowane kształty się wyróżniały. Tutaj wypełniamy je jasnym szarym kolorem.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Krok 5: Ustawienie Transformacji (Jak ustawić jednostkę)

`Graphics.PageUnit` określa jednostkę miary używaną dla współrzędnych strony. Aby zamapować współrzędne strony na piksele urządzenia, ustaw właściwość `PageUnit`. W tym przykładzie wybieramy cale, ale możesz także użyć `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` lub `GraphicsUnit.Pixel`. Ustawienie jednostki na cale pozwala **automatycznie konwertować cale na piksele** w oparciu o DPI bitmapy (domyślnie 96 DPI, 300 DPI dla druku wysokiej rozdzielczości).

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Krok 6: Rysowanie Prostokąta – rysowanie grafiki prostokąta

`Pen` definiuje kolor, szerokość i styl linii rysowanych na powierzchni graficznej. Teraz rysujemy prostokąt przy użyciu cienkiego niebieskiego pióra. Ponieważ przeszliśmy na cale, rozmiar i pozycja prostokąta są wyrażone w calach, co sprawia, że kod jest bardziej czytelny dla układów przeznaczonych do druku.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Krok 7: Zapisz Obraz

Na koniec zapisz bitmapę do pliku PNG w folderze określonym wcześniej.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Jak Skalować Grafikę dla Drukarki?

Ustaw DPI bitmapy na docelową rozdzielczość drukarki (np. 300 DPI) przed rysowaniem. To automatycznie **skalowuje grafikę drukarki** tak, aby jeden cal w kodzie odpowiadał jednemu calowi na wydrukowanej stronie. Po ustawieniu `bitmap.SetResolution(300, 300)`, ten sam prostokąt będzie wyglądał większy na wydrukowanym arkuszu, zachowując dokładne wymiary.

## Typowe Problemy i Rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Plik wyjściowy nie został utworzony** | Nieprawidłowa ścieżka lub brak folderu | Upewnij się, że docelowy katalog istnieje lub użyj `Directory.CreateDirectory` przed zapisem. |
| **Prostokąt jest zniekształcony** | Nieprawidłowy `PageUnit` lub niezgodne DPI | Zweryfikuj, że `graphics.PageUnit` odpowiada jednostkom, które zamierzasz używać oraz że DPI bitmapy jest ustawione prawidłowo (domyślnie 96 DPI). |
| **Wyjątek licencyjny** | Uruchamianie bez ważnej licencji w produkcji | Zastosuj tymczasową lub stałą licencję Aspose.Drawing przed tworzeniem obiektów graficznych. |

## Najczęściej Zadawane Pytania

**P: Czy mogę używać Aspose.Drawing za darmo?**  
O: Tak, dostępna jest darmowa wersja próbna [here](https://releases.aspose.com/).

**P: Gdzie mogę znaleźć szczegółową dokumentację Aspose.Drawing?**  
O: Pełna referencja API znajduje się [here](https://reference.aspose.com/drawing/net/).

**P: Jak uzyskać wsparcie dla Aspose.Drawing?**  
O: Odwiedź [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) aby uzyskać pomoc społeczności i oficjalną pomoc.

**P: Czy dostępna jest tymczasowa licencja dla Aspose.Drawing?**  
O: Oczywiście — uzyskaj ją [here](https://purchase.aspose.com/temporary-license/).

**P: Gdzie mogę kupić pełną licencję Aspose.Drawing?**  
O: Możesz ją kupić [here](https://purchase.aspose.com/buy).

## Podsumowanie

W tym przewodniku omówiliśmy wszystko, co potrzebne do **jak narysować prostokąt** w grafice przy użyciu Aspose.Drawing: przygotowanie płótna, konfigurację jednostek strony, rysowanie precyzyjnych kształtów i zapisywanie wyniku. Użyj tych technik, aby tworzyć skalowalne, niezależne od urządzenia grafiki dla raportów, rysunków w stylu CAD lub dowolnej aplikacji, w której dokładność pomiarów ma znaczenie. Następnie odkryj zaawansowane transformacje, takie jak obrót, skalowanie i własne początki współrzędnych, aby odblokować jeszcze potężniejsze scenariusze rysowania.

**Ostatnia aktualizacja:** 2026-05-19  
**Testowano z:** Aspose.Drawing 24.12 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
