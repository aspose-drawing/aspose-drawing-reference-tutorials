---
date: 2026-02-09
description: Lär dig hur du ställer in Aspose.Drawing-licens i .NET. Bemästra licensieringsmetoder
  för att låsa upp alla funktioner utan vattenstämplar.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Ställ in Aspose.Drawing-licens – Hur du ställer in Aspose.Drawing-licens
url: /sv/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ställ in Aspose.Drawing-licens

## Introduktion

Om du bygger .NET‑applikationer som förlitar sig på kraftfull grafik och bildmanipulering, **att ställa in en Aspose.Drawing‑licens** är det första steget för att ta bort utvärderingsbegränsningar och få tillgång till hela funktionsuppsättningen. I den här handledningen kommer du att lära dig tre praktiska sätt att ställa in Aspose.Drawing‑licensen—laddning från en fil, laddning från en ström och användning av den meterbaserade modellen—så att du kan integrera biblioteket med förtroende.

## Snabba svar
- **Vad är det primära sättet att aktivera Aspose.Drawing?** Ladda en licensfil med `License.SetLicense("Aspose.Drawing.lic")`.
- **Kan jag tillämpa en licens vid körning?** Ja, du kan ladda licensen från en `Stream` för dynamiska scenarier.
- **Stöds en meterbaserad licens?** Absolut; använd `Metered.SetMeteredKey(publicKey, privateKey)` för att aktivera konsumtionsbaserad fakturering.
- **Behöver jag en licens för utvecklingsbyggen?** En provlicens fungerar för testning, men en giltig licens tar bort vattenstämplar och låser upp alla API:er.
- **Vilka .NET‑versioner är kompatibla?** Aspose.Drawing stödjer .NET Framework 4.x, .NET Core 3.1+ och .NET 5/6+.

## Förutsättningar

Innan du börjar, se till att du har:

- **Aspose.Drawing Library** – ladda ner det senaste paketet från [här](https://releases.aspose.com/drawing/net/).
- **License File** – skaffa en giltig `.lic`‑fil från [Aspose](https://purchase.aspose.com/buy).
- **.NET Development Environment** – Visual Studio, Rider eller någon IDE som riktar sig mot .NETFramework/.NETCore.

## Importera namnområden

Vi behöver de standard .NET‑namnutrymmena plus Aspose.Drawing‑namnutrymmet för licensiering. Lägg till följande `using`‑satser högst upp i din C#‑fil:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Laddar licens från en fil

Att ladda en licens från en fil är det mest enkla tillvägagångssättet. Följ dessa tre steg:

### Steg 1: Initiera licensobjektet

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Steg 2: Ställ in licensen från `.lic`‑filen

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Steg 3: Bekräfta framgång

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro tip:** Placera `.lic`‑filen i samma mapp som din körbara fil eller ange en absolut sökväg för att undvika felmeddelandet “file not found”.

## Laddar licens från en ström

När din licensfil är inbäddad som en resurs eller hämtas från en fjärrplats, ger laddning från en `Stream` dig flexibilitet.

### Steg 1: Initiera licensobjektet

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Steg 2: Ladda licensen med en `FileStream`

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Steg 3: Bekräfta framgång

```csharp
Console.WriteLine("License set successfully.");
```

> **Warning:** Kom ihåg att disponera `FileStream` (eller använda ett `using`‑block) för att frigöra filhandtag.

## Användning av mätlicens

Meterbaserad licensiering är idealisk för SaaS‑ eller pay‑per‑use‑scenarier. Den spårar konsumtion och fakturerar dig baserat på faktisk användning.

### Steg 1: Initiera det meterbaserade objektet

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Steg 2: Ställ in offentliga och privata nycklar

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Steg 3: Utför din bildbehandling

```csharp
// Your image processing logic here
```

### Steg 4: Hämta konsumtionsinformation

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Steg 5: Visa konsumtionsdetaljer

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Common pitfall:** Om du glömmer att anropa `SetMeteredKey` kommer API:et att återgå till provläge och du kommer att se vattenstämplar i resultatet.

## Varför ställa in Aspose.Drawing-licensen korrekt?

- **Tar bort vattenstämplar** som visa i provläge.
- **Låser upp premium‑API:er** såsom avancerade bildfilter och PDF‑konvertering.
- **Säkerställer efterlevnad** av Asposes licensvillkor för kommersiell distribution.
- **Möjliggör meterbaserad fakturering**, så att du bara betalar för det du använder.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|-------|-----|
| "Licensfil hittades inte"-fel | Fel sökväg eller saknad fil i utdata‑mappen | Använd en absolut sökväg eller sätt filer *Kopiera till utdatakatalog*-egenskap till *Kopiera alltid*. |
| Vattenstämpel visa fortfarande efter licensinställning | Licensen har inte laddats innan första API‑anropet | Ladda licensen **innan** någon Aspose.Drawing-operation. |
| Meterad konsumtion alltid noll | Nycklarna är inte satta eller fel miljövariabler | Verifiera offentliga/privata nycklar och säkerställt internetanslutning till Asposes meterade server. |

## Vanliga frågor

**Q1: ​​Kan jag använda Aspose.Drawing utan licens?**
A1: Ja, en provlicens fungerar för utveckling och utvärdering, men den lägger till vattenstämplar och begränsar vissa funktioner.

**Q2: Hur ofta måste jag förnya min Aspose.Drawing‑licens?**
A2: Licensgivaren är eviga för den köpta versionen. Förnyelse krävs endast för support och uppgraderingar.

**Q3: Vad är meterbaserad licensiering, och när bör jag använda den?**
A3: Meterbaserad licensiering debiterar baserat på användning (operationer eller data som bearbetas). Den är perfekt för molntjänster eller pay-per-use-modeller.

**Q4: Kan jag använda Aspose.Drawing i kommersiella projekt?**
A4: Absolut—när du har en giltig licens kan du bädda i Aspose.Drawing i vilken kommersiell applikation som helst.

**F5: Var kan jag hitta community‑support för Aspose.Drawing?**
A5: Besök [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) för gemenskapshjälp, exempel och diskussioner.

## Slutsats

Att behärska hur man **ställer in Aspose.Drawing‑licensen**—oavsett om det är från en fil, en ström eller via meterbaserad användning—säkerställer att du får ut det mesta av detta kraftfulla .NET‑grafikbibliotek. Följ stegen ovan, håll utkik efter vanliga fallgropar, så är du redo att bygga robusta bildbehandlingslösningar utan licensrelaterade hinder.

---

**Senast uppdaterad:** 2026-02-09
**Testat med:** Aspose.Drawing 24.11 för .NET
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}