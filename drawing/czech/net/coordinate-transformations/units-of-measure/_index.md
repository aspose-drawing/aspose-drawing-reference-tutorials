---
date: 2026-05-24
description: Zjistěte, jak nastavit jednotku v Aspose.Drawing pro .NET, snadno převádět
  jednotky grafiky a ovládnout přesná měření pro vykreslování grafiky.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Jednotky měření v Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak nastavit jednotku v Aspose.Drawing pro .NET – Jednotky měření
url: /cs/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nastavit jednotku v Aspose.Drawing pro .NET – Jednotky měření

## Úvod

Vítejte ve světě Aspose.Drawing pro .NET, kde se setkává přesnost a flexibilita při manipulaci s grafikou. V tomto tutoriálu objevíte **jak nastavit jednotku** pro vaše kresby, naučíte se **převádět grafické jednotky** mezi body, milimetry a palci a uvidíte reálné příklady, které vaše obrázky učiní pixel‑dokonalými. Ať už vytváříte zprávy, miniatury nebo vlastní grafy, ovládání jednotek měření je nezbytné pro konzistentní vykreslování napříč zařízeními.

## Rychlé odpovědi
- **Jaký je hlavní způsob změny jednotek?** Zavolejte `graphics.PageUnit = PageUnit.Point` (nebo `.Millimeter`, `.Inch`) na objektu `Graphics`.  
- **Která jednotka odpovídá 1/72 palce?** Points.  
- **Kolik milimetrů je v jednom palci?** 25.4 mm = 1 inch.  
- **Potřebuji další knihovny pro používání jednotek?** Ne, jádro knihovny Aspose.Drawing poskytuje všechny konstanty jednotek.  
- **Mohu v jednom obrázku kombinovat jednotky?** Nastavte jednotku jednou pro každou instanci `Graphics`; kreslete vše pomocí této jednotky pro zachování konzistence.

## Požadavky

Než se ponoříme do tutoriálu, ujistěte se, že máte následující požadavky připravené:

- Aspose.Drawing pro .NET: Ujistěte se, že máte knihovnu nainstalovanou. Můžete si ji stáhnout [zde](https://releases.aspose.com/drawing/net/).
- Dokumentový adresář: Mějte určený adresář, kam chcete ukládat vytvořené dokumenty.
- Základní znalost C#: Doporučuje se základní znalost C#, aby bylo možné plně využít tento průvodce.

## Importovat jmenné prostory

Než začneme, importujme potřebné jmenné prostory pro efektivní používání Aspose.Drawing:

```csharp
using System.Drawing;
```

Nyní rozdělíme každý příklad do několika kroků:

## Jak nastavit jednotku na Points?

`Bitmap` třída představuje obrázek v paměti, který slouží jako kreslicí plátno. Načtěte svůj bitmap, vytvořte objekt `Graphics` a nastavte jednotku stránky na body — to říká Aspose.Drawing, aby interpretoval všechny souřadnice jako hodnoty 1/72 palce. Používání bodů vám poskytuje jemnou kontrolu pro grafiku připravenou k tisku a umožňuje specifikovat šířky čar s vysokou přesností.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Krok 1: Vytvořit Bitmap  
`Bitmap` třída představuje obrázek v paměti, který slouží jako kreslicí plátno.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Krok 2: Vytvořit objekt Graphics  
`Graphics` poskytuje kreslicí metody pro vykreslování tvarů a textu na `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Krok 3: Nastavit jednotku stránky na Points  
`PageUnit` je výčet, který určuje jednotku měření pro souřadnice stránky. `PageUnit.Point` definuje body jako jednotku měření (1 point = 1/72 inch). Toto nastavení se vztahuje na všechny následující kreslicí volání.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Krok 4: Nakreslit obdélník v Points  
Když nakreslíte obdélník po nastavení jednotky, zadané rozměry jsou interpretovány jako body, což zajišťuje přesné rozměry.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Jak nastavit jednotku na Millimeters?

`PageUnit` je výčet, který určuje jednotku měření pro souřadnice stránky. Přepnutí na milimetry je užitečné, když potřebujete metrické rozměry, například při generování technických diagramů. Aspose.Drawing považuje 1 mm za 1/25.4 inch, což vám umožňuje zarovnat grafiku s fyzickými měřeními používanými ve výrobě a technické dokumentaci.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Krok 1: Nastavit jednotku stránky na Millimeters  
Přiřaďte `PageUnit.Millimeter` objektu `Graphics`; všechny souřadnice nyní odpovídají metrickému systému.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Krok 2: Nakreslit obdélník v Millimeters  
Šířka a výška obdélníku jsou nyní vyjádřeny v milimetrech, což usnadňuje zarovnání s fyzickými měřeními a zajišťuje, že tištěný výstup odpovídá reálným rozměrům.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Jak nastavit jednotku na Inches?

`Graphics` poskytuje kreslicí metody pro vykreslování tvarů a textu na `Bitmap`. Palce jsou výchozí jednotkou pro mnoho amerických designových nástrojů. Nastavení jednotky na palce vám umožní myslet v známých termínech při rozvrhování UI prvků a usnadňuje přechod od návrhu obrazovky k tisku, kde se palce běžně používají.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Krok 1: Nastavit jednotku stránky na Inches  
`PageUnit.Inch` mění souřadnicový systém tak, že 1 jednotka odpovídá 1 inch, což poskytuje jednoduchý způsob, jak dimenzovat prvky pro tiskové rozvržení.

CODE_BLOCK_PLACEHOLDER_10_END

### Krok 2: Nakreslit obdélník v Inches  
Nyní jakýkoli tvar, který nakreslíte, používá palce jako základ měření, což je ideální pro tiskové rozvržení a pro komunikaci rozměrů se zúčastněnými, kteří jsou zvyklí na imperiální jednotky.

CODE_BLOCK_PLACEHOLDER_11_END

## Uložit výsledek

Po dokončení příkladů uložte výsledný obrázek do svého dokumentového adresáře. Metoda `Bitmap.Save` zapíše soubor ve formátu, který specifikujete (PNG, JPEG, atd.).

CODE_BLOCK_PLACEHOLDER_12_END

Nyní jste úspěšně zvládli různé jednotky měření v Aspose.Drawing pro .NET a vytvořili vizuální reprezentaci obdélníků pomocí bodů, milimetrů a palců.

## Proč používat jednotkový systém Aspose.Drawing?

Aspose.Drawing podporuje **30+ formátů obrázků** a může zpracovávat obrázky až do **5000 × 5000 pixelů** bez načítání celého souboru do paměti, což poskytuje vysoký výkon pro generování grafiky ve velkém měřítku. Explicitním nastavením jednotky eliminujete hádání, snižujete chyby při konverzi a zajišťujete, že váš výstup odpovídá přesným fyzickým rozměrům napříč všemi platformami.

## Časté problémy a řešení

- **Neočekávaná velikost po uložení** – Ověřte, že jste nastavili `graphics.PageUnit` **před** jakýmikoli kreslicími voláními; změna jednotky později neprovádí retroaktivní změnu velikosti existujících tvarů.  
- **Rozmazaný výstup na obrazovkách s vysokým DPI** – Zvyšte rozlišení bitmapy (např. `new Bitmap(width, height, 300)`) tak, aby odpovídalo cílovému DPI.  
- **Kombinace jednotek v jednom obrázku** – Vytvořte samostatné instance `Graphics` pro každou jednotku nebo proveďte ruční konverzi před kreslením.

## Často kladené otázky

### Q1: Mohu použít Aspose.Drawing pro .NET s jinými .NET frameworky?
A1: Ano, Aspose.Drawing je kompatibilní s různými .NET frameworky, což poskytuje flexibilitu ve vašem vývojovém prostředí.

### Q2: Je k dispozici bezplatná zkušební verze?
A2: Ano, můžete si vyzkoušet Aspose.Drawing s bezplatnou zkušební verzí [zde](https://releases.aspose.com/).

### Q3: Jak získám podporu pro Aspose.Drawing pro .NET?
A3: Navštivte [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) pro komunitní podporu a diskuse.

### Q4: Mohu zakoupit dočasnou licenci pro krátkodobé projekty?
A4: Ano, můžete získat dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu podrobnou dokumentaci pro Aspose.Drawing?
A5: Komplexní dokumentace je k dispozici [zde](https://reference.aspose.com/drawing/net/).

---

**Poslední aktualizace:** 2026-05-24  
**Testováno s:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Transformace souřadnicového systému – Transformace stránky v Aspose.Drawing pro .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Tutoriál transformace matic: Transformace matic v Aspose.Drawing pro .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Jak použít transformaci: Lokální transformace v Aspose.Drawing pro .NET](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}