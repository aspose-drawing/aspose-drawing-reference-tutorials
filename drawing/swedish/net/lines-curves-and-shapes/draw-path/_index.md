---
date: 2026-07-22
description: Lär dig hur du sparar bitmap som PNG och exporterar bild till JPEG med
  Aspose.Drawing. En steg‑för‑steg‑guide visar hur man ritar banor, skapar bilder
  och exporterar format.
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: Rita banor i Aspose.Drawing
og_description: Spara bitmap som PNG och exportera bild till JPEG med Aspose.Drawing
  för .NET. Följ den här handledningen för att rita komplexa banor, skapa högkvalitativa
  bilder och producera flera format.
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: Spara bitmap som PNG – Rita banor med Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: Spara bitmap som PNG – Använda GraphicsPath i Aspose.Drawing
url: /sv/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Rita banor i Aspose.Drawing

## Hur man använder GraphicsPath – Introduktion

**Save bitmap as PNG** är ofta det första steget när du behöver en förlustfri bild för vidare bearbetning eller publicering. I den här handledningen kommer du att lära dig hur du ritar sofistikerade vektorbanor med `GraphicsPath`, renderar dem på en bitmap, och sedan **save bitmap as PNG** eller till och med **export image to JPEG**. Oavsett om du bygger en rapportmotor, ett anpassat diagrambibliotek, eller helt enkelt behöver generera dynamisk grafik, ger Aspose.Drawing dig ett fullt hanterat, plattformsoberoende API som ersätter System.Drawing.Common.

## Snabba svar
- **What can I draw with GraphicsPath?** Linjer, rektanglar, ellipser, kurvor och anpassade former.  
- **Do I need a license?** En provversion är gratis; en kommersiell licens krävs för produktion.  
- **Which .NET versions are supported?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Is System.Drawing.Common required?** Nej, Aspose.Drawing fungerar självständigt.  
- **Can I save to different formats?** Ja – PNG, JPEG, BMP, GIF och mer.

## Vad är GraphicsPath?
`GraphicsPath` är Aspose.Drawings vektorkontainer som lagrar en sekvens av ritningsprimitiver såsom linjer, bågar och kurvor som ett enda objekt. Genom att gruppera dessa primitiv kan du tillämpa transformationer, fyllningsregler och linjestilar enhetligt, vilket förenklar skapandet av komplex grafik och säkerställer konsekvent rendering över olika utdataformat.

## Varför använda GraphicsPath med Aspose.Drawing?
Att använda GraphicsPath med Aspose.Drawing ger dig precisa, flexibla och högpresterande vektorritningsmöjligheter. Det låter dig bygga komplexa former, tillämpa transformationer och rendera dem effektivt, samtidigt som du behåller plattformsoberoende konsistens och stöd för storskalig bildbehandling. Dessutom integreras det sömlöst med andra .NET‑bibliotek, vilket gör att du kan kombinera raster‑ och vektorarbetsflöden i en enda applikation.

- **Precision:** Hanterar 50+ vektorprimitiver med sub‑pixel‑noggrannhet, vilket säkerställer att när du **save bitmap as PNG** förblir utdata skarpa i alla upplösningar.  
- **Flexibility:** Kombinera linjer, bågar och Bezier‑kurvor till en bana, och rendera den med ett enda anrop till `Graphics.DrawPath`.  
- **Performance:** Optimerad renderingspipeline bearbetar bilder upp till 400 MP utan att ladda hela filen i minnet, vilket gör storskaliga batchjobb möjliga.  
- **Cross‑Platform:** Identiska resultat på Windows, Linux och macOS‑körningar, vilket eliminerar plattforms‑specifika buggar.

## Förutsättningar

Innan du dyker ner i handledningen, se till att du har följande förutsättningar:

- **Aspose.Drawing Library:** Ladda ner och installera Aspose.Drawing‑biblioteket. Du kan hitta biblioteket [here](https://releases.aspose.com/drawing/net/).
- **Other Aspose Products:** Utforska ytterligare Aspose‑produkter [here](https://releases.aspose.com/).
- **Development Environment:** Ställ in din .NET‑utvecklingsmiljö med nödvändiga verktyg (Visual Studio, .NET SDK, etc.).

## Importera namnrymder

Börja med att importera de nödvändiga namnrymderna i ditt projekt:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Steg 1: Skapa Bitmap och Graphics

Bitmap representerar en bild i minnet, medan Graphics tillhandahåller ritningsmetoder för att rendera på den bilden. Börja med att skapa ett `Bitmap`‑objekt och ett `Graphics`‑objekt att arbeta med. Denna bitmap blir duken där `GraphicsPath` renderas, och senare kommer du att **save bitmap as PNG**:

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## Steg 2: Definiera Pen och GraphicsPath

Pen definierar linjefärg, bredd och stil; GraphicsPath lagrar en samling ritningsprimitiver som ett enda vektorobjekt. Nästa steg är att definiera en `Pen` för att ange ritningsattribut och skapa en `GraphicsPath`. `GraphicsPath`‑objektet innehåller vektordatan innan den ritas:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## Steg 3: Lägg till linjer och former

AddLine, AddRectangle och AddEllipse lägger till respektive former i GraphicsPath för senare rendering. Lägg till linjer, rektanglar och ellipser i `GraphicsPath` för att skapa en komplex bana. Du kan också lägga till anpassade Bezier‑kurvor för släta former:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## Steg 4: Rita bana

DrawPath renderar vektordatan från en GraphicsPath på Graphics‑ytan med den angivna Pen. Rita banan på `Graphics`‑objektet med den angivna `Pen`. Denna operation rasteriserar vektordatan på bitmap‑duken:

```csharp
graphics.DrawPath(pen, path);
```

## Steg 5: Spara bild – Exportera till PNG eller JPEG

Bitmap.Save‑metoden skriver bilden till disk i det valda formatet, t.ex. PNG eller JPEG. Efter ritning kan du **save bitmap as PNG** för förlustfri kvalitet eller **export image to JPEG** för mindre filstorlek. Välj det format som bäst passar ditt efterföljande scenario:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

Upprepa dessa steg efter behov för att skapa komplexa och visuellt tilltalande banor.

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Banan syns inte** | Se till att Pen‑färgen kontrasterar mot bakgrunden och att bitmapen sparas korrekt. |
| **Oväntad bildstorlek** | Verifiera att bitmapens dimensioner och pixelformat matchar dina krav. |
| **Licensundantag** | Använd en provlicens för testning; tillämpa en giltig licens innan du går i produktion. |

## Vanliga frågor

### Q1: Kan jag använda Aspose.Drawing med andra .NET‑bibliotek?

A1: Ja, Aspose.Drawing integreras sömlöst med andra .NET‑bibliotek, vilket ger mångsidighet i dina utvecklingsprojekt.

### Q2: Finns det en provversion tillgänglig?

A2: Ja, du kan komma åt den kostnadsfria provversionen [here](https://releases.aspose.com/).

### Q3: Var kan jag hitta support för Aspose.Drawing?

A3: Besök Aspose.Drawing‑[forum](https://forum.aspose.com/c/drawing/44) för hjälp och gemenskapsstöd.

### Q4: Hur får jag en tillfällig licens?

A4: Skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

### Q5: Kan jag köpa Aspose.Drawing?

A5: Ja, du kan köpa Aspose.Drawing [here](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Kan jag rita anpassade Bezier‑kurvor med GraphicsPath?**  
A: Absolut – använd `path.AddBezier(...)` för att definiera släta kurvor.

**Q: Hur rensar jag en GraphicsPath innan jag återanvänder den?**  
A: Anropa `path.Reset()` för att ta bort alla figurer och börja om.

## Slutsats

Grattis! Du har framgångsrikt lärt dig **how to use GraphicsPath** för att rita banor och sedan **save bitmap as PNG** eller **export image to JPEG** med Aspose.Drawing för .NET. Denna handledning täckte skapandet av en bitmap, definition av en pen, konstruktion av en `GraphicsPath`, rendering av olika former och export av den slutgiltiga bilden i flera format. Experimentera med olika koordinater, färger och linjebredder för att frigöra Aspose.Drawings fulla kreativa potential.

---

**Senast uppdaterad:** 2026-07-22  
**Testat med:** Aspose.Drawing 24.12 för .NET  
**Författare:** Aspose

## Relaterade handledningar

- [Spara bitmap som PNG & rita slutna kurvor med Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Spara bitmap C# – rita Bezier‑splines med Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Hur man sparar bild och ritar kardinal‑splines i Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}