---
date: 2026-05-29
description: Leer hoe u PNG kunt opslaan en cardinal splines kunt tekenen in .NET
  met Aspose.Drawing. Sla de curve op als PNG, maak vloeiende graphics en genereer
  moeiteloos een bitmap naar een bestand.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Cardinal Splines tekenen in Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hoe PNG op te slaan en Cardinal Splines te tekenen met Aspose.Drawing
url: /nl/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe PNG op te slaan en Cardinal Splines te tekenen met Aspose.Drawing

## Inleiding

In deze tutorial ontdek je **how to save PNG** bestanden terwijl je vloeiende cardinal splines tekent met Aspose.Drawing voor .NET. Of je nu een chart‑component bouwt, een diagrameditor, of simpelweg een aangepaste curve als PNG wilt exporteren, de onderstaande stappen leiden je door het maken van een bitmap‑canvas, het tekenen van een spline met een pen, en het opslaan van het resultaat op schijf. Je ziet ook waarom Aspose.Drawing een betrouwbare cross‑platform alternatief is voor System.Drawing.Common.

## Snelle antwoorden
- **Wat doet de primaire methode?** `Graphics.DrawCurve` interpoleert een reeks punten tot een vloeiende cardinal spline.  
- **Welk formaat wordt gebruikt om de afbeelding op te slaan?** PNG via `Bitmap.Save`.  
- **Heb ik een licentie nodig om afbeeldingen op te slaan?** Een proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Kan ik de spanning van de curve aanpassen?** Ja, overloads van `DrawCurve` laten je spanning specificeren.  
- **Is Aspose.Drawing compatibel met .NET 6+?** Absoluut – het ondersteunt .NET Framework en .NET Core/5/6.

## Wat betekent “how to save PNG” in de context van Aspose.Drawing?

Een PNG opslaan betekent het converteren van de in‑memory bitmap waarop je tekent naar een fysiek PNG‑bestand op schijf. Het proces schrijft de pixelgegevens met verliesloze compressie, waardoor de exacte kleuren en eventuele alfa‑kanaalinformatie behouden blijven. De `Bitmap.Save`‑methode van Aspose.Drawing verwerkt de PNG‑codering automatisch, zodat je zelf geen formatdetails hoeft te beheren.

## Waarom een cardinal spline tekenen met Aspose.Drawing?

Een cardinal spline produceert een vloeiende, vloeiende curve die nauwkeurig een reeks controlepunten volgt, waardoor hij perfect is voor datavisualisaties, UI‑graphics en aangepaste vormen. Aspose.Drawing ondersteunt **30+ image formats** en kan multi‑honderd‑pagina graphics renderen zonder het volledige bestand in het geheugen te laden, wat je zowel snelheid als flexibiliteit biedt.

## Vereisten

Voordat we beginnen, zorg ervoor dat je het volgende hebt:

- Visual Studio (een recente versie) geïnstalleerd.  
- Aspose.Drawing voor .NET bibliotheek. Je kunt het downloaden [hier](https://releases.aspose.com/drawing/net/).  
- Basiskennis van C# programmeren.

## Namespaces importeren

In je C#‑bestand begin je met het importeren van de benodigde namespace:

De `Aspose.Drawing` namespace bevat alle kern‑typen zoals `Bitmap`, `Graphics` en `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Stap 1: Maak een Bitmap (Canvas)

Eerst maak je een bitmap die fungeert als canvas voor je tekening. Deze bitmap is waar de spline wordt gerenderd voordat je **de afbeelding opslaan**.

Bitmap vertegenwoordigt een in‑memory afbeelding met een gedefinieerd pixelformaat en afmetingen.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Stap 2: Maak een Graphics‑object

Vervolgens haal je een `Graphics`‑object op uit de bitmap. Dit object biedt het tekenoppervlak.

Graphics biedt een tekenoppervlak voor het renderen van vormen, tekst en afbeeldingen op een bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Stap 3: Definieer Pen en Teken Curve

Definieer een `Pen` met de gewenste kleur en breedte, en teken vervolgens de cardinal spline met `DrawCurve`. Dit demonstreert de **draw curve with pen** techniek en dient als een **cardinal spline example**.

Pen omvat de kleur, breedte en lijnstijl die worden gebruikt voor het tekenen van lijnen en curves.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Stap 4: Sla de afbeelding op (Curve opslaan als PNG)

Tot slot sla je de bitmap op als een PNG‑bestand. Dit is de kern van **how to save PNG** in deze tutorial.

`Bitmap.Save` schrijft de afbeelding naar een bestand in het opgegeven formaat, zoals PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Pro tip:** Gebruik `Path.Combine` om bestands‑paden veilig op te bouwen over platformen.

Gefeliciteerd! Je hebt met succes een cardinal spline getekend en het resultaat opgeslagen als een PNG‑afbeelding met Aspose.Drawing voor .NET. Voel je vrij om te experimenteren met verschillende punt‑arrays, pen‑kleuren of lijndiktes om je curves aan te passen.

## Veelvoorkomende gebruikssituaties

- **Data visualizations** – vloeiende lijndiagrammen die precieze controlepunten nodig hebben.  
- **Custom UI components** – knoppen, schuifregelaars of decoratieve randen tekenen.  
- **Exportable graphics** – PNG‑assets on‑the‑fly genereren voor rapporten of webinhoud.

## Problemen oplossen & Tips

- **Image appears blank?** Zorg ervoor dat het pixelformaat van de bitmap alfa ondersteunt (`Format32bppPArgb`) en dat je `graphics.Clear(Color.Transparent)` aanroept indien nodig.  
- **Unexpected curve shape?** Pas de spanningsparameter aan door de overload `DrawCurve(pen, points, tension)` te gebruiken.  
- **File access errors?** Controleer of de doelmap bestaat en dat je applicatie schrijfrechten heeft.

## Veelgestelde vragen

**Q1: Kan ik Aspose.Drawing gebruiken voor commerciële projecten?**  
A1: Ja, Aspose.Drawing is geschikt voor zowel persoonlijke als commerciële projecten. Bekijk de licentie‑details op de [purchase page](https://purchase.aspose.com/buy).

**Q2: Hoe kan ik een tijdelijke licentie krijgen voor testen?**  
A2: Verkrijg een tijdelijke licentie voor testdoeleinden [hier](https://purchase.aspose.com/temporary-license/).

**Q3: Waar kan ik extra ondersteuning vinden?**  
A3: Bezoek het [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) voor community‑ondersteuning en discussies.

**Q4: Is er een gratis proefversie beschikbaar?**  
A4: Ja, verken de functies met de [free trial](https://releases.aspose.com/) versie voordat je een aankoop doet.

**Q5: Hoe krijg ik toegang tot de documentatie?**  
A5: Raadpleeg de uitgebreide [documentation](https://reference.aspose.com/drawing/net/) voor gedetailleerde informatie en voorbeelden.

---

**Laatst bijgewerkt:** 2026-05-29  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde tutorials

- [Bitmap opslaan als PNG & Gesloten Curves tekenen met Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Bitmap opslaan C# – Bezier Splines tekenen met Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Bitmap opslaan als PNG met Solid Brushes in Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}