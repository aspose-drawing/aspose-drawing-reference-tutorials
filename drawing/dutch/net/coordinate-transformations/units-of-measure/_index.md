---
date: 2026-02-04
description: Leer hoe u een bitmap maakt met Aspose.Drawing voor .NET, een rechthoek
  tekent met punten en de meeteenheden onder de knie krijgt voor nauwkeurige graphics.
linktitle: Units of Measure in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Bitmap maken met Aspose.Drawing – Eenheden van meting
url: /nl/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maak een bitmap met Aspose.Drawing – Eenheden van Maat

## Inleiding

In deze tutorial **maak je een bitmap met Aspose.Drawing** voor .NET en verken je hoe verschillende eenheden van maat je tekeningen beïnvloeden. We lopen door het tekenen van rechthoeken met punten, millimeters en inches, zodat je de juiste eenheid kunt kiezen voor elke grafisch intensieve situatie. Aan het einde kun je gemakkelijk tussen eenheden schakelen en pixel‑perfecte afbeeldingen produceren.

## Snelle Antwoorden
- **Wat is het primaire doel van deze gids?** Om te laten zien hoe je een bitmap maakt met Aspose.Drawing en vormen tekent met verschillende eenheden van maat.  
- **Welke eenheden worden gedemonstreerd?** Punten, millimeters en inches.  
- **Heb ik een licentie nodig om de voorbeelden uit te voeren?** Een gratis proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productie.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Waar kan ik Aspose.Drawing downloaden?** Van de officiële downloadpagina die hieronder is gelinkt.

## Wat is “bitmap maken met Aspose.Drawing”?
Een bitmap maken met Aspose.Drawing betekent het instantieren van een `Bitmap`‑object waarop je kunt tekenen met de Aspose.Drawing graphics‑API. In tegenstelling tot System.Drawing werkt Aspose.Drawing consistent op alle .NET‑platformen.

## Waarom verschillende eenheden van maat gebruiken?
De juiste eenheid kiezen (punten, millimeters, inches) stelt je in staat grafische elementen af te stemmen op echte afmetingen, waardoor het eenvoudiger wordt om tekeningen te integreren in gedrukte media, PDF‑bestanden of UI‑lay-outs waar fysieke afmetingen van belang zijn.

## Vereisten

- **Aspose.Drawing voor .NET** – download het [hier](https://releases.aspose.com/drawing/net/).  
- **Documentmap** – een map op je computer waar de gegenereerde afbeelding wordt opgeslagen.  
- **Basiskennis van C#** – bekendheid met klassen, objecten en methode‑aanroepen.

## Namespaces importeren

Eerst importeer je de essentiële namespace zodat je met de tekenobjecten kunt werken:

```csharp
using System.Drawing;
```

## Bitmap maken met Aspose.Drawing – Eenheden van Maat begrijpen

### Stap 1: Een bitmap maken

We beginnen met het maken van een bitmap van 1000 × 800 pixels die als ons canvas dient.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Stap 2: Een Graphics‑object maken

Het `Graphics`‑object geeft ons tekenmogelijkheden op de bitmap.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Rechthoek tekenen met punten

Punten zijn een traditionele drukeenheid (1 punt = 1/72 inch). Het instellen van de paginanaam op punten stelt je in staat te werken met vertrouwde typografische maten.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

Teken nu een rechthoek met punten. De penbreedte is ingesteld op 36 punten (½ inch) voor duidelijke zichtbaarheid.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

**Pro tip:** De coördinaten `(72,72)` komen overeen met een offset van 1 inch vanaf de linkerbovenhoek omdat 72 punten = 1 inch.

## Rechthoek tekenen in millimeters

Millimeters zijn ideaal voor technische tekeningen of wanneer je metrische precisie nodig hebt.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

De volgende rechthoek gebruikt een pen van 6,35 mm (gelijk aan 0,25 mm) en een zijde van 25,4 mm (1 inch).

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Rechthoek tekenen in inches

Inches zijn gebruikelijk in Amerikaanse drukwerk en UI‑ontwerp. Overschakelen naar inches maakt het eenvoudig om af te stemmen op de DPI‑instellingen van het scherm.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

Hier tekenen we een blauwe rechthoek met een dunne pen van 0,125 inch.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Het resultaat opslaan

Na het tekenen van alle vormen, sla je de bitmap op in het bestandssysteem. Pas het pad aan zodat het overeenkomt met je documentmap.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Wanneer je de opgeslagen PNG opent, zie je drie rechthoeken—elk gerenderd met een andere eenheid van maat.

## Veelvoorkomende problemen & oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Afbeelding is leeg** | Graphics‑object niet geflusht vóór het opslaan. | Roep `graphics.Dispose();` aan vóór `bitmap.Save()`. |
| **Onjuiste afmetingen** | Verkeerde `PageUnit`‑waarde. | Controleer of je `graphics.PageUnit` hebt ingesteld op de gewenste `GraphicsUnit`. |
| **Fout in bestandspad** | Ontbrekende map of ongeldige tekens. | Zorg dat de doelmap bestaat en gebruik `Path.Combine`. |

## Veelgestelde vragen

### Q1: Kan ik Aspose.Drawing voor .NET gebruiken met andere .NET‑frameworks?

A1: Ja, Aspose.Drawing is compatibel met verschillende .NET‑frameworks, wat flexibiliteit biedt in je ontwikkelomgeving.

### Q2: Is er een gratis proefversie beschikbaar?

A2: Ja, je kunt Aspose.Drawing verkennen met een gratis proefversie [hier](https://releases.aspose.com/).

### Q3: Hoe krijg ik ondersteuning voor Aspose.Drawing voor .NET?

A3: Bezoek het [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) voor community‑ondersteuning en discussies.

### Q4: Kan ik een tijdelijke licentie aanschaffen voor kortlopende projecten?

A4: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

### Q5: Waar vind ik gedetailleerde documentatie voor Aspose.Drawing?

A5: De uitgebreide documentatie is beschikbaar [hier](https://reference.aspose.com/drawing/net/).

## Veelgestelde vragen

**Q: Ondersteunt Aspose.Drawing rendering met hoge DPI?**  
A: Absoluut. De bibliotheek respecteert de DPI‑instellingen van de bitmap, waardoor er scherpe output ontstaat op hoge‑resolutie displays.

**Q: Kan ik meerdere eenheden combineren in één tekening?**  
A: Je kunt `Graphics.PageUnit` op elk moment wijzigen, maar houd de huidige eenheid bij om mismatches in afmetingen te voorkomen.

**Q: Is anti‑aliasing standaard ingeschakeld?**  
A: Ja, Aspose.Drawing past anti‑aliasing toe op vormen en tekst, tenzij je dit expliciet uitschakelt via `graphics.SmoothingMode`.

**Q: Hoe kan ik bronnen vrijgeven na het tekenen?**  
A: Roep `graphics.Dispose();` en `bitmap.Dispose();` aan wanneer je klaar bent om ongeheugeld geheugen vrij te maken.

**Q: Kan ik de bitmap exporteren naar andere formaten dan PNG?**  
A: De `Bitmap.Save`‑methode ondersteunt JPEG, BMP, GIF en TIFF—verander gewoon de bestandsextensie.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2026-02-04  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose