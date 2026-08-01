---
date: 2026-08-01
description: Lär dig hur du lägger till callouts till bilder med Aspose.Drawing för
  .NET – step‑by‑step guide med code placeholders, tips och FAQs.
keywords:
- how to add callouts
- Aspose.Drawing callout tutorial
- .NET image annotation
lastmod: 2026-08-01
linktitle: Skapa callouts i Aspose.Drawing
og_description: Upptäck hur du lägger till callouts i Aspose.Drawing för .NET. Denna
  tutorial täcker prerequisites, step‑by‑step implementation, tips och FAQs för utvecklare.
og_image_alt: Screenshot showing callout annotation on an image using Aspose.Drawing
og_title: Hur man lägger till callouts med Aspose.Drawing för .NET – Quick Guide
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to add callouts to images using Aspose.Drawing for .NET –
    step‑by‑step guide with code placeholders, tips, and FAQs.
  headline: How to Add Callouts with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, Aspose.Drawing supports a wide range of drawing operations for diagrams,
      charts, and custom graphics beyond simple callouts.
    question: Can I use Aspose.Drawing for other types of illustrations?
  - answer: Absolutely! Aspose.Drawing handles PNG, JPEG, GIF, BMP, TIFF, and many
      more formats.
    question: Is Aspose.Drawing compatible with different image formats?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find more examples and documentation?
  - answer: Visit the [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44)
      for community assistance and official support.
    question: How do I get support if I encounter issues?
  - answer: Certainly! Get started with a free trial [here](https://releases.aspose.com/).
    question: Can I try Aspose.Drawing before purchasing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- callout
- Aspose.Drawing
- .NET graphics
- image annotation
title: Hur man lägger till callouts med Aspose.Drawing för .NET
url: /sv/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man lägger till förklarande textrutor med Aspose.Drawing för .NET

## Introduktion
Om du letar efter **hur man lägger till förklarande textrutor** i dina bilder eller diagram med Aspose.Drawing för .NET, har du hamnat på rätt ställe. I den här handledningen går vi igenom varje steg—från att ladda en bitmap, skapa en `Graphics`‑canvas, definiera förklarande textrutors geometri, till att rendera stylade förklarande textrutor—så att dina visuella element blir tydligare och mer informativa.

## Snabba svar
- **Vilket bibliotek behöver jag?** Aspose.Drawing för .NET (nedladdningsbart från den officiella webbplatsen).  
- **Vilka .NET‑versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Hur lång tid tar implementeringen?** Vanligtvis under 10 minuter för en grundläggande förklarande textruta.  
- **Kan jag anpassa färger och typsnitt?** Ja—allt styrs av standard‑GDI+‑objekt (Pen, Font, Brush).

## Vad är en förklarande textruta?
En förklarande textruta är en grafisk annotering som kombinerar en linje (eller pil) med en textetikett för att markera en specifik del av en bild. Den används ofta i tekniska diagram, skärmdumpar och presentationer för att rikta uppmärksamheten mot ett särskilt element, förklara en funktion eller ge måttinformation, vilket gör den visuella kommunikationen tydligare och mer effektiv.

## Varför använda Aspose.Drawing för förklarande textrutor?
Aspose.Drawing är byggt för högpresterande bildbehandling och stödjer ett brett spektrum av format, vilket gör det idealiskt för att lägga till förklarande textrutor i stora eller komplexa grafik. Dess minnes‑effektiva arkitektur kan hantera filer upp till **500 MB** utan att ladda hela bitmapen i RAM, och den erbjuder fin‑granulär kontroll över ritningsprimitiver, färger och textrendering, vilket säkerställer skarpa, professionellt utseende annoteringar.

## Förutsättningar
- Grundläggande kunskap i programmeringsspråket C#.  
- Aspose.Drawing‑biblioteket installerat. Du kan ladda ner det [här](https://releases.aspose.com/drawing/net/).  
- Ett dokument eller en bild där du vill lägga till förklarande textrutor.

## Importera namnrymder
Följande namnrymder ger dig åtkomst till de centrala ritningsklasserna:

`System.Drawing` tillhandahåller GDI+-typer såsom `Bitmap`, `Graphics`, `Pen`, `Font` och `Brush`. Importera dem innan du börjar koda.

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Hur man lägger till förklarande textrutor i Aspose.Drawing
Läs in din källbild, skapa en `Graphics`‑canvas, definiera start‑/slutpunkter och anropa en hjälpfunktion som ritar linjen, pilspetsen och etiketten—allt i några koncisa satser. Detta tillvägagångssätt fungerar för PNG-, JPEG-, BMP- och GIF‑filer och låter dig fullt ut anpassa färger, typsnitt och linjestilar.

## Steg 1: Ladda bilden
`Image` representerar en rasterbild och tillhandahåller metoder för att läsa in, spara och manipulera bitmap‑data. Börja med att läsa in bilden där du vill lägga till förklarande textrutor. Ersätt `"Your Document Directory"` och `"gears.png"` med din faktiska katalog och bildfilnamn.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Steg 2: Skapa Graphics‑objekt
`Graphics` tillhandahåller metoder för ritningsytan för att rendera former, text och bilder på en bitmap. Ett `Graphics`‑objekt från bilden låter dig utföra ritningsoperationer.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Steg 3: Definiera förklarande textrutors positioner
`PointF` definierar en punkt i tvådimensionellt utrymme med flyttalskoordinater. Ange start‑ (ankare) och slut‑ (etikett) punkter för varje förklarande textruta. Dessa koordinater måste ligga inom bildens gränser; annars kommer textrutan att klippas bort.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## Steg 4: Rita förklarande textrutor
Implementera metoden `DrawCallOut` för att rendera linjen, eventuell pilspets och textetiketten. Metoden använder `Pen` för linjen, `Font` för etiketten och `SolidBrush` för fyllningsfärger.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Steg 5: Spara bilden
Spara den annoterade bitmapen till disk. Du kan välja vilket som helst av de stödjade formaten, såsom PNG eller JPEG.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Källkod för att rita förklarande textrutor
Den fullständiga källkoden som binder ihop alla stegen finns i platshållaren nedan. Infoga dina egna implementationsdetaljer där det anges.

```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## Vanliga problem & tips
- **Felaktiga ankarkoordinater** – se till att start‑ och slutpunkterna ligger inom bildens gränser; annars kan förklarande textrutan klippas bort.  
- **Text som överlappar** – justera `spaceSize` eller teckenstorleken om etiketten kolliderar med annan grafik.  
- **Prestanda** – för mycket stora bilder, överväg att avyttra `Pen`-, `Font`- och `Brush`‑objekt efter användning för att frigöra resurser.

## Slutsats
Du har nu ett komplett, produktionsklart mönster för **hur man lägger till förklarande textrutor** i vilken bild som helst med Aspose.Drawing för .NET. Känn dig fri att experimentera med olika färger, linjestilar och teckensnittsfamiljer för att matcha ditt varumärke.

## Vanliga frågor

**Q: Kan jag använda Aspose.Drawing för andra typer av illustrationer?**  
A: Ja, Aspose.Drawing stödjer ett brett spektrum av ritningsoperationer för diagram, grafer och anpassad grafik utöver enkla förklarande textrutor.

**Q: Är Aspose.Drawing kompatibelt med olika bildformat?**  
A: Absolut! Aspose.Drawing hanterar PNG, JPEG, GIF, BMP, TIFF och många fler format.

**Q: Var kan jag hitta fler exempel och dokumentation?**  
A: Utforska den omfattande dokumentationen [här](https://reference.aspose.com/drawing/net/).

**Q: Hur får jag support om jag stöter på problem?**  
A: Besök [Aspose.Drawing‑forumet](https://forum.aspose.com/c/drawing/44) för gemenskapsstöd och officiell support.

**Q: Kan jag prova Aspose.Drawing innan jag köper?**  
A: Självklart! Kom igång med en gratis provversion [här](https://releases.aspose.com/).

---

**Senast uppdaterad:** 2026-08-01  
**Testat med:** Aspose.Drawing 24.11 för .NET  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Hur man ritar bågar och andra former med Aspose.Drawing för .NET](/drawing/net/lines-curves-and-shapes/)
- [Matrix‑transformationshandledning: Matrix‑transformeringar i Aspose.Drawing för .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [Hur man förenar banor med Pen i Aspose.Drawing .NET](/drawing/net/pens/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}