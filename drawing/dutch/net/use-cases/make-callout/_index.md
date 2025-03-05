---
title: Bijschriften maken in Aspose.Drawing
linktitle: Bijschriften maken in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternatief voor System.Drawing.Common
description: Verbeter uw documentillustraties met Aspose.Drawing voor .NET! Leer stap voor stap hoe u highlights kunt toevoegen voor duidelijkere en informatieve beelden.
type: docs
weight: 10
url: /nl/net/use-cases/make-callout/
---
## Invoering
Welkom bij onze stapsgewijze handleiding voor het maken van highlights in Aspose.Drawing voor .NET! Als u uw documentillustraties wilt verfraaien met toelichtingen, bent u hier aan het juiste adres. In deze zelfstudie splitsen we het proces op in beheersbare stappen met behulp van de Aspose.Drawing-bibliotheek.
## Vereisten
Voordat u in de zelfstudie duikt, moet u ervoor zorgen dat u aan de volgende vereisten voldoet:
- Basiskennis van de programmeertaal C#.
-  Aspose.Tekeningbibliotheek geïnstalleerd. Je kunt het downloaden[hier](https://releases.aspose.com/drawing/net/).
- Een document of afbeelding waaraan u highlights wilt toevoegen.
## Naamruimten importeren
Zorg ervoor dat de benodigde naamruimten in uw project zijn opgenomen:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Stap 1: Laad de afbeelding
 Begin met het laden van de afbeelding waar u highlights wilt toevoegen. Vervangen`"Your Document Directory"` En`"gears.png"` met uw werkelijke map en afbeeldingsbestandsnaam.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Jouw code hier
}
```
## Stap 2: Maak een grafisch object
 Maak een`Graphics` object uit de afbeelding om tekenbewerkingen uit te voeren.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Stap 3: Definieer calloutposities
Definieer het begin- en eindpunt voor elke callout, samen met de calloutwaarde en -eenheid.
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
## Stap 4: Teken toelichtingen
 Implementeer de`DrawCallOut` methode om toelichtingen op de afbeelding te tekenen.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Stap 5: Sla de afbeelding op
Sla de afbeelding met bijschriften op in de gewenste map.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Teken de broncode van de toelichting
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
## Conclusie

Gefeliciteerd! U hebt met succes highlights aan uw afbeelding toegevoegd met Aspose.Drawing voor .NET. Experimenteer gerust met verschillende posities en waarden om uw highlights verder aan te passen.

## Veelgestelde vragen

### Kan ik Aspose.Drawing gebruiken voor andere soorten illustraties?

Ja, Aspose.Drawing ondersteunt een breed scala aan tekenbewerkingen voor verschillende soorten illustraties.

### Is Aspose.Drawing compatibel met verschillende afbeeldingsformaten?

Absoluut! Aspose.Drawing ondersteunt populaire afbeeldingsformaten zoals PNG, JPEG, GIF en meer.

### Waar kan ik meer voorbeelden en documentatie vinden?

 Ontdek de uitgebreide documentatie[hier](https://reference.aspose.com/drawing/net/).

### Hoe krijg ik ondersteuning als ik problemen tegenkom?

 Bezoek de[Aspose.Tekenforum](https://forum.aspose.com/c/diagram/17) voor gemeenschapssteun.

### Kan ik Aspose.Drawing uitproberen voordat ik een aankoop doe?

 Zeker! Ga aan de slag met een gratis proefperiode[hier](https://releases.aspose.com/).