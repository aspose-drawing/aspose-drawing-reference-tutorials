---
date: 2026-09-23
description: Leer hoe u tekst op een afbeelding kunt tekenen met Aspose.Drawing voor
  .NET. Genereer een afbeelding met tekst, voeg tekst toe aan een bitmap en sla de
  bitmap op als PNG met aangepaste lettertypen.
keywords:
- draw text on image
- generate image with text
- custom font on image
- save bitmap as png
- add text to bitmap
lastmod: 2026-09-23
linktitle: Hoe tekst te tekenen met Aspose.Drawing
og_description: Leer hoe u tekst op een afbeelding kunt tekenen met Aspose.Drawing
  voor .NET. Deze tutorial laat zien hoe u een afbeelding met tekst genereert, tekst
  toevoegt aan een bitmap en de bitmap opslaat als PNG met aangepaste lettertypen.
og_image_alt: Screenshot of a PNG image created with Aspose.Drawing showing custom
  text
og_title: Tekst op afbeelding tekenen met Aspose.Drawing voor .NET – Snelle gids
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
title: Hoe tekst op een afbeelding te tekenen met Aspose.Drawing voor .NET
url: /nl/net/text-and-fonts/draw-text/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe tekst op afbeelding te tekenen met Aspose.Drawing voor .NET

## Introductie

In deze stapsgewijze gids leer je **hoe je tekst op een afbeelding tekent** met Aspose.Drawing voor .NET. Of je nu een *dynamische tekstafbeelding* wilt maken, tekst wilt toevoegen aan een bestaande bitmap, of een grafisch element met aangepaste lettertypen wilt genereren, deze tutorial leidt je door elk detail zodat je binnen enkele minuten tekst kunt tekenen. De bibliotheek ondersteunt meer dan 30 GDI+-methoden, werkt op Windows, Linux en macOS, en heeft **nul externe afhankelijkheden**, waardoor het een betrouwbare keuze is voor server‑side beeldgeneratie.

## Snelle antwoorden
- **Welke bibliotheek wordt gebruikt?** Aspose.Drawing for .NET  
- **Primaire taak?** Tekst op een afbeelding tekenen (afbeelding met tekst maken)  
- **Belangrijke methode?** `Graphics.DrawString` (teken string op afbeelding)  
- **Uitvoerformaat?** PNG (bitmap opslaan als PNG)  
- **Voorvereisten?** .NET-ontwikkelomgeving en Aspose.Drawing-bibliotheek  

## Wat is tekst tekenen met Aspose.Drawing?

Tekst tekenen met Aspose.Drawing betekent dat je de GDI+‑compatibele API van de bibliotheek gebruikt om Unicode‑strings op een rastercanvas weer te geven. De methode `Graphics.DrawString` schrijft de tekst in een bitmap, waardoor je lettertype, kleur, uitlijning en anti‑aliasing kunt regelen. Deze aanpak stelt je in staat om afbeeldingen van hoge kwaliteit te genereren zonder System.Drawing.Common te installeren.

## Waarom Aspose.Drawing gebruiken om tekst aan afbeeldingen toe te voegen?

Aspose.Drawing biedt een betrouwbare, cross‑platform manier om tekst op afbeeldingen weer te geven zonder native GDI+-bibliotheken, en levert consistente kwaliteit en prestaties op elk besturingssysteem. Het ondersteunt geavanceerde anti‑aliasing, Unicode‑tekens en aangepaste lettertypen, en integreert naadloos met .NET‑toepassingen, waardoor het ideaal is voor server‑side beeldgeneratie en desktop‑tools.

- **Cross‑platform betrouwbaarheid** – werkt op Windows, Linux en macOS.  
- **Geavanceerde weergave** – anti‑aliasing en sub‑pixel tekstverzachting voor scherpe output.  
- **Geen externe afhankelijkheden** – de bibliotheek bevat alles wat je nodig hebt om *afbeelding met tekst te maken*.

## Voorvereisten

Voordat je begint, zorg ervoor dat je het volgende hebt:

