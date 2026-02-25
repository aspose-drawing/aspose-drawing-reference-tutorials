---
date: 2026-02-25
description: Leer hoe u tekstuitlijning instelt in Aspose.Drawing voor .NET en tekst
  toevoegt aan afbeeldingen. Stapsgewijze handleiding met voorbeelden.
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Tekstuitlijning instellen met Aspose.Drawing voor .NET
url: /nl/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tekstuitlijning instellen in Aspose.Drawing

## Introduction

Als het gaat om **set text alignment** en het opmaken van tekst in uw .NET‑toepassingen, is Aspose.Drawing de bibliotheek bij uitstek voor ontwikkelaars die precisie, prestaties en een rijke API‑omgeving nodig hebben. Of u nu een rapportage‑engine, een dynamische badge‑generator of een andere grafisch intensieve oplossing bouwt, de mogelijkheid om te bepalen hoe tekst binnen vormen wordt uitgelijnd, zorgt ervoor dat uw output er gepolijst en professioneel uitziet. In deze tutorial lopen we het volledige proces door — van het maken van een bitmap‑canvas tot het tekenen van een rechthoek met tekst, het afhandelen van overflow en uiteindelijk het opslaan van de afbeelding.

## Quick Answers
- **Wat betekent “set text alignment”?** Het bepaalt hoe tekst horizontaal en verticaal binnen een tekenrechthoek wordt gepositioneerd.  
- **Welke klasse regelt de uitlijning?** `StringFormat` laat u `Alignment` en `LineAlignment` instellen.  
- **Kan ik een string en een rechthoek samen tekenen?** Ja — gebruik `Graphics.DrawRectangle` gevolgd door `Graphics.DrawString`.  
- **Hoe voorkom ik tekst‑overflow?** Pas de grootte van de rechthoek aan of splits de tekst handmatig in meerdere regels.  
- **Heb ik een licentie nodig voor productie?** Een commerciële Aspose.Drawing‑licentie is vereist voor niet‑evaluatiegebruik.

## What is **set text alignment** in Aspose.Drawing?

`set text alignment` verwijst naar de configuratie van horizontale (`StringAlignment`) en verticale (`LineAlignment`) positionering van tekst binnen een `Rectangle` of een willekeurig tekengebied. Door deze instellingen aan te passen, bepaalt u of de tekst links‑uitgelijnd, gecentreerd, rechts‑uitgelijnd, boven‑uitgelijnd, midden‑uitgelijnd of onder‑uitgelijnd verschijnt.

## Why use Aspose.Drawing for text alignment?

- **Volledige .NET‑compatibiliteit** – werkt met .NET Framework, .NET Core en .NET 5/6+.  
- **Pixel‑perfecte weergave** – anti‑aliasing en high‑DPI‑ondersteuning direct beschikbaar.  
- **Geen GDI+ beperkingen** – in tegenstelling tot `System.Drawing.Common` draait Aspose.Drawing op Linux‑containers zonder native afhankelijkheden.  
- **Rijke styling** – combineer lettertypen, penselen, pennen en aangepaste `StringFormat`‑objecten voor geavanceerde lay‑outs.

## Prerequisites

1. **Aspose.Drawing Library** – download deze [hier](https://releases.aspose.com/drawing/net/).  
2. **Ontwikkelomgeving** – Visual Studio 2022 (of een andere C#‑IDE).  
3. **Basis .NET‑kennis** – u moet vertrouwd zijn met C#‑projecten en NuGet‑pakketten.

## Import Namespaces

Om te beginnen, brengt u de benodigde namespaces in scope. Deze geven u toegang tot graphics, tekstweergave en teken‑primitieven.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Step 1: Create Bitmap and Graphics Objects  

Het maken van een bitmap levert een canvas waarop u kunt tekenen. Het `Graphics`‑object is het tekenoppervlak, en we schakelen high‑quality tekstweergave in met `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Step 2: Define **StringFormat** and Styling  

Hier **stellen we tekstuitlijning in** door een `StringFormat`‑instantie te configureren. We bereiden ook penselen, pennen en een lettertype voor die gebruikt zullen worden bij het tekenen van de string.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Step 3: Create and Format Text – **how to draw string** and **draw rectangle with text**

We stellen de tekst samen, definiëren de rechthoek die deze zal bevatten, en tekenen vervolgens zowel de rechthoekrand als de string zelf.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### How to handle text overflow

Als de opgegeven `text` de grenzen van de rechthoek overschrijdt, heeft u twee veelvoorkomende opties:

1. **De rechthoek vergroten** – vergroot `rectangle.Width` of `rectangle.Height`.  
2. **De tekst splitsen** – splits de string in regels die passen, roep vervolgens `DrawString` aan voor elke regel met aangepaste Y‑coördinaten.

## Step 4: Save the Output – **add text to image**

Tot slot schrijft u de bitmap naar schijf. Deze stap demonstreert **add text to image** in één enkele aanroep.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Common Issues and Solutions

| Probleem | Oplossing |
|----------|-----------|
| **Tekst is wazig** | Zorg ervoor dat `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` is ingesteld. |
| **Tekst wordt afgesneden** | Vergroot de grootte van de rechthoek of schakel woord‑wrap‑logica in door de stringgrootte te meten (`Graphics.MeasureString`). |
| **Lettertype niet gevonden** | Controleer of het lettertype is geïnstalleerd op de hostmachine of embed een privé‑lettertype met `PrivateFontCollection`. |
| **Onverwachte kleuren** | Controleer de kleuren van penselen en pennen; onthoud dat `Color.FromKnownColor` systeem‑gedefinieerde kleuren gebruikt. |

## Frequently Asked Questions

### Q1: Is Aspose.Drawing compatibel met alle .NET‑versies?

A1: Ja, Aspose.Drawing is ontworpen om compatibel te zijn met een breed scala aan .NET‑versies, waardoor flexibiliteit voor ontwikkelaars wordt gegarandeerd.

### Q2: Kan ik de lettertype‑stijl verder aanpassen?

A2: Absoluut! Pas de parameters van het `Font`‑object aan om de gewenste lettergrootte, stijl en familie te bereiken.

### Q3: Hoe kan ik tekst‑overflow binnen de gedefinieerde rechthoek afhandelen?

A3: U kunt tekst‑overflow beheren door de grootte van de rechthoek aan te passen of aangepaste logica te implementeren om lange tekst te verwerken.

### Q4: Zijn er andere opmaakopties beschikbaar in Aspose.Drawing?

A4: Ja, Aspose.Drawing biedt een uitgebreide set tools voor grafische manipulatie, inclusief diverse opmaakopties voor tekst, vormen en meer.

### Q5: Waar kan ik extra ondersteuning voor Aspose.Drawing vinden?

A5: Verken het Aspose.Drawing‑forum [hier](https://forum.aspose.com/c/drawing/44) voor community‑ondersteuning en discussies.

**Additional Q&A**

**Q: Hoe teken ik een string zonder een omringende rechthoek?**  
A: Laat de `DrawRectangle`‑aanroep weg en geef de gewenste `PointF`‑locatie door aan `Graphics.DrawString`.

**Q: Kan ik de tekst roteren terwijl ik de uitlijning behoud?**  
A: Ja — pas een `Matrix`‑transformatie toe op het `Graphics`‑object vóór het tekenen, en reset het daarna.

**Q: Is het mogelijk om de afbeelding als JPEG in plaats van PNG te exporteren?**  
A: Verander simpelweg de bestandsextensie in `bitmap.Save` en specificeer eventueel `ImageFormat.Jpeg`.

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}