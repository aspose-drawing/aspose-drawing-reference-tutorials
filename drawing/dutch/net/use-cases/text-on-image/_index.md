---
date: 2026-02-27
description: Leer hoe je een verjaardagskaartafbeelding maakt met Aspose.Drawing voor
  .NET. Deze gids laat zien hoe je een tekenreeks op een afbeelding tekent, tekst
  op een foto overlayt en snel een bijschrift aan een foto toevoegt.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hoe maak je een verjaardagskaartafbeelding met Aspose.Drawing
url: /nl/net/use-cases/text-on-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hoe maak je een verjaardagskaartafbeelding met Aspose.Drawing

## Introductie
In de dynamische wereld van .NET‑ontwikkeling steekt Aspose.Drawing eruit als een krachtig hulpmiddel voor het moeiteloos manipuleren van afbeeldingen. Of je nu een **verjaardagskaartafbeelding wilt maken**, een watermerk wilt toevoegen, of simpelweg tekst over een foto wilt leggen, deze tutorial leidt je stap voor stap door het tekenen van een string op een afbeelding met C#. Aan het einde van deze gids heb je een gepersonaliseerde verjaardagskaart klaar om te delen.

## Snelle antwoorden
- **Welke bibliotheek moet ik gebruiken?** Aspose.Drawing for .NET  
- **Kan ik een bijschrift aan een foto toevoegen?** Ja – gebruik `Graphics.DrawString` met aangepaste lettertypen.  
- **Is een licentie vereist voor productie?** Ja, een commerciële licentie is nodig.  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een eenvoudige kaart.

## Wat is een verjaardagskaartafbeelding?
Een verjaardagskaartafbeelding is een gepersonaliseerde foto die een achtergrondafbeelding combineert met aangepaste tekst—zoals een groet, de naam van de ontvanger, of een feestelijke boodschap. Met Aspose.Drawing kun je deze kaarten programmatically genereren zonder handmatige grafische ontwerptools.

## Waarom Aspose.Drawing gebruiken om tekst op een afbeelding te plaatsen?
- **Cross‑platformondersteuning:** Werkt op Windows, Linux en macOS.  
- **Rijke teken‑API:** Volledige controle over lettertypen, kleuren en lay‑out.  
- **Geen externe afhankelijkheden:** Vervangt `System.Drawing.Common` door een volledig beheerde bibliotheek.  
- **Hoge prestaties:** Geoptimaliseerd voor bulkafbeeldingsverwerking.

## Voorvereisten
Voordat je aan de tutorial begint, zorg dat je het volgende hebt:

1. Aspose.Drawing‑bibliotheek: Download en installeer de Aspose.Drawing‑bibliotheek vanaf de [Aspose.Drawing for .NET documentation](https://reference.aspose.com/drawing/net/).  
2. Ontwikkelomgeving: Een werkende .NET‑ontwikkelomgeving, zoals Visual Studio of Visual Studio Code, met .NET 6 SDK of later geïnstalleerd.

Laten we nu de stap‑voor‑stap‑gids doorlopen om tekst aan een afbeelding toe te voegen en deze op te slaan als een verjaardagskaart.

## Importeer namespaces
Begin met het importeren van de benodigde namespaces in je C#‑project:

```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```

## Stap 1: Laad de afbeelding
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Hier laden we de afbeelding vanaf het opgegeven bestandspad en initialiseren we het graphics‑object voor verdere verwerking.

## Stap 2: Stel teksteigenschappen in
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Definieer de teksteigenschappen zoals kleur, lettertype en padding. Pas deze parameters aan volgens je ontwerpvoorkeuren.

## Stap 3: Meet de tekstgrootte
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Bereken de benodigde grootte voor de tekst door elk woord afzonderlijk te meten. Dit zorgt voor een juiste plaatsing en voorkomt overlapping van tekst.

## Stap 4: Teken tekst op afbeelding
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Plaats nu de tekst op de afbeelding op basis van de berekende grootte en teken deze met het opgegeven lettertype en kleur.

## Stap 5: Sla de afbeelding op
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Sla de gewijzigde afbeelding op in de gewenste map. Het resulterende bestand is een klaar‑om‑te‑versturen verjaardagskaartafbeelding.

## Veelvoorkomende gebruikssituaties & tips
- **Bijschrift aan foto toevoegen:** Vervang `text` door elk bijschrift dat je nodig hebt, bijvoorbeeld “Celebrating 30 Years!”.  
- **Tekst op bitmap tekenen:** Dezelfde aanpak werkt voor `Bitmap`‑objecten die vanaf nul zijn gemaakt.  
- **Meerdere regels overlayen:** Loop door een array van strings en pas de Y‑coördinaat van de `Rectangle` voor elke regel aan.  
- **Pro‑tip:** Gebruik `Graphics.SmoothingMode = SmoothingMode.AntiAlias` voor nog vloeiender tekstrenderen.

## Conclusie
Aspose.Drawing vereenvoudigt beeldbewerkings‑taken in .NET en biedt ontwikkelaars een robuuste toolkit. Het toevoegen van tekst aan afbeeldingen—of het nu gaat om **verjaardagskaartafbeelding maken**, **string op afbeelding tekenen**, of **bijschrift aan foto toevoegen**—is slechts één voorbeeld van de veelzijdigheid bij het omgaan met grafische elementen.

## Veelgestelde vragen
### Is Aspose.Drawing compatibel met alle afbeeldingsformaten?
Aspose.Drawing ondersteunt een breed scala aan afbeeldingsformaten, waaronder populaire zoals JPEG, PNG en GIF. Raadpleeg de [documentation](https://reference.aspose.com/drawing/net/) voor een volledige lijst.

### Kan ik Aspose.Drawing gebruiken voor commerciële projecten?
Ja, Aspose.Drawing is geschikt voor zowel persoonlijke als commerciële projecten. Voor licentie‑details, bezoek de [purchase page](https://purchase.aspose.com/buy).

### Zijn tijdelijke licenties beschikbaar voor testdoeleinden?
Ja, je kunt een tijdelijke licentie voor testdoeleinden verkrijgen via [Temporary License](https://purchase.aspose.com/temporary-license/).

### Waar kan ik community‑ondersteuning vinden voor Aspose.Drawing?
Doe mee met de community en krijg ondersteuning op het [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).

### Hoe begin ik met Aspose.Drawing?
Begin met het downloaden van de bibliotheek vanaf [here](https://releases.aspose.com/drawing/net/) en verken de uitgebreide [documentation](https://reference.aspose.com/drawing/net/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-02-27  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose