---
date: 2026-02-19
description: Lär dig hur du ritar banor och förenar banor med pennor i Aspose.Drawing,
  och sedan sparar bilden som PNG med enkel C#‑kod.
linktitle: Joining Paths with Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hur man ritar en bana och sammanfogar banor med pennor i Aspose.Drawing
url: /sv/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ritar Path och förenar Paths med Pens i Aspose.Drawing

## Introduktion

Välkommen till världen av **Aspose.Drawing for .NET**! I den här handledningen kommer du att upptäcka **how to draw path**‑objekt, förena dem med olika line‑join‑stilar och slutligen **spara bilden som PNG**. Oavsett om du bygger ett rapportverktyg, en designredigerare eller bara behöver skarpa vektorgrafik, ger dig behärskning av path‑ritning med pens fin kontroll över den visuella utdata.

## Snabba svar
- **Vad betyder “draw path”?** Det skapar vektorbaserade linje‑ eller formdefinitioner som ett `Graphics`‑objekt kan rendera.  
- **Vilka line‑joins finns tillgängliga?** `Bevel`, `Miter`, `Round` och `BevelClipped`.  
- **Kan jag exportera resultatet som PNG?** Ja—använd `Bitmap.Save` med en `.png`‑extension.  
- **Behöver jag en licens?** En provversion fungerar för utvärdering; en kommersiell licens krävs för produktion.  
- **Vilka .NET‑versioner stöds?** .NET Framework 4.6+, .NET Core 3.1+ och .NET 6+.

## Vad är “how to draw path” i Aspose.Drawing?

Att rita en path betyder att konstruera ett `GraphicsPath` som innehåller en serie linjer, kurvor eller former. När pathen är byggd målar du den på en `Graphics`‑yta med en `Pen`. Detta tillvägagångssätt är mer flexibelt än att rita enskilda linjer eftersom du kan applicera transformationer, clipping och olika join‑stilar på hela formen.

## Varför använda Aspose.Drawing för att förena banor?

- **Full .NET‑kompatibilitet** – fungerar på Windows, Linux och macOS.  
- **Rika line‑join‑alternativ** – skapa avfasade, rundade eller miterade hörn med en enda egenskap.  
- **Högkvalitativ rasterutdata** – spara direkt till PNG, JPEG, BMP osv., utan extra konverteringssteg.  
- **Inga GDI+‑begränsningar** – idealiskt för server‑sid rendering där `System.Drawing.Common` kan vara begränsad.

## Förutsättningar

Innan vi dyker ner i koden, se till att du har:

1. **Aspose.Drawing Library** – ladda ner den **[here](https://releases.aspose.com/drawing/net/)**.  
2. **.NET Development Environment** – Visual Studio, VS Code eller någon IDE som stödjer C#.

Nu när allt är klart, låt oss gå igenom varje steg.

## Importera namnrymder

Lägg till de nödvändiga namnrymderna högst upp i din fil så att kompilatorn vet var den ska hitta grafikklasserna:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Steg 1: Skapa en Bitmap och Graphics‑objekt

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Vi börjar med en tom canvas (`Bitmap`) med storleken 1000 × 800 pixlar och får ett `Graphics`‑objekt som kommer att rendera våra ritkommandon.

## Steg 2: Definiera DrawPath‑metoden

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

Denna hjälpfunktion kapslar in ritlogiken:

- **Pen** – anger färg och tjocklek (30 px).  
- **GraphicsPath** – definierar två sammankopplade linjer som bildar en “L”-form.  
- **LineJoin** – styr hur hörnet mellan de två linjerna renderas (`Bevel`, `Round`, osv.).  

Du kan anropa den här metoden med vilket `LineJoin`‑värde som helst för att se den visuella skillnaden.

## Steg 3: Förena banor med Bevel LineJoin

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

Att använda `LineJoin.Bevel` skapar ett plattat hörn där de två linjerna möts.

## Steg 4: Förena banor med Round LineJoin

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

`LineJoin.Round` ger ett mjukt, rundat hörn—perfekt för ett mer polerat utseende.

## Steg 5: Spara resultatet som PNG

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

`Save`‑anropet skriver bitmapen till en fil i PNG‑format. Anpassa sökvägen så att den matchar din miljö.

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|-------|----------------|-----|
| **Bild visas tom** | Grafik‑objektet rensades inte eller bitmap‑storleken är för liten. | Anropa `graphics.Clear(Color.White);` innan du ritar, eller öka bitmap‑dimensionerna. |
| **Hörnet ser hackigt ut** | Användning av en lågupplöst bitmap med en tjock penna. | Öka bitmap‑DPI (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) eller minska pen‑bredden. |
| **Fil‑ej‑hittad‑fel** | Ogiltig spar‑sökväg. | Använd `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## Vanliga frågor

### Q1: Kan jag använda Aspose.Drawing gratis?

A1: Aspose.Drawing är en kommersiell produkt, men du kan utforska dess funktioner med en **[free trial](https://releases.aspose.com/)**.

### Q2: Var kan jag hitta Aspose.Drawing‑dokumentationen?

A2: Se **[documentation](https://reference.aspose.com/drawing/net/)** för omfattande vägledning.

### Q3: Hur kan jag få support för Aspose.Drawing?

A3: Besök **[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)** för gemenskaps‑hjälp och officiell support.

### Q4: Finns tillfälliga licenser för Aspose.Drawing?

A4: Ja, du kan skaffa en **[temporary license](https://purchase.aspose.com/temporary-license/)** för korttidsanvändning.

### Q5: Var kan jag köpa Aspose.Drawing?

A5: Köp Aspose.Drawing **[here](https://purchase.aspose.com/buy)**.

## Slutsats

I den här guiden gick vi igenom **how to draw path**‑objekt, använde olika `LineJoin`‑stilar och sparade den slutliga grafiken som en PNG‑fil med Aspose.Drawing för .NET. Genom att behärska dessa steg kan du skapa sofistikerade vektorgrafik, anpassade ikoner eller dynamiska diagram direkt från din server‑sid kod.

---

**Senast uppdaterad:** 2026-02-19  
**Testad med:** Aspose.Drawing 24.11 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}