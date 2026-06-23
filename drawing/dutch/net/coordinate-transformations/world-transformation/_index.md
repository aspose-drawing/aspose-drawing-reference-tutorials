---
date: 2026-06-23
description: Leer hoe u PNG kunt opslaan met Aspose.Drawing, wereldtransformaties
  toepast en graphics naar PNG converteert. Bevat voorbeelden van translate transform
  in C# en meerdere grafische transformaties.
keywords:
- how to save png
- translate transform c#
- multiple graphics transformations
- convert graphics to png
- how to rotate bitmap
linktitle: Wereldtransformatie in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-06-23'
  description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  headline: How to Save PNG with Aspose.Drawing – World Transformation
  type: TechArticle
- description: Learn how to save PNG using Aspose.Drawing, apply world transformations,
    and convert graphics to PNG. Includes translate transform C# examples and multiple
    graphics transformations.
  name: How to Save PNG with Aspose.Drawing – World Transformation
  steps:
  - name: Create a Bitmap
    text: We start by creating a blank canvas that will hold our drawing. `new Bitmap(width,
      height, PixelFormat.Format32bppPArgb)` creates a 32‑bit per pixel bitmap with
      premultiplied alpha, which is the optimal format for PNG output because it preserves
      transparency without extra conversion steps. - **Why 3
  - name: Set the World Transformation (Graphics Translate Example)
    text: '`TranslateTransform` moves the origin of the coordinate system to a new
      location. `graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)`
      shifts the (0,0) point to the canvas centre. After this call, any shape you
      draw using coordinates (0,0) will appear in the middle of the image. - This'
  - name: Draw a Rectangle Using the Transformed Coordinates
    text: '`DrawRectangle` draws a rectangle using the specified pen and coordinates.
      `graphics.DrawRectangle(pen, -150, -100, 300, 200)` draws a rectangle centered
      on the canvas because its top‑left corner is offset by half its width and height
      from the transformed origin. - The rectangle’s top‑left corner st'
  - name: Save the Result – Convert Graphics to PNG
    text: '`Save` writes the bitmap to a file in the specified image format. `ImageFormat`
      specifies the file format for saving images, such as PNG. `bitmap.Save(outputPath,
      ImageFormat.Png)` writes a lossless PNG file that can be used directly in web
      pages or UI components. - PNG preserves the exact colors an'
  type: HowTo
- questions:
  - answer: Yes – you can chain `TranslateTransform`, `RotateTransform`, and `ScaleTransform`
      to achieve complex effects in a single graphics pipeline.
    question: Can I apply more than one transformation?
  - answer: A free trial is available for evaluation, but a commercial license is
      required for production use.
    question: Is Aspose.Drawing free for commercial projects?
  - answer: Absolutely. Aspose.Drawing supports all modern .NET runtimes, including
      .NET Core, .NET 5, .NET 6, and .NET 7.
    question: Does this work with .NET Core and .NET 5/6/7?
  - answer: The complete documentation is available [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find the full API reference?
  - answer: Verify the path string, ensure write permissions, and confirm the directory
      exists before calling `Save`.
    question: How do I troubleshoot a missing output file?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hoe PNG op te slaan met Aspose.Drawing – Wereldtransformatie
url: /nl/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG opslaan met Aspose.Drawing – Wereldtransformatie

## Bitmap opslaan als PNG – Introductie

**How to save PNG** gebruiken met Aspose.Drawing is een veelvoorkomende eis wanneer je hoogwaardige, transparante afbeeldingen on‑the‑fly moet genereren. In deze tutorial leer je hoe je **bitmap opslaat als PNG**, wereldtransformaties toepast zoals vertalen, roteren en schalen, en uiteindelijk graphics converteert naar PNG — allemaal met schone, onderhoudbare C#‑code. Of je nu een rapportage‑engine, een grafiekcomponent of een aangepaste UI‑renderer bouwt, het beheersen van deze stappen stelt je in staat dynamische afbeeldingen te maken die er op elk apparaat geweldig uitzien.

## Snelle antwoorden
- **Wat betekent “world transformation”?** Het map jouw tekening's logische (wereld) coördinaten naar de pagina (apparaat) coördinaten.  
- **Kan ik het resultaat exporteren als PNG?** Ja – na het tekenen roep je simpelweg `bitmap.Save(...)` aan met een `.png` extensie.  
- **Heb ik een licentie nodig voor Aspose.Drawing?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Is dit compatibel met .NET 6/7?** Absoluut – Aspose.Drawing ondersteunt .NET Framework 4.5+ en .NET Core/5/6/7.  
- **Hoeveel transformaties kan ik achter elkaar toepassen?** Je kunt **meerdere graphics‑transformaties** in volgorde toepassen (vertalen, roteren, schalen, enz.).

## Wat is een World Transformation in Aspose.Drawing?

Een wereldtransformatie wijzigt het coördinatensysteem dat je teken‑commando's gebruiken. Standaard is (0,0) de linkerbovenhoek van de bitmap. Met `TranslateTransform`, `RotateTransform` of `ScaleTransform` kun je die oorsprong verplaatsen, vormen roteren of hun grootte aanpassen zonder de oorspronkelijke geometrie te wijzigen.

## Hoe PNG opslaan met Aspose.Drawing?

Laad een `Bitmap`‑object, stel de gewenste wereldtransformaties in op de `Graphics`‑instantie, teken je vormen, en roep tenslotte `bitmap.Save("output.png", ImageFormat.Png)` aan. Deze één‑regelige opslaan‑aanroep schrijft een verliesvrije PNG‑bestand dat transparantie en kleurnauwkeurigheid behoudt, waardoor het ideaal is voor web‑assets en UI‑overlays.

## Waarom een Graphics Translate‑voorbeeld gebruiken?

Een graphics‑translate‑voorbeeld laat je de teken‑oorsprong één keer verplaatsen in plaats van elk punt opnieuw te berekenen. Deze aanpak vermindert de code‑complexiteit, verbetert de leesbaarheid, en laat de graphics‑engine de matrix‑wiskunde efficiënt afhandelen, wat de render‑prestaties tot wel 30 % kan verhogen op grote canvassen.

## Graphics Translate‑voorbeeld

Een **graphics translate‑voorbeeld** laat zien hoe het verplaatsen van de oorsprong positionering vereenvoudigt. In plaats van elk punt opnieuw te berekenen, verschuif je het coördinatensysteem één keer en teken je alsof de nieuwe oorsprong het midden van het canvas is.

## Vereisten

- **Aspose.Drawing library** geïntegreerd in je .NET‑project – download deze van de officiële [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/).  
- Een **document directory** waar de uitvoer‑afbeelding wordt opgeslagen.  
- Basiskennis van **C#**‑syntaxis en Visual Studio of je favoriete IDE.  

Laten we nu in de code duiken!

## Namespaces importeren

De `Bitmap`, `Graphics` en Aspose‑teken‑hulpmiddelen bevinden zich in deze namespaces.  
**Definitie:** `System.Drawing` levert de kern‑GDI+‑typen, terwijl `Aspose.Drawing` ze uitbreidt met cross‑platform mogelijkheden.

## Stapsgewijze handleiding

### Stap 1: Maak een Bitmap

We beginnen met het maken van een leeg canvas dat onze tekening zal bevatten.

`new Bitmap(width, height, PixelFormat.Format32bppPArgb)` maakt een 32‑bit per pixel bitmap met premultiplied alpha, wat het optimale formaat is voor PNG‑output omdat het transparantie behoudt zonder extra conversiestappen.

- **Waarom 32bppPArgb?** Dit pixel‑formaat ondersteunt alfa‑transparantie en hoogwaardige kleurrendering, perfect voor PNG‑output.  
- **Pro tip:** Pas de breedte/hoogte aan om overeen te komen met de gewenste afbeeldingsgrootte.

### Stap 2: Stel de World Transformation in (Graphics Translate‑voorbeeld)

`TranslateTransform` verplaatst de oorsprong van het coördinatensysteem naar een nieuwe locatie.  
`graphics.TranslateTransform(bitmap.Width / 2, bitmap.Height / 2)` verschuift het (0,0)‑punt naar het midden van het canvas. Na deze aanroep zal elke vorm die je tekent met coördinaten (0,0) in het midden van de afbeelding verschijnen.

- Dit verplaatst het (0,0)‑punt naar (500, 400) – het midden van een 1000 × 800 canvas.  
- Je kunt extra transformaties ketenen: `RotateTransform` roteert het coördinatensysteem, en `ScaleTransform` schaalt het, waardoor **meerdere graphics‑transformaties** mogelijk zijn.

### Stap 3: Teken een rechthoek met de getransformeerde coördinaten

`DrawRectangle` tekent een rechthoek met de opgegeven pen en coördinaten.

`graphics.DrawRectangle(pen, -150, -100, 300, 200)` tekent een rechthoek gecentreerd op het canvas omdat de linkerbovenhoek wordt verschoven met de helft van de breedte en hoogte ten opzichte van de getransformeerde oorsprong.

- De linkerbovenhoek van de rechthoek begint bij de getransformeerde oorsprong (midden van de afbeelding).  
- Voel je vrij om te experimenteren met andere vormen — ellipsen, lijnen of aangepaste paden.

### Stap 4: Sla het resultaat op – Converteer graphics naar PNG

`Save` schrijft de bitmap naar een bestand in het opgegeven afbeeldingsformaat.  
`ImageFormat` geeft het bestandsformaat aan voor het opslaan van afbeeldingen, zoals PNG.

`bitmap.Save(outputPath, ImageFormat.Png)` schrijft een verliesvrij PNG‑bestand dat direct kan worden gebruikt in webpagina's of UI‑componenten.

- PNG behoudt de exacte kleuren en transparantie die we eerder hebben ingesteld.  
- Vervang `"Your Document Directory"` door het daadwerkelijke pad op jouw machine.

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **File not found error** bij het opslaan | De doelmap bestaat niet. | Maak de map programmatically (`Directory.CreateDirectory`) aan voordat `Save` wordt aangeroepen. |
| **Blank image** na transformatie | `TranslateTransform` aangeroepen na het tekenen. | Zorg ervoor dat de transformatie **vóór** alle teken‑commando's wordt ingesteld. |
| **Distorted colors** | Gebruik van een incompatibel pixel‑formaat. | Blijf bij `Format32bppPArgb` voor PNG‑output. |

## Veelgestelde vragen

Q: Kan ik meer dan één transformatie toepassen?  
A: Ja – je kunt `TranslateTransform`, `RotateTransform` en `ScaleTransform` ketenen om complexe effecten te bereiken in één enkele graphics‑pipeline.

Q: Is Aspose.Drawing gratis voor commerciële projecten?  
A: Een gratis proefversie is beschikbaar voor evaluatie, maar een commerciële licentie is vereist voor productiegebruik.

Q: Werkt dit met .NET Core en .NET 5/6/7?  
A: Absoluut. Aspose.Drawing ondersteunt alle moderne .NET‑runtimes, inclusief .NET Core, .NET 5, .NET 6 en .NET 7.

Q: Waar kan ik de volledige API‑referentie vinden?  
A: De volledige documentatie is beschikbaar [hier](https://reference.aspose.com/drawing/net/).

Q: Hoe los ik een ontbrekend uitvoerbestand op?  
A: Controleer de pad‑string, zorg voor schrijfrechten, en bevestig dat de map bestaat voordat `Save` wordt aangeroepen.

## Conclusie

Je hebt nu geleerd **hoe PNG op te slaan** met Aspose.Drawing, een **world transformation** toegepast, en een **graphics translate‑voorbeeld** uitgevoerd dat kan worden uitgebreid met rotatie of schaling. Door deze bouwblokken te beheersen kun je dynamische afbeeldingen genereren, aangepaste grafieken maken, of on‑the‑fly graphics bouwen voor elke .NET‑applicatie.

---

**Laatst bijgewerkt:** 2026-06-23  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose  
**Gerelateerde bronnen:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

```csharp
using System.Drawing;
using Aspose.Drawing;
```

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

## Gerelateerde tutorials

- [Matrix Transformatietutorial: Matrix Transformaties in Aspose.Drawing voor .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Hoe afbeelding te roteren met Aspose.Drawing Global Transformation](/drawing/net/coordinate-transformations/global-transformation/)
- [Coördinatensysteemtransformatie – Paginatransformatie in Aspose.Drawing voor .NET](/drawing/net/coordinate-transformations/page-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}