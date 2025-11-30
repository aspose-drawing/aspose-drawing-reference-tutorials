---
date: 2025-11-30
description: Leer hoe u coördinatensysteemtransformatie toepast, een rechthoek bitmap
  tekent en pagina's transformeert met Aspose.Drawing voor .NET.
language: nl
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Coördinatensysteemtransformatie (Paginastransformatie) in Aspose.Drawing voor
  .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Coördinatensysteemtransformatie (Pagina‑transformatie) in Aspose.Drawing voor .NET

## Introductie

Welkom! In deze tutorial ontdek je **hoe je een coördinatensysteemtransformatie** op een pagina uitvoert met Aspose.Drawing voor .NET. Of je nu **rechthoek‑bitmap**‑objecten wilt tekenen, tekeningen wilt schalen, of simpelweg paginabeenheden wilt omzetten naar apparaat‑eenheden, de onderstaande stappen begeleiden je door het hele proces—duidelijk, beknopt en klaar om te copy‑pasten in je project.

## Snelle antwoorden
- **Wat is de primaire klasse voor tekenen?** `Graphics` van Aspose.Drawing.
- **Hoe stel ik paginabeenheden in?** Gebruik `graphics.PageUnit = GraphicsUnit.Inch;`.
- **Kan ik een rechthoek tekenen op een getransformeerde pagina?** Ja—maak een `Pen` aan en roep `DrawRectangle` aan.
- **Waar wordt de output opgeslagen?** In de map die je opgeeft in `bitmap.Save`.
- **Heb ik een licentie nodig voor productie?** Een geldige Aspose.Drawing‑licentie is vereist voor commercieel gebruik.

## Wat is coördinatensysteemtransformatie?

Een **coördinatensysteemtransformatie** verandert de manier waarop logische paginacoördinaten (zoals inches of millimeters) worden gemapt naar fysieke apparaatcoördinaten (pixels). Door de transformatie aan te passen, beheer je schaal, rotatie en translatie van alle tekenbewerkingen, waardoor het makkelijker wordt om graphics te ontwerpen die resolutie‑onafhankelijk zijn.

## Waarom Aspose.Drawing gebruiken voor paginatransformaties?

- **Volledige .NET‑compatibiliteit** – werkt met .NET Framework, .NET Core en .NET 5/6.  
- **Rijke graphics‑API** – biedt dezelfde functionaliteit als System.Drawing.Common zonder platformbeperkingen.  
- **Eenvoudige eenheidsafhandeling** – schakel tussen inches, millimeters, points, enz. met één eigenschap.  
- **Uitvoer van hoge kwaliteit** – genereer PNG, JPEG, BMP en andere formaten met precieze controle.

## Vereisten

Zorg ervoor dat je het volgende hebt voordat we beginnen:

- **Aspose.Drawing‑bibliotheek** – download de nieuwste versie van de officiële site [hier](https://releases.aspose.com/drawing/net/).  
- **Ontwikkelomgeving** – Visual Studio (elke editie) of een andere .NET‑IDE.  
- **Schrijftoegang** – een map op je computer waar de getransformeerde afbeelding wordt opgeslagen (vervang `"Your Document Directory"` in de code door het daadwerkelijke pad).

Nu we klaar zijn, doorlopen we stap voor stap elke handeling.

## Namespaces importeren

Breng eerst de benodigde namespace in scope:

```csharp
using System.Drawing;
```

> *Waarom dit belangrijk is*: `System.Drawing` bevat de `Bitmap`, `Graphics`, `Pen` en kleurstructuren die we door de hele tutorial gebruiken.

## Stap 1: Een Bitmap maken

Maak een leeg canvas dat de getransformeerde tekening zal hosten. We geven een grootte op van **1000 × 800 pixels** en een pixelindeling die alfa‑transparantie ondersteunt.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> Deze bitmap fungeert als het tekenoppervlak. Het gekozen pixelformaat (`Format32bppPArgb`) zorgt voor renderen van hoge kwaliteit met premultiplied alpha.

## Stap 2: Een Graphics‑object maken

Een `Graphics`‑object levert de tekenmethoden (lijnen, vormen, tekst). We verkrijgen het van de bitmap die we zojuist hebben aangemaakt.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> Het `Graphics`‑object is de kern van alle renderbewerkingen; het respecteert de transformatiesettings die we vervolgens toepassen.

## Stap 3: Het canvas wissen

Voordat er iets wordt getekend, wissen we het canvas naar een neutrale achtergrondkleur (grijs in dit voorbeeld). Deze stap laat ook zien hoe je het volledige bitmap met een effen kleur vult.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Stap 4: Transformatie instellen (Pagina‑transformatie toepassen)

Hier **passen we de paginatransformatie** toe door `PageUnit` op inches te zetten. Dit vertelt de grafische engine om alle volgende coördinaten als inches te interpreteren in plaats van pixels.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *Tip*: Het wijzigen van `PageUnit` is een eenvoudige manier om **hoe je pagina‑coördinaten transformeert** zonder handmatig pixelwaarden te berekenen.

## Stap 5: Een rechthoek tekenen (draw rectangle bitmap)

Nu tekenen we een rechthoek van **1 inch × 1 inch** op positie (1, 1) inches. De `Pen`‑dikte is ingesteld op `0.1f` inches, waardoor een dunne maar zichtbare lijn ontstaat.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> Dit toont **draw rectangle bitmap** na het toepassen van de transformatie—let op dat de afmetingen in inches worden opgegeven, niet in pixels.

## Stap 6: De afbeelding opslaan

Sla tenslotte de getransformeerde bitmap op schijf op. Vervang `"Your Document Directory"` door het daadwerkelijke mappad op jouw machine.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> Het uitvoerbestand (`PageTransformation_out.png`) bevat de rechthoek die is getekend met de coördinatensysteemtransformatie die we eerder hebben ingesteld.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Afbeelding is leeg** | Canvas niet gewist of tekening uitgevoerd buiten het zichtbare gebied. | Controleer `graphics.PageUnit` en coördinaten; zorg dat de rechthoek binnen de bitmap‑grenzen ligt. |
| **Onjuiste schaal** | Verkeerde `GraphicsUnit` gebruikt. | Controleer of `graphics.PageUnit` overeenkomt met de eenheid die je wilt (bijv. `GraphicsUnit.Inch`). |
| **Bestandspad‑fouten** | Ontbrekende map of ongeldige tekens. | Maak de doelmap vooraf aan of gebruik `Path.Combine` om het pad veilig op te bouwen. |

## Veelgestelde vragen

**V: Kan ik Aspose.Drawing gratis gebruiken?**  
A: Aspose.Drawing biedt een gratis proefversie die je kunt verkrijgen [hier](https://releases.aspose.com/).

**V: Waar vind ik uitgebreide documentatie voor Aspose.Drawing?**  
A: De documentatie is beschikbaar [hier](https://reference.aspose.com/drawing/net/).

**V: Hoe krijg ik ondersteuning voor Aspose.Drawing?**  
A: Voor ondersteuning, bezoek het [Aspose.Drawing‑forum](https://forum.aspose.com/c/diagram/17).

**V: Is er een tijdelijke licentie beschikbaar voor Aspose.Drawing?**  
A: Ja, je kunt een tijdelijke licentie verkrijgen [hier](https://purchase.aspose.com/temporary-license/).

**V: Waar kan ik Aspose.Drawing aanschaffen?**  
A: Je kunt Aspose.Drawing kopen [hier](https://purchase.aspose.com/buy).

## Conclusie

Je hebt nu geleerd hoe je **een coördinatensysteemtransformatie toepast**, **rechthoek‑bitmap**‑objecten tekent en **het resultaat opslaat** met Aspose.Drawing voor .NET. Deze bouwstenen stellen je in staat om resolutie‑onafhankelijke graphics te maken, perfect voor rapporten, UI‑elementen of elke situatie waarin precieze afmetingen belangrijk zijn. Experimenteer met andere `GraphicsUnit`‑waarden (zoals `Millimeter` of `Point`) om te zien hoe ze je tekeningen beïnvloeden.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2025-11-30  
**Getest met:** Aspose.Drawing 24.11 voor .NET  
**Auteur:** Aspose