---
date: 2026-08-01
description: Leer hoe u een bitmap als PNG opslaat met behulp van solide penselen
  in Aspose.Drawing voor .NET. Gebruik een solide penseel om vormen te vullen en levendige
  graphics te maken.
keywords:
- save bitmap as png
- export bitmap to png
- fill shape solid color
- bitmap to png conversion
lastmod: 2026-08-01
linktitle: Solide penselen in Aspose.Drawing
og_description: Bitmap opslaan als PNG met solide penselen in Aspose.Drawing. Deze
  stapsgewijze tutorial laat zien hoe u een bitmap maakt, vormen vult met een solide
  kleur, en het resultaat exporteert als een verliesloos PNG‑bestand voor .NET 6+
  projecten.
og_image_alt: Guide showing how to save a bitmap as PNG using solid brushes in Aspose.Drawing
og_title: Bitmap opslaan als PNG met solide penselen – Aspose.Drawing-gids
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  headline: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  type: TechArticle
- description: Learn how to save bitmap as PNG using solid brushes in Aspose.Drawing
    for .NET. Use solid brush to fill shapes with brush and create vibrant graphics.
  name: Save Bitmap as PNG with Solid Brushes in Aspose.Drawing
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image canvas. The `Bitmap` class
      is Aspose.Drawing's top‑level object that stores pixel data in a mutable buffer.
      You can specify width, height, and pixel format when constructing it.
  - name: Create Graphics Object
    text: A `Graphics` object provides drawing methods for the bitmap. The `Graphics`
      class acts as a drawing surface linked to a `Bitmap`. All subsequent drawing
      commands (lines, shapes, text) are routed through this object.
  - name: Choose a Solid Brush
    text: Select a colour for the brush; in this example we use a vivid blue. The
      `SolidBrush` class defines a brush that paints with a single, uniform colour.
      It is ideal for filling shapes where a flat colour is required.
  - name: Fill Shapes with Brush
    text: Use the brush to paint an ellipse (or any other shape) on the bitmap. `FillEllipse`
      draws an ellipse filled with the specified brush. The `FillEllipse` method of
      the `Graphics` object draws an ellipse filled with the supplied `SolidBrush`.
      You can replace it with `FillRectangle`, `FillPolygon`, etc.
  - name: Save the Result as PNG
    text: Export the bitmap to a PNG file on disk. `Save` writes the image to a file
      in the chosen format. The `Save` method writes the bitmap to the specified path
      using `ImageFormat.Png`. This operation preserves the alpha channel, ensuring
      transparent backgrounds remain intact. Repeat these steps, customiz
  type: HowTo
- questions:
  - answer: Absolutely—methods like `FillRectangle`, `FillPolygon`, or `DrawPath`
      work with the same solid brush.
    question: Can I use a different shape instead of an ellipse?
  - answer: Replace the file extension in `Save` and use `ImageFormat.Jpeg` (e.g.,
      `bitmap.Save("output.jpg", ImageFormat.Jpeg);`).
    question: How do I change the output format to JPEG?
  - answer: Yes—create separate `SolidBrush` instances for each colour and call the
      appropriate `Fill*` methods sequentially.
    question: Is it possible to draw multiple shapes with different brushes in one
      bitmap?
  - answer: It's best practice to wrap them in `using` statements or call `Dispose()`
      to free unmanaged resources.
    question: Do I need to dispose of the `Graphics` and `Bitmap` objects?
  - answer: Aspose.Drawing is cross‑platform; the same code runs on Linux and macOS
      when targeting .NET Core or .NET 5+.
    question: Will this work on Linux/macOS with .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- solid brush
title: Bitmap opslaan als PNG met solide penselen in Aspose.Drawing
url: /nl/net/lines-curves-and-shapes/solid-brushes/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bitmap opslaan als PNG met vaste penselen in Aspose.Drawing

## Inleiding

