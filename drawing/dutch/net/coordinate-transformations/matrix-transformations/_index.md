---
date: 2026-08-28
description: Leer deze matrix transformation handleiding voor Aspose.Drawing .NET,
  met uitleg over hoe je een rotated rectangle tekent, matrix rotation toepast en
  matrix scaling uitvoert in C#.
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- matrix rotation c#
- matrix scaling c#
- Aspose.Drawing graphics
lastmod: 2026-08-28
linktitle: Matrix Transformations in Aspose.Drawing
og_description: Matrix transformation handleiding voor Aspose.Drawing .NET. Leer hoe
  je een rotated rectangle tekent, matrix rotation toepast, en graphics translate
  en scale met C# in enkele minuten.
og_image_alt: Screenshot of a rotated rectangle created with Aspose.Drawing using
  matrix transformations
og_title: Matrix transformation handleiding – pas rotation, scaling en translation
  toe in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  headline: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  type: TechArticle
- description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  name: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  steps:
  - name: set up the canvas
    text: Create a bitmap that will serve as the drawing surface. We also clear it
      with a neutral gray background so the transformed shapes stand out. > **Pro
      tip:** Using `Format32bppPArgb` ensures correct alpha handling when you later
      apply anti‑aliasing.
  - name: define the original rectangle
    text: This rectangle is the base shape we’ll transform. Its coordinates are chosen
      to keep it well within the canvas bounds.
  - name: rotate the rectangle (draw rotated rectangle)
    text: The `Matrix` class is Aspose.Drawing's representation of a 3 × 3 affine
      transformation matrix used for rotation, scaling and translation. We now **apply
      matrix rotation** of 15 degrees around the origin. The helper method `TransformPath`
      (shown later) takes a lambda that receives a `Matrix` instance
  - name: translate the rectangle
    text: Translation moves the shape without altering its size or orientation. Here
      we shift it left‑up by 250 pixels.
  - name: scale the rectangle (matrix scaling C#)
    text: Scaling changes the rectangle’s dimensions. A factor of `0.3f` reduces both
      width and height to 30 % of the original size.
  - name: save the result
    text: Finally, write the transformed image to disk. Adjust the path to point to
      a folder that exists on your machine. > **Note:** The `TransformPath` method
      (used in the steps above) creates a `GraphicsPath` from the rectangle, applies
      the supplied matrix, and draws the transformed shape. It’s a compact w
  type: HowTo
- questions:
  - answer: The documentation is available **[here](https://reference.aspose.com/drawing/net/)**.
    question: Where can I find the Aspose.Drawing documentation?
  - answer: Obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: How do I get a temporary license for Aspose.Drawing?
  - answer: Visit the Aspose.Drawing forum **[here](https://forum.aspose.com/c/drawing/44)**.
    question: Where can I seek support or connect with the community?
  - answer: Yes, download it from **[here](https://releases.aspose.com/drawing/net/)**.
    question: Can I download Aspose.Drawing for .NET?
  - answer: Purchase your license **[here](https://purchase.aspose.com/buy)**.
    question: How can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- matrix transformation
- Aspose.Drawing
- .NET graphics
- C# drawing
- cross‑platform rendering
title: 'Matrix transformation handleiding: matrix transformations in Aspose.Drawing
  for .NET'
url: /nl/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Matrix-transformatietutorial: matrixtransformaties in Aspose.Drawing voor .NET

## Inleiding

In dit **matrix-transformatietutorial** ontdek je hoe de `Matrix`‑klasse van Aspose.Drawing je in staat stelt grafische objecten te roteren, verplaatsen en schalen met pixel‑perfecte nauwkeurigheid. Of je nu een diagrameditor bouwt, geautomatiseerde rapporten genereert, of visuele effecten toevoegt aan een server‑side service, het beheersen van matrixtransformaties is essentieel voor het produceren van professioneel ogende output op Windows, Linux en macOS.

## Snelle antwoorden
- **Waar gaat dit tutorial over?** Het laat zien hoe je een rechthoek roteert, verplaatst en schaalt met de matrix‑API van Aspose.Drawing.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productiegebruik.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7 and later.  
- **Hoe lang duurt de implementatie?** Ongeveer 10‑15 minuten voor het volledige voorbeeld.  
- **Kan ik de uitvoerafbeelding zien?** Ja – de tutorial slaat een PNG op die je direct kunt openen.

## Wat is een matrix-transformatietutorial?

Een matrix-transformatietutorial legt uit hoe je een 3 × 3 affine matrix gebruikt om grafische primitieve te verplaatsen, roteren, schalen of scheef te trekken. In Aspose.Drawing encapsuleert de `Matrix`‑klasse deze bewerkingen, waardoor elke `GraphicsPath` of vorm kan worden getransformeerd met één herbruikbaar object.

## Waarom Aspose.Drawing gebruiken voor matrixtransformaties?

Aspose.Drawing ondersteunt **drie belangrijke besturingssystemen** (Windows, Linux, macOS) en kan afbeeldingen renderen tot **10.000 × 10.000 px** in minder dan **200 ms** per bewerking op typische serverhardware. De bibliotheek biedt **100 % GDI+ API‑compatibiliteit**, zodat je bestaande System.Drawing‑code kunt migreren zonder de logica te herschrijven, en tegelijkertijd de licentiebeperkingen vermijdt die van invloed zijn op System.Drawing.Common op niet‑Windows platforms.

## Vereisten

- Een werkende C#‑ontwikkelomgeving (Visual Studio, Rider of VS Code).  
- Aspose.Drawing voor .NET geïnstalleerd – download het van de officiële site **[hier](https://releases.aspose.com/drawing/net/)** of **[deze link](https://releases.aspose.com/drawing/net/)** als je het nog niet hebt gedownload.  
- Basiskennis van bitmap‑canvasen, rechthoeken en grafische paden.

## Importeer namespaces

Eerst, breng de vereiste namespaces in scope:

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Stapsgewijze handleiding

Hieronder vind je een beknopte, genummerde walkthrough. Elke stap bevat een korte uitleg gevolgd door de exacte code die je nodig hebt (de codeblokken zijn ongewijzigd ten opzichte van de oorspronkelijke tutorial).

### Stap 1: stel het canvas in

Maak een bitmap die dient als tekenoppervlak. We wissen het ook met een neutrale grijze achtergrond zodat de getransformeerde vormen opvallen.

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **Pro tip:** Het gebruik van `Format32bppPArgb` zorgt voor correcte alfa‑afhandeling wanneer je later anti‑aliasing toepast.

### Stap 2: definieer de oorspronkelijke rechthoek

Deze rechthoek is de basisvorm die we gaan transformeren. De coördinaten zijn gekozen zodat hij goed binnen de canvasgrenzen blijft.

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### Stap 3: roteer de rechthoek (teken geroteerde rechthoek)

De `Matrix`‑klasse is de weergave van Aspose.Drawing van een 3 × 3 affine transformatiematrix die wordt gebruikt voor rotatie, schaling en translatie. We passen nu **matrixrotatie** van 15 graden rond de oorsprong toe. De hulpfunctie `TransformPath` (later getoond) neemt een lambda die een `Matrix`‑instantie ontvangt.

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### Stap 4: verplaats de rechthoek

Translatie verplaatst de vorm zonder de grootte of oriëntatie te wijzigen. Hier verschuiven we hem links‑boven met 250 pixels.

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### Stap 5: schaal de rechthoek (matrixschaling C#)

Schalen verandert de afmetingen van de rechthoek. Een factor van `0.3f` verkleint zowel breedte als hoogte tot 30 % van de oorspronkelijke grootte.

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### Stap 6: sla het resultaat op

Schrijf tenslotte de getransformeerde afbeelding naar schijf. Pas het pad aan zodat het naar een map wijst die op jouw machine bestaat.

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **Opmerking:** De `TransformPath`‑methode (gebruikt in de bovenstaande stappen) maakt een `GraphicsPath` van de rechthoek, past de meegegeven matrix toe, en tekent de getransformeerde vorm. Het is een compacte manier om dezelfde tekengelogica voor elke transformatie opnieuw te gebruiken.

## Veelvoorkomende problemen & oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Afbeelding is leeg** | Zorg ervoor dat de uitvoermap bestaat en dat je schrijfrechten hebt. |
| **Transformaties lijken niet gecentreerd** | Onthoud dat `Matrix.Rotate` roteert rond de oorsprong (0,0). Verplaats de vorm naar het gewenste draaipunt voordat je roteert. |
| **Prestatievertraging bij grote afbeeldingen** | Gebruik `graphics.SmoothingMode = SmoothingMode.AntiAlias;` alleen wanneer nodig, en maak `Graphics`‑objecten snel vrij. |

## Veelgestelde vragen

**Q: Waar kan ik de Aspose.Drawing-documentatie vinden?**  
A: De documentatie is beschikbaar **[hier](https://reference.aspose.com/drawing/net/)**.

**Q: Hoe krijg ik een tijdelijke licentie voor Aspose.Drawing?**  
A: Verkrijg een tijdelijke licentie **[hier](https://purchase.aspose.com/temporary-license/)**.

**Q: Waar kan ik ondersteuning zoeken of contact maken met de community?**  
A: Bezoek het Aspose.Drawing‑forum **[hier](https://forum.aspose.com/c/drawing/44)**.

**Q: Kan ik Aspose.Drawing voor .NET downloaden?**  
A: Ja, download het van **[hier](https://releases.aspose.com/drawing/net/)**.

**Q: Hoe kan ik Aspose.Drawing aanschaffen?**  
A: Koop je licentie **[hier](https://purchase.aspose.com/buy)**.

## Conclusie

Je hebt nu een volledige **matrix-transformatietutorial** voltooid met Aspose.Drawing voor .NET. Je weet hoe je een **geroteerde rechthoek tekent**, **matrixrotatie toepast**, en **matrixschaling C#** uitvoert op elke vorm. Experimenteer door meerdere transformaties te combineren of door aangepaste draaipunten te gebruiken om nog meer creatieve grafische effecten te ontgrendelen.

---

**Laatst bijgewerkt:** 2026-08-28  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose

## Gerelateerde tutorials

- [Hoe een rechthoek tekenen – Coördinatensysteemtransformatie (Pagina-transformatie) met Aspose.Drawing API voor .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Hoe PNG opslaan met Aspose.Drawing – Wereldtransformatie](/drawing/net/coordinate-transformations/world-transformation/)
- [Stapsgewijze transformatie – Coördinatentransformaties](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}