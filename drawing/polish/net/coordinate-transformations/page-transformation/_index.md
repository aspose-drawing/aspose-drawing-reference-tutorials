---
date: 2026-11-04
description: Dowiedz się, jak tworzyć grafikę prostokąta, wykonując transformację
  układu współrzędnych w .NET przy użyciu API Aspose.Drawing. Ten przewodnik krok
  po kroku pokazuje, jak przeliczyć cale na piksele i ustawić jednostki strony.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Transformacja układu współrzędnych w Aspose.Drawing
og_description: Dowiedz się, jak tworzyć grafikę prostokąta, przeliczając cale na
  piksele i ustawiając jednostki strony w Aspose.Drawing dla .NET. Postępuj zgodnie
  z przewodnikiem krok po kroku, aby uzyskać precyzyjną transformację strony.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Jak narysować prostokąt z transformacją strony przy użyciu Aspose.Drawing
  dla .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Jak narysować prostokąt – transformacja układu współrzędnych (transformacja
  strony) w Aspose.Drawing dla .NET
url: /pl/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak narysować prostokąt – transformacja układu współrzędnych (transformacja strony) w Aspose.Drawing dla .NET

## Wprowadzenie

W tym samouczku nauczysz się **jak narysować prostokąt** grafiki, jednocześnie wykonując transformację układu współrzędnych na poziomie strony przy użyciu Aspose.Drawing dla .NET. Niezależnie od tego, czy tworzysz silnik raportowania, narzędzie do szkicowania w stylu CAD, czy dowolną aplikację wymagającą precyzyjnych pomiarów rzeczywistych, ten przewodnik przeprowadzi Cię przez każdy krok — od tworzenia bitmapy po zapisanie finalnego pliku PNG. Po zakończeniu będziesz swobodnie konwertować cale na piksele, czyścić tło płótna i ustawiać jednostki strony dla gotowego do druku wyniku.

## Szybkie odpowiedzi
- **Co to jest transformacja układu współrzędnych?** Mapuje jednostki na poziomie strony (takie jak cale) na piksele na poziomie urządzenia, dzięki czemu rysunki skalują się prawidłowo na każdym urządzeniu wyjściowym.  
- **Dlaczego wybrać Aspose.Drawing?** Dostarcza w pełni zarządzane, wieloplatformowe API graficzne, które zastępuje System.Drawing.Common i obsługuje ponad 30 formatów obrazów.  
- **Jak długo trwa implementacja przykładu?** Około 5‑10 minut dla podstawowego prostokąta z transformacją strony.  
- **Czy potrzebna jest licencja do rozwoju?** Darmowa wersja próbna działa w fazie rozwoju; licencja komercyjna jest wymagana przy wdrożeniach produkcyjnych.  
- **Jakie środowiska uruchomieniowe .NET są obsługiwane?** .NET Framework 4.6+, .NET Core 3.1+, oraz .NET 5/6/7.

## Co to jest Aspose.Drawing?

Aspose.Drawing to biblioteka graficzna .NET, która zapewnia **device‑independent API** do tworzenia i manipulacji obrazami rastrowymi, wektorowymi oraz rysunkami na poziomie strony, bez polegania na GDI+. Obsługuje **30+ image formats** i może przetwarzać obrazy o rozmiarze do **10,000 × 10,000 pixels**, przy jednoczesnym niskim zużyciu pamięci.

## Dlaczego używać transformacji układu współrzędnych z Aspose.Drawing?

Transformacja układu współrzędnych pozwala projektować grafikę w jednostkach rzeczywistych, podczas gdy biblioteka automatycznie obsługuje skalowanie pikseli dla dowolnego urządzenia wyjściowego. Takie podejście gwarantuje, że prostokąt o wymiarze 5 cali zostanie wydrukowany dokładnie na pięć cali na drukarce 300 DPI i będzie proporcjonalny na ekranie 96 DPI, eliminując błędy ręcznej konwersji.

- **Device‑independent design:** Napisz kod raz; Aspose.Drawing skaluje go dla ekranów, drukarek lub PDF‑ów.  
- **Precision drawing:** Idealne do diagramów technicznych, schematów inżynieryjnych lub wszelkich scenariuszy, w których istotne są dokładne wymiary.  
- **Cross‑platform reliability:** Działa konsekwentnie na Windows, Linux i macOS, bez ograniczeń GDI+ znanych z System.Drawing.  
- **Performance:** Na typowym procesorze 2.5 GHz rysowanie prostokąta 5‑calowego przy 300 DPI kończy się w mniej niż **15 ms**, a biblioteka może renderować **50 frames per second** w scenariuszach podglądu w czasie rzeczywistym.

## Wymagania wstępne

