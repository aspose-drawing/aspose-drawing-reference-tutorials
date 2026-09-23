---
date: 2026-09-23
description: Naučte se, jak nakreslit text na obrázek pomocí Aspose.Drawing for .NET.
  Vytvořte obrázek s textem, přidejte text do bitmap a uložte bitmap jako PNG s custom
  fonts.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Jak nakreslit text s Aspose.Drawing for .NET
og_description: Naučte se, jak nakreslit text na obrázek pomocí Aspose.Drawing for
  .NET. Tento tutoriál vám ukáže, jak vytvořit obrázek s textem, přidat text do bitmap
  a uložit bitmap jako PNG s custom fonts.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Nakreslete text na obrázek pomocí Aspose.Drawing for .NET – Rychlý průvodce
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to draw text on image using Aspose.Drawing for .NET. Generate
    image with text, add text to bitmap, and save bitmap as PNG with custom fonts.
  headline: How to draw text on image with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Replace the `.png` extension with `.jpg` in the `Save` method and optionally
      specify an `ImageCodecInfo` for JPEG quality.
    question: How do I change the output format to JPEG?
  - answer: Yes, include line‑break characters (`\n`) in the string or use `StringFormat`
      with `FormatFlags.LineLimit`.
    question: Can I draw multi‑line text?
  - answer: Use `Graphics.MeasureString` to get the exact dimensions of the rendered
      text.
    question: Is there a way to measure text size before drawing?
  - answer: Absolutely. Provide a font that contains the required glyphs and the library
      will render them correctly.
    question: Does Aspose.Drawing support Unicode characters?
  - answer: The examples were tested with Aspose.Drawing 24.11 for .NET.
    question: What version of Aspose.Drawing was used for testing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- draw text on image
- Aspose.Drawing
- .NET image processing
- generate image with text
- custom font on image
title: Jak nakreslit text na obrázek pomocí Aspose.Drawing for .NET
url: /cs/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak nakreslit text na obrázek pomocí Aspose.Drawing pro .NET

## Úvod

V tomto podrobném průvodci se naučíte **jak nakreslit text na obrázek** pomocí Aspose.Drawing pro .NET. Ať už potřebujete vytvořit *dynamický textový obrázek*, přidat text k existujícímu bitmapu nebo vygenerovat grafiku s vlastními fonty, tento tutoriál vás provede každým detailem, abyste mohli začít kreslit text během několika minut. Knihovna podporuje více než 30 metod GDI+, běží na Windows, Linuxu i macOS a má **nulové externí závislosti**, což z ní činí spolehlivou volbu pro server‑side generování obrázků.

## Rychlé odpovědi
- **Jaká knihovna se používá?** Aspose.Drawing for .NET  
- **Hlavní úkol?** Nakreslit text na obrázek (vytvořit obrázek s textem)  
- **Klíčová metoda?** `Graphics.DrawString` (nakreslit řetězec na obrázek)  
- **Formát výstupu?** PNG (uložit bitmapu jako PNG)  
- **Požadavky?** .NET vývojové prostředí a knihovna Aspose.Drawing  

## Co je kreslení textu pomocí Aspose.Drawing?

Kreslení textu pomocí Aspose.Drawing znamená použití API kompatibilního s GDI+, které umožňuje vykreslovat Unicode řetězce na rastrové plátno. Metoda `Graphics.DrawString` zapisuje text do bitmapy, což vám umožňuje řídit font, barvu, zarovnání a anti‑aliasing. Tento přístup vám umožní generovat vysoce kvalitní obrázky bez instalace System.Drawing.Common.

## Proč použít Aspose.Drawing k přidání textu na obrázky?

Aspose.Drawing nabízí spolehlivý, multiplatformní způsob, jak vykreslovat text na obrázky bez nutnosti nativních knihoven GDI+, poskytující konzistentní kvalitu a výkon na jakémkoli operačním systému. Podporuje pokročilý anti‑aliasing, Unicode znaky a vlastní fonty a bezproblémově se integruje s .NET aplikacemi, což z něj činí ideální řešení pro server‑side generování obrázků i desktopové nástroje.

- **Spolehlivost napříč platformami** – funguje na Windows, Linuxu i macOS.  
- **Pokročilé vykreslování** – anti‑aliasing a subpixelové vyhlazování textu pro ostrý výstup.  
- **Žádné externí závislosti** – knihovna obsahuje vše, co potřebujete k *vytvoření obrázku s textem*.

## Požadavky

Předtím, než se pustíte do práce, ujistěte se, že máte:

- **Aspose.Drawing for .NET** – stáhněte si jej z [Aspose.Drawing dokumentace](https://reference.aspose.com/drawing/net/).  
- **IDE pro .NET** jako Visual Studio nebo VS Code.

## Importovat jmenné prostory

Začněte importováním požadovaných jmenných prostorů:

Tyto jmenné prostory poskytují základní typy GDI+ jako `Bitmap`, `Graphics` a nástroje pro vykreslování textu.
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Krok 1: vytvořit bitmapu a grafické objekty

`Bitmap` je rasterový kontejner obrázku Aspose.Drawing pro data pixelů a `Graphics` poskytuje kreslicí metody pro vykreslování tvarů a textu na něj.

`Bitmap` představuje obrázek v paměti, zatímco `Graphics` poskytuje kreslicí metody pro vykreslování na tuto bitmapu.
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Zde vytváříme `Bitmap`, který bude obsahovat finální obrázek, a objekt `Graphics`, který nám umožní na něj kreslit. Nastavení anti‑aliasingu zajišťuje, že text vypadá hladce.

## Krok 2: nastavit štětec, pero a font

`Brush` určuje barvu výplně, `Pen` obkresluje tvary a `Font` specifikuje typ písma, velikost a styl pro vykreslování textu.

`Brush` vyplňuje tvary barvou, `Pen` obkresluje tvary a `Font` určuje typ písma a velikost pro vykreslování textu.
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** definuje barvu textu.  
- **Pen** se později používá k nakreslení obdélníku kolem textu (volitelné).  
- **Font** určuje typ písma, velikost a styl pro operaci *nakreslit řetězec na obrázek*.

## Krok 3: definovat text a obdélník

`Rectangle` určuje ohraničující rámeček, kam bude text umístěn, specifikuje souřadnice X/Y a šířku/výšku.

`Rectangle` určuje pozici a velikost obdélníkového prostoru, který se zde používá k ohraničení vykresleného textu.
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` určuje, kde bude text umístěn. Přizpůsobte souřadnice a velikost podle vašeho rozvržení.

## Krok 4: nakreslit obdélník a text

`Graphics.DrawString` vykreslí zadaný text uvnitř daného obdélníku pomocí poskytnutého fontu a štětce.

`Graphics.DrawString` vykreslí řetězec textu uvnitř specifikovaného obdélníku pomocí daného fontu a štětce.
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Nejprve ohraničíme oblast modrým obdélníkem, poté **přidáme text do bitmapy** voláním `DrawString`. Toto je jádro *kreslení textu* na obrázku.

## Krok 5: uložit výsledek

Obrázek je uložen jako soubor PNG, čímž splňuje požadavek *uložit bitmapu jako PNG*. Nahraďte zástupnou cestu skutečnou složkou, kam chcete soubor uložit.

`bitmap.Save` zapíše obrázek do souboru ve zvoleném formátu, například PNG.
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Běžné případy použití

- **Generování certifikátů** s personalizovanými jmény.  
- **Vytváření vodoznakových miniatur** pro webové galerie.  
- **Vytváření dynamických grafů** obsahujících popisky nebo anotace.

## Odstraňování problémů a tipy

- **Font nenalezen?** Ujistěte se, že je font nainstalován na hostitelském počítači, nebo použijte soukromou kolekci fontů.  
- **Text oříznut?** Zvětšete velikost obdélníku nebo snižte velikost fontu.  
- **Obavy o výkon?** Pokud je to možné, znovu použijte stejný objekt `Graphics` pro více kreslicích operací.

## Často kladené otázky

**Q: Jak změním výstupní formát na JPEG?**  
A: Nahraďte příponu `.png` příponou `.jpg` v metodě `Save` a volitelně specifikujte `ImageCodecInfo` pro kvalitu JPEG.

**Q: Mohu kreslit víceřádkový text?**  
A: Ano, zahrňte znaky pro zalomení řádku (`\n`) do řetězce nebo použijte `StringFormat` s `FormatFlags.LineLimit`.

**Q: Existuje způsob, jak změřit velikost textu před kreslením?**  
A: Použijte `Graphics.MeasureString` k získání přesných rozměrů vykresleného textu.

**Q: Podporuje Aspose.Drawing Unicode znaky?**  
A: Rozhodně. Poskytněte font, který obsahuje požadované glyfy, a knihovna je vykreslí správně.

**Q: Jaká verze Aspose.Drawing byla použita pro testování?**  
A: Příklady byly testovány s Aspose.Drawing 24.11 pro .NET.

---

**Poslední aktualizace:** 2026-09-23  
**Testováno s:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose

## Související tutoriály

- [Vytvořit bitmapovou grafiku C# – uložit PNG obrázek a pracovat s nainstalovanými fonty v Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Jak uložit bitmapu jako PNG pomocí Aspose.Drawing API pro .NET](/drawing/net/image-editing/display/)
- [Text na obrázku](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}