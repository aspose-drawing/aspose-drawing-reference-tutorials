---
date: 2026-09-23
description: Lär dig hur du ritar text på bild med Aspose.Drawing för .NET. Generera
  bild med text, lägg till text i bitmap, och spara bitmap som PNG med anpassade typsnitt.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Hur man ritar text med Aspose.Drawing
og_description: Lär dig hur du ritar text på bild med Aspose.Drawing för .NET. Den
  här handledningen visar hur du genererar bild med text, lägger till text i bitmap,
  och sparar bitmap som PNG med anpassade typsnitt.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Rita text på bild med Aspose.Drawing för .NET – Snabbguide
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
title: Hur man ritar text på bild med Aspose.Drawing för .NET
url: /sv/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ritar text på bild med Aspose.Drawing för .NET

## Introduktion

I den här steg‑för‑steg‑guiden kommer du att lära dig **hur man ritar text på en bild** med Aspose.Drawing för .NET. Oavsett om du behöver skapa en *dynamisk textbild*, lägga till text på en befintlig bitmap eller generera en grafik med anpassade typsnitt, så går den här handledningen igenom varje detalj så att du kan börja rita text på några minuter. Biblioteket stöder över 30 GDI+-metoder, kör på Windows, Linux och macOS, och har **inga externa beroenden**, vilket gör det till ett pålitligt val för server‑sidig bildgenerering.

## Snabba svar
- **Vilket bibliotek används?** Aspose.Drawing för .NET  
- **Primär uppgift?** Rita text på en bild (skapa bild med text)  
- **Viktig metod?** `Graphics.DrawString` (rita sträng på bild)  
- **Utdataformat?** PNG (spara bitmap som PNG)  
- **Förutsättningar?** .NET‑utvecklingsmiljö och Aspose.Drawing‑bibliotek  

## Vad innebär att rita text med Aspose.Drawing?

Att rita text med Aspose.Drawing betyder att använda bibliotekets GDI+‑kompatibla API för att rendera Unicode‑strängar på en raster‑canvas. Metoden `Graphics.DrawString` skriver texten i en bitmap, vilket låter dig kontrollera typsnitt, färg, justering och anti‑aliasing. Detta tillvägagångssätt låter dig generera högkvalitativa bilder utan att installera System.Drawing.Common.

## Varför använda Aspose.Drawing för att lägga till text på bilder?

Aspose.Drawing erbjuder ett pålitligt, plattformsoberoende sätt att rendera text på bilder utan att behöva inhemska GDI+-bibliotek, vilket ger konsekvent kvalitet och prestanda på alla operativsystem. Det stöder avancerad anti‑aliasing, Unicode‑tecken och anpassade typsnitt, och integreras sömlöst med .NET‑applikationer, vilket gör det idealiskt för server‑sidig bildgenerering och skrivbordsverktyg.

- **Plattformsoberoende pålitlighet** – fungerar på Windows, Linux och macOS.  
- **Avancerad rendering** – anti‑aliasing och sub‑pixel‑textutjämning för skarpt resultat.  
- **Inga externa beroenden** – biblioteket samlar allt du behöver för att *skapa bild med text*.

## Förutsättningar

Innan du dyker ner, se till att du har:

- **Aspose.Drawing för .NET** – ladda ner det från [Aspose.Drawing-dokumentationen](https://reference.aspose.com/drawing/net/).  
- **En .NET‑IDE** såsom Visual Studio eller VS Code.

## Importera namnrymder

Börja med att importera de nödvändiga namnrymderna:

Dessa namnrymder tillhandahåller de grundläggande GDI+-typerna såsom `Bitmap`, `Graphics` och verktyg för textrendering.
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Steg 1: skapa bitmap‑ och grafikobjekt

`Bitmap` är Aspose.Drawings raster‑bildbehållare för pixeldata, och `Graphics` tillhandahåller ritmetoder för att rendera former och text på den.

`Bitmap` representerar en bild i minnet, medan `Graphics` erbjuder ritmetoder för att rendera på den bitmapen.
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Här skapar vi en `Bitmap` som kommer att hålla den slutliga bilden och ett `Graphics`‑objekt som låter oss rita på den. Anti‑aliasing‑hintet säkerställer att texten ser mjuk ut.

## Steg 2: konfigurera pensel, penna och teckensnitt

`Brush` definierar fyllningsfärgen, `Pen` konturerar former, och `Font` specificerar teckensnitt, storlek och stil för textrendering.

`Brush` fyller former med färg, `Pen` konturerar former, och `Font` definierar teckensnittet och storleken för textrendering.
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** definierar textfärgen.  
- **Pen** används senare för att rita en rektangel runt texten (valfritt).  
- **Font** specificerar teckensnitt, storlek och stil för *draw string on image*-operationen.

## Steg 3: definiera text och rektangel

`Rectangle` definierar den avgränsande rutan där texten kommer att placeras, med X/Y‑koordinater samt bredd/höjd.

`Rectangle` anger position och storlek på ett rektangulärt område, som här används för att avgränsa den ritade texten.
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

`Rectangle` bestämmer var texten kommer att placeras. Justera koordinaterna och storleken för att passa din layout.

## Steg 4: rita rektangel och text

`Graphics.DrawString` renderar den angivna texten inom den givna rektangeln med det angivna teckensnittet och penseln.

`Graphics.DrawString` renderar en textsträng inom en specificerad rektangel med det angivna teckensnittet och penseln.
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Först konturerar vi området med en blå rektangel, sedan **lägger vi till text i bitmapen** genom att anropa `DrawString`. Detta är kärnan i *drawing text* på bilden.

## Steg 5: spara resultatet

Bilden sparas som en PNG‑fil, vilket uppfyller kravet *save bitmap as PNG*. Ersätt platshållarens sökväg med den faktiska mappen där du vill lagra filen.

`bitmap.Save` skriver bilden till en fil i det valda formatet, exempelvis PNG.
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Vanliga användningsfall

- **Generera certifikat** med personliga namn.  
- **Skapa vattenmärkta miniatyrbilder** för webbgalerier.  
- **Bygga dynamiska diagram** som inkluderar etiketter eller kommentarer.  

## Felsökning & tips

- **Typsnitt ej hittat?** Se till att typsnittet är installerat på värddatorn eller använd en privat typsnittssamling.  
- **Text avklippt?** Öka rektangelns storlek eller minska typsnittsstorleken.  
- **Prestandaproblem?** Återanvänd samma `Graphics`‑objekt för flera ritoperationer när det är möjligt.  

## Vanliga frågor

**Q: Hur ändrar jag utdataformatet till JPEG?**  
A: Ersätt `.png`‑extensionen med `.jpg` i `Save`‑metoden och ange eventuellt en `ImageCodecInfo` för JPEG‑kvalitet.

**Q: Kan jag rita flerradig text?**  
A: Ja, inkludera radbrytningstecken (`\n`) i strängen eller använd `StringFormat` med `FormatFlags.LineLimit`.

**Q: Finns det ett sätt att mäta textstorlek innan ritning?**  
A: Använd `Graphics.MeasureString` för att få de exakta dimensionerna på den renderade texten.

**Q: Stöder Aspose.Drawing Unicode‑tecken?**  
A: Absolut. Tillhandahåll ett typsnitt som innehåller de nödvändiga glyferna så renderar biblioteket dem korrekt.

**Q: Vilken version av Aspose.Drawing användes för testning?**  
A: Exemplen testades med Aspose.Drawing 24.11 för .NET.

---

**Senast uppdaterad:** 2026-09-23  
**Testad med:** Aspose.Drawing 24.11 för .NET  
**Författare:** Aspose

## Relaterade handledningar

- [Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts in Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [How to save a bitmap as PNG using the Aspose.Drawing API for .NET](/drawing/net/image-editing/display/)
- [Text On Image](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}