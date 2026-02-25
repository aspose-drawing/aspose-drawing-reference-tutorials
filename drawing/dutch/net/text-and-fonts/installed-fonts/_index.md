---
date: 2026-02-25
description: Leer hoe je bitmapgrafieken maakt in C# en PNG-afbeeldingen opslaat,
  terwijl je geïnstalleerde lettertypen opsomt, tekst tekent met lettertypen en de
  resolutie van de bitmap aanpast met Aspose.Drawing voor .NET.
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Bitmapgrafieken maken in C# – PNG-afbeelding opslaan en werken met geïnstalleerde
  lettertypen in Aspose.Drawing
url: /nl/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG-afbeelding opslaan en werken met geïnstalleerde lettertypen in Aspose.Drawing

## Inleiding

Als je **PNG-afbeeldingen** moet **opslaan** en tegelijkertijd **bitmap‑graphics C#** wilt **maken**, biedt Aspose.Drawing voor .NET een nette, cross‑platform manier om dit te doen. In deze tutorial lopen we door het opsommen van geïnstalleerde lettertypen, het tonen van lettertype‑families, het maken van graphics vanuit een bitmap en het tekenen van tekst met lettertypen — en slaan uiteindelijk het resultaat op als een PNG‑afbeelding. Aan het einde heb je een herbruikbaar fragment dat je in elk .NET‑project kunt gebruiken.

## Snelle antwoorden
- **Wat maakt deze tutorial?** Een PNG‑afbeelding die geïnstalleerde lettertype‑families opsomt.  
- **Welke bibliotheek is vereist?** Aspose.Drawing voor .NET (geen System.Drawing.Common nodig).  
- **Kan ik aangepaste lettertypen gebruiken?** Ja — laad ze gewoon in een `InstalledFontCollection`.  
- **Is de uitvoerresolutie aanpasbaar?** Absoluut — verander de bitmap‑grootte of pixel‑formaat om **bitmap‑resolutie C#** aan te passen.  
- **Heb ik een licentie nodig om de code uit te voeren?** Een tijdelijke licentie werkt voor evaluatie; een volledige licentie is vereist voor productie.

## Wat betekent “PNG‑afbeelding opslaan” in de context van Aspose.Drawing?
Een PNG‑afbeelding opslaan betekent dat je je tekenoppervlak (een `Bitmap`) rendert naar een bestand met de extensie `.png`. Aspose.Drawing verzorgt de codering voor je, zodat je alleen `bitmap.Save(...)` hoeft aan te roepen met het gewenste pad.

## Waarom geïnstalleerde lettertypen opsommen en lettertype‑families tonen?
Weten welke lettertypen beschikbaar zijn, stelt je in staat dynamische graphics te maken die zich aanpassen aan de omgeving van de eindgebruiker. Dit is vooral handig voor het genereren van rapporten, certificaten of andere visuele content die moet overeenkomen met de huisstijl zonder lettertype‑bestanden mee te leveren.

## Hoe maak je bitmap‑graphics C# met Aspose.Drawing?
Hieronder vind je een praktische, stap‑voor‑stap walkthrough die precies laat zien hoe je **bitmap‑graphics C#** maakt, tekst met lettertypen tekent en de bitmap‑resolutie indien nodig aanpast.

## Vereisten

- **Aspose.Drawing Library** – download de nieuwste versie van de [Aspose Drawing download page](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider of een andere .NET‑compatibele editor.  
- **Basiskennis C#** – je moet vertrouwd zijn met klassen, objecten en eenvoudige lussen.

## Namespaces importeren
Om met lettertypen en graphics te werken, importeer je de volgende namespaces bovenaan je C#‑bestand:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Stapsgewijze handleiding

### Stap 1: Een bitmap maken (het canvas)
Eerst maken we een bitmap die de uiteindelijke afbeelding zal bevatten. De bitmap‑grootte en pixel‑formaat bepalen de kwaliteit van de opgeslagen PNG en laten je **bitmap‑resolutie C#** aanpassen.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Stap 2: Graphics maken vanuit bitmap
Vervolgens verkrijgen we een `Graphics`‑object van de bitmap. Dit object stelt ons in staat vormen, tekst en afbeeldingen op het canvas te tekenen.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Stap 3: Brush en font instellen (tekst met lettertypen tekenen)
We hebben een brush nodig voor de tekstkleur en een `Font`‑object dat het lettertype, de grootte en de stijl definieert. Hier komt **draw text with fonts** van pas.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Stap 4: Geïnstalleerde lettertypen opsommen en lettertype‑families tonen
Nu geven we het aantal lettertype‑families en de eerste paar namen direct op de bitmap weer. Dit demonstreert de mogelijkheden **list installed fonts** en **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Stap 5: PNG‑afbeelding opslaan
Tot slot schrijven we de bitmap naar schijf als een PNG‑bestand. Dit is de kernoperatie **save png image**.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tip:** Gebruik `Path.Combine` voor het bouwen van bestands‑paden om problemen met scheidingstekens op verschillende besturingssystemen te voorkomen.

## Veelvoorkomende problemen en oplossingen
| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| **Geen lettertypen zichtbaar** | `InstalledFontCollection` niet gevuld (bijv. op een headless server zonder lettertypen). | Installeer de benodigde lettertypen op de server of embed aangepaste lettertypen in je applicatie. |
| **Opgeslagen bestand is corrupt** | Onjuist pixel‑formaat of ontbrekende schrijfrechten. | Zorg dat de doelmap bestaat en de app schrijfrechten heeft; behoud `Format32bppPArgb`. |
| **Tekst ziet er wazig uit** | Lage DPI‑instellingen. | Verhoog de bitmap‑afmetingen of stel `graphics.SmoothingMode = SmoothingMode.AntiAlias` in. |

## Veelgestelde vragen

**Q: Kan ik aangepaste lettertypen gebruiken die niet op de machine geïnstalleerd zijn?**  
A: Ja. Laad het lettertype‑bestand in een `PrivateFontCollection` en maak een `Font` vanuit die collectie.

**Q: Hoe ga ik om met font‑gerelateerde uitzonderingen?**  
A: Plaats de font‑creatie in een `try/catch`‑blok en controleer `ArgumentException` voor ontbrekende families.

**Q: Is Aspose.Drawing geschikt voor webapplicaties?**  
A: Absoluut. De bibliotheek werkt in ASP.NET Core, Azure Functions en andere server‑side omgevingen.

**Q: Kan ik de tekstkleur of -stijl wijzigen?**  
A: Ja. Gebruik verschillende `Brush`‑types (bijv. `LinearGradientBrush`) en wijzig de `FontStyle`‑enum.

**Q: Waar kan ik een tijdelijke licentie voor testdoeleinden krijgen?**  
A: Download een proeflicentie van de [Aspose temporary‑license page](https://purchase.aspose.com/temporary-license/).

## Conclusie

Door deze stappen te volgen heb je geleerd hoe je **PNG‑afbeeldingen** maakt die dynamisch **geïnstalleerde lettertypen opsommen**, **lettertype‑families tonen**, **graphics vanuit bitmap creëren** en **tekst met lettertypen tekenen** met Aspose.Drawing voor .NET. Je weet nu hoe je **bitmap‑graphics C#** maakt, de bitmap‑resolutie aanpast en indien nodig aangepaste lettertypen integreert. Voel je vrij om te experimenteren met andere lettertypen, kleuren en bitmap‑groottes om te voldoen aan de visuele eisen van je project.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-02-25  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose