---
date: 2026-02-01
description: Leer hoe u een bitmap als PNG opslaat met Aspose.Drawing, wereldtransformaties
  toepast en graphics converteert naar PNG. Stapsgewijze handleiding voor .NET‑ontwikkelaars.
linktitle: World Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Bitmap opslaan als PNG met Aspose.Drawing – Wereldtransformatie
url: /nl/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bitmap opslaan als PNG met Aspose.Drawing – Wereldtransformatie

## Bitmap opslaan als PNG – Introductie

Welkom! In deze tutorial leer je hoe je **save bitmap as PNG** met Aspose.Drawing kunt gebruiken en wereldtransformaties kunt verkennen die je in staat stellen om grafische elementen te verschuiven, roteren of schalen met gemak. Of je nu een **graphics translate example** nodig hebt, **convert graphics to PNG** wilt doen, of **multiple graphics transformations** plant, deze gids leidt je tekening naar de pagina (apparaat) coördinaten.  
- **Kan ik het resultaat exporteren als PNG?** Ja – na het tekenen roep je simpelweg `bitmap.Save(...)` aan met een `.png` extensie.  
- **Heb ik een licentie nodig voor Aspose.Drawing?** Een gratis proefversie werkt voor ontwikkeling; een commerciële dit compatibel met .NET 6/7?** Absoluut – Aspose.Drawing ondersteunt .NET Framework 4.5+ en .NET Core/5/6/7.  
- **Hoeveel transformaties kan ik achter elkaar toepassen?** Je kunt **multiple graphics transformations World Transformation in Aspose.Drawing?

Een worldTranslateTransform`, `RotateTransform` of `ScaleTransform` kun je die oorsprong verplaatsen, vormen roteren of hun grootte aanpassen zonder de oorspronkelijke geometrie te positionering vereenvoudigt. In plaats van elk punt opnieuw te berekenen, verschuif je het coördinatensysteem één keer en teken je alsof de nieuwe oorsprong het Example gebruiken?

- **Vereenvoudigt positionering** – verplaats objecten zonder elk punt opnieuw te berekenen.  
- **Houdt code schoon** – één transformatie‑aanroep vervangt vele handmatige coördinatie‑aanpassingen.  
- **Verhoogt de prestaties** – de graphics‑engine verwerkt de wiskunde intern.  

## Voorwaarden

Voordat we beginnen, zorg ervoor dat je het volgende hebt:

- **Aspose.Drawing library** geïntegreerd in je .NET‑project, te downloaden van de officiële [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/).  
- Een **document directory** waar de uitvoerafbeelding wordt opgeslagen.  
- Basiskennis van **C#**‑syntaxis en Visual Studio of je favoriete IDE.  

Laten we nu in de code duiken!

## Namespaces importeren

Eerst importeer je de benodigde namespaces:

```csharp
using System.Drawing;
using Aspose.Drawing;
```

Deze geven je toegang tot `Bitmap`, `Graphics` en de Aspose‑teken‑hulpmiddelen.

## Stapsgewijze gids

### Stap 1: Maak een Bitmap

We beginnen met het maken van een leeg canvas dat onze tekening zal bevatten.

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

- **Waarom 32bppPArgb?** Dit pixelformaat ondersteunt alfa‑transparantie en hoogwaardige kleurweergave, perfect voor PNG‑output.  
- afbeeldingsg Example)

Hier verschuiven we de oorsprong naar het midden van de bitmap zodat tekenopdrachten relatief zijn aan dat punt.

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

- Dit verplaatst het (0,0) punt naar (500, 400) – hetTransform`) achter elkaar uitvoeren voor **multiple graphics transformations**.

### Stap 3: Teken een rechthoek met de getransformeerde coördinaten

Nu zal elke vorm die we tekenen gepositioneerd worden ten opzichte van de nieuwe oorsprong.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

- De linkerbovenhoek van de rechthoek begint bij de getransformeerde oorsprong (midden van de afbeelding).  
- Voel je vrij om te experimenteren met andere vormen — ellipsen, lijnen of aangepaste paden.

### Stap 4: Sla het resultaat op – Convert Graphics to PNG

Ten slotte sla je de bitmap op als een PNG‑bestand. Deze stap **saves the bitmap as PNG** terwijl kleuren en transparantie behouden blijven.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

- PNG behoudt de exacte kleuren en transparantie die we eerder hebben ingesteld.  
- Vervang `"Your Document Directory"` door het daadwerkelijke pad op jouw machine.

## Veelvoorkomende problemen en oplossingen

| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **File not found error** bij opslaan | De doelmap bestaat niet. | Maak de map programmatisch (`Directory.CreateDirectory`) aan voordat `Save` wordt aangeroepen. |
| **Blank image** na transformatie | `TranslateTransform` aangeroepen na het tekenen. | Zorg ervoor dat de transformatie **vóór** enige tekenopdrachten wordt ingesteld. |
| **Distorted colors** | Een incompatibel pixelformaat gebruiken. | Gebruik `Format32bppPArgb` voor PNG-output. |

## Veelgestelde vragen

**V: Kan ik meer dan één transformatie toepassen?**  
A: Ja – je kunt `TranslateTransform`, `RotateTransform` en `ScaleTransform` achter elkaar uitvoeren om complexe effecten te bereiken.

**V: Is Aspose.Drawing gratis voor commerciële projecten?**  
A: Een gratis proefversie is beschikbaar voor evaluatie, maar een commerciële licentie is vereist voor productiegebruik.

**V: Werkt dit met .NET Core en .NET 5/6/7?**  
A: Absoluut. Aspose.Drawing ondersteunt alle moderne .NET‑runtime‑omgevingen.

**V: Waar kan ik de volledige API‑referentie vinden?**  
A: De volledige documentatie is beschikbaar [hier](https://reference.aspose.com/drawing/net/).

**V: Hoe los ik een ontbrekend uitvoerbestand op?**  
A: Controleer de pad‑string, zorg voor schrijfrechten, en bevestig dat de map bestaat voordat `Save` wordt aangeroepen.

## Conclusie

Je hebt nu geleerd hoe je **save bitmap as PNG** met Aspose.Drawing kunt gebruiken, een **world transformation** kunt toepassen, en **convert graphics to PNG**. Door deze basisprincipes onder de knie te krijgen, kun je rijkere graphics bouwen, dynamische afbeeldingen genereren en geavanceerde visuele effecten integreren in elke .NET‑applicatie.

---

**Laatst bijgewerkt:** 202-02-01  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose  
**Gerelateerde bronnen:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}