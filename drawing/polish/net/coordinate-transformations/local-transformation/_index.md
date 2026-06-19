---
date: 2026-04-22
description: Naucz się zapisywać bitmapę jako PNG przy użyciu Aspose.Drawing dla .NET
  z przykładem macierzy transformacji. Przewodnik krok po kroku z przykładami kodu.
keywords:
- save bitmap as png
- transformation matrix example
- draw rotated ellipse
- convert graphics to png
- high-quality png output
linktitle: Lokalna transformacja w Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Zapisz bitmapę jako PNG przy użyciu transformacji w Aspose.Drawing
url: /pl/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zapisz bitmapę jako PNG przy użyciu transformacji w Aspose.Drawing

## Wprowadzenie

Jeśli potrzebujesz **zapisać bitmapę jako PNG** stosując lokalną transformację grafiki w aplikacji .NET, Aspose.Drawing sprawia, że proces jest prosty i niezawodny. W tym samouczku zobaczysz dokładnie, jak zastosować macierz transformacji do kształtu, wyrenderować wynik i w końcu **przekształcić grafikę do PNG** w celu przechowywania lub dalszego przetwarzania. Po zakończeniu będziesz mieć wielokrotnego użytku wzorzec kodu, który możesz dostosować do dowolnego scenariusza lokalnej transformacji.

## Szybkie odpowiedzi
- **Co to jest lokalna transformacja?** To operacja oparta na macierzy (obrót, skalowanie, przesunięcie, pochylenie) stosowana do konkretnego elementu rysunku bez wpływu na całą płótno.  
- **Która biblioteka wspiera to w .NET?** Aspose.Drawing dla .NET zapewnia w pełni funkcjonalne API, które działa we wszystkich obsługiwanych wersjach .NET.  
- **Czy mogę zapisać wynik jako PNG?** Tak — po prostu wywołaj `Bitmap.Save` z nazwą pliku “.png”, a Aspose.Drawing zajmie się konwersją.  
- **Czy potrzebuję licencji do rozwoju?** Darmowa wersja próbna działa do testów; licencja komercyjna jest wymagana do użytku produkcyjnego.  
- **Jak długo trwa implementacja?** Około 10‑15 minut dla podstawowego przykładu.

## Jak zapisać bitmapę jako PNG

Poniżej znajdziesz kompletny, krok po kroku przewodnik, który demonstruje **przykład macierzy transformacji** i kończy się wysokiej jakości plikiem PNG.

## Co to jest „jak zastosować transformację” w programowaniu grafiki?

Zastosowanie transformacji oznacza modyfikację układu współrzędnych obiektu rysunkowego przy użyciu **Matrix**. Macierz określa, jak punkty są obracane, skalowane lub przesuwane, co pozwala tworzyć zaawansowane efekty wizualne przy minimalnym kodzie.

## Dlaczego warto używać Aspose.Drawing do **konwersji grafiki do PNG**?

- **Cross‑platform**: Działa na .NET Framework, .NET Core oraz .NET 5/6+.  
- **Brak zależności od GDI+**: Unika problemów `System.Drawing.Common` na platformach nie‑Windows.  
- **Wysokiej jakości wyjście PNG**: Antyaliasing i renderowanie piksel‑perfekcyjne dla plików PNG.  
- **Bogate API**: Pełne wsparcie dla ścieżek, piór, pędzli i macierzy transformacji.

## Wymagania wstępne

Zanim rozpoczniesz, upewnij się, że masz:

1. **Aspose.Drawing for .NET** – pobierz i zainstaluj z [linku do pobrania](https://releases.aspose.com/drawing/net/).  
2. Folder na swoim komputerze, w którym zostanie zapisana wygenerowana grafika (np. `C:\MyImages\`).  
3. Podstawową znajomość C# oraz konfiguracji projektu .NET.  

## Importowanie przestrzeni nazw

Najpierw wprowadź wymagane przestrzenie nazw do swojego pliku C#:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Te przestrzenie nazw dają dostęp do klas `Bitmap`, `Graphics`, `GraphicsPath` i `Matrix` potrzebnych do przepływu pracy transformacji.

## Przewodnik krok po kroku

### Krok 1: Utwórz bitmapę

Zaczynamy od pustego płótna. Rozmiar bitmapy i format pikseli są dobrane, aby uzyskać wysokiej jakości, 32‑bitowy obraz wspierający przezroczystość alfa.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Wskazówka:** Użycie `Format32bppPArgb` zapewnia, że obraz zachowuje premultypowaną alfę, co jest idealne dla wyjścia PNG.

### Krok 2: Utwórz obiekt Graphics

Obiekt `Graphics` udostępnia metody rysowania działające na bitmapie. Czyścimy tło do neutralnego szarego, aby przekształcony kształt wyróżniał się.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Krok 3: Utwórz GraphicsPath

`GraphicsPath` pozwala definiować złożone kształty. Tutaj dodajemy elipsę umieszczoną w (300, 300) o szerokości 400 i wysokości 200 — efektywnie **rysując obróconą elipsę** po transformacji.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### Krok 4: Zastosuj lokalną transformację (przykład macierzy transformacji)

Teraz odpowiadamy na kluczowe pytanie: **jak zastosować transformację**. Tworzymy `Matrix`, obracamy ją o 45° wokół środka elipsy (500, 400) i stosujemy macierz do ścieżki.

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **Dlaczego obracać wokół środka?** Obracanie wokół środka kształtu zapobiega jego krążeniu wokół początku układu, co daje naturalny wygląd.

### Krok 5: Narysuj przekształconą ścieżkę

Po zastosowaniu transformacji renderujemy ścieżkę przy użyciu niebieskiego pióra o grubości 2. Ten krok efektywnie **rysuje obróconą elipsę** na płótnie.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### Krok 6: Zapisz przekształcony obraz (konwersja grafiki do PNG)

Na koniec zapisujemy bitmapę jako plik PNG. Ścieżka łączy wybrany katalog z podfolderem dla przykładów transformacji.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **Uwaga:** Rozszerzenie `.png` automatycznie wywołuje enkoder PNG Aspose.Drawing, spełniając wymaganie **zapisz bitmapę jako png**.

## Typowe problemy i rozwiązania

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| **Pusty obraz wyjściowy** | Grafika nie została wyczyszczona lub kolor pióra jest taki sam jak tło | Wywołaj `graphics.Clear` z kontrastowym kolorem i upewnij się, że kolor pióra jest widoczny. |
| **Zniekształcony obrót** | Użycie `Rotate` zamiast `RotateAt` | Użyj `RotateAt` i określ punkt środkowy kształtu. |
| **Plik nie został zapisany** | Nieprawidłowa ścieżka katalogu lub brak uprawnień do zapisu | Sprawdź, czy katalog istnieje i aplikacja ma dostęp do zapisu. |
| **PNG wydaje się rozmyty** | Niska wartość DPI bitmapy | Utwórz bitmapę o wyższej rozdzielczości lub ustaw `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Najczęściej zadawane pytania

**P:** Czy mogę łączyć wiele transformacji (np. skalowanie, a potem obrót)?  
**O:** Tak. Utwórz jedną `Matrix` i wywołaj metody takie jak `Scale`, `RotateAt` i `Translate` w wymaganej kolejności, a następnie zastosuj ją za pomocą `path.Transform(matrix);`.

**P:** Czy Aspose.Drawing jest odpowiedni do renderowania o wysokiej wydajności?  
**O:** Zdecydowanie tak. Biblioteka jest zoptymalizowana pod kątem zarówno szybkości, jak i jakości, i unika ograniczeń GDI+ na platformach nie‑Windows.

**P:** Jakie inne typy transformacji są obsługiwane?  
**O:** Oprócz obrotu możesz wykonywać translację, skalowanie i pochylenie przy użyciu tej samej klasy `Matrix`.

**P:** Jak obsłużyć wyjątki podczas procesu transformacji?  
**O:** Umieść kod rysowania w bloku `try‑catch` i sprawdź wyjątki `System.Drawing.Drawing2D`. Odwołaj się do oficjalnej [dokumentacji Aspose.Drawing](https://reference.aspose.com/drawing/net/) po szczegółowe wskazówki dotyczące obsługi błędów.

**P:** Czy mogę wypróbować Aspose.Drawing przed zakupem?  
**O:** Tak, w pełni funkcjonalna wersja próbna jest dostępna przez [link do pobrania](https://releases.aspose.com/drawing/net/).

## Podsumowanie

Korzystając z tego przewodnika, teraz wiesz **jak zapisać bitmapę jako PNG** po zastosowaniu lokalnej transformacji przy użyciu Aspose.Drawing dla .NET. Ten sam wzorzec można ponownie wykorzystać do skalowania, translacji lub pochylenia dowolnego kształtu, umożliwiając budowanie bogatych, interaktywnych komponentów wizualnych w aplikacjach przy jednoczesnym dostarczaniu wysokiej jakości plików PNG.

---

**Ostatnia aktualizacja:** 2026-04-22  
**Testowano z:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}