---
date: 2025-11-30
description: Lär dig hur du tillämpar koordinatsystemstransformation, ritar rektangel‑bitmap
  och transformerar sidor med Aspose.Drawing för .NET.
language: sv
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Koordinatsystemtransformation (Sidtransformation) i Aspose.Drawing för .NET
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Koordinatsystemtransformation (Sidtransformation) i Aspose.Drawing för .NET

## Introduktion

Välkommen! I den här handledningen kommer du att upptäcka **hur man utför en koordinatsystemtransformation** på en sida med Aspose.Drawing för .NET. Oavsett om du behöver **draw rectangle bitmap**-objekt, skala ritningar eller helt enkelt mappa sidunitar till enhetsunitar, så kommer stegen nedan att guida dig genom hela processen—klara, koncisa och redo att kopiera‑klistra in i ditt projekt.

## Snabba svar
- **Vad är den primära klassen för ritning?** `Graphics` from Aspose.Drawing.
- **Hur ställer jag in sidunitar?** Use `graphics.PageUnit = GraphicsUnit.Inch;`.
- **Kan jag rita en rektangel på en transformerad sida?** Yes—create a `Pen` and call `DrawRectangle`.
- **Var sparas resultatet?** To the folder you specify in `bitmap.Save`.
- **Behöver jag en licens för produktion?** A valid Aspose.Drawing license is required for commercial use.

## Vad är koordinatsystemtransformation?

En **coordinate system transformation** ändrar hur logiska sidkoordinater (som tum eller millimeter) mappar till fysiska enhetskoordinater (pixlar). Genom att justera transformationen kan du kontrollera skalning, rotation och förflyttning av alla ritningsoperationer, vilket gör det enklare att designa grafik som är upplösningsoberoende.

## Varför använda Aspose.Drawing för sidtransformationer?

- **Full .NET-kompatibilitet** – fungerar med .NET Framework, .NET Core och .NET 5/6.
- **Rik grafik-API** – erbjuder samma funktionalitet som System.Drawing.Common utan plattformsrestriktioner.
- **Enkel enhetshantering** – växla mellan tum, millimeter, punkter osv. med en enda egenskap.
- **Högkvalitativt resultat** – generera PNG, JPEG, BMP och andra format med exakt kontroll.

## Förutsättningar

Innan vi dyker ner, se till att du har:

- **Aspose.Drawing Library** – ladda ner den senaste versionen från den officiella webbplatsen [here](https://releases.aspose.com/drawing/net/).
- **Utvecklingsmiljö** – Visual Studio (valfri edition) eller en annan .NET-IDE.
- **Skrivbehörighet** – en mapp på din maskin där den transformerade bilden kommer att sparas (ersätt `"Your Document Directory"` i koden med den faktiska sökvägen).

Nu när vi är klara, låt oss gå igenom varje steg.

## Importera namnrymder

Först, importera den nödvändiga namnrymden:

```csharp
using System.Drawing;
```

> *Varför detta är viktigt*: `System.Drawing` innehåller `Bitmap`, `Graphics`, `Pen` och färgstrukturer som vi kommer att använda genom hela handledningen.

## Steg 1: Skapa en Bitmap

Skapa en tom duk som kommer att hysa den transformerade ritningen. Vi specificerar en storlek på **1000 × 800 pixlar** och ett pixelformat som stödjer alfa‑transparens.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> Denna bitmap fungerar som ritningsytan. Det valda pixelformatet (`Format32bppPArgb`) säkerställer högkvalitativ rendering med förmultiplicerad alfa.

## Steg 2: Skapa ett Graphics-objekt

Ett `Graphics`-objekt tillhandahåller ritningsmetoderna (linjer, former, text). Vi får det från den bitmap vi just skapade.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> `Graphics`-objektet är kärnan i alla renderingsoperationer; det respekterar de transformationsinställningar vi kommer att applicera härnäst.

## Steg 3: Rensa duken

Innan du ritar något, rensa duken till en neutral bakgrundsfärg (grå i detta exempel). Detta steg visar också hur man fyller hela bitmapen med en solid färg.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Steg 4: Ställ in transformation (Applicera sidtransformation)

Här **applicerar vi sidtransformationen** genom att sätta `PageUnit` till inches. Detta talar om för grafikmotorn att tolka alla efterföljande koordinater som tum istället för pixlar.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *Tips*: Att ändra `PageUnit` är ett enkelt sätt att **how to transform page** koordinater utan att manuellt beräkna pixelvärden.

## Steg 5: Rita en rektangel (Draw rectangle bitmap)

Nu ritar vi en rektangel som mäter **1 tum × 1 tum** på position (1, 1) tum. `Pen`-bredden är satt till `0.1f` tum, vilket ger en tunn men synlig linje.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> Det demonstrerar **draw rectangle bitmap** efter att transformationen har applicerats—observera hur rektangelns storlek definieras i tum, inte pixlar.

## Steg 6: Spara bilden

Slutligen, spara den transformerade bitmapen till disk. Ersätt `"Your Document Directory"` med den faktiska sökvägen på din maskin.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> Utdatafilen (`PageTransformation_out.png`) kommer att innehålla rektangeln som ritats med den koordinatsystemtransformation vi satte tidigare.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|-------|----------|
| **Bild visas tom** | Duken har inte rensats eller ritning utfördes utanför det synliga området. | Verifiera `graphics.PageUnit` och koordinatvärden; säkerställ att rektangeln ligger inom bitmapens gränser. |
| **Felaktig skalning** | Använder fel `GraphicsUnit`. | Dubbelkolla att `graphics.PageUnit` matchar den enhet du avser (t.ex. `GraphicsUnit.Inch`). |
| **Fel i filsökväg** | Saknad katalog eller ogiltiga tecken. | Skapa målmappen i förväg eller använd `Path.Combine` för att bygga sökvägen på ett säkert sätt. |

## Vanliga frågor

**Q: Kan jag använda Aspose.Drawing gratis?**  
A: Aspose.Drawing erbjuder en gratis provversion som du kan komma åt [here](https://releases.aspose.com/).

**Q: Var kan jag hitta detaljerad dokumentation för Aspose.Drawing?**  
A: Dokumentationen finns tillgänglig [here](https://reference.aspose.com/drawing/net/).

**Q: Hur kan jag få support för Aspose.Drawing?**  
A: För support, besök [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17).

**Q: Finns en tillfällig licens tillgänglig för Aspose.Drawing?**  
A: Ja, du kan få en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag köpa Aspose.Drawing?**  
A: Du kan köpa Aspose.Drawing [here](https://purchase.aspose.com/buy).

## Slutsats

Du har nu lärt dig hur man **applierar en koordinatsystemtransformation**, **draw rectangle bitmap**-objekt, och **sparar resultatet** med Aspose.Drawing för .NET. Dessa byggstenar låter dig skapa upplösningsoberoende grafik, perfekt för rapporter, UI-element eller någon situation där exakt storlek är viktigt. Experimentera med andra `GraphicsUnit`-värden (som `Millimeter` eller `Point`) för att se hur de påverkar dina ritningar.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Senast uppdaterad:** 2025-11-30  
**Testad med:** Aspose.Drawing 24.11 for .NET  
**Författare:** Aspose