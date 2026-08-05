---
date: 2026-05-24
description: Leer hoe u een eenheid instelt in Aspose.Drawing voor .NET, grafische
  eenheden eenvoudig converteert en precieze metingen voor graphics rendering onder
  de knie krijgt.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Units of Measure in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hoe een eenheid instellen in Aspose.Drawing voor .NET – Units of Measure
url: /nl/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe een Eenheid Instellen in Aspose.Drawing voor .NET – Eenheden van Maat

## Introductie

Welkom in de wereld van Aspose.Drawing voor .NET, waar precisie en flexibiliteit samenkomen in grafische manipulatie. In deze tutorial ontdek je **hoe een eenheid in te stellen** voor je tekeningen, leer je **grafische eenheden om te zetten** tussen points, millimeters en inches, en zie je praktijkvoorbeelden die je afbeeldingen pixel‑perfect maken. Of je nu rapporten, miniaturen of aangepaste grafieken maakt, het beheersen van eenheden van maat is essentieel voor consistente weergave op verschillende apparaten.

## Snelle Antwoorden
- **Wat is de primaire manier om eenheden te wijzigen?** Roep `graphics.PageUnit = PageUnit.Point` (of `.Millimeter`, `.Inch`) aan op het `Graphics`‑object.  
- **Welke eenheid is gelijk aan 1/72 inch?** Points.  
- **Hoeveel millimeters zitten er in een inch?** 25.4 mm = 1 inch.  
- **Heb ik extra bibliotheken nodig om eenheden te gebruiken?** Nee, de Aspose.Drawing core‑bibliotheek levert alle eenheidsconstanten.  
- **Kan ik eenheden mixen in één afbeelding?** Stel de eenheid één keer in per `Graphics`‑instantie; teken alles met die eenheid voor consistentie.

## Voorwaarden

Voordat we in de tutorial duiken, zorg ervoor dat je de volgende voorwaarden hebt:

- Aspose.Drawing for .NET: Zorg ervoor dat je de bibliotheek geïnstalleerd hebt. Je kunt het downloaden [hier](https://releases.aspose.com/drawing/net/).
- Documentdirectory: Heb een aangewezen map waar je je gemaakte documenten wilt opslaan.
- Basis C#‑kennis: Een fundamenteel begrip van C# wordt aanbevolen om het meeste uit deze gids te halen.

## Namespaces Importeren

Voordat we beginnen, laten we de benodigde namespaces importeren om Aspose.Drawing effectief te gebruiken:

```csharp
using System.Drawing;
```

Laten we nu elk voorbeeld in meerdere stappen opsplitsen:

## Hoe eenheid instellen op Points?

De `Bitmap`‑klasse vertegenwoordigt een in‑memory afbeelding die dient als tekencanvas. Laad je bitmap, maak een `Graphics`‑object aan, en stel de paginanaam in op points — dit vertelt Aspose.Drawing om alle coördinaten te interpreteren als 1/72 inch‑waarden. Het gebruik van points geeft je fijnmazige controle voor print‑klare graphics en laat je lijndiktes met hoge precisie specificeren.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Stap 1: Een Bitmap Maken  
De `Bitmap`‑klasse vertegenwoordigt een in‑memory afbeelding die dient als tekencanvas.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Stap 2: Een Graphics‑object Maken  
`Graphics` biedt tekenmethoden voor het renderen van vormen en tekst op een `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Stap 3: Paginanaam Instellen op Points  
`PageUnit` is een enumeratie die de eenheid van maat voor paginacoördinaten specificeert. `PageUnit.Point` definieert points als de eenheid van maat (1 point = 1/72 inch). Deze instelling geldt voor alle volgende tekenaanroepen.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Stap 4: Een Rechthoek Tekenen in Points  
Wanneer je een rechthoek tekent nadat je de eenheid hebt ingesteld, worden de opgegeven afmetingen geïnterpreteerd als points, wat zorgt voor precieze afmetingen.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Hoe eenheid instellen op Millimeters?

`PageUnit` is een enumeratie die de eenheid van maat voor paginacoördinaten specificeert. Overschakelen naar millimeters is handig wanneer je metrische afmetingen nodig hebt, bijvoorbeeld bij het genereren van technische diagrammen. Aspose.Drawing behandelt 1 mm als 1/25.4 inch, waardoor je graphics kunt afstemmen op fysieke metingen die in de productie en technische documentatie worden gebruikt.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Stap 1: Paginanaam Instellen op Millimeters  
Wijs `PageUnit.Millimeter` toe aan het `Graphics`‑object; alle coördinaten worden nu gekoppeld aan het metrische systeem.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Stap 2: Een Rechthoek Tekenen in Millimeters  
De breedte en hoogte van de rechthoek worden nu uitgedrukt in millimeters, waardoor het eenvoudig is om af te stemmen op fysieke metingen en ervoor te zorgen dat de afgedrukte output overeenkomt met de werkelijke afmetingen.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Hoe eenheid instellen op Inches?

`Graphics` biedt tekenmethoden voor het renderen van vormen en tekst op een `Bitmap`. Inches zijn de standaard eenheid voor veel Amerikaanse ontwerptools. Het instellen van de eenheid op inches laat je in vertrouwde termen denken bij het opmaken van UI‑elementen, en het vereenvoudigt de overgang van schermontwerp naar print waar inches vaak worden gebruikt.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Stap 1: Paginanaam Instellen op Inches  
`PageUnit.Inch` wijzigt het coördinatensysteem zodat 1 eenheid gelijk is aan 1 inch, wat een eenvoudige manier biedt om elementen te dimensioneren voor print‑gerichte lay-outs.

CODE_BLOCK_PLACEHOLDER_10_END

### Stap 2: Een Rechthoek Tekenen in Inches  
Nu gebruikt elke vorm die je tekent inches als meetbasis, wat ideaal is voor print‑lay-outs en voor het communiceren van afmetingen aan belanghebbenden die gewend zijn aan imperiale eenheden.

CODE_BLOCK_PLACEHOLDER_11_END

## Resultaat Opslaan

Na het voltooien van de voorbeelden, sla je de resulterende afbeelding op in je documentdirectory. De `Bitmap.Save`‑methode schrijft het bestand in het formaat dat je opgeeft (PNG, JPEG, enz.).

CODE_BLOCK_PLACEHOLDER_12_END

Nu heb je met succes de verschillende eenheden van maat in Aspose.Drawing voor .NET doorlopen, en een visuele weergave van rechthoeken gemaakt met points, millimeters en inches.

## Waarom het eenheidssysteem van Aspose.Drawing gebruiken?

Aspose.Drawing ondersteunt **30+ beeldformaten** en kan afbeeldingen verwerken tot **5000 × 5000 pixels** zonder het volledige bestand in het geheugen te laden, wat hoge prestaties levert voor grootschalige graphics‑generatie. Door de eenheid expliciet in te stellen, elimineer je giswerk, verminder je conversiefouten, en zorg je ervoor dat je output exact overeenkomt met fysieke afmetingen op alle platformen.

## Veelvoorkomende Problemen en Oplossingen

- **Onverwachte grootte na het opslaan** – Controleer dat je `graphics.PageUnit` **voor** enige tekenaanroepen instelt; het later wijzigen van de eenheid vergroot bestaande vormen niet retroactief.  
- **Vage output op high‑DPI schermen** – Verhoog de resolutie van de bitmap (bijv. `new Bitmap(width, height, 300)`) om overeen te komen met de doel‑DPI.  
- **Gemengde eenheden in één afbeelding** – Maak aparte `Graphics`‑instanties voor elke eenheid of voer handmatige conversie uit vóór het tekenen.

## Veelgestelde Vragen

### V1: Kan ik Aspose.Drawing voor .NET gebruiken met andere .NET‑frameworks?
A1: Ja, Aspose.Drawing is compatibel met verschillende .NET‑frameworks, wat flexibiliteit biedt in je ontwikkelomgeving.

### V2: Is er een gratis proefversie beschikbaar?
A2: Ja, je kunt Aspose.Drawing verkennen met een gratis proefversie [hier](https://releases.aspose.com/).

### V3: Hoe krijg ik ondersteuning voor Aspose.Drawing voor .NET?
A3: Bezoek het [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) voor community‑ondersteuning en discussies.

### V4: Kan ik een tijdelijke licentie aanschaffen voor kortetermijnprojecten?
A4: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

### V5: Waar kan ik gedetailleerde documentatie voor Aspose.Drawing vinden?
A5: De uitgebreide documentatie is beschikbaar [hier](https://reference.aspose.com/drawing/net/).

---

**Laatst Bijgewerkt:** 2026-05-24  
**Getest Met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
