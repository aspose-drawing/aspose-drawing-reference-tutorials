---
title: Jednotky měření v Aspose.Drawing pro .NET
linktitle: Jednotky měření v Aspose.Drawing
second_title: Aspose.Drawing .NET API – alternativa k System.Drawing.Common
description: Prozkoumejte všestrannost Aspose.Drawing pro .NET v tomto podrobném kurzu, který vám pomůže zvládnout měrné jednotky pro přesnou grafiku.
weight: 14
url: /cs/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jednotky měření v Aspose.Drawing pro .NET

## Úvod

Vítejte ve světě Aspose.Drawing for .NET, kde se přesnost a flexibilita setkávají při grafické manipulaci. V tomto tutoriálu se ponoříme do složitosti měrných jednotek v Aspose.Drawing a poskytneme vám průvodce krok za krokem, jak využít sílu této pozoruhodné knihovny.

## Předpoklady

Než se pustíme do výukového programu, ujistěte se, že máte splněny následující předpoklady:

-  Aspose.Drawing for .NET: Ujistěte se, že máte nainstalovanou knihovnu. Můžete si jej stáhnout[tady](https://releases.aspose.com/drawing/net/).

- Adresář dokumentů: Mějte určený adresář, kam chcete ukládat vytvořené dokumenty.

- Základní znalosti C#: Aby bylo možné co nejlépe využít tuto příručku, doporučuje se základní znalost C#.

## Importovat jmenné prostory

Než začneme, importujme potřebné jmenné prostory pro efektivní použití Aspose.Drawing:

```csharp
using System.Drawing;
```

Nyní si každý příklad rozdělíme do několika kroků:

## Body jako měrné jednotky

1. Vytvořit bitmapu: Inicializujte bitmapu se zadanou šířkou a výškou.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Vytvořit grafiku: Vygenerujte z bitmapy objekt Graphics, na který budete kreslit.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Nastavit jednotku stránky na body: Definujte body jako měrnou jednotku (1 bod = 1/72 palce).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Draw Rectangle: Nakreslete obdélník pomocí bodů jako jednotky.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Milimetry jako měrné jednotky

1. Nastavit jednotku stránky na milimetry: Změňte měrnou jednotku na milimetry (1 mm = 1/25,4 palce).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Kreslit obdélník v milimetrech: Nakreslete další obdélník s použitím milimetrů jako jednotek.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Palce jako měrné jednotky

1. Nastavit jednotku stránky na palce: Přepněte měrnou jednotku na palce.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Kreslit obdélník v palcích: Nakreslete obdélník pomocí palců jako jednotky.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Uložte výsledek

Po dokončení příkladů uložte výsledný obrázek do adresáře dokumentů:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Nyní jste úspěšně prošli různými měrnými jednotkami v Aspose.Drawing pro .NET a vytvořili jste vizuální reprezentaci obdélníků pomocí bodů, milimetrů a palců.

## Závěr

V tomto tutoriálu jsme prozkoumali, jak Aspose.Drawing for .NET zpracovává různé měrné jednotky. Manipulací s body, milimetry a palci můžete ve svých grafických výtvorech dosáhnout přesnosti a přizpůsobivosti. Experimentujte s těmito koncepty a odemkněte plný potenciál Aspose.Drawing.

## FAQ

### Q1: Mohu použít Aspose.Drawing for .NET s jinými frameworky .NET?

Odpověď 1: Ano, Aspose.Drawing je kompatibilní s různými frameworky .NET a poskytuje flexibilitu ve vašem vývojovém prostředí.

### Q2: Je k dispozici bezplatná zkušební verze?

 A2: Ano, můžete prozkoumat Aspose.Drawing s bezplatnou zkušební verzí[tady](https://releases.aspose.com/).

### Q3: Jak získám podporu pro Aspose.Drawing for .NET?

 A3: Navštivte[Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) za podporu komunity a diskuze.

### Q4: Mohu si zakoupit dočasnou licenci pro krátkodobé projekty?

 A4: Ano, můžete získat dočasnou licenci[tady](https://purchase.aspose.com/temporary-license/).

### Q5: Kde najdu podrobnou dokumentaci k Aspose.Drawing?

 A5: K dispozici je komplexní dokumentace[tady](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
