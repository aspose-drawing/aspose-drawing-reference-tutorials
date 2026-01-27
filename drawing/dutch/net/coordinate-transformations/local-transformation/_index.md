---
date: 2026-01-27
description: Leer hoe u een ellips roteert en graphics converteert naar PNG met Aspose.Drawing
  voor .NET. Stapsgewijze handleiding met codevoorbeelden.
linktitle: Local Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 'Hoe een ellips te roteren: lokale transformatie in Aspose.Drawing voor .NET'
url: /nl/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een ellips te roteren: Lokale transformatie in Aspose.Drawing voor .NET

## Introductie

Als u een **ellipse wilt roteren** binnen een .NET‑applicatie, biedt Aspose.Drawing een eenvoudige en betrouwbare manier om dit te doen. In deze tutorial leert u **hoe u een ellips roteert** met behulp van een transformatie‑matrix, het resultaat rendert, en uiteindelijk **grafische afbeeldingen naar PNG converteert** voor opslag of verdere verwerking. Aan het einde heeft u een herbruikbaar patroon dat werkt voor elke lokale transformatiescenario.

## Snelle antwoorden
- **Wat is een lokale transformatie?** Het is een matrix‑gebaseerde bewerking (roteren, schalen, verplaatsen, scheefzetten) die wordt toegepast op een specifiek tekenelement zonder het hele canvas te beïnvloeden.  
- **Welke bibliotheek ondersteunt dit in .NET?** Aspose.Drawing voor .NET biedt een volledig uitgeruste API die werkt op alle ondersteunde .NET‑versies.  
- **Kan ik het resultaat opslaan als PNG?** Ja—roep simpelweg `Bitmap.Save` aan met een “.png” bestandsnaam, en Aspose.Drawing verzorgt de conversie.  
- **Heb ik een licentie nodig voor ontwikkeling?** Een gratis proefversie werkt voor testen; een commerciële licentie is vereist voor productiegebruik.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor een basisvoorbeeld.

## Hoe een ellips roteren met Aspose.Drawing

Een ellips roteren is in wezen **een vorm roteren met een matrix**. U maakt een `Matrix`, stelt de rotatiehoek in, specificeert het middelpunt van de ellips, en past vervolgens die matrix toe op de `GraphicsPath`. Hierdoor blijft de rotatie gelokaliseerd tot de ellips terwijl de rest van het canvas ongewijzigd blijft.

## Wat betekent “transformatie toepassen” in graphics‑programmering?

Een transformatie toepassen betekent het coördinatensysteem van een tekenobject wijzigen met behulp van een **Matrix**. De matrix bepaalt hoe punten worden geroteerd, geschaald of verplaatst, waardoor u met minimale code geavanceerde visuele effecten kunt creëren.

## Waarom Aspose.Drawing gebruiken om **grafische afbeeldingen naar PNG te converteren**?

- **Cross‑platform**: Werkt op .NET Framework, .NET Core en .NET 5/6+.  
- **Geen GDI+ afhankelijkheden**: Vermijdt de valkuilen van `System.Drawing.Common` op niet‑Windows platformen.  
- **Hoogwaardige rendering**: Anti‑aliasing en pixel‑perfecte output voor PNG‑bestanden.  
- **Rijke API**: Volledige ondersteuning voor paden, pennen, penselen en transformatie‑matrices.

## Vereisten

Voordat u begint, zorg ervoor dat u het volgende heeft:

1. **Aspose.Drawing voor .NET** – download en installeer vanaf de [download link](https://releases.aspose.com/drawing/net/).  
2. Een map op uw computer waar de uitvoerafbeelding wordt opgeslagen (bijv. `C:\MyImages\`).  
3. Basiskennis van C# en .NET projectconfiguratie.  

## Namespaces importeren

Eerst brengt u de vereiste namespaces in uw C#‑bestand:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Deze namespaces geven u toegang tot de klassen `Bitmap`, `Graphics`, `GraphicsPath` en `Matrix` die nodig zijn voor de transformatie‑workflow.

## Stapsgewijze handleiding

### Stap 1: Een Bitmap maken

We beginnen met een leeg canvas. De bitmap‑grootte en pixelindeling zijn gekozen om ons een hoogwaardige, 32‑bit afbeelding te geven die alfa‑transparantie ondersteunt.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Pro tip:** Het gebruik van `Format32bppPArgb` zorgt ervoor dat de afbeelding premultiplied alfa behoudt, wat ideaal is voor PNG‑output.

### Stap 2: Een Graphics‑object maken

Een `Graphics`‑object biedt tekenmethoden die op de bitmap werken. We wissen de achtergrond naar een neutraal grijs zodat de getransformeerde vorm opvalt.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Stap 3: Een GraphicsPath maken

Een `GraphicsPath` stelt u in staat complexe vormen te definiëren. Hier voegen we een ellips toe gepositioneerd op (300, 300) met een breedte van 400 en een hoogte van 200.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### Stap 4: Lokale transformatie toepassen (vorm roteren met matrix)

Nu beantwoorden we de kernvraag: **hoe een ellips roteren**. We maken een `Matrix`, roteren deze 45° rond het middelpunt van de ellips (500, 400), en passen de matrix toe op het pad.

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **Waarom roteren rond een punt?** Roteren rond het midden van de vorm voorkomt dat deze om de oorsprong draait, wat een natuurlijke uitstraling geeft.

### Stap 5: Het getransformeerde pad tekenen

Met de transformatie toegepast, renderen we het pad met een blauwe pen van dikte 2.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### Stap 6: Het getransformeerde beeld opslaan (grafische afbeeldingen naar PNG converteren)

Tot slot slaan we de bitmap op als een PNG‑bestand. Het pad combineert uw gekozen directory met een submap voor transformatie‑voorbeelden.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **Opmerking:** Deze regel toont ook hoe u **bitmap als PNG opslaat**. De `.png` extensie activeert automatisch de PNG‑encoder van Aspose.Drawing, waarmee aan de **grafische afbeeldingen naar PNG converteren**‑vereiste wordt voldaan.

## Veelvoorkomende problemen & oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Lege uitvoerafbeelding** | Graphics niet gewist of penkleur komt overeen met achtergrond | Roep `graphics.Clear` aan met een contrasterende kleur en zorg dat de penkleur zichtbaar is. |
| **Vervormde rotatie** | `Rotate` gebruikt in plaats van `RotateAt` | Gebruik `RotateAt` en specificeer het middelpunt van de vorm. |
| **Bestand niet opgeslagen** | Ongeldig directory‑pad of ontbrekende schrijfrechten | Controleer of de directory bestaat en de applicatie schrijfrechten heeft. |
| **PNG ziet er wazig uit** | Lage DPI‑instelling op de bitmap | Maak de bitmap met een hogere resolutie of stel `graphics.SmoothingMode = SmoothingMode.AntiAlias` in. |

## Veelgestelde vragen

**V:** Kan ik meerdere transformaties combineren (bijv. schalen dan roteren)?  
**A:** Ja. Maak één `Matrix` en roep methoden aan zoals `Scale`, `RotateAt` en `Translate` in de gewenste volgorde, en pas deze vervolgens toe met `path.Transform(matrix);`.

**V:** Is Aspose.Drawing geschikt voor high‑performance rendering?  
**A:** Absoluut. De bibliotheek is geoptimaliseerd voor zowel snelheid als kwaliteit, en vermijdt de GDI+ beperkingen op niet‑Windows platformen.

**V:** Welke andere transformatietypen worden ondersteund?  
**A:** Naast rotatie kunt u translatie, schaling en scheefzetten uitvoeren met dezelfde `Matrix`‑klasse.

**V:** Hoe ga ik om met uitzonderingen tijdens het transformatieproces?  
**A:** Plaats de tekencode in een `try‑catch`‑blok en inspecteer `System.Drawing.Drawing2D`‑uitzonderingen. Raadpleeg de officiële [Aspose.Drawing documentatie](https://reference.aspose.com/drawing/net/) voor gedetailleerde foutafhandelingsrichtlijnen.

**V:** Kan ik Aspose.Drawing uitproberen voordat ik koop?  
**A:** Ja, een volledig functionele gratis proefversie is beschikbaar via de [gratis proefversie](https://releases.aspose.com/) link.

## Conclusie

Door deze gids te volgen weet u nu **hoe u een ellips roteert** met Aspose.Drawing voor .NET en hoe u **grafische afbeeldingen naar PNG converteert** voor permanente opslag. Hetzelfde patroon kan worden hergebruikt voor schalen, vertalen of scheefzetten van elke vorm, waardoor u rijke, interactieve visuele componenten in uw applicaties kunt bouwen.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-27  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

---