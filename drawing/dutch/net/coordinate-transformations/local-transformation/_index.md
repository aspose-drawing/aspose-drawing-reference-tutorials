---
date: 2026-04-22
description: Leer hoe je een bitmap als PNG opslaat met Aspose.Drawing voor .NET met
  een voorbeeld van een transformatiematrix. Stapsgewijze handleiding met codevoorbeelden.
keywords:
- save bitmap as png
- transformation matrix example
- draw rotated ellipse
- convert graphics to png
- high-quality png output
linktitle: Lokale transformatie in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Bitmap opslaan als PNG met behulp van transformatie in Aspose.Drawing
url: /nl/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bitmap opslaan als PNG met transformatie in Aspose.Drawing

## Inleiding

Als u **bitmap als PNG wilt opslaan** terwijl u een lokale transformatie toepast op graphics binnen een .NET‑applicatie, maakt Aspose.Drawing het proces eenvoudig en betrouwbaar. In deze tutorial ziet u precies hoe u een transformatie‑matrix op een vorm toepast, het resultaat rendert en uiteindelijk **graphics naar PNG converteert** voor opslag of verdere verwerking. Aan het einde heeft u een herbruikbaar code‑patroon dat u kunt aanpassen aan elke lokale transformatiesituatie.

## Snelle antwoorden
- **Wat is een lokale transformatie?** Het is een matrix‑gebaseerde bewerking (roteren, schalen, verplaatsen, scheefzetten) die wordt toegepast op een specifiek tekenelement zonder het hele canvas te beïnvloeden.  
- **Welke bibliotheek ondersteunt dit in .NET?** Aspose.Drawing voor .NET biedt een volledig uitgeruste API die werkt op alle ondersteunde .NET‑versies.  
- **Kan ik het resultaat opslaan als PNG?** Ja—roep eenvoudig `Bitmap.Save` aan met een “.png” bestandsnaam, en Aspose.Drawing verzorgt de conversie.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productiegebruik.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisvoorbeeld.

## Hoe bitmap opslaan als PNG

Hieronder vindt u een volledige, stap‑voor‑stap walkthrough die een **transformatie‑matrixvoorbeeld** demonstreert en eindigt met een PNG‑output van hoge kwaliteit.

## Wat betekent “hoe transformatie toe te passen” in graphics‑programmering?

Een transformatie toepassen betekent het coördinatensysteem van een tekenobject wijzigen met behulp van een **Matrix**. De matrix bepaalt hoe punten worden geroteerd, geschaald of verplaatst, waardoor u met minimale code geavanceerde visuele effecten kunt creëren.

## Waarom Aspose.Drawing gebruiken om **graphics naar PNG te converteren**?
- **Cross‑platform**: Werkt op .NET Framework, .NET Core en .NET 5/6+.  
- **No GDI+ dependencies**: Vermijdt de valkuilen van `System.Drawing.Common` op niet‑Windows platforms.  
- **High‑quality PNG output**: Anti‑aliasing en pixel‑perfecte rendering voor PNG‑bestanden.  
- **Rich API**: Volledige ondersteuning voor paden, pennen, penselen en transformatie‑matrices.

## Vereisten

Before you start, make sure you have:

1. **Aspose.Drawing for .NET** – download en installeer vanaf de [download link](https://releases.aspose.com/drawing/net/).  
2. Een map op uw computer waar de uitvoerafbeelding wordt opgeslagen (bijv. `C:\MyImages\`).  
3. Basiskennis van C# en .NET‑projectopzet.

## Namespaces importeren

First, bring the required namespaces into your C# file:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Stapsgewijze gids

### Stap 1: Een bitmap maken

We beginnen met een leeg canvas. De bitmapgrootte en pixelindeling zijn gekozen om ons een afbeelding van hoge kwaliteit, 32‑bit, te geven die alfa‑transparantie ondersteunt.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Pro tip:** Het gebruik van `Format32bppPArgb` zorgt ervoor dat de afbeelding premultiplied alfa behoudt, wat ideaal is voor PNG‑output.

### Stap 2: Een Graphics‑object maken

Een `Graphics`‑object biedt tekenmethoden die op de bitmap werken. We maken de achtergrond heldergrijs zodat de getransformeerde vorm opvalt.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Stap 3: Een GraphicsPath maken

Een `GraphicsPath` stelt u in staat complexe vormen te definiëren. Hier voegen we een ellips toe op positie (300, 300) met een breedte van 400 en een hoogte van 200 – effectief **een geroteerde ellips tekenen** na de transformatie.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### Stap 4: Lokale transformatie toepassen (Transformatie‑matrixvoorbeeld)

Nu beantwoorden we de kernvraag: **hoe transformatie toe te passen**. We maken een `Matrix`, roteren deze 45° rond het centrum van de ellips (500, 400), en passen de matrix toe op het pad.

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **Waarom rond het centrum roteren?** Roteren rond het centrum van de vorm voorkomt dat deze om de oorsprong draait, wat een natuurlijke uitstraling geeft.

### Stap 5: Het getransformeerde pad tekenen

Met de transformatie toegepast, renderen we het pad met een blauwe pen van dikte 2. Deze stap tekent effectief **een geroteerde ellips** op het canvas.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### Stap 6: Het getransformeerde beeld opslaan (Graphics naar PNG converteren)

Tot slot slaan we de bitmap op als een PNG‑bestand. Het pad combineert uw gekozen map met een submap voor transformatie‑voorbeelden.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **Opmerking:** De `.png`‑extensie activeert automatisch de PNG‑encoder van Aspose.Drawing, waardoor aan de **bitmap opslaan als png**‑vereiste wordt voldaan.

## Veelvoorkomende problemen & oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Lege uitvoerafbeelding** | Graphics niet gewist of penkleur komt overeen met de achtergrond | Roep `graphics.Clear` aan met een contrasterende kleur en zorg ervoor dat de penkleur zichtbaar is. |
| **Vervormde rotatie** | `Rotate` gebruiken in plaats van `RotateAt` | Gebruik `RotateAt` en specificeer het middelpunt van de vorm. |
| **Bestand niet opgeslagen** | Ongeldig mappad of ontbrekende schrijfrechten | Controleer of de map bestaat en de applicatie schrijfrechten heeft. |
| **PNG ziet er wazig uit** | Lage DPI-instelling op de bitmap | Maak de bitmap met een hogere resolutie of stel `graphics.SmoothingMode = SmoothingMode.AntiAlias` in. |

## Veelgestelde vragen

**Q: Kan ik meerdere transformaties combineren (bijv. schalen en dan roteren)?**  
A: Ja. Maak één enkele `Matrix` en roep methoden zoals `Scale`, `RotateAt` en `Translate` aan in de gewenste volgorde, en pas deze toe met `path.Transform(matrix);`.

**Q: Is Aspose.Drawing geschikt voor high‑performance rendering?**  
A: Absoluut. De bibliotheek is geoptimaliseerd voor zowel snelheid als kwaliteit, en vermijdt de GDI+ beperkingen op niet‑Windows platforms.

**Q: Welke andere transformatietypen worden ondersteund?**  
A: Naast rotatie kunt u translatie, schaling en scheefzetten uitvoeren met dezelfde `Matrix`‑klasse.

**Q: Hoe ga ik om met uitzonderingen tijdens het transformatieproces?**  
A: Plaats de tekencode in een `try‑catch`‑blok en inspecteer `System.Drawing.Drawing2D`‑uitzonderingen. Raadpleeg de officiële [Aspose.Drawing documentatie](https://reference.aspose.com/drawing/net/) voor gedetailleerde richtlijnen over foutafhandeling.

**Q: Kan ik Aspose.Drawing uitproberen voordat ik koop?**  
A: Ja, een volledig functionele gratis proefversie is beschikbaar via de [download link](https://releases.aspose.com/drawing/net/).

## Conclusie

Door deze gids te volgen weet u nu **hoe bitmap als PNG op te slaan** na het toepassen van een lokale transformatie met Aspose.Drawing voor .NET. Hetzelfde patroon kan worden hergebruikt voor schalen, vertalen of scheefzetten van elke vorm, waardoor u rijke, interactieve visuele componenten in uw applicaties kunt bouwen en tegelijkertijd PNG‑output van hoge kwaliteit levert.

---

**Laatst bijgewerkt:** 2026-04-22  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}