- **Aspose.Drawing for .NET** – download het van de [Aspose.Drawing documentatie](https://reference.aspose.com/drawing/net/).  
- **Een .NET IDE** zoals Visual Studio of VS Code.

## Namespaces importeren

Begin met het importeren van de vereiste namespaces:

Deze namespaces bieden de kern GDI+-typen zoals `Bitmap`, `Graphics` en hulpprogramma's voor tekstreeksen.
```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Stap 1: bitmap- en graphicsobjecten maken

`Bitmap` is de rasterafbeeldingscontainer van Aspose.Drawing voor pixelgegevens, en `Graphics` levert tekenmethoden om vormen en tekst erop weer te geven.

`Bitmap` vertegenwoordigt een afbeelding in het geheugen, terwijl `Graphics` tekenmethoden biedt om op die bitmap te renderen.
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

Hier maken we een `Bitmap` die de uiteindelijke afbeelding zal bevatten en een `Graphics`‑object waarmee we erop kunnen tekenen. De anti‑aliasing‑hint zorgt ervoor dat de tekst er vloeiend uitziet.

## Stap 2: brush, pen en font instellen

`Brush` bepaalt de vulkleur, `Pen` omlijnt vormen, en `Font` specificeert het lettertype, de grootte en de stijl voor het renderen van tekst.

`Brush` vult vormen met kleur, `Pen` omlijnt vormen, en `Font` bepaalt het lettertype en de grootte voor het renderen van tekst.
```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

- **Brush** bepaalt de tekstkleur.  
- **Pen** wordt later gebruikt om een rechthoek rond de tekst te tekenen (optioneel).  
- **Font** specificeert het lettertype, de grootte en de stijl voor de *draw string on image*‑bewerking.

## Stap 3: tekst en rechthoek definiëren

`Rectangle` definieert de begrenzende doos waar de tekst wordt geplaatst, met X/Y‑coördinaten en breedte/hoogte.

`Rectangle` geeft de positie en grootte van een rechthoekig gebied aan, hier gebruikt om de getekende tekst te begrenzen.
```csharp
string text = "Lorem ipsum..."; // (Your desired text)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
```

De `Rectangle` bepaalt waar de tekst wordt geplaatst. Pas de coördinaten en grootte aan naar jouw lay-out.

## Stap 4: rechthoek en tekst tekenen

`Graphics.DrawString` rendert de opgegeven tekst binnen de gegeven rechthoek met het opgegeven lettertype en de brush.

`Graphics.DrawString` rendert een tekenreeks binnen een gespecificeerde rechthoek met het opgegeven lettertype en de brush.
```csharp
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle);
```

Eerst omlijnen we het gebied met een blauwe rechthoek, daarna **voegen we tekst toe aan de bitmap** door `DrawString` aan te roepen. Dit is de kern van *tekst tekenen* op de afbeelding.

## Stap 5: resultaat opslaan

De afbeelding wordt opgeslagen als een PNG‑bestand, waarmee aan de *save bitmap as PNG*‑vereiste wordt voldaan. Vervang het tijdelijke pad door de daadwerkelijke map waar je het bestand wilt opslaan.

`bitmap.Save` schrijft de afbeelding naar een bestand in het gekozen formaat, zoals PNG.
```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\DrawText_out.png");
```

## Veelvoorkomende gebruikssituaties

- **Certificaten genereren** met gepersonaliseerde namen.  
- **Watermerk-miniaturen maken** voor webgalerijen.  
- **Dynamische grafieken bouwen** die labels of annotaties bevatten.

## Probleemoplossing & tips

- **Lettertype niet gevonden?** Zorg ervoor dat het lettertype op de hostmachine is geïnstalleerd of gebruik een private font‑collectie.  
- **Tekst afgekapt?** Vergroot de rechthoek of verklein de lettergrootte.  
- **Prestatiezorgen?** Hergebruik hetzelfde `Graphics`‑object voor meerdere tekenbewerkingen wanneer mogelijk.

## Veelgestelde vragen

**V: Hoe wijzig ik het uitvoerformaat naar JPEG?**  
A: Vervang de `.png`‑extensie door `.jpg` in de `Save`‑methode en specificeer eventueel een `ImageCodecInfo` voor JPEG‑kwaliteit.

**V: Kan ik meerregelige tekst tekenen?**  
A: Ja, voeg regeleinde‑tekens (`\n`) toe aan de string of gebruik `StringFormat` met `FormatFlags.LineLimit`.

**V: Is er een manier om de tekstgrootte te meten vóór het tekenen?**  
A: Gebruik `Graphics.MeasureString` om de exacte afmetingen van de gerenderde tekst te krijgen.

**V: Ondersteunt Aspose.Drawing Unicode‑tekens?**  
A: Absoluut. Lever een lettertype dat de benodigde glyphs bevat en de bibliotheek zal ze correct renderen.

**V: Welke versie van Aspose.Drawing werd gebruikt voor testen?**  
A: De voorbeelden zijn getest met Aspose.Drawing 24.11 voor .NET.

---

**Laatst bijgewerkt:** 2026-09-23  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Bitmap Graphics maken C# – PNG-afbeelding opslaan en werken met geïnstalleerde lettertypen in Aspose.Drawing](/drawing/net/text-and-fonts/installed-fonts/)
- [Hoe een bitmap opslaan als PNG met de Aspose.Drawing API voor .NET](/drawing/net/image-editing/display/)
- [Tekst op afbeelding](/drawing/net/use-cases/text-on-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}