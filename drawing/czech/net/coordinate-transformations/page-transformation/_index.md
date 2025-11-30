---
date: 2025-11-30
description: Naučte se, jak použít transformaci souřadnicového systému, kreslit bitmapu
  obdélníku a transformovat stránky pomocí Aspose.Drawing pro .NET.
language: cs
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Transformace souřadnicového systému (transformace stránky) v Aspose.Drawing
  pro .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Transformace souřadnicového systému (Transformace stránky) v Aspose.Drawing pro .NET

## Úvod

Vítejte! V tomto tutoriálu se dozvíte **jak provést transformaci souřadnicového systému** na stránce pomocí Aspose.Drawing pro .NET. Ať už potřebujete **kreslit bitmapové obdélníky**, měřítkovat kresby nebo jen mapovat jednotky stránky na jednotky zařízení, níže uvedené kroky vás provedou celým procesem – jasně, stručně a připravené ke zkopírování do vašeho projektu.

## Rychlé odpovědi
- **Jaká je hlavní třída pro kreslení?** `Graphics` z Aspose.Drawing.
- **Jak nastavit jednotky stránky?** Použijte `graphics.PageUnit = GraphicsUnit.Inch;`.
- **Mohu nakreslit obdélník na transformované stránce?** Ano – vytvořte `Pen` a zavolejte `DrawRectangle`.
- **Kam se ukládá výstup?** Do složky, kterou určíte v `bitmap.Save`.
- **Potřebuji licenci pro produkci?** Pro komerční použití je vyžadována platná licence Aspose.Drawing.

## Co je transformace souřadnicového systému?

**Transformace souřadnicového systému** mění způsob, jakým se logické souřadnice stránky (např. palce nebo milimetry) mapují na fyzické souřadnice zařízení (pixely). Úpravou transformace řídíte měřítko, rotaci a posunutí všech kreslicích operací, což usnadňuje tvorbu grafiky nezávislé na rozlišení.

## Proč použít Aspose.Drawing pro transformace stránek?

- **Plná kompatibilita s .NET** – funguje s .NET Framework, .NET Core i .NET 5/6.
- **Bohaté grafické API** – nabízí stejnou funkčnost jako System.Drawing.Common bez omezení platformy.
- **Jednoduchá práce s jednotkami** – přepínání mezi palci, milimetry, body atd. jednou vlastností.
- **Výstup vysoké kvality** – generujte PNG, JPEG, BMP a další formáty s přesnou kontrolou.

## Předpoklady

Než se pustíme dál, ujistěte se, že máte:

- **Knihovnu Aspose.Drawing** – stáhněte nejnovější verzi z oficiálního webu [here](https://releases.aspose.com/drawing/net/).
- **Vývojové prostředí** – Visual Studio (libovolná edice) nebo jiné .NET IDE.
- **Zápisová práva** – složku ve vašem počítači, kam bude transformovaný obrázek uložen (nahraďte `"Your Document Directory"` ve kódu skutečnou cestou).

Nyní, když je vše připraveno, projděme jednotlivé kroky.

## Import Namespaces

Nejprve načtěte požadovaný namespace:

```csharp
using System.Drawing;
```

> *Proč je to důležité*: `System.Drawing` obsahuje `Bitmap`, `Graphics`, `Pen` a struktury barev, které během tutoriálu použijeme.

## Krok 1: Vytvoření bitmapy

Vytvořte prázdné plátno, které bude hostit transformované kreslení. Specifikujeme velikost **1000 × 800 pixelů** a formát pixelu podporující alfa průhlednost.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> Tato bitmapa slouží jako kreslicí plocha. Zvolený formát pixelu (`Format32bppPArgb`) zajišťuje vykreslování vysoké kvality s přednásobenou alfou.

## Krok 2: Vytvoření objektu Graphics

Objekt `Graphics` poskytuje kreslicí metody (čáry, tvary, text). Získáme jej z bitmapy, kterou jsme právě vytvořili.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> Objekt `Graphics` je jádrem všech vykreslovacích operací; respektuje nastavení transformace, která bude aplikována dále.

## Krok 3: Vymazání plátna

Před kreslením vymažte plátno na neutrální barvu pozadí (v tomto příkladu šedou). Tento krok také ukazuje, jak vyplnit celou bitmapu jednotnou barvou.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Krok 4: Nastavení transformace (Aplikace transformace stránky)

Zde **aplikujeme transformaci stránky** nastavením `PageUnit` na palce. Tím říkáme grafickému enginu, aby všechny následující souřadnice interpretoval jako palce místo pixelů.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *Tip*: Změna `PageUnit` je jednoduchý způsob, **jak transformovat souřadnice stránky** bez ručního počítání pixelových hodnot.

## Krok 5: Kreslení obdélníku (Draw rectangle bitmap)

Nyní nakreslíme obdélník o rozměrech **1 palec × 1 palec** na pozici (1, 1) palců. Šířka `Pen` je nastavena na `0.1f` palců, což dává tenkou, ale viditelnou čáru.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> Toto ukazuje **draw rectangle bitmap** po aplikaci transformace – všimněte si, že velikost obdélníku je definována v palcích, nikoli v pixelech.

## Krok 6: Uložení obrázku

Nakonec uložte transformovanou bitmapu na disk. Nahraďte `"Your Document Directory"` skutečnou cestou ke složce ve vašem počítači.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> Výstupní soubor (`PageTransformation_out.png`) bude obsahovat obdélník nakreslený pomocí transformace souřadnicového systému, kterou jsme nastavili dříve.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|---------|---------|--------|
| **Obrázek je prázdný** | Plátno nebylo vymazáno nebo kreslení proběhlo mimo viditelnou oblast. | Ověřte `graphics.PageUnit` a hodnoty souřadnic; ujistěte se, že obdélník leží v mezích bitmapy. |
| **Nesprávné měřítko** | Použit nesprávný `GraphicsUnit`. | Zkontrolujte, že `graphics.PageUnit` odpovídá jednotce, kterou chcete použít (např. `GraphicsUnit.Inch`). |
| **Chyby v cestě k souboru** | Chybějící adresář nebo neplatné znaky. | Vytvořte cílovou složku předem nebo použijte `Path.Combine` pro bezpečnou konstrukci cesty. |

## Často kladené otázky

**Q: Mohu Aspose.Drawing používat zdarma?**  
A: Aspose.Drawing nabízí bezplatnou zkušební verzi, kterou můžete získat [here](https://releases.aspose.com/).

**Q: Kde najdu podrobnou dokumentaci k Aspose.Drawing?**  
A: Dokumentace je k dispozici [here](https://reference.aspose.com/drawing/net/).

**Q: Jak mohu získat podporu pro Aspose.Drawing?**  
A: Pro podporu navštivte [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17).

**Q: Je k dispozici dočasná licence pro Aspose.Drawing?**  
A: Ano, dočasnou licenci můžete získat [here](https://purchase.aspose.com/temporary-license/).

**Q: Kde mohu zakoupit Aspose.Drawing?**  
A: Aspose.Drawing můžete zakoupit [here](https://purchase.aspose.com/buy).

## Závěr

Nyní jste se naučili **aplikovat transformaci souřadnicového systému**, **kreslit bitmapové obdélníky** a **uložit výsledek** pomocí Aspose.Drawing pro .NET. Tyto stavební bloky vám umožní vytvářet grafiku nezávislou na rozlišení, ideální pro zprávy, UI komponenty nebo jakýkoli scénář, kde je důležitá přesná velikost. Vyzkoušejte další hodnoty `GraphicsUnit` (např. `Millimeter` nebo `Point`) a zjistěte, jak ovlivní vaše kresby.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-11-30  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose