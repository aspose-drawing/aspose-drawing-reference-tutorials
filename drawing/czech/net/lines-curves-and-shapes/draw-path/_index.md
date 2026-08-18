---
date: 2026-07-22
description: Naučte se, jak uložit bitmapu jako PNG a exportovat obrázek do JPEG pomocí
  Aspose.Drawing. Praktický návod krok za krokem ukazuje kreslení cest, vytváření
  obrázků a export formátů.
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: Kreslení cest v Aspose.Drawing
og_description: Uložte bitmapu jako PNG a exportujte obrázek do JPEG pomocí Aspose.Drawing
  pro .NET. Postupujte podle tohoto tutoriálu, abyste kreslili složité cesty, vytvářeli
  vysoce kvalitní obrázky a výstupně generovali více formátů.
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: Uložit bitmapu jako PNG – Kreslení cest s Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: Uložit bitmapu jako PNG – Použití GraphicsPath v Aspose.Drawing
url: /cs/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Kreslení cest v Aspose.Drawing

## Jak používat GraphicsPath – Úvod

**Save bitmap as PNG** je často prvním krokem, když potřebujete bezztrátový obrázek pro další zpracování nebo publikaci. V tomto tutoriálu se naučíte, jak kreslit složité vektorové cesty pomocí `GraphicsPath`, vykreslit je na bitmapu a poté **save bitmap as PNG** nebo dokonce **export image to JPEG**. Ať už vytváříte reportingový engine, vlastní knihovnu grafů, nebo jen potřebujete generovat dynamické grafiky, Aspose.Drawing vám poskytuje plně spravované, multiplatformní API, které nahrazuje System.Drawing.Common.

## Rychlé odpovědi
- **What can I draw with GraphicsPath?** Čáry, obdélníky, elipsy, křivky a vlastní tvary.  
- **Do I need a license?** Zkušební verze je zdarma; pro produkci je vyžadována komerční licence.  
- **Which .NET versions are supported?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Is System.Drawing.Common required?** Ne, Aspose.Drawing funguje nezávisle.  
- **Can I save to different formats?** Ano – PNG, JPEG, BMP, GIF a další.

## Co je GraphicsPath?
`GraphicsPath` je vektorový kontejner Aspose.Drawing, který ukládá sekvenci kreslicích primitiv, jako jsou čáry, oblouky a křivky, jako jeden objekt. Skupinováním těchto primitiv můžete jednotně aplikovat transformace, pravidla výplně a nastavení tahu, což zjednodušuje tvorbu složitých grafik a zajišťuje konzistentní vykreslování napříč různými výstupními formáty.

## Proč používat GraphicsPath s Aspose.Drawing?
Používání GraphicsPath s Aspose.Drawing vám poskytuje přesné, flexibilní a výkonné vektorové kreslicí schopnosti. Umožňuje vám stavět složité tvary, aplikovat transformace a efektivně je vykreslovat, přičemž zachovává multiplatformní konzistenci a podporuje zpracování obrázků ve velkém měřítku. Navíc se bez problémů integruje s dalšími .NET knihovnami, což vám umožní kombinovat rastrové i vektorové pracovní postupy v jedné aplikaci.

- **Precision:** Zpracovává více než 50 vektorových primitiv s subpixelovou přesností, což zajišťuje, že při **save bitmap as PNG** výstup zůstane ostrý při jakémkoli rozlišení.  
- **Flexibility:** Kombinujte čáry, oblouky a Bezierovy křivky do jedné cesty a poté ji vykreslete jedním voláním `Graphics.DrawPath`.  
- **Performance:** Optimalizovaná renderovací pipeline zpracovává obrázky až do 400 MP bez načítání celého souboru do paměti, což umožňuje provádět rozsáhlé dávkové úlohy.  
- **Cross‑Platform:** Identické výsledky na Windows, Linux a macOS runtimech, odstraňující platformně specifické chyby.

## Požadavky

Před tím, než se ponoříte do tutoriálu, ujistěte se, že máte následující požadavky:

- **Aspose.Drawing Library:** Stáhněte a nainstalujte knihovnu Aspose.Drawing. Knihovnu najdete [zde](https://releases.aspose.com/drawing/net/).
- **Other Aspose Products:** Prozkoumejte další nabídky Aspose [zde](https://releases.aspose.com/).
- **Development Environment:** Nastavte své .NET vývojové prostředí s potřebnými nástroji (Visual Studio, .NET SDK atd.).

## Importovat jmenné prostory

Začněte importováním požadovaných jmenných prostorů ve vašem projektu:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Krok 1: Vytvořit Bitmap a Graphics

Bitmap představuje obrázek v paměti, zatímco Graphics poskytuje kreslicí metody pro vykreslení na tento obrázek. Začněte vytvořením objektu `Bitmap` a `Graphics`, se kterými budete pracovat. Tento bitmap bude plátnem, na kterém bude vykreslen `GraphicsPath`, a později **save bitmap as PNG**:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Krok 2: Definovat Pen a GraphicsPath

Pen určuje barvu čáry, šířku a styl; GraphicsPath ukládá kolekci kreslicích primitiv jako jeden vektorový objekt. Dále definujte `Pen` pro specifikaci kreslicích atributů a vytvořte instanci `GraphicsPath`. Objekt `GraphicsPath` drží vektorová data před jejich vykreslením:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## Krok 3: Přidat čáry a tvary

Metody AddLine, AddRectangle a AddEllipse přidávají příslušné tvary do GraphicsPath pro pozdější vykreslení. Přidejte čáry, obdélníky a elipsy do `GraphicsPath`, abyste vytvořili složitou cestu. Můžete také přidat vlastní Bezierovy křivky pro hladké tvary:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## Krok 4: Vykreslit cestu

DrawPath vykresluje vektorová data z GraphicsPath na povrch Graphics pomocí zadaného pera. Vykreslete cestu na objekt `Graphics` pomocí specifikovaného `Pen`. Tato operace rasterizuje vektorová data na bitmapové plátno:

```csharp
graphics.DrawPath(pen, path);
```

## Krok 5: Uložit obrázek – Export do PNG nebo JPEG

Metoda Bitmap.Save zapisuje obrázek na disk ve zvoleném formátu, například PNG nebo JPEG. Po vykreslení můžete **save bitmap as PNG** pro bezztrátovou kvalitu nebo **export image to JPEG** pro menší velikost souboru. Vyberte formát, který nejlépe vyhovuje vašemu následnému scénáři:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

Opakujte tyto kroky podle potřeby k vytvoření složitých a vizuálně atraktivních cest.

## Časté problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Path not visible** | Ujistěte se, že barva pera kontrastuje s pozadím a že bitmapa je správně uložena. |
| **Unexpected image size** | Zkontrolujte, že rozměry bitmapy a formát pixelů odpovídají vašim požadavkům. |
| **License exception** | Použijte zkušební licenci pro testování; před nasazením do produkce použijte platnou licenci. |

## Často kladené otázky

### Q1: Mohu používat Aspose.Drawing s jinými .NET knihovnami?

A1: Ano, Aspose.Drawing se bez problémů integruje s jinými .NET knihovnami, poskytuje všestrannost ve vašich vývojových projektech.

### Q2: Je k dispozici zkušební verze?

A2: Ano, můžete získat bezplatnou zkušební verzi [zde](https://releases.aspose.com/).

### Q3: Kde mohu najít podporu pro Aspose.Drawing?

A3: Navštivte fórum Aspose.Drawing [forum](https://forum.aspose.com/c/drawing/44) pro pomoc a komunitní podporu.

### Q4: Jak získat dočasnou licenci?

A4: Získat dočasnou licenci [zde](https://purchase.aspose.com/temporary-license/).

### Q5: Mohu zakoupit Aspose.Drawing?

A5: Ano, můžete zakoupit Aspose.Drawing [zde](https://purchase.aspose.com/buy).

**Další Q&A**

**Q: Mohu kreslit vlastní Bezierovy křivky pomocí GraphicsPath?**  
A: Ano – použijte `path.AddBezier(...)` k definování hladkých křivek.

**Q: Jak vyčistit GraphicsPath před opětovným použitím?**  
A: Zavolejte `path.Reset()` k odstranění všech figur a začněte znovu.

## Závěr

Gratulujeme! Úspěšně jste se naučili **jak používat GraphicsPath** k vykreslení cest a poté **save bitmap as PNG** nebo **export image to JPEG** pomocí Aspose.Drawing pro .NET. Tento tutoriál pokrýval vytvoření bitmapy, definování pera, konstrukci `GraphicsPath`, vykreslení různých tvarů a export finálního obrázku v několika formátech. Experimentujte s různými souřadnicemi, barvami a šířkami čar a odhalte plný tvůrčí potenciál Aspose.Drawing.

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose

## Související tutoriály

- [Uložit bitmapu jako PNG a kreslit uzavřené křivky s Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Uložit bitmapu C# – Kreslit Bezierovy splajny s Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Jak uložit obrázek a kreslit kardinální splajny v Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}