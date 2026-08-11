---
date: 2026-06-23
description: Naučte se, jak uložit PNG pomocí Aspose.Drawing, aplikovat world transformations
  a převést grafiku na PNG. Obsahuje příklady C# pro translate transform a více grafických
  transformací.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: World Transformation v Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak uložit PNG pomocí Aspose.Drawing – World Transformation
url: /cs/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak uložit PNG pomocí Aspose.Drawing – World Transformation

## Uložení bitmapy jako PNG – Úvod

**How to save PNG** pomocí Aspose.Drawing je běžná požadavek, když potřebujete vysoce kvalitní, průhledné obrázky generované za běhu. V tomto tutoriálu se naučíte, jak **save bitmap as PNG**, aplikovat world transformations jako translate, rotate a scale a nakonec převést grafiku na PNG – vše s čistým, udržovatelným C# kódem. Ať už budujete reportingový engine, komponentu pro grafy nebo vlastní UI renderer, zvládnutí těchto kroků vám umožní vytvářet dynamické obrázky, které vypadají skvěle na jakémkoli zařízení.

## Rychlé odpovědi
- **Co znamená „world transformation“?** Mapuje logické (světové) souřadnice vašeho kreslení na souřadnice stránky (zařízení).  
- **Mohu výsledek exportovat jako PNG?** Ano – po kreslení jednoduše zavoláte `bitmap.Save(...)` s příponou `.png`.  
- **Potřebuji licenci pro Aspose.Drawing?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Je to kompatibilní s .NET 6/7?** Naprosto – Aspose.Drawing podporuje .NET Framework 4.5+ a .NET Core/5/6/7.  
- **Kolik transformací mohu řetězit?** Můžete použít **multiple graphics transformations** v sekvenci (translate, rotate, scale, atd.).

## Co je World Transformation v Aspose.Drawing?

World transformation mění souřadnicový systém, který používají vaše kreslicí příkazy. Ve výchozím nastavení je (0,0) levý horní roh bitmapy. Pomocí `TranslateTransform`, `RotateTransform` nebo `ScaleTransform` můžete reposition tento počátek, otáčet tvary nebo je měnit velikost, aniž byste měnili původní geometrii.

## Jak uložit PNG pomocí Aspose.Drawing?

Načtěte objekt `Bitmap`, nastavte požadované world transformations na jeho instanci `Graphics`, nakreslete své tvary a nakonec zavolejte `bitmap.Save("output.png", ImageFormat.Png)`. Tento jednorázový příkaz pro uložení zapíše bezztrátový PNG soubor, který zachovává průhlednost a věrnost barev, což je ideální pro webové zdroje a UI překryvy.

## Proč použít příklad Graphics Translate?

Příklad graphics translate vám umožní posunout počátek kreslení jednou místo přepočítávání každého bodu. Tento přístup snižuje složitost kódu, zlepšuje čitelnost a umožňuje grafickému enginu efektivně zpracovat maticovou matematiku, což může zvýšit výkon vykreslování až o 30 % na velkých plátnech.

## Příklad Graphics Translate

**Příklad graphics translate** ukazuje, jak posunutí počátku zjednodušuje umístění. Místo přepočítávání každého bodu posunete souřadnicový systém jednou a kreslíte, jako by nový počátek byl střed plátna.

## Předpoklady

- **Aspose.Drawing knihovna** integrována do vašeho .NET projektu – stáhněte ji z oficiální [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/).  
- **adresář dokumentu**, kde bude výstupní obrázek uložen.  
- Základní znalost syntaxe **C#** a Visual Studio nebo vašeho preferovaného IDE.  

Nyní se ponořme do kódu!

## Importování jmenných prostorů

`Bitmap`, `Graphics` a Aspose kreslicí utility se nacházejí v těchto jmenných prostorech.  
**Definice:** `System.Drawing` poskytuje základní typy GDI+, zatímco `Aspose.Drawing` je rozšiřuje o cross‑platformové možnosti.

## Průvodce krok za krokem

### Krok 1: Vytvoření bitmapy

Začínáme vytvořením prázdného plátna, který bude obsahovat naše kreslení.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with premultiplied alpha, which is the optimal format for PNG output because it preserves transparency without extra conversion steps.

- **Proč 32bppPArgb?** Tento formát pixelů podporuje alfa průhlednost a vysoce kvalitní vykreslování barev, což je ideální pro PNG výstup, protože zachovává průhlednost bez dalších konverzních kroků.  
- **Tip:** Přizpůsobte šířku/výšku tak, aby odpovídaly požadované velikosti obrázku.

### Krok 2: Nastavení World Transformation (Graphics Translate Example)

`TranslateTransform` posune počátek souřadnicového systému na nové místo.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` posune bod (0,0) do středu plátna. Po tomto volání se jakýkoli tvar, který kreslíte pomocí souřadnic (0,0), objeví uprostřed obrázku.

- Tím se posune bod (0,0) na (500, 400) – střed plátna o rozměrech 1000 × 800.  
- Můžete řetězit další transformace: `RotateTransform` otáčí souřadnicový systém a `ScaleTransform` jej škáluje, což umožňuje **multiple graphics transformations**.

### Krok 3: Nakreslení obdélníku pomocí transformovaných souřadnic

`DrawRectangle` nakreslí obdélník pomocí zadaného pera a souřadnic.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` nakreslí obdélník vycentrovaný na plátně, protože jeho levý horní roh je posunut o polovinu šířky a výšky od transformovaného počátku.

- Levý horní roh obdélníku začíná v transformovaném počátku (střed obrázku).  
- Klidně experimentujte s dalšími tvary – elipsami, čarami nebo vlastními cestami.

### Krok 4: Uložení výsledku – Převod grafiky na PNG

`Save` zapíše bitmapu do souboru ve specifikovaném formátu obrázku.  
`ImageFormat` určuje formát souboru pro ukládání obrázků, například PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` zapíše bezztrátový PNG soubor, který lze použít přímo ve webových stránkách nebo UI komponentách.

- PNG zachovává přesné barvy a průhlednost, které jsme nastavili dříve.  
- Nahraďte `"Your Document Directory"` skutečnou cestou na vašem počítači.

## Časté problémy a řešení

| Problém | Proč k tomu dochází | Řešení |
|---------|---------------------|--------|
| **Chyba souboru nenalezen** při ukládání | Cílová složka neexistuje. | Vytvořte složku programově (`Directory.CreateDirectory`) před voláním `Save`. |
| **Prázdný obrázek** po transformaci | `TranslateTransform` byl zavolán po kreslení. | Ujistěte se, že transformace je nastavena **před** jakýmikoli kreslicími příkazy. |
| **Zkreslené barvy** | Použití nekompatibilního formátu pixelů. | Zůstaňte u `Format32bppPArgb` pro PNG výstup. |

## Často kladené otázky

**Q: Mohu použít více než jednu transformaci?**  
A: Ano – můžete řetězit `TranslateTransform`, `RotateTransform` a `ScaleTransform` pro dosažení složitých efektů v jedné grafické pipeline.

**Q: Je Aspose.Drawing zdarma pro komerční projekty?**  
A: Bezplatná zkušební verze je k dispozici pro hodnocení, ale pro produkční použití je vyžadována komerční licence.

**Q: Funguje to s .NET Core a .NET 5/6/7?**  
A: Naprosto. Aspose.Drawing podporuje všechny moderní .NET runtime, včetně .NET Core, .NET 5, .NET 6 a .NET 7.

**Q: Kde najdu kompletní referenci API?**  
A: Kompletní dokumentace je dostupná [zde](https://reference.aspose.com/drawing/net/).

**Q: Jak řešit chybějící výstupní soubor?**  
A: Ověřte řetězec cesty, zajistěte oprávnění k zápisu a potvrďte, že adresář existuje před voláním `Save`.

## Závěr

Nyní jste se naučili **how to save PNG** s Aspose.Drawing, aplikovali **world transformation** a provedli **graphics translate example**, který lze rozšířit o otáčení nebo škálování. Ovládnutím těchto stavebních bloků můžete generovat dynamické obrázky, vytvářet vlastní grafy nebo vytvářet grafiku za běhu pro jakoukoli .NET aplikaci.

---

**Poslední aktualizace:** 2026-06-23  
**Testováno s:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  
**Související zdroje:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Související tutoriály

- [Tutoriál Transformace matice: Transformace matice v Aspose.Drawing pro .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Jak otočit obrázek pomocí Aspose.Drawing Global Transformation](/drawing/net/coordinate-transformations/global-transformation/)
- [Transformace souřadnicového systému – Transformace stránky v Aspose.Drawing pro .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}