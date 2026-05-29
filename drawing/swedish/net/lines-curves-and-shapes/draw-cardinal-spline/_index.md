---
date: 2026-05-29
description: Lär dig hur du sparar PNG och ritar kardinalsplines i .NET med Aspose.Drawing.
  Spara kurvan som PNG, skapa mjuk grafik och generera bitmap till fil utan ansträngning.
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: Rita kardinalsplines i Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hur du sparar PNG och ritar kardinalsplines med Aspose.Drawing
url: /sv/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man sparar PNG och ritar kardinalsplines med Aspose.Drawing

## Introduktion

I den här handledningen kommer du att upptäcka **hur man sparar PNG**‑filer medan du ritar jämna kardinalsplines med Aspose.Drawing för .NET. Oavsett om du bygger en diagramkomponent, en diagramredigerare eller helt enkelt behöver exportera en anpassad kurva som PNG, så guidar stegen nedan dig genom att skapa en bitmap‑canvas, rita en spline med en penna och spara resultatet till disk. Du kommer också att se varför Aspose.Drawing är ett pålitligt plattformsoberoende alternativ till System.Drawing.Common.

## Snabba svar
- **Vad gör huvudmetoden?** `Graphics.DrawCurve` interpolerar en serie punkter till en jämn kardinalspline.  
- **Vilket format används för att spara bilden?** PNG via `Bitmap.Save`.  
- **Behöver jag en licens för att spara bilder?** En provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Kan jag ändra kurvans spänning?** Ja, överlagringar av `DrawCurve` låter dig ange spänning.  
- **Är Aspose.Drawing kompatibel med .NET 6+?** Absolut – den stödjer .NET Framework och .NET Core/5/6.

## Vad betyder “hur man sparar PNG” i samband med Aspose.Drawing?

Att spara en PNG innebär att konvertera den bitmap i minnet som du ritar på till en fysisk PNG‑fil på disk. Processen skriver pixeldata med förlustfri komprimering, vilket bevarar de exakta färgerna och eventuell alfa‑kanalinformation. Aspose.Drawings `Bitmap.Save`‑metod hanterar PNG‑kodningen automatiskt, så du behöver inte hantera formatdetaljerna själv.

## Varför rita en kardinalspline med Aspose.Drawing?

En kardinalspline skapar en jämn, flytande kurva som följer en uppsättning kontrollpunkter nära, vilket gör den perfekt för datavisualiseringar, UI‑grafik och anpassade former. Aspose.Drawing stödjer **30+ bildformat** och kan rendera grafik med hundratals sidor utan att ladda hela filen i minnet, vilket ger både hastighet och flexibilitet.

## Förutsättningar

Innan vi dyker ner, se till att du har:

- Visual Studio (valfri nyare version) installerad.  
- Aspose.Drawing för .NET‑biblioteket. Du kan ladda ner det [här](https://releases.aspose.com/drawing/net/).  
- Grundläggande kunskap i C#‑programmering.

## Importera namnrymder

I din C#‑fil, börja med att importera den nödvändiga namnrymden:

`Aspose.Drawing`‑namnrymden innehåller alla kärntyper såsom `Bitmap`, `Graphics` och `Pen`.  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## Steg 1: Skapa en Bitmap (duk)

Först, skapa en bitmap som kommer att fungera som duk för din ritning. Denna bitmap är där splinen renderas innan du **sparar bilden**.

Bitmap representerar en bild i minnet med ett definierat pixelformat och dimensioner.  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Steg 2: Skapa ett Graphics‑objekt

Nästa steg, hämta ett `Graphics`‑objekt från bitmapen. Detta objekt tillhandahåller ritningsytan.

Graphics ger en ritningsyta för att rendera former, text och bilder på en bitmap.  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Steg 3: Definiera Pen och rita kurva

Definiera en `Pen` med önskad färg och bredd, och rita sedan den kardinalspline med `DrawCurve`. Detta demonstrerar tekniken **draw curve with pen** och fungerar som ett **cardinal spline‑exempel**.

Pen kapslar in färg, bredd och linjestil som används för att rita linjer och kurvor.  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## Steg 4: Spara bilden (Spara kurva som PNG)

Slutligen, spara bitmapen till en PNG‑fil. Detta är kärnan i **hur man sparar PNG** i den här handledningen.

`Bitmap.Save` skriver bilden till en fil i det angivna formatet, exempelvis PNG.  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **Proffstips:** Använd `Path.Combine` för att bygga filsökvägar säkert över plattformar.

Grattis! Du har framgångsrikt ritat en kardinalspline och sparat resultatet som en PNG‑bild med Aspose.Drawing för .NET. Känn dig fri att experimentera med olika punktarrayer, pen‑färger eller linjebredder för att anpassa dina kurvor.

## Vanliga användningsområden

- **Datavisualiseringar** – jämna linjediagram som kräver precisa kontrollpunkter.  
- **Anpassade UI‑komponenter** – rita rattar, reglage eller dekorativa ramar.  
- **Exportbar grafik** – generera PNG‑tillgångar i farten för rapporter eller webb­innehåll.

## Felsökning & Tips

- **Bilden visas tom?** Säkerställ att bitmapens pixelformat stödjer alfa (`Format32bppPArgb`) och att du anropar `graphics.Clear(Color.Transparent)` om det behövs.  
- **Oväntad kurvform?** Justera spänningsparametern genom att använda överlagringen `DrawCurve(pen, points, tension)`.  
- **Filåtkomstfel?** Verifiera att mål‑katalogen finns och att din applikation har skrivbehörighet.

## Vanliga frågor

**Q1: Kan jag använda Aspose.Drawing för kommersiella projekt?**  
A1: Ja, Aspose.Drawing är lämplig för både personliga och kommersiella projekt. Kontrollera licensdetaljerna på den [köpsidan](https://purchase.aspose.com/buy).

**Q2: Hur kan jag få en tillfällig licens för testning?**  
A2: Skaffa en tillfällig licens för teständamål [här](https://purchase.aspose.com/temporary-license/).

**Q3: Var kan jag hitta ytterligare support?**  
A3: Besök [Aspose.Drawing‑forumet](https://forum.aspose.com/c/drawing/44) för community‑support och diskussioner.

**Q4: Finns det en gratis provversion?**  
A4: Ja, utforska funktionerna med [gratis provversion](https://releases.aspose.com/) innan du köper.

**Q5: Hur får jag åtkomst till dokumentationen?**  
A5: Se den omfattande [dokumentationen](https://reference.aspose.com/drawing/net/) för detaljerad information och exempel.

---

**Senast uppdaterad:** 2026-05-29  
**Testat med:** Aspose.Drawing 24.11 för .NET  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Save Bitmap as PNG & Draw Closed Curves with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Save Bitmap C# – Draw Bezier Splines with Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Save Bitmap as PNG with Solid Brushes in Aspose.Drawing](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}