---
title: Maateenheden in Aspose.Drawing voor .NET
linktitle: Maateenheden in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternatief voor System.Drawing.Common
description: Ontdek de veelzijdigheid van Aspose.Drawing voor .NET in deze uitgebreide tutorial, waarin je de maateenheden voor nauwkeurige graphics onder de knie krijgt.
type: docs
weight: 14
url: /nl/net/coordinate-transformations/units-of-measure/
---
## Invoering

Welkom in de wereld van Aspose.Drawing voor .NET, waar precisie en flexibiliteit samenkomen bij grafische manipulatie. In deze zelfstudie verdiepen we ons in de fijne kneepjes van de maateenheden binnen Aspose.Drawing, waardoor u stapsgewijze handleiding krijgt om de kracht van deze opmerkelijke bibliotheek te benutten.

## Vereisten

Voordat we ingaan op de tutorial, zorg ervoor dat je aan de volgende vereisten voldoet:

-  Aspose.Drawing voor .NET: Zorg ervoor dat de bibliotheek is geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/drawing/net/).

- Documentmap: Zorg voor een aangewezen map waarin u uw gemaakte documenten wilt opslaan.

- Basiskennis van C#: Een fundamenteel begrip van C# wordt aanbevolen om het meeste uit deze handleiding te halen.

## Naamruimten importeren

Laten we, voordat we beginnen, de benodigde naamruimten importeren om Aspose.Drawing effectief te gebruiken:

```csharp
using System.Drawing;
```

Laten we nu elk voorbeeld in meerdere stappen opsplitsen:

## Punten als maateenheden

1. Een bitmap maken: Initialiseer een bitmap met een opgegeven breedte en hoogte.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Afbeeldingen maken: genereer een grafisch object uit de bitmap om erop te tekenen.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Pagina-eenheid instellen op punten: Definieer punten als maateenheid (1 punt = 1/72 inch).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Rechthoek tekenen: Teken een rechthoek met punten als eenheid.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Millimeters als maateenheden

1. Pagina-eenheid instellen op millimeters: Wijzig de maateenheid in millimeters (1 mm = 1/25,4 inch).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Teken een rechthoek in millimeters: Teken nog een rechthoek met millimeters als eenheid.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Inches als maateenheden

1. Pagina-eenheid instellen op inches: Wijzig de maateenheid naar inches.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Teken een rechthoek in inches: teken een rechthoek met inches als eenheid.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Bewaar het resultaat

Nadat u de voorbeelden hebt voltooid, slaat u de resulterende afbeelding op in uw documentmap:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Nu hebt u met succes door de verschillende maateenheden in Aspose.Drawing voor .NET genavigeerd, waardoor een visuele weergave van rechthoeken is gemaakt met behulp van punten, millimeters en inches.

## Conclusie

In deze zelfstudie hebben we onderzocht hoe Aspose.Drawing voor .NET met verschillende maateenheden omgaat. Door punten, millimeters en inches te manipuleren, kunt u precisie en aanpassingsvermogen in uw grafische creaties bereiken. Experimenteer met deze concepten om het volledige potentieel van Aspose.Drawing te ontsluiten.

## Veelgestelde vragen

### V1: Kan ik Aspose.Drawing voor .NET gebruiken met andere .NET-frameworks?

A1: Ja, Aspose.Drawing is compatibel met verschillende .NET-frameworks en biedt flexibiliteit in uw ontwikkelomgeving.

### Vraag 2: Is er een gratis proefversie beschikbaar?

 A2: Ja, u kunt Aspose.Drawing verkennen met een gratis proefperiode[hier](https://releases.aspose.com/).

### V3: Hoe krijg ik ondersteuning voor Aspose.Drawing voor .NET?

 A3: Bezoek de[Aspose.Tekenforum](https://forum.aspose.com/c/diagram/17) voor gemeenschapsondersteuning en discussies.

### Vraag 4: Kan ik een tijdelijke licentie kopen voor kortetermijnprojecten?

 A4: Ja, u kunt een tijdelijke licentie verkrijgen[hier](https://purchase.aspose.com/temporary-license/).

### V5: Waar kan ik gedetailleerde documentatie voor Aspose.Drawing vinden?

 A5: De uitgebreide documentatie is beschikbaar[hier](https://reference.aspose.com/drawing/net/).