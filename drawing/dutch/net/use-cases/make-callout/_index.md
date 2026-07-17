---
date: 2026-03-02
description: Verbeter uw documentillustraties met Aspose.Drawing voor .NET! Leer stap
  voor stap hoe u callouts toevoegt voor duidelijkere en informatieve visualisaties.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hoe callouts toe te voegen met Aspose.Drawing voor .NET
url: /nl/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Callouts maken in Aspose.Drawing

## Introductie
Als je je afvraagt **hoe je callouts** aan je afbeeldingen of diagrammen kunt toevoegen met Aspose.Drawing voor .NET, ben je op de juiste plek. In deze tutorial lopen we het volledige proces door—van het laden van een afbeelding tot het tekenen van prachtig gestylede callouts—zodat je je illustraties duidelijker en informatiever kunt maken.

## Snelle antwoorden
- **Welke bibliotheek heb ik nodig?** Aspose.Drawing voor .NET (downloadbaar van de officiële site).  
- **Welke .NET‑versies worden ondersteund?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een commerciële licentie is vereist voor productie.  
- **Hoe lang duurt de implementatie?** Meestal minder dan 10 minuten voor een basis‑callout.  
- **Kan ik kleuren en lettertypen aanpassen?** Ja—alles wordt aangestuurd door standaard GDI+ objecten (Pen, Font, Brush).

## Hoe callouts toe te voegen in Aspose.Drawing
Hieronder vind je een beknopte, stapsgewijze handleiding die precies laat zien **hoe je callouts** aan een afbeelding kunt toevoegen. Voel je vrij om de code te kopiëren, te experimenteren met de posities, en de styling aan te passen aan je merk.

## Vereisten
Voordat je begint, zorg ervoor dat je het volgende hebt:

- Basiskennis van de programmeertaal C#.
- Aspose.Drawing bibliotheek geïnstalleerd. Je kunt het downloaden [hier](https://releases.aspose.com/drawing/net/).
- Een document of afbeelding waarin je callouts wilt toevoegen.

## Namespaces importeren
Zorg ervoor dat je de benodigde namespaces in je project hebt opgenomen:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Stap 1: Afbeelding laden
Begin met het laden van de afbeelding waarin je callouts wilt toevoegen. Vervang `"Your Document Directory"` en `"gears.png"` door je eigen map en bestandsnaam van de afbeelding.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Stap 2: Graphics‑object maken
Maak een `Graphics`‑object van de afbeelding om tekenbewerkingen uit te voeren.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Stap 3: Callout‑posities definiëren
Definieer de start‑ en eindpunten voor elke callout, samen met de callout‑waarde en eenheid.

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

## Stap 4: Callouts tekenen
Implementeer de `DrawCallOut`‑methode om callouts op de afbeelding te tekenen.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Stap 5: Afbeelding opslaan
Sla de afbeelding met callouts op in de gewenste map.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Broncode voor DrawCallout
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

## Veelvoorkomende problemen & tips
- **Onjuiste ankercoördinaten** – zorg ervoor dat de start‑ en eindpunten binnen de afbeelding liggen; anders kan de callout worden afgesneden.  
- **Tekst overlapt** – pas `spaceSize` of de lettergrootte aan als het label botst met andere graphics.  
- **Prestaties** – bij zeer grote afbeeldingen, overweeg om `Pen`, `Font` en `Brush` objecten na gebruik te disposen om bronnen vrij te maken.

## Conclusie
Gefeliciteerd! Je weet nu **hoe je callouts** aan een afbeelding kunt toevoegen met Aspose.Drawing voor .NET. Voel je vrij om te experimenteren met verschillende posities, kleuren en lettertypen om je visuele stijl te matchen.

## Veelgestelde vragen

### Kan ik Aspose.Drawing gebruiken voor andere soorten illustraties?
Ja, Aspose.Drawing ondersteunt een breed scala aan tekenbewerkingen voor verschillende soorten illustraties.

### Is Aspose.Drawing compatibel met verschillende afbeeldingsformaten?
Zeker! Aspose.Drawing ondersteunt populaire afbeeldingsformaten zoals PNG, JPEG, GIF en meer.

### Waar kan ik meer voorbeelden en documentatie vinden?
Bekijk de uitgebreide documentatie [hier](https://reference.aspose.com/drawing/net/).

### Hoe krijg ik ondersteuning als ik problemen ondervind?
Bezoek het [Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44) voor community‑ondersteuning.

### Kan ik Aspose.Drawing uitproberen voordat ik het koop?
Zeker! Begin met een gratis proefversie [hier](https://releases.aspose.com/).

**Aanvullende V&A**

**V: Kan ik de lijnstijl van de callout wijzigen (gestreept, gestippeld)?**  
**A: Ja—configureer eenvoudig de `Pen.DashStyle` eigenschap voordat je de lijn tekent.**

**V: Is het mogelijk om een achtergrondkleur toe te voegen aan het callout‑label?**  
**A: Absoluut. Maak een `SolidBrush` met de gewenste kleur en vul een rechthoek achter de tekst voordat je `DrawString` aanroept.**

**V: Hoe zorg ik ervoor dat de callout er hetzelfde uitziet op high‑DPI schermen?**  
**A: Stel `graphics.PageUnit = GraphicsUnit.Pixel` in (zoals getoond) en gebruik vector‑gebaseerde metingen om de schaal consistent te houden.**

---

**Laatst bijgewerkt:** 2026-03-02  
**Getest met:** Aspose.Drawing 24.11 voor .NET  
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}