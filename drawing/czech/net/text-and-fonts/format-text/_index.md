---
date: 2026-07-17
description: Naučte se, jak zabránit text overflow nastavením Text Alignment v Aspose.Drawing
  for .NET a přidávat text do obrázků. Praktický návod krok za krokem s příklady.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Nastavit Text Alignment pomocí Aspose.Drawing for .NET
og_description: Zabránit text overflow nastavením Text Alignment v Aspose.Drawing
  for .NET. Naučte se kreslit řetězec na obrázek, centrovat text v obdélníku a nahradit
  System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Zabránit Text Overflow – nastavit Text Alignment pomocí Aspose.Drawing for
  .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Zabránit Text Overflow – nastavit Text Alignment pomocí Aspose.Drawing for
  .NET
url: /cs/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Zabránit přetečení textu – Nastavit zarovnání textu pomocí Aspose.Drawing

## Úvod

Když potřebujete **zabránit přetečení textu** při vykreslování grafiky v .NET, Aspose.Drawing vám poskytuje detailní kontrolu nad umístěním textu, jeho zarovnáním a zalamováním. Ať už vytváříte generátor odznaků, dynamickou zprávu nebo jakýkoli výstup založený na obrázcích, zvládnutí zarovnání textu zajistí, že text zůstane uvnitř zamýšleného obdélníku a bude vypadat profesionálně. V tomto průvodci si ukážeme, jak vytvořit bitmapové plátno, nakonfigurovat `StringFormat`, nakreslit obdélník se zarovnaným textem, řešit přetečení a nakonec uložit obrázek.

## Rychlé odpovědi
- **Co znamená „nastavit zarovnání textu“?** Definuje, jak je text umístěn vodorovně a svisle v rámci kreslicího obdélníku.  
- **Která třída řídí zarovnání?** `StringFormat` vám umožňuje nastavit `Alignment` a `LineAlignment`.  
- **Mohu nakreslit řetězec a obdélník najednou?** Ano — použijte `Graphics.DrawRectangle` a poté `Graphics.DrawString`.  
- **Jak zabránit přetečení textu?** Upravte velikost obdélníku nebo ručně rozdělte text do více řádků.  
- **Potřebuji licenci pro produkci?** Pro ne‑evaluační použití je vyžadována komerční licence Aspose.Drawing.

## Co je **nastavit zarovnání textu** v Aspose.Drawing?

`set text alignment` konfiguruje vodorovné (`StringAlignment`) a svislé (`LineAlignment`) umístění textu v rámci `Rectangle` nebo kreslicí oblasti. Úpravou těchto vlastností určujete, zda se text zobrazí zarovnaný vlevo, na střed, vpravo, nahoře, uprostřed nebo dole, což umožňuje přesné rozvržení v grafice, odznacích a zprávách generovaných pomocí Aspose.Drawing.

## Proč používat Aspose.Drawing pro zarovnání textu?

Aspose.Drawing odstraňuje omezení GDI+, která trápí `System.Drawing.Common`. Podporuje **5 hlavních .NET runtime** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 a .NET 7 – a dokáže vykreslovat obrázky až do **4000 × 4000 px** (≈ 100 MB) bez vyčerpání paměti. Anti‑aliasing, škálování pro vysoké DPI a plná kompatibilita s Linux kontejnery vám umožní generovat pixel‑perfektní grafiku v jakémkoli nasazovacím scénáři.

## Požadavky

1. **Aspose.Drawing Library** – stáhněte ji [zde](https://releases.aspose.com/drawing/net/).  
2. **Vývojové prostředí** – Visual Studio 2022 (nebo jakékoli C# IDE).  
3. **Základní znalosti .NET** – měli byste se dobře orientovat v projektech C# a balíčcích NuGet.

## Importovat jmenné prostory

Pro začátek přidejte požadované jmenné prostory do rozsahu. Ty vám umožní přístup k grafice, vykreslování textu a kreslicím primitivům.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Jak zabránit přetečení textu pomocí Aspose.Drawing?

Bitmap je třída představující obrázek uložený v paměti, zatímco `RectangleF` definuje oblast s plovoucí desetinnou čárkou pro kreslení. Použitím `StringFormat` s nastaveným `Trimming` na `StringTrimming.EllipsisCharacter` jsou nadbytečné znaky automaticky nahrazeny elipsou, což zajišťuje, že text nikdy nepřesáhne hranice obdélníku. Změřením řetězce nejprve můžete rozhodnout, zda zmenšit obdélník nebo rozdělit text do více řádků, čímž získáte čisté rozvržení bez přetečení.

Načtěte bitmapu, definujte vhodně velký `RectangleF` a použijte `StringFormat` s `Trimming` nastaveným na `StringTrimming.EllipsisCharacter`, aby se automaticky ořízl přebytečný text. Pro plnou kontrolu změřte řetězec pomocí `Graphics.MeasureString` a zmenšete obdélník nebo rozdělte text do řádků před kreslením. Tento přístup zaručuje, že žádné znaky nevyčnívají mimo vizuální hranice.

## Krok 1: Vytvořit objekty Bitmap a Graphics

Bitmap představuje obrázek v paměti, zatímco Graphics poskytuje kreslicí metody pro tento bitmap. Vytvoření bitmapy poskytuje plátno, na které můžete kreslit. Objekt `Graphics` je kreslicí povrch a povolíme vysoce kvalitní vykreslování textu pomocí `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Krok 2: Definovat **StringFormat** a stylování

StringFormat specifikuje možnosti rozvržení textu, jako je zarovnání, řádkování a ořezávání. Zde **nastavujeme zarovnání textu** konfigurací instance `StringFormat`. Také připravíme štětce, pera a font, které budou použity při kreslení řetězce.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Krok 3: Vytvořit a formátovat text – **jak nakreslit řetězec** a **nakreslit obdélník s textem**

Graphics.DrawString vykresluje text na plátno a Graphics.DrawRectangle kreslí obdélníkový tvar. Sestavíme text, definujeme obdélník, který jej bude obsahovat, a poté nakreslíme jak okraj obdélníku, tak samotný řetězec.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Jak zacházet s přetečením textu

Pokud dodaný `text` přesahuje hranice obdélníku, máte dvě běžné možnosti:

1. **Zvětšit obdélník** — zvětšete `rectangle.Width` nebo `rectangle.Height`.  
2. **Rozdělit text** — rozdělte řetězec na řádky, které se vejdou, a poté zavolejte `DrawString` pro každý řádek s upravenými Y‑souřadnicemi.

## Jak nakreslit řetězec na obrázek pomocí Aspose.Drawing?

Graphics.DrawString vykresluje zadaný text pomocí fontu a možností formátování. Vytvořte objekt `Graphics` z vaší bitmapy a poté zavolejte `DrawString` s připraveným `StringFormat`. Tento jediný volání vykreslí text přesně tam, kde ho chcete, s ohledem na zarovnání, ořezávání a jakoukoli transformační matici, kterou jste aplikovali. Přidání vysoce kvalitního vykreslovacího tipu zajišťuje, že výstup zůstane ostrý na displejích s vysokým DPI.

## Jak centrovat text v obdélníku?

StringAlignment určuje vodorovné zarovnání textu v rozvrhovém obdélníku. Nastavte `stringFormat.Alignment = StringAlignment.Center` a `stringFormat.LineAlignment = StringAlignment.Center`. Toto vycentruje text vodorovně i svisle uvnitř obdélníku, což je ideální pro odznaky, tlačítka nebo překrytí popisků. Centrované umístění funguje konzistentně napříč různými velikostmi obrázků a nastaveními DPI, poskytující vyvážený vizuální vzhled.

## Jak dosáhnout svislého zarovnání textu?

LineAlignment řídí svislé umístění textu uvnitř obdélníku. Použijte `stringFormat.LineAlignment` s hodnotami `StringAlignment.Near`, `Center` nebo `Far` pro umístění textu nahoře, uprostřed nebo dole v obdélníku. Kombinujte to s `Graphics.TranslateTransform`, pokud potřebujete text otočit a přitom zachovat svislé zarovnání. Úprava řádkového zarovnání zajišťuje, že bloky více řádků jsou přesně tam, kde očekáváte, i po transformacích.

## Krok 4: Uložit výstup – **přidat text k obrázku**

Nakonec zapíšete bitmapu na disk. Tento krok demonstruje **přidání textu k obrázku** v jediném volání.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Běžné problémy a řešení

| Problém | Řešení |
|-------|----------|
| **Text je rozmazaný** | Ujistěte se, že je nastaveno `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;`. |
| **Text je oříznutý** | Zvětšete velikost obdélníku nebo povolte logiku zalamování slov měřením velikosti řetězce (`Graphics.MeasureString`). |
| **Písmo nenalezeno** | Ověřte, že je písmo nainstalováno na hostitelském počítači, nebo vložte soukromé písmo pomocí `PrivateFontCollection`. |
| **Neočekávané barvy** | Zkontrolujte barvy štětců a tužek; pamatujte, že `Color.FromKnownColor` používá systémově definované barvy. |

## Často kladené otázky

**Q1: Je Aspose.Drawing kompatibilní se všemi verzemi .NET?**  
A1: Ano, Aspose.Drawing je navržen tak, aby byl kompatibilní s širokou škálou verzí .NET, což zajišťuje flexibilitu pro vývojáře.

**Q2: Mohu dále přizpůsobit styl písma?**  
A2: Rozhodně! Upravením parametrů objektu `Font` můžete dosáhnout požadované velikosti, stylu a rodiny písma.

**Q3: Jak mohu zacházet s přetečením textu v definovaném obdélníku?**  
A3: Přetečení textu můžete řešit úpravou velikosti obdélníku nebo implementací vlastní logiky pro zpracování dlouhých textů.

**Q4: Existují další možnosti formátování v Aspose.Drawing?**  
A4: Ano, Aspose.Drawing poskytuje komplexní sadu nástrojů pro manipulaci s grafikou, včetně různých možností formátování textu, tvarů a dalších.

**Q5: Kde mohu najít další podporu pro Aspose.Drawing?**  
A5: Prozkoumejte fórum Aspose.Drawing [zde](https://forum.aspose.com/c/drawing/44) pro komunitní podporu a diskuse.

**Další Q&A**

**Q: Jak nakreslím řetězec bez okolního obdélníku?**  
A: Vynechejte volání `DrawRectangle` a předávejte požadovanou polohu `PointF` přímo do `Graphics.DrawString`.

**Q: Mohu otáčet text při zachování zarovnání?**  
A: Ano — aplikujte transformaci `Matrix` na objekt `Graphics` před kreslením a poté ji po vykreslení resetujte.

**Q: Je možné exportovat obrázek jako JPEG místo PNG?**  
A: Jednoduše změňte příponu souboru v `bitmap.Save` a případně specifikujte `ImageFormat.Jpeg`.

**Poslední aktualizace:** 2026-07-17  
**Testováno s:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Související tutoriály

- [Jak nakreslit text pomocí Aspose.Drawing pro .NET](/drawing/net/text-and-fonts/draw-text/)
- [Přidání textu na obrázky v Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [Jak nakreslit text a písma pomocí Aspose.Drawing pro .NET](/drawing/net/text-and-fonts/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}