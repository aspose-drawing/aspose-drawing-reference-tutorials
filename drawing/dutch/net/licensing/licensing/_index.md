---
date: 2026-02-09
description: Leer hoe u de Aspose.Drawing‑licentie instelt in .NET. Beheers licentiemethoden
  om alle functies te ontgrendelen zonder watermerken.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Stel Aspose.Drawing-licentie in – Hoe de Aspose.Drawing-licentie in te stellen
url: /nl/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Stel Aspose.Drawing-licentie in

## Introductie

Als u .NET-toepassingen bouwt die afhankelijk zijn van krachtige grafische en beeldbewerkingsfuncties, **het instellen van een Aspose.Drawing-licentie** is de eerste stap om evaluatiebeperkingen te verwijderen en toegang te krijgen tot de volledige functionaliteit. In deze tutorial leert u drie praktische manieren om de Aspose.Drawing-licentie in te stellen—laden vanuit een bestand, laden vanuit een stream, en het gebruik van het metered‑usage‑model—zodat u de bibliotheek met vertrouwen kunt integreren.

## Snelle antwoorden
- **Wat is de primaire manier om Aspose.Drawing te activeren?** Laad een licentiebestand met `License.SetLicense("Aspose.Drawing.lic")`.  
- **Kan ik een licentie toepassen tijdens runtime?** Ja, u kunt de licentie laden vanuit een `Stream` voor dynamische scenario's.  
- **Wordt een metered-licentie ondersteund?** Zeker; gebruik `Metered.SetMeteredKey(publicKey, privateKey)` om facturering op basis van verbruik in te schakelen.  
- **Heb ik een licentie nodig voor ontwikkelbuilds?** Een proefversie werkt voor testen, maar een geldige licentie verwijdert watermerken en ontgrendelt alle API's.  
- **Welke .NET‑versies zijn compatibel?** Aspose.Drawing ondersteunt .NET Framework 4.x, .NET Core 3.1+ en .NET 5/6+.

## Voorvereisten

Voor u begint, zorg dat u het volgende heeft:

- **Aspose.Drawing Library** – download het nieuwste pakket van [hier](https://releases.aspose.com/drawing/net/).  
- **Licentiebestand** – verkrijg een geldig `.lic`‑bestand van [Aspose](https://purchase.aspose.com/buy).  
- **.NET-ontwikkelomgeving** – Visual Studio, Rider, of elke IDE die .NET Framework/.NET Core target.

## Namespaces importeren

We hebben de standaard .NET‑namespaces nodig plus de Aspose.Drawing‑namespace voor licenties. Voeg de volgende `using`‑statements toe aan de bovenkant van uw C#‑bestand:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Licentie laden vanuit een bestand

Het laden van een licentie vanuit een bestand is de meest eenvoudige aanpak. Volg deze drie stappen:

### Stap 1: Initialiseer het licentie‑object

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Stap 2: Stel de licentie in vanuit het `.lic`‑bestand

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Stap 3: Bevestig succes

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro tip:** Plaats het `.lic`‑bestand in dezelfde map als uw uitvoerbare bestand of geef een absoluut pad op om “bestand niet gevonden” fouten te voorkomen.

## Licentie laden vanuit een stream

Wanneer uw licentiebestand is ingebed als resource of opgehaald wordt van een externe locatie, geeft het laden vanuit een `Stream` u flexibiliteit.

### Stap 1: Initialiseer het licentie‑object

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Stap 2: Laad de licentie met een `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Stap 3: Bevestig succes

```csharp
Console.WriteLine("License set successfully.");
```

> **Waarschuwing:** Vergeet niet de `FileStream` te disposen (of gebruik een `using`‑blok) om bestands‑handles vrij te geven.

## Metered-licentie gebruiken

Metered-licenties zijn ideaal voor SaaS- of pay‑per‑use‑scenario's. Ze volgen het verbruik en factureren op basis van daadwerkelijk gebruik.

### Stap 1: Initialiseer het Metered‑object

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Stap 2: Stel de publieke en private sleutels in

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Stap 3: Voer uw beeldverwerking uit

```csharp
// Your image processing logic here
```

### Stap 4: Haal verbruiksinformatie op

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Stap 5: Toon de verbruiksdetails

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Veelvoorkomend valkuil:** Als u vergeet `SetMeteredKey` aan te roepen, zal de API terugvallen op de proefmodus en ziet u watermerken in de output.

## Waarom de Aspose.Drawing-licentie correct instellen?

- **Verwijdert watermerken** die verschijnen in de proefmodus.  
- **Ontgrendelt premium API's** zoals geavanceerde beeldfilters en PDF-conversie.  
- **Zorgt voor naleving** van de licentievoorwaarden van Aspose voor commerciële distributie.  
- **Stelt metered facturering in**, zodat u alleen betaalt voor wat u gebruikt.

## Veelvoorkomende problemen en oplossingen

| Probleem | Oorzaak | Oplossing |
|----------|---------|-----------|
| “License file not found” error | Verkeerd pad of ontbrekend bestand in de outputmap | Gebruik een absoluut pad of stel de eigenschap *Copy to Output Directory* van het bestand in op *Copy always*. |
| Watermerk verschijnt nog steeds na het instellen van de licentie | Licentie niet geladen vóór de eerste API‑aanroep | Laad de licentie **vóór** elke Aspose.Drawing‑bewerking. |
| Metered verbruik is altijd nul | Sleutels niet ingesteld of verkeerde omgevingsvariabelen | Controleer de publieke/private sleutels en zorg voor internetconnectiviteit naar de metered‑server van Aspose. |

## Veelgestelde vragen

**Q1: Kan ik Aspose.Drawing zonder licentie gebruiken?**  
A1: Ja, een proeflicentie werkt voor ontwikkeling en evaluatie, maar voegt watermerken toe en beperkt enkele functies.

**Q2: Hoe vaak moet ik mijn Aspose.Drawing-licentie vernieuwen?**  
A2: Licenties zijn eeuwigdurend voor de aangeschafte versie. Vernieuwing is alleen nodig voor ondersteuning en upgrades.

**Q3: Wat is metered-licensing en wanneer moet ik het gebruiken?**  
A3: Metered-licensing brengt kosten in rekening op basis van gebruik (operaties of verwerkte data). Het is perfect voor cloudservices of pay‑per‑use‑modellen.

**Q4: Kan ik Aspose.Drawing gebruiken in commerciële projecten?**  
A4: Absoluut—zodra u een geldige licentie heeft, kunt u Aspose.Drawing in elke commerciële applicatie integreren.

**Q5: Waar kan ik community‑ondersteuning vinden voor Aspose.Drawing?**  
A5: Bezoek het [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) voor community‑hulp, voorbeelden en discussies.

## Conclusie

Het beheersen van het **instellen van de Aspose.Drawing-licentie**—of dit nu vanuit een bestand, een stream, of via metered usage gebeurt—zorgt ervoor dat u het maximale uit deze krachtige .NET‑grafiekbibliotheek haalt. Volg de bovenstaande stappen, let op de veelvoorkomende valkuilen, en u bent klaar om robuuste beeldverwerkingsoplossingen te bouwen zonder licentie‑obstakels.

---

**Laatst bijgewerkt:** 2026-02-09  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}