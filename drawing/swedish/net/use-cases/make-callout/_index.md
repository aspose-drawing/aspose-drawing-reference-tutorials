---
title: Göra bildtexter i Aspose.Drawing
linktitle: Göra bildtexter i Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternativ till System.Drawing.Common
description: Förbättra dina dokumentillustrationer med Aspose.Drawing för .NET! Lär dig steg för steg hur du lägger till bildtexter för tydligare och informativa bilder.
type: docs
weight: 10
url: /sv/net/use-cases/make-callout/
---
## Introduktion
Välkommen till vår steg-för-steg-guide om hur du gör bildtexter i Aspose.Drawing för .NET! Om du vill förbättra dina dokumentillustrationer med bildtexter är du på rätt plats. I den här handledningen delar vi upp processen i hanterbara steg med hjälp av biblioteket Aspose.Drawing.
## Förutsättningar
Innan du dyker in i handledningen, se till att du har följande förutsättningar:
- Grundläggande kunskaper i programmeringsspråket C#.
-  Aspose.Drawing-biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/drawing/net/).
- Ett dokument eller en bild där du vill lägga till länktexter.
## Importera namnområden
Se till att du har de nödvändiga namnrymden inkluderade i ditt projekt:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Steg 1: Ladda bilden
 Börja med att ladda bilden där du vill lägga till bildtexter. Byta ut`"Your Document Directory"` och`"gears.png"` med din faktiska katalog och bildfilnamn.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Din kod här
}
```
## Steg 2: Skapa grafikobjekt
 Skapa en`Graphics` objekt från bilden för att utföra ritoperationer.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Steg 3: Definiera bildtextpositioner
Definiera start- och slutpunkterna för varje bildtext tillsammans med bildtextens värde och enhet.
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
## Steg 4: Rita bildtexter
 Implementera`DrawCallOut` metod för att rita bildtexter på bilden.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Steg 5: Spara bilden
Spara bilden med bildtexter i önskad katalog.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Rita bildtextens källkod
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
## Slutsats

Grattis! Du har framgångsrikt lagt till bildtexter till din bild med Aspose.Drawing för .NET. Experimentera gärna med olika positioner och värden för att anpassa dina länktexter ytterligare.

## Vanliga frågor

### Kan jag använda Aspose.Drawing för andra typer av illustrationer?

Ja, Aspose.Drawing stöder ett brett utbud av ritoperationer för olika typer av illustrationer.

### Är Aspose.Drawing kompatibel med olika bildformat?

Absolut! Aspose.Drawing stöder populära bildformat som PNG, JPEG, GIF och mer.

### Var kan jag hitta fler exempel och dokumentation?

 Utforska den omfattande dokumentationen[här](https://reference.aspose.com/drawing/net/).

### Hur får jag support om jag stöter på problem?

 Besök[Aspose.Drawing forum](https://forum.aspose.com/c/diagram/17) för samhällsstöd.

### Kan jag prova Aspose.Drawing innan jag köper?

 Säkert! Kom igång med en gratis provperiod[här](https://releases.aspose.com/).