- **Aspose.Drawing library:** Pobierz najnowszą wersję ze strony oficjalnej [here](https://releases.aspose.com/drawing/net/).  
- **IDE:** Visual Studio, Rider lub dowolny edytor kompatybilny z .NET.  
- **Output folder:** Zastąp `"Your Document Directory"` w przykładowym kodzie folderem, w którym chcesz zapisać plik PNG.  
- **Optional ASP.NET support:** Możesz dodać pakiet NuGet do projektu ASP.NET Core i używać tego samego API; wzorzec jest zgodny z typowym podejściem **how to use aspnet** dla bibliotek .NET.

## Jak narysować prostokąt z transformacją strony?

Wczytaj pustą bitmapę, ustaw jednostkę strony na cale i narysuj prostokąt używając cienkiego niebieskiego pióra — to zakończy rysowanie prostokąta w zaledwie kilku linijkach kodu. Właściwość `Graphics.PageUnit` instruuje silnik, aby interpretował wszystkie współrzędne jako cale, dzięki czemu możesz myśleć w jednostkach rzeczywistych zamiast surowych pikseli, a biblioteka automatycznie **convert inches to pixels** na podstawie DPI bitmapy.

### Krok 1: importowanie przestrzeni nazw

Instrukcje `using` zapewniają dostęp do podstawowych klas rysunkowych.

```csharp
using System.Drawing;
```

### Krok 2: utworzenie bitmapy

`Bitmap` jest kontenerem obrazu w pamięci, na którym rysujesz. Przechowuje bufor pikseli i udostępnia metody zapisu do plików. Tworzenie bitmapy definiuje rozmiar płótna i format pikseli.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Krok 3: utworzenie obiektu graphics

`Graphics` zapewnia powierzchnię rysowania dla bitmapy. Tłumaczy polecenia rysowania wysokiego poziomu (linie, kształty, tekst) na operacje pikseli na bazowej bitmapie.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Krok 4: wyczyszczenie tła płótna

Wyczyszczenie płótna neutralnym kolorem zapewnia wyraźność kształtów. W tym przykładzie wypełniamy tło jasnym szarym, co jednocześnie demonstruje technikę **clear canvas background**.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Krok 5: ustawienie transformacji (jak ustawić jednostki)

`Graphics.PageUnit` określa jednostkę miary używaną dla współrzędnych strony. Ustawienie jej na `GraphicsUnit.Inch` informuje Aspose.Drawing, aby **convert inches to pixels** automatycznie na podstawie DPI bitmapy (domyślnie 96 DPI, 300 DPI dla druku wysokiej rozdzielczości). Możesz również wybrać `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` lub `GraphicsUnit.Pixel` w zależności od wymagań układu.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Krok 6: narysowanie prostokąta – rysowanie grafiki prostokąta

`Pen` definiuje kolor, szerokość i styl linii rysowanych na powierzchni graficznej. Używając cienkiego niebieskiego pióra, rysujemy prostokąt, którego wymiary wyrażone są w calach, co sprawia, że kod jest bardziej czytelny w układach przeznaczonych do druku.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Krok 7: zapisanie bitmapy jako PNG

Na koniec zapisz bitmapę do pliku PNG w folderze określonym wcześniej. Zapis w formacie PNG zachowuje jakość bezstratną i jest szeroko wspierany na różnych platformach.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Jak skalować grafikę dla drukarki?

Ustaw DPI bitmapy na docelową rozdzielczość drukarki (np. 300 DPI) przed rysowaniem. To automatycznie **scale graphics printer** wynik, tak aby jeden cal w kodzie odpowiadał jednemu calowi na wydrukowanej stronie, przy jednoczesnym zachowaniu niezmienionego logicznego rozmiaru prostokąta. Po wywołaniu `bitmap.SetResolution(300, 300)`, ten sam prostokąt będzie wyglądał większy na papierze, ale zachowa dokładne wymiary.

## Typowe problemy i rozwiązania

| Problem | Dlaczego się pojawia | Rozwiązanie |
|---------|----------------------|-------------|
| **Plik wyjściowy nie został utworzony** | Nieprawidłowa ścieżka lub brak folderu | Upewnij się, że docelowy katalog istnieje lub wywołaj `Directory.CreateDirectory` przed zapisem. |
| **Prostokąt jest zniekształcony** | Niezgodny `PageUnit` lub DPI | Sprawdź, czy `graphics.PageUnit` odpowiada zamierzonej jednostce oraz czy DPI bitmapy jest ustawione prawidłowo (domyślnie 96 DPI, 300 DPI dla druku). |
| **Wyjątek licencyjny** | Uruchamianie bez ważnej licencji w środowisku produkcyjnym | Zastosuj tymczasową lub stałą licencję Aspose.Drawing przed tworzeniem obiektów graficznych. |

## Najczęściej zadawane pytania

**Q: Czy mogę używać Aspose.Drawing za darmo?**  
A: Tak, dostępna jest darmowa wersja próbna [here](https://releases.aspose.com/).

**Q: Gdzie mogę znaleźć szczegółową dokumentację Aspose.Drawing?**  
A: Pełna referencja API znajduje się [here](https://reference.aspose.com/drawing/net/).

**Q: Jak uzyskać wsparcie dla Aspose.Drawing?**  
A: Odwiedź [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) aby uzyskać pomoc społeczności i oficjalne wsparcie.

**Q: Czy dostępna jest tymczasowa licencja dla Aspose.Drawing?**  
A: Oczywiście — uzyskaj ją [here](https://purchase.aspose.com/temporary-license/).

**Q: Gdzie mogę kupić pełną licencję Aspose.Drawing?**  
A: Możesz ją kupić [here](https://purchase.aspose.com/buy).

## Podsumowanie

Teraz wiesz **jak narysować prostokąt** grafiki z transformacją na poziomie strony przy użyciu Aspose.Drawing dla .NET. Ustawiając jednostkę strony na cale, czyszcząc tło płótna i zapisując wynik jako PNG, uzyskasz precyzyjny, niezależny od urządzenia wynik, odpowiedni zarówno do wyświetlania na ekranie, jak i druku w wysokiej rozdzielczości. Eksperymentuj z innymi jednostkami, obrotami lub własnymi początkami współrzędnych, aby odblokować jeszcze potężniejsze scenariusze rysowania.

---

**Ostatnia aktualizacja:** 2026-11-04  
**Testowano z:** Aspose.Drawing 24.12 dla .NET  
**Autor:** Aspose

## Powiązane samouczki

- [Jak ustawić jednostkę w Aspose.Drawing dla .NET – Jednostki miary](/drawing/net/coordinate-transformations/units-of-measure/)
- [Transformacja globalna](/drawing/net/coordinate-transformations/global-transformation/)
- [Krok po kroku transformacja – Transformacje współrzędnych](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}