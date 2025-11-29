---
date: 2025-11-29
description: Leer hoe je een bitmap maakt met Aspose.Drawing, wereldtransformaties
  toepast en graphics converteert naar PNG. Stapsgewijze handleiding voor .NET‑ontwikkelaars.
language: nl
linktitle: World Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Maak een bitmap met Aspose.Drawing – Gids voor wereldtransformatie
url: /net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bitmap maken met Aspose.Drawing – Wereldtransformatie

## Introductie

Welkom! In deze tutorial **maak je een bitmap met Aspose.Drawing** en verken je wereldtransformaties die je in staat stellen om grafische elementen eenvoudig te verschuiven, roteren of schalen. Of je nu een **graphics translate‑voorbeeld** nodig hebt, **graphics wilt converteren naar PNG**, of **meerdere graphics‑transformaties** plant, deze gids leidt je stap voor stap in een duidelijke, gesprekachtige stijl.

## Snelle antwoorden
- **Wat betekent “wereldtransformatie”?** Het brengt de logische (wereld‑)coördinaten van je tekening in kaart naar de pagina‑ (apparaat‑)coördinaten.  
- **Kan ik het resultaat exporteren als PNG?** Ja – na het tekenen roep je simpelweg `bitmap.Save(...)` aan met een `.png` extensie.  
- **Heb ik een licentie nodig voor Aspose.Drawing?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Is dit compatibel met .NET 6/7?** Absoluut – Aspose.Drawing ondersteunt .NET Framework 4.5+ en .NET Core/5/6/7.  
- **Hoeveel transformaties kan ik achter elkaar toepassen?** Je kunt **meerdere graphics‑transformaties** in volgorde toepassen (translate, rotate, scale, enz.).

## Wat is een wereldtransformatie in Aspose.Drawing?

Een wereldtransformatie wijzigt het coördinatensysteem dat je teken‑commando’s gebruiken. Standaard is (0,0) de linkerbovenhoek van de bitmap. Met `TranslateTransform`, `RotateTransform` of `ScaleTransform` kun je die oorsprong verplaatsen, vormen roteren of hun grootte aanpassen zonder de oorspronkelijke geometrie te wijzigen.

## Waarom een graphics translate‑voorbeeld gebruiken?

- **Vereenvoudigt positionering** – verplaats objecten zonder elk punt opnieuw te berekenen.  
- **Houdt code schoon** – één transformatie‑aanroep vervangt vele handmatige coördinaten‑aanpassingen.  
- **Verhoogt prestaties** – de graphics‑engine verwerkt de wiskunde intern.  

## Voorvereisten

Voordat we beginnen, zorg dat je het volgende hebt:

- **Aspose.Drawing‑bibliotheek** geïntegreerd in je .NET‑project (download van de officiële [Aspose.Drawing release‑pagina](https://releases.aspose.com/drawing/net/)).  
- Een **document directory** waar de uitvoer‑afbeelding wordt opgeslagen.  
- Basiskennis van **C#**‑syntaxis en Visual Studio of je favoriete IDE.  

Laten we nu in de code duiken!

## Namespaces importeren

Breng eerst de benodigde namespaces binnen:

```csharp
using System.Drawing;
using Aspose.Drawing;
```

Deze geven je toegang tot `Bitmap`, `Graphics` en de Aspose‑teken‑hulpmiddelen.

## Stapsgewijze gids

### Stap 1: Een bitmap maken

We beginnen met het maken van een leeg canvas dat onze tekening zal bevatten.

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

- **Waarom 32bppPArgb?** Dit pixel‑formaat ondersteunt alfa‑transparantie en hoogwaardige kleurrendering, perfect voor PNG‑output.  
- **Pro‑tip:** Pas de breedte/hoogte aan om overeen te komen met de gewenste afbeeldingsgrootte.

### Stap 2: De wereldtransformatie instellen (Graphics Translate‑voorbeeld)

Hier verschuiven we de oorsprong naar het midden van de bitmap zodat tekenopdrachten relatief aan dat punt zijn.

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

- Dit verplaatst het punt (0,0) naar (500, 400) – het midden van een canvas van 1000 × 800.  
- U kunt extra transformaties achter elkaar zetten (bijv. `RotateTransform`, `ScaleTransform`) voor **meerdere graphics‑transformaties**.

### Stap 3: Een rechthoek tekenen met de getransformeerde coördinaten

Nu wordt elke vorm die we tekenen gepositioneerd ten opzichte van de nieuwe oorsprong.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

- De linkerbovenhoek van de rechthoek begint bij de getransformeerde oorsprong (midden van de afbeelding).  
- Voel u vrij om te experimenteren met andere vormen — ellipsen, lijnen of aangepaste paden.

### Stap 4: Het resultaat opslaan – graphics converteren naar PNG

Sla tenslotte de bitmap op als een PNG‑bestand.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

- PNG behoudt de exacte kleuren en transparantie die we eerder hebben ingesteld.  
- Vervang `"Your Document Directory"` door het daadwerkelijke pad op uw machine.

## Veelvoorkomende problemen en oplossingen

| Probleem | Waarom het gebeurt | Oplossing |
|----------|--------------------|-----------|
| **Bestand niet gevonden fout** bij het opslaan | De doelmap bestaat niet. | Maak de map programmatisch (`Directory.CreateDirectory`) voordat u `Save` aanroept. |
| **Lege afbeelding** na transformatie | `TranslateTransform` aangeroepen na het tekenen. | Zorg ervoor dat de transformatie **vóór** alle tekenopdrachten is ingesteld. |
| **Vervormde kleuren** | Een incompatibel pixelformaat gebruiken. | Gebruik `Format32bppPArgb` voor PNG‑output. |

## Veelgestelde vragen

**V: Kan ik meer dan één transformatie toepassen?**  
A: Ja – u kunt `TranslateTransform`, `RotateTransform` en `ScaleTransform` combineren om complexe effecten te bereiken.

**V: Is Aspose.Drawing gratis voor commerciële projecten?**  
A: Een gratis proefversie is beschikbaar voor evaluatie, maar een commerciële licentie is vereist voor productie.

**V: Werkt dit met .NET Core en .NET 5/6/7?**  
A: Absoluut. Aspose.Drawing ondersteunt alle moderne .NET‑runtime‑omgevingen.

**V: Waar kan ik de volledige API‑referentie vinden?**  
A: De volledige documentatie is beschikbaar [hier](https://reference.aspose.com/drawing/net/).

**V: Hoe los ik een ontbrekend uitvoerbestand op?**  
A: Controleer de pad‑string, zorg voor schrijfrechten en bevestig dat de map bestaat voordat u `Save` aanroept.

## Conclusie

U heeft nu geleerd hoe u **een bitmap maakt met Aspose.Drawing**, een **wereldtransformatie** toepast en **graphics converteert naar PNG**. Door deze basisprincipes onder de knie te krijgen, kunt u rijkere graphics maken, dynamische afbeeldingen genereren en geavanceerde visuele effecten integreren in elke .NET‑applicatie.

---

**Laatst bijgewerkt:** 2025-11-29  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose  
**Gerelateerde bronnen:** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}