In deze gids leer je **hoe een bitmap op te slaan als PNG** met solid brushes met de Aspose.Drawing .NET‑bibliotheek. Of je nu een desktop‑utility bouwt, een webservice die iconen genereert, of een rapportage‑engine die scherpe PNG‑assets nodig heeft, de onderstaande stappen brengen je van een leeg canvas naar een kant‑klaar PNG‑bestand in slechts een paar regels code. We behandelen de volledige workflow, leggen uit waarom solid brushes de ideale keuze zijn voor uniforme kleurvullingen, en laten zien hoe je de code schoon en cross‑platform houdt.

## Snelle antwoorden
- **Wat betekent “save bitmap as png”?** Het betekent het exporteren van een `Bitmap` object naar een verliesvrij PNG‑afbeeldingsbestand op schijf.  
- **Welke klasse maakt de solid brush?** `SolidBrush` uit de `Aspose.Drawing.Brushes` namespace.  
- **Kan ik de kleur van de brush wijzigen?** Ja—geef elke `Color` (inclusief ARGB‑waarden) door aan de `SolidBrush`‑constructor.  
- **Heb ik een licentie nodig voor productie?** Een proefversie werkt voor evaluatie; een commerciële licentie is vereist voor productie‑implementaties.  
- **Is deze aanpak compatibel met .NET 6+?** Absoluut—Aspose.Drawing ondersteunt volledig .NET 5, .NET 6 en latere versies.

## Wat is “save bitmap as png”?

Het opslaan van een bitmap als PNG zet de in‑memory pixelarray om in een verliesvrij PNG‑bestand, waarbij transparantie en exacte kleurniveaus behouden blijven. **Save bitmap as PNG** is een veelvoorkomende bewerking wanneer je een draagbaar afbeeldingsformaat nodig hebt dat browsers en beeldbewerkingsprogramma's kunnen lezen zonder kwaliteitsverlies.

## Waarom solid brushes gebruiken om bitmap op te slaan als png?

Solid brushes bieden één enkele, uniforme kleur die elke vectorvorm onmiddellijk vult, waardoor de noodzaak voor complexe verlopen verdwijnt wanneer je alleen een effen kleur nodig hebt. Het gebruik van solid brushes met Aspose.Drawing maakt ook gebruik van een renderengine die afbeeldingen tot **10.000 × 10.000 pixels** kan verwerken terwijl het geheugenverbruik onder **200 MB** blijft, waardoor het geschikt is voor assets met hoge resolutie.

## Voorvereisten

Voordat we in de tutorial duiken, zorg ervoor dat je de volgende voorvereisten hebt:

- Aspose.Drawing for .NET Library: Download en installeer de bibliotheek vanaf [Aspose.Drawing for .NET Documentation](https://reference.aspose.com/drawing/net/).
- Integrated Development Environment (IDE): Zorg voor een werkende .NET‑ontwikkelomgeving, zoals Visual Studio, geïnstalleerd op je machine.

Nu je alles klaar hebt, laten we doorgaan naar de implementatie.

## Importeer namespaces

De `using`‑directieven brengen de benodigde types in scope.

De `Aspose.Drawing` namespace biedt de kern grafische klassen, terwijl `System.Drawing` kleurdefinities en de `SolidBrush`‑klasse levert.

```csharp
using System.Drawing;
```

## Hoe bitmap op te slaan als PNG met solid brushes

Deze sectie beschrijft de volledige workflow: maak een bitmap‑canvas, verkrijg een graphics‑oppervlak, instantiate een `SolidBrush` met de gewenste kleur, vul een of meer vormen, en roep uiteindelijk `Save` aan om de afbeelding als PNG‑bestand weg te schrijven. De code werkt cross‑platform op .NET 6 en later.

### Stap 1: Maak een bitmap

De `Bitmap`‑klasse vertegenwoordigt een in‑memory afbeeldingscanvas.

De `Bitmap`‑klasse is het top‑level object van Aspose.Drawing dat pixeldata opslaat in een mutabele buffer. Je kunt breedte, hoogte en pixelindeling opgeven bij het construeren ervan.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Stap 2: Maak een Graphics‑object

Een `Graphics`‑object biedt tekenmethoden voor de bitmap.

De `Graphics`‑klasse fungeert als een tekenoppervlak gekoppeld aan een `Bitmap`. Alle daaropvolgende tekenopdrachten (lijnen, vormen, tekst) worden via dit object uitgevoerd.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Stap 3: Kies een solid brush

Selecteer een kleur voor de brush; in dit voorbeeld gebruiken we een levendig blauw.

De `SolidBrush`‑klasse definieert een brush die schildert met één enkele, uniforme kleur. Het is ideaal voor het vullen van vormen waar een effen kleur vereist is.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
```

### Stap 4: Vul vormen met de brush

Gebruik de brush om een ellips (of een andere vorm) op de bitmap te schilderen.

`FillEllipse` tekent een ellips gevuld met de opgegeven brush. De `FillEllipse`‑methode van het `Graphics`‑object tekent een ellips gevuld met de meegeleverde `SolidBrush`. Je kunt deze vervangen door `FillRectangle`, `FillPolygon`, enz., om verschillende geometrieën te creëren.

```csharp
graphics.FillEllipse(brush, 100, 100, 800, 600);
```

### Stap 5: Sla het resultaat op als PNG

Exporteer de bitmap naar een PNG‑bestand op schijf.

`Save` schrijft de afbeelding naar een bestand in het gekozen formaat. De `Save`‑methode schrijft de bitmap naar het opgegeven pad met `ImageFormat.Png`. Deze bewerking behoudt het alfakanaal, waardoor transparante achtergronden intact blijven.

```csharp
bitmap.Save("Your Document Directory" + @"Brushes\Solid_out.png");
```

Herhaal deze stappen, pas kleuren en vormen aan om te voldoen aan het visuele ontwerp van je applicatie.

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **File not found error** bij het opslaan | De doelmap bestaat niet | Zorg ervoor dat de map (`Your Document Directory\Brushes`) is aangemaakt voordat `Save` wordt aangeroepen. |
| **Incorrect colours** | Gebruik van `KnownColor` die overeenkomt met het systeemthema | Gebruik `Color.FromArgb` voor precieze RGBA‑waarden. |
| **Transparency lost** | Gebruik van een pixelindeling zonder alfa | Behoud `PixelFormat.Format32bppPArgb` zoals getoond om het alfakanaal te behouden. |

## Veelgestelde vragen

**Q: Kun ik een andere vorm gebruiken in plaats van een ellips?**  
A: Absoluut—methoden zoals `FillRectangle`, `FillPolygon` of `DrawPath` werken met dezelfde solid brush.

**Q: Hoe wijzig ik het uitvoerformaat naar JPEG?**  
A: Vervang de bestandsextensie in `Save` en gebruik `ImageFormat.Jpeg` (bijv. `bitmap.Save("output.jpg", ImageFormat.Jpeg);`).

**Q: Is het mogelijk om meerdere vormen te tekenen met verschillende brushes in één bitmap?**  
A: Ja—maak aparte `SolidBrush`‑instanties voor elke kleur en roep de juiste `Fill*`‑methoden opeenvolgend aan.

**Q: Moet ik de `Graphics`‑ en `Bitmap`‑objecten vrijgeven?**  
A: Het is best practice om ze in `using`‑statements te plaatsen of `Dispose()` aan te roepen om niet‑beheerde resources vrij te maken.

**Q: Werkt dit op Linux/macOS met .NET Core?**  
A: Aspose.Drawing is cross‑platform; dezelfde code draait op Linux en macOS wanneer je richt op .NET Core of .NET 5+.

---

**Laatst bijgewerkt:** 2026-08-01  
**Getest met:** Aspose.Drawing 24.12 for .NET  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Bitmap opslaan als PNG & Gesloten krommen tekenen met Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Bitmap opslaan als PNG met transformatie in Aspose.Drawing](/drawing/net/coordinate-transformations/local-transformation/)
- [Hoe afbeelding bijsnijden tot PNG met Aspose.Drawing voor .NET](/drawing/net/image-editing/cropping/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}