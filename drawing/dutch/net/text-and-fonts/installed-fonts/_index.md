---
date: 2025-12-06
description: Leer hoe u PNG‑afbeeldingsbestanden opslaat, geïnstalleerde lettertypen
  opsomt, lettertypefamilies weergeeft, graphics maakt van een bitmap en tekst tekent
  met lettertypen, met behulp van Aspose.Drawing voor .NET.
language: nl
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: PNG-afbeelding opslaan en werken met geïnstalleerde lettertypen in Aspose.Drawing
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG-afbeelding opslaan en werken met geïnstalleerde lettertypen in Aspose.Drawing

## Inleiding

Als je **PNG‑afbeeldingsbestanden** moet opslaan die ook informatie over de op een machine geïnstalleerde lettertypen weergeven, biedt Aspose.Drawing voor .NET een nette, platformonafhankelijke manier om dit te doen. In deze tutorial lopen we door het opsommen van geïnstalleerde lettertypen, het tonen van lettertypefamilies, het maken van graphics vanuit een bitmap en het tekenen van tekst met lettertypen – alles terwijl we uiteindelijk het resultaat opslaan als een PNG‑afbeelding. Aan het einde heb je een herbruikbare code‑snippet die je in elk .NET‑project kunt gebruiken.

## Snelle antwoorden
- **Wat maakt deze tutorial?** Een PNG‑afbeelding die geïnstalleerde lettertypefamilies opsomt.  
- **Welke bibliotheek is vereist?** Aspose.Drawing voor .NET (geen System.Drawing.Common nodig).  
- **Kan ik aangepaste lettertypen gebruiken?** Ja – laad ze gewoon in een `InstalledFontCollection`.  
- **Is de uitvoerresolutie aanpasbaar?** Absoluut – wijzig de bitmap‑grootte of pixel‑formaat.  
- **Heb ik een licentie nodig om de code uit te voeren?** Een tijdelijke licentie werkt voor evaluatie; een volledige licentie is vereist voor productie.

## Wat betekent “PNG‑afbeelding opslaan” in de context van Aspose.Drawing?
Een PNG‑afbeelding opslaan betekent dat je je tekenoppervlak (een `Bitmap`) rendert naar een bestand met de extensie `.png`. Aspose.Drawing verzorgt de codering voor je, dus je hoeft alleen `bitmap.Save(...)` aan te roepen met het gewenste pad.

## Waarom geïnstalleerde lettertypen opsommen en lettertypefamilies tonen?
Weten welke lettertypen beschikbaar zijn, stelt je in staat dynamische graphics te maken die zich aanpassen aan de omgeving van de eindgebruiker. Dit is vooral handig voor het genereren van rapporten, certificaten of andere visuele content die moet overeenkomen met de huisstijl zonder lettertypebestanden mee te leveren.

## Voorvereisten

- **Aspose.Drawing‑bibliotheek** – download de nieuwste versie vanaf de [Aspose Drawing downloadpagina](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider of een andere .NET‑compatibele editor.  
- **Basiskennis C#** – je moet vertrouwd zijn met klassen, objecten en eenvoudige lussen.

## Namespaces importeren
Om met lettertypen en graphics te werken, importeer je deze namespaces bovenaan je C#‑bestand:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Stapsgewijze handleiding

### Stap 1: Een bitmap maken (het canvas)
Eerst maken we een bitmap die de uiteindelijke afbeelding zal bevatten. De bitmap‑grootte en pixel‑formaat bepalen de kwaliteit van de opgeslagen PNG.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Stap 2: Graphics van bitmap maken
Vervolgens verkrijgen we een `Graphics`‑object van de bitmap. Dit object laat ons vormen, tekst en afbeeldingen op het canvas tekenen.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Stap 3: Brush en font instellen (tekst tekenen met lettertypen)
We hebben een brush nodig voor de tekstkleur en een `Font`‑object dat het lettertype, de grootte en de stijl definieert.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Stap 4: Geïnstalleerde lettertypen opsommen en lettertypefamilies tonen
Nu tonen we het aantal lettertypefamilies en de eerste paar namen direct op de bitmap. Dit demonstreert de **list installed fonts**‑ en **show font families**‑functionaliteit.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Stap 5: PNG‑afbeelding opslaan
Tot slot schrijven we de bitmap naar schijf als een PNG‑bestand. Dit is de kern van de **save png image**‑operatie.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tip:** Gebruik `Path.Combine` voor het bouwen van bestands‑paden om problemen met scheidingstekens op verschillende besturingssystemen te voorkomen.

## Veelvoorkomende problemen en oplossingen
| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Geen lettertypen weergegeven** | `InstalledFontCollection` niet gevuld (bijv. draaien op een headless server zonder lettertypen). | Installeer de benodigde lettertypen op de server of embed aangepaste lettertypen in je applicatie. |
| **Opgeslagen bestand is corrupt** | Onjuist pixel‑formaat of ontbrekende schrijfrechten. | Zorg dat de doelmap bestaat en de app schrijfrechten heeft; behoud `Format32bppPArgb`. |
| **Tekst ziet er wazig uit** | Lage DPI‑instellingen. | Vergroot de bitmap‑afmetingen of stel `graphics.SmoothingMode = SmoothingMode.AntiAlias` in. |

## Veelgestelde vragen

**V: Kan ik aangepaste lettertypen gebruiken die niet op de machine geïnstalleerd zijn?**  
A: Ja. Laad het lettertypebestand in een `PrivateFontCollection` en maak een `Font` vanuit die collectie.

**V: Hoe ga ik om met lettertype‑gerelateerde uitzonderingen?**  
A: Plaats het maken van het lettertype in een `try/catch`‑blok en inspecteer `ArgumentException` voor ontbrekende families.

**V: Is Aspose.Drawing geschikt voor webapplicaties?**  
A: Absoluut. De bibliotheek werkt in ASP.NET Core, Azure Functions en andere server‑side omgevingen.

**V: Kan ik de tekstkleur of stijl wijzigen?**  
A: Ja. Gebruik verschillende `Brush`‑types (bijv. `LinearGradientBrush`) en wijzig de `FontStyle`‑enum.

**V: Waar kan ik een tijdelijke licentie voor testdoeleinden krijgen?**  
A: Download een proeflicentie vanaf de [Aspose tijdelijke‑licentiepagina](https://purchase.aspose.com/temporary-license/).

## Conclusie

Door deze stappen te volgen heb je geleerd hoe je **PNG‑afbeeldingsbestanden** kunt **opslaan** die dynamisch **geïnstalleerde lettertypen opsommen**, **lettertypefamilies tonen**, **graphics van bitmap maken** en **tekst met lettertypen tekenen** met Aspose.Drawing voor .NET. Voel je vrij om te experimenteren met andere lettertypen, kleuren en bitmap‑groottes om te voldoen aan de visuele eisen van je project.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2025-12-06  
**Getest met:** Aspose.Drawing 24.11 voor .NET  
**Auteur:** Aspose