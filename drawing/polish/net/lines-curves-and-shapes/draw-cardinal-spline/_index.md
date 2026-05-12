---
date: 2026-02-12
description: Dowiedz się, jak zapisywać obrazy i rysować krzywe kardynalne w .NET
  przy użyciu Aspose.Drawing. Zapisz krzywą jako PNG i twórz płynne grafiki bez wysiłku.
linktitle: Drawing Cardinal Splines in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak zapisać obraz i rysować splajny kardynalne w Aspose.Drawing
url: /pl/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak zapisać obraz i rysować splajny kardynalne w Aspose.Drawing

## Wprowadzenie

## Szybkie odpowiedzi
- **Co robi główna metoda?** `Graphics.DrawCurve` interpoluje serię punktów w płynny splajn kardynalny.  
- **Jaki format jest używany do zapisu obrazu?** PNG za pomocą `Bitmap.Save`.  
- **Czy potrzebna jest licencja do zapisywania obrazów?** Wersja próbna działa w środowisku deweloperskim; licencja komercyjna jest wymagana w produkcji.  
- **Czy mogę zmienić napięcie krzywej?** Tak, przeciążenia `DrawCurve` pozwalają określić napięcie.  
- **Czy Aspose.Drawing jest kompatybilny z .NET 6+?** Absolutnie – obsługuje .NET Framework oraz .NET Core/5/6.

## Co oznacza „jak zapisać obraz” w kontekście Aspose.Drawing?
Zapisanie obrazu oznacza konwersję bitmapy w pamięci, na której rysujesz, do fizycznego pliku takiego jak PNG, JPEG lub BMP. Aspose.Drawing udostępnia prostą metodę `Bitmap.Save`, która zajmuje się kodowaniem dla Ciebie.

## Dlaczego rysować splajn kardynalny przy użyciu Aspose.Drawing?
Splajny kardynalne zapewniają płynną, płynącą krzywą, która przechodzi blisko zestawu punktów kontrolnych, idealną do wizualizacji danych, grafiki interfejsu użytkownika i kształtów niestandardowych. Korzystając z Aspose.Drawing, omijasz ograniczenia `System.Drawing.Common` i uzyskujesz spójność międzyplatformową.

## Wymagania wstępne

- Visual Studio (dowolna aktualna wersja) zainstalowane.  
- Biblioteka Aspose.Drawing dla .NET. Możesz ją pobrać [tutaj](https://releases.aspose.com/drawing/net/).  
- Podstawowa znajomość programowania w C#.

## Importowanie przestrzeni nazw

W swoim pliku C# rozpocznij od zaimportowania niezbędnej przestrzeni nazw:

```csharp
using System.Drawing;
```

## Krok 1: Utwórz bitmapę (płótno)

Najpierw utwórz bitmapę, która będzie pełnić rolę płótna dla twojego rysunku. Ta bitmapa jest miejscem, w którym splajn zostanie wyrenderowany przed **zapisaniem obrazu**.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Krok 2: Utwórz obiekt Graphics

Następnie uzyskaj obiekt `Graphics` z bitmapy. Ten obiekt zapewnia powierzchnię do rysowania.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Krok 3: Zdefiniuj pióro i narysuj krzywą

Zdefiniuj `Pen` z żądanym kolorem i szerokością, a następnie narysuj splajn kardynalny przy użyciu `DrawCurve`. To demonstruje technikę **rysowania krzywej piórem** i służy jako **przykład splajnu kardynalnego**.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Krok 4: Zapisz obraz (zapisz krzywą jako PNG)

Na koniec zapisz bitmapę do pliku PNG. To jest sedno **jak zapisać obraz** w tym samouczku.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Wskazówka:** Użyj `Path.Combine`, aby tworzyć ścieżki plików bezpiecznie na różnych platformach.

Gratulacje! Pomyślnie narysowałeś splajn kardynalny i zapisałeś wynik jako obraz PNG przy użyciu Aspose.Drawing dla .NET. Śmiało eksperymentuj z różnymi tablicami punktów, kolorami pióra lub szerokościami linii, aby dostosować swoje krzywe.

## Typowe przypadki użycia

- **Wizualizacje danych** – płynne wykresy liniowe, które wymagają precyzyjnych punktów kontrolnych.  
- **Niestandardowe komponenty UI** – rysowanie pokręteł, suwaków lub dekoracyjnych obramowań.  
- **Grafika eksportowalna** – generowanie zasobów PNG w locie dla raportów lub treści internetowych.

## Rozwiązywanie problemów i wskazówki

- **Obraz jest pusty?** Upewnij się, że format pikseli bitmapy obsługuje alfa (`Format32bppPArgb`) oraz że wywołujesz `graphics.Clear(Color.Transparent)`, jeśli to konieczne.  
- **Nieoczekiwany kształt krzywej?** Dostosuj parametr napięcia, używając przeciążenia `DrawCurve(pen, points, tension)`.  
- **Błędy dostępu do pliku?** Sprawdź, czy docelowy katalog istnieje i czy aplikacja ma uprawnienia do zapisu.

## Najczęściej zadawane pytania

### P1: Czy mogę używać Aspose.Drawing w projektach komercyjnych?
A1: Tak, Aspose.Drawing jest odpowiedni zarówno do projektów prywatnych, jak i komercyjnych. Sprawdź szczegóły licencjonowania na [stronie zakupu](https://purchase.aspose.com/buy).

### P2: Jak mogę uzyskać tymczasową licencję do testów?
A2: Uzyskaj tymczasową licencję do celów testowych [tutaj](https://purchase.aspose.com/temporary-license/).

### P3: Gdzie mogę znaleźć dodatkowe wsparcie?
A3: Odwiedź [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) w celu uzyskania wsparcia społeczności i dyskusji.

### P4: Czy dostępna jest darmowa wersja próbna?
A4: Tak, wypróbuj funkcje w wersji [darmowej wersji próbnej](https://releases.aspose.com/) przed zakupem.

### P5: Jak uzyskać dostęp do dokumentacji?
A5: Odwołaj się do obszernej [dokumentacji](https://reference.aspose.com/drawing/net/) w celu uzyskania szczegółowych informacji i przykładów.

### P6: Czy mogę zmienić format wyjściowy na JPEG?
A6: Oczywiście. Zastąp rozszerzenie `.png` na `.jpg` i określ `ImageFormat.Jpeg` w metodzie `Save`.

### P7: Czy można narysować wiele splajnów na tej samej bitmapie?
A7: Tak, po prostu wywołaj `graphics.DrawCurve` wielokrotnie z różnymi tablicami punktów i piórami.

## Podsumowanie

W tym przewodniku omówiliśmy **jak zapisać obraz** po narysowaniu splajnu kardynalnego, zaprezentowaliśmy praktyczną **techniki rysowania krzywej w C#** i podkreśliliśmy typowe scenariusze, w których ta metoda się wyróżnia. Masz teraz solidne podstawy do integracji płynnych grafik splajnowych w dowolnej aplikacji .NET.

---

**Ostatnia aktualizacja:** 2026-02-12  
**Testowano z:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}