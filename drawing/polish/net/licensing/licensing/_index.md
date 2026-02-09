---
date: 2026-02-09
description: Dowiedz się, jak ustawić licencję Aspose.Drawing w .NET. Opanuj metody
  licencjonowania, aby odblokować pełne funkcje bez znaków wodnych.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Ustaw licencję Aspose.Drawing – Jak ustawić licencję Aspose.Drawing
url: /pl/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Aspose.Drawing License

## Introduction

Jeśli tworzysz aplikacje .NET, które korzystają z potężnych funkcji graficznych i manipulacji obrazami, **ustawienie licencji Aspose.Drawing** jest pierwszym krokiem do usunięcia ograniczeń wersji próbnej i uzyskania pełnego zestawu funkcji. W tym samouczku poznasz trzy praktyczne sposoby ustawienia licencji Aspose.Drawing — ładowanie z pliku, ładowanie ze strumienia oraz użycie modelu rozliczania na podstawie zużycia — abyś mógł zintegrować bibliotekę z pewnością.

## Quick Answers
- **Jaki jest podstawowy sposób aktywacji Aspose.Drawing?** Załaduj plik licencji używając `License.SetLicense("Aspose.Drawing.lic")`.  
- **Czy mogę zastosować licencję w czasie działania?** Tak, możesz załadować licencję ze `Stream` w dynamicznych scenariuszach.  
- **Czy licencja rozliczana na podstawie zużycia jest obsługiwana?** Zdecydowanie; użyj `Metered.SetMeteredKey(publicKey, privateKey)`, aby włączyć rozliczanie oparte na konsumpcji.  
- **Czy potrzebuję licencji do wersji deweloperskich?** Wersja próbna działa do testów, ale ważna licencja usuwa znaki wodne i odblokowuje wszystkie API.  
- **Które wersje .NET są kompatybilne?** Aspose.Drawing obsługuje .NET Framework 4.x, .NET Core 3.1+ oraz .NET 5/6+.

## Prerequisites

Before you start, make sure you have:

- **Aspose.Drawing Library** – download the latest package from [here](https://releases.aspose.com/drawing/net/).  
- **License File** – obtain a valid `.lic` file from [Aspose](https://purchase.aspose.com/buy).  
- **.NET Development Environment** – Visual Studio, Rider, or any IDE that targets .NET Framework/.NET Core.

## Import Namespaces

Potrzebujemy standardowych przestrzeni nazw .NET oraz przestrzeni nazw Aspose.Drawing do licencjonowania. Dodaj następujące instrukcje `using` na początku swojego pliku C#:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Loading License from a File

Ładowanie licencji z pliku jest najprostszym podejściem. Postępuj zgodnie z tymi trzema krokami:

### Step 1: Initialize the License Object

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Step 2: Set the License from the `.lic` File

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Step 3: Confirm Success

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro tip:** Umieść plik `.lic` w tym samym folderze co Twój plik wykonywalny lub podaj pełną ścieżkę, aby uniknąć błędów „plik nie znaleziony”.

## Loading License from a Stream

Kiedy plik licencji jest osadzony jako zasób lub pobierany zdalnie, ładowanie go ze `Stream` zapewnia elastyczność.

### Step 1: Initialize the License Object

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Step 2: Load the License Using a `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Step 3: Confirm Success

```csharp
Console.WriteLine("License set successfully.");
```

> **Warning:** Pamiętaj, aby zwolnić `FileStream` (lub użyć bloku `using`), aby zwolnić uchwyty plików.

## Using Metered License

Licencjonowanie rozliczane na podstawie zużycia jest idealne dla SaaS lub modeli płatności za użycie. Śledzi zużycie i fakturuje na podstawie rzeczywistego wykorzystania.

### Step 1: Initialize the Metered Object

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Step 2: Set Public and Private Keys

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Step 3: Perform Your Image Processing

```csharp
// Your image processing logic here
```

### Step 4: Retrieve Consumption Information

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Step 5: Display the Consumption Details

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Common pitfall:** Typowy problem: Jeśli zapomnisz wywołać `SetMeteredKey`, API przełączy się w tryb próbny i zobaczysz znaki wodne w wyniku.

## Why Set the Aspose.Drawing License Correctly?

- **Usuwa znaki wodne**, które pojawiają się w trybie próbnym.  
- **Odblokowuje premium API**, takie jak zaawansowane filtry obrazu i konwersja do PDF.  
- **Zapewnia zgodność** z warunkami licencjonowania Aspose dla dystrybucji komercyjnej.  
- **Umożliwia rozliczanie na podstawie zużycia**, pozwalając płacić tylko za to, co wykorzystasz.

## Common Issues and Solutions

| Problem | Przyczyna | Rozwiązanie |
|-------|-------|-----|
| Błąd „License file not found” | Nieprawidłowa ścieżka lub brak pliku w folderze wyjściowym | Użyj pełnej ścieżki lub ustaw właściwość pliku *Copy to Output Directory* na *Copy always*. |
| Znak wodny nadal się pojawia po ustawieniu licencji | Licencja nie została załadowana przed pierwszym wywołaniem API | Załaduj licencję **przed** jakąkolwiek operacją Aspose.Drawing. |
| Zużycie w modelu rozliczanym zawsze zero | Nie ustawiono kluczy lub błędne zmienne środowiskowe | Sprawdź klucze publiczny/prywatny i zapewnij połączenie internetowe z serwerem rozliczania Aspose. |

## Frequently Asked Questions

**Q1: Czy mogę używać Aspose.Drawing bez licencji?**  
A1: Tak, licencja próbna działa w celach rozwojowych i ewaluacyjnych, ale dodaje znaki wodne i ogranicza niektóre funkcje.

**Q2: Jak często muszę odnawiać licencję Aspose.Drawing?**  
A2: Licencje są wieczyste dla zakupionej wersji. Odnowienie jest wymagane tylko w celu uzyskania wsparcia i aktualizacji.

**Q3: Czym jest licencjonowanie rozliczane na podstawie zużycia i kiedy powinienem je stosować?**  
A3: Licencjonowanie rozliczane nalicza opłaty w zależności od użycia (operacji lub przetworzonych danych). Jest idealne dla usług w chmurze lub modeli płatności za użycie.

**Q4: Czy mogę używać Aspose.Drawing w projektach komercyjnych?**  
A4: Absolutnie — po uzyskaniu ważnej licencji możesz osadzać Aspose.Drawing w dowolnej aplikacji komercyjnej.

**Q5: Gdzie mogę znaleźć wsparcie społeczności dla Aspose.Drawing?**  
A5: Odwiedź [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44), aby uzyskać pomoc społeczności, przykłady i dyskusje.

## Conclusion

Opanowanie sposobu **ustawiania licencji Aspose.Drawing** — niezależnie od tego, czy z pliku, ze strumienia, czy poprzez model rozliczania — zapewnia maksymalne wykorzystanie tej potężnej biblioteki graficznej .NET. Postępuj zgodnie z powyższymi krokami, zwracaj uwagę na typowe pułapki i będziesz gotowy tworzyć solidne rozwiązania przetwarzania obrazów bez żadnych przeszkód licencyjnych.

---

**Ostatnia aktualizacja:** 2026-02-09  
**Testowano z:** Aspose.Drawing 24.11 dla .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}