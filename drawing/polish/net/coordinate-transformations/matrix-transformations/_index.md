---
date: 2026-08-28
description: Poznaj ten samouczek matrix transformation dla Aspose.Drawing .NET, obejmujący
  sposób rysowania rotated rectangle, zastosowanie matrix rotation oraz wykonanie
  matrix scaling w C#.
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- matrix rotation c#
- matrix scaling c#
- Aspose.Drawing graphics
lastmod: 2026-08-28
linktitle: Matrix Transformations w Aspose.Drawing
og_description: Samouczek matrix transformation dla Aspose.Drawing .NET. Dowiedz się,
  jak rysować rotated rectangle, zastosować matrix rotation, translate i scale grafikę
  w C# w kilka minut.
og_image_alt: Screenshot of a rotated rectangle created with Aspose.Drawing using
  matrix transformations
og_title: Samouczek matrix transformation – apply rotation, scaling and translation
  w Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  headline: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  type: TechArticle
- description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  name: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  steps:
  - name: set up the canvas
    text: Create a bitmap that will serve as the drawing surface. We also clear it
      with a neutral gray background so the transformed shapes stand out. > **Pro
      tip:** Using `Format32bppPArgb` ensures correct alpha handling when you later
      apply anti‑aliasing.
  - name: define the original rectangle
    text: This rectangle is the base shape we’ll transform. Its coordinates are chosen
      to keep it well within the canvas bounds.
  - name: rotate the rectangle (draw rotated rectangle)
    text: The `Matrix` class is Aspose.Drawing's representation of a 3 × 3 affine
      transformation matrix used for rotation, scaling and translation. We now **apply
      matrix rotation** of 15 degrees around the origin. The helper method `TransformPath`
      (shown later) takes a lambda that receives a `Matrix` instance
  - name: translate the rectangle
    text: Translation moves the shape without altering its size or orientation. Here
      we shift it left‑up by 250 pixels.
  - name: scale the rectangle (matrix scaling C#)
    text: Scaling changes the rectangle’s dimensions. A factor of `0.3f` reduces both
      width and height to 30 % of the original size.
  - name: save the result
    text: Finally, write the transformed image to disk. Adjust the path to point to
      a folder that exists on your machine. > **Note:** The `TransformPath` method
      (used in the steps above) creates a `GraphicsPath` from the rectangle, applies
      the supplied matrix, and draws the transformed shape. It’s a compact w
  type: HowTo
- questions:
  - answer: The documentation is available **[here](https://reference.aspose.com/drawing/net/)**.
    question: Where can I find the Aspose.Drawing documentation?
  - answer: Obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: How do I get a temporary license for Aspose.Drawing?
  - answer: Visit the Aspose.Drawing forum **[here](https://forum.aspose.com/c/drawing/44)**.
    question: Where can I seek support or connect with the community?
  - answer: Yes, download it from **[here](https://releases.aspose.com/drawing/net/)**.
    question: Can I download Aspose.Drawing for .NET?
  - answer: Purchase your license **[here](https://purchase.aspose.com/buy)**.
    question: How can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- matrix transformation
- Aspose.Drawing
- .NET graphics
- C# drawing
- cross‑platform rendering
title: 'Samouczek matrix transformation: matrix transformations w Aspose.Drawing dla
  .NET'
url: /pl/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Samouczek transformacji macierzy: transformacje macierzy w Aspose.Drawing dla .NET

## Wprowadzenie

W tym **samouczku transformacji macierzy** odkryjesz, jak klasa `Matrix` w Aspose.Drawing pozwala obracać, przesuwać i skalować obiekty graficzne z dokładnością do pojedynczego piksela. Niezależnie od tego, czy tworzysz edytor diagramów, generujesz automatyczne raporty, czy dodajesz efekty wizualne do usługi po stronie serwera, opanowanie transformacji macierzy jest niezbędne do uzyskania profesjonalnie wyglądających wyników na Windows, Linux i macOS.

## Szybkie odpowiedzi
- **Co obejmuje ten samouczek?** Pokazuje, jak obracać, przesuwać i skalować prostokąt przy użyciu API macierzy Aspose.Drawing.  
- **Czy potrzebna jest licencja?** Darmowa wersja próbna działa w trakcie rozwoju; licencja komercyjna jest wymagana w środowisku produkcyjnym.  
- **Jakie wersje .NET są obsługiwane?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7 i nowsze.  
- **Jak długo potrwa implementacja?** Około 10‑15 minut dla pełnego przykładu.  
- **Czy mogę zobaczyć obraz wyjściowy?** Tak – samouczek zapisuje plik PNG, który możesz od razu otworzyć.

## Czym jest samouczek transformacji macierzy?

Samouczek transformacji macierzy wyjaśnia, jak używać macierzy afinicznej 3 × 3 do przesuwania, obracania, skalowania lub ścinania prymitywów graficznych. W Aspose.Drawing klasa `Matrix` kapsułkuje te operacje, umożliwiając transformację dowolnego `GraphicsPath` lub kształtu przy użyciu jednego wielokrotnego użytku obiektu.

## Dlaczego używać Aspose.Drawing do transformacji macierzy?

Aspose.Drawing obsługuje **trzy główne systemy operacyjne** (Windows, Linux, macOS) i potrafi renderować obrazy do **10 000 × 10 000 px** w czasie krótszym niż **200 ms** na typowym sprzęcie serwerowym. Biblioteka zapewnia **100 % zgodność z API GDI+**, dzięki czemu możesz migrować istniejący kod System.Drawing bez przepisywania logiki, jednocześnie unikając ograniczeń licencyjnych, które dotyczą System.Drawing.Common na platformach nie‑Windows.

## Wymagania wstępne

- Działające środowisko programistyczne C# (Visual Studio, Rider lub VS Code).  
- Aspose.Drawing dla .NET zainstalowane – pobierz je z oficjalnej strony **[tutaj](https://releases.aspose.com/drawing/net/)** lub **[ten link](https://releases.aspose.com/drawing/net/)**, jeśli jeszcze go nie pobrałeś.  
- Podstawowa znajomość bitmapowych płócien, prostokątów i ścieżek graficznych.

## Importowanie przestrzeni nazw

Najpierw wprowadź wymagane przestrzenie nazw do zasięgu:

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

Te przestrzenie nazw dają dostęp do `Bitmap`, `Graphics` oraz klasy `Matrix` potrzebnych do transformacji.

## Przewodnik krok po kroku

Poniżej znajduje się zwięzły, numerowany przewodnik. Każdy krok zawiera krótkie wyjaśnienie, po którym następuje dokładny kod, którego będziesz potrzebować (bloki kodu pozostają niezmienione w stosunku do oryginalnego samouczka).

### Krok 1: przygotowanie płótna

Utwórz bitmapę, która będzie służyć jako powierzchnia rysowania. Następnie wyczyść ją neutralnym szarym tłem, aby przekształcone kształty się wyróżniały.

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **Wskazówka:** Użycie `Format32bppPArgb` zapewnia prawidłowe obsługiwanie alfa przy późniejszym stosowaniu antyaliasingu.

### Krok 2: zdefiniowanie pierwotnego prostokąta

Ten prostokąt jest bazowym kształtem, który będziemy transformować. Jego współrzędne zostały dobrane tak, aby znajdował się w pełni w granicach płótna.

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### Krok 3: obrócenie prostokąta (rysowanie obróconego prostokąta)

Klasa `Matrix` jest reprezentacją w Aspose.Drawing macierzy afinicznej 3 × 3 używanej do rotacji, skalowania i translacji. Teraz **stosujemy rotację macierzy** o 15 stopni wokół początku układu współrzędnych. Metoda pomocnicza `TransformPath` (pokazana później) przyjmuje wyrażenie lambda, które otrzymuje instancję `Matrix`.

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### Krok 4: przesunięcie prostokąta

Translacja przesuwa kształt bez zmiany jego rozmiaru ani orientacji. Tutaj przesuwamy go w lewo‑górę o 250 pikseli.

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### Krok 5: skalowanie prostokąta (skalowanie macierzy C#)

Skalowanie zmienia wymiary prostokąta. Współczynnik `0.3f` zmniejsza zarówno szerokość, jak i wysokość do 30 % pierwotnego rozmiaru.

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### Krok 6: zapisanie wyniku

Na koniec zapisz przekształcony obraz na dysku. Dostosuj ścieżkę, aby wskazywała na folder istniejący w Twoim systemie.

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **Uwaga:** Metoda `TransformPath` (używana w powyższych krokach) tworzy `GraphicsPath` z prostokąta, stosuje podaną macierz i rysuje przekształcony kształt. To zwięzły sposób na ponowne użycie tej samej logiki rysowania dla każdej transformacji.

## Częste problemy i rozwiązania

| Problem | Rozwiązanie |
|-------|----------|
| **Obraz jest pusty** | Upewnij się, że katalog wyjściowy istnieje i masz uprawnienia do zapisu. |
| **Transformacje wyglądają na niecentralne** | Pamiętaj, że `Matrix.Rotate` obraca wokół początku układu (0,0). Przesuń kształt do pożądanego punktu obrotu przed rotacją. |
| **Opóźnienie wydajności przy dużych obrazach** | Używaj `graphics.SmoothingMode = SmoothingMode.AntiAlias;` tylko w razie potrzeby i niezwłocznie zwalniaj obiekty `Graphics`. |

## Najczęściej zadawane pytania

**P:** Gdzie mogę znaleźć dokumentację Aspose.Drawing?  
**O:** Dokumentacja jest dostępna **[tutaj](https://reference.aspose.com/drawing/net/)**.

**P:** Jak uzyskać tymczasową licencję na Aspose.Drawing?  
**O:** Uzyskaj tymczasową licencję **[tutaj](https://purchase.aspose.com/temporary-license/)**.

**P:** Gdzie mogę uzyskać wsparcie lub połączyć się ze społecznością?  
**O:** Odwiedź forum Aspose.Drawing **[tutaj](https://forum.aspose.com/c/drawing/44)**.

**P:** Czy mogę pobrać Aspose.Drawing dla .NET?  
**O:** Tak, pobierz go **[tutaj](https://releases.aspose.com/drawing/net/)**.

**P:** Jak mogę zakupić Aspose.Drawing?  
**O:** Zakup licencję **[tutaj](https://purchase.aspose.com/buy)**.

## Zakończenie

Ukończyłeś pełny **samouczek transformacji macierzy** przy użyciu Aspose.Drawing dla .NET. Wiesz, jak **narysować obrócony prostokąt**, **zastosować rotację macierzy** oraz wykonać **skalowanie macierzy C#** na dowolnym kształcie. Eksperymentuj, łącząc wiele transformacji lub używając własnych punktów obrotu, aby odblokować jeszcze więcej kreatywnych efektów graficznych.

---

**Ostatnia aktualizacja:** 2026-08-28  
**Testowano z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose

## Powiązane samouczki

- [Jak narysować prostokąt – Transformacja układu współrzędnych (Transformacja strony) przy użyciu Aspose.Drawing API dla .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Jak zapisać PNG przy użyciu Aspose.Drawing – Transformacja świata](/drawing/net/coordinate-transformations/world-transformation/)
- [Krok po kroku Transformacja – Transformacje współrzędnych](/drawing/net/coordinate-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}