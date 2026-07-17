---
date: 2026-03-02
description: Förbättra dina dokumentillustrationer med Aspose.Drawing för .NET! Lär
  dig steg för steg hur du lägger till förklarande textrutor för tydligare och mer
  informativa bilder.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hur man lägger till anmärkningar med Aspose.Drawing för .NET
url: /sv/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Skapa anmärkningar i Aspose.Drawing

## Introduktion
Om du undrar **hur du lägger till anmärkningar** i dina bilder eller diagram med Aspose.Drawing för .NET, har du kommit till rätt ställe. I den här handledningen går vi igenom hela processen—från att ladda en bild till att rita vackert stylade anmärkningar—så att du kan göra dina illustrationer tydligare och mer informativa.

## Snabba svar
- **Vilket bibliotek behöver jag?** Aspose.Drawing for .NET (nedladdningsbart från den officiella webbplatsen).  
- **Vilka .NET-versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Behöver jag en licens?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktion.  
- **Hur lång tid tar implementeringen?** Vanligtvis under 10 minuter för en grundläggande anmärkning.  
- **Kan jag anpassa färger och typsnitt?** Ja—allt styrs av standard‑GDI+‑objekt (Pen, Font, Brush).

## Hur man lägger till anmärkningar i Aspose.Drawing
Nedan följer en kortfattad, steg‑för‑steg‑guide som visar exakt **hur du lägger till anmärkningar** i en bild. Känn dig fri att kopiera koden, experimentera med positionerna och anpassa stilen så att den matchar ditt varumärke.

## Förutsättningar
Innan du dyker ner, se till att du har:

- Grundläggande kunskap i programmeringsspråket C#.  
- Aspose.Drawing‑biblioteket installerat. Du kan ladda ner det [här](https://releases.aspose.com/drawing/net/).  
- Ett dokument eller en bild där du vill lägga till anmärkningar.

## Importera namnrymder
Se till att du har de nödvändiga namnrymderna inkluderade i ditt projekt:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Steg 1: Ladda bilden
Börja med att ladda bilden där du vill lägga till anmärkningar. Ersätt `"Your Document Directory"` och `"gears.png"` med din faktiska katalog och bildfilnamn.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Steg 2: Skapa Graphics‑objekt
Skapa ett `Graphics`‑objekt från bilden för att utföra ritoperationer.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Steg 3: Definiera anmärkningspositioner
Definiera start‑ och slutpunkterna för varje anmärkning samt anmälningsvärdet och enheten.

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

## Steg 4: Rita anmärkningar
Implementera metoden `DrawCallOut` för att rita anmärkningar på bilden.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Steg 5: Spara bilden
Spara bilden med anmärkningar till den önskade katalogen.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Källkod för att rita anmärkning
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
- **Felaktiga ankordningskoordinater** – se till att start‑ och slutpunkterna ligger inom bildens gränser; annars kan anmärkningen klippas av.  
- **Text som överlappar** – justera `spaceSize` eller teckenstorleken om etiketten kolliderar med annan grafik.  
- **Prestanda** – för mycket stora bilder, överväg att avyttra `Pen`, `Font` och `Brush`‑objekt efter användning för att frigöra resurser.

## Slutsats
Grattis! Du vet nu **hur du lägger till anmärkningar** i en bild med Aspose.Drawing för .NET. Känn dig fri att experimentera med olika positioner, färger och typsnitt för att matcha din visuella stil.

## Vanliga frågor

### Kan jag använda Aspose.Drawing för andra typer av illustrationer?
Ja, Aspose.Drawing stöder ett brett spektrum av ritoperationer för olika typer av illustrationer.

### Är Aspose.Drawing kompatibel med olika bildformat?
Absolut! Aspose.Drawing stöder populära bildformat som PNG, JPEG, GIF och fler.

### Var kan jag hitta fler exempel och dokumentation?
Utforska den omfattande dokumentationen [här](https://reference.aspose.com/drawing/net/).

### Hur får jag support om jag stöter på problem?
Besök [Aspose.Drawing‑forumet](https://forum.aspose.com/c/drawing/44) för community‑support.

### Kan jag prova Aspose.Drawing innan jag köper?
Självklart! Kom igång med en gratis provversion [här](https://releases.aspose.com/).

**Ytterligare frågor & svar**

**Q: Kan jag ändra linjestilen för anmärkningen (streckad, prickad)?**  
**A:** Ja—konfigurera helt enkelt `Pen.DashStyle`‑egenskapen innan du ritar linjen.

**Q: Är det möjligt att lägga till en bakgrundsfärg på anmärkningsetiketten?**  
**A:** Absolut. Skapa en `SolidBrush` med önskad färg och fyll en rektangel bakom texten innan du anropar `DrawString`.

**Q: Hur säkerställer jag att anmärkningen ser likadan ut på hög‑DPI-skärmar?**  
**A:** Ställ in `graphics.PageUnit = GraphicsUnit.Pixel` (som visat) och använd vektorbaserade mått för att hålla skalningen konsekvent.

---

**Senast uppdaterad:** 2026-03-02  
**Testad med:** Aspose.Drawing 24.11 for .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}