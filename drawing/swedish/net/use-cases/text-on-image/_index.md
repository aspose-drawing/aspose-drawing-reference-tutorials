---
title: Lägga till text på bilder i Aspose.Drawing
linktitle: Lägga till text på bilder i Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternativ till System.Drawing.Common
description: Utforska den sömlösa integreringen av text i bilder med Aspose.Drawing för .NET. Följ vår steg-för-steg-guide för enkel bildmanipulering. Ladda ner nu!
weight: 12
url: /sv/net/use-cases/text-on-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Lägga till text på bilder i Aspose.Drawing

## Introduktion
den dynamiska världen av .NET-utveckling framstår Aspose.Drawing som ett kraftfullt verktyg för att enkelt manipulera bilder. Att lägga till text i bilder är ett vanligt krav, oavsett om det är för vattenmärkning, anteckningar eller att skapa personlig grafik. I den här handledningen kommer vi att utforska hur man kan utnyttja Aspose.Drawing för att sömlöst integrera text i dina bilder med C#.
## Förutsättningar
Innan du dyker in i handledningen, se till att du har följande på plats:
1.  Aspose.Drawing Library: Ladda ner och installera Aspose.Drawing-biblioteket från[Aspose.Drawing för .NET-dokumentation](https://reference.aspose.com/drawing/net/).
2. Utvecklingsmiljö: Ha en fungerande .NET-utvecklingsmiljö, inklusive Visual Studio eller någon annan kompatibel IDE.
Låt oss nu komma igång med steg-för-steg-guiden.
## Importera namnområden
Börja med att importera de nödvändiga namnrymden till ditt C#-projekt:
```csharp
using System;
using System.Drawing;
using System.Drawing.Text;
using System.Linq;
```
## Steg 1: Ladda bilden
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "UseCases", "girl.jpg")))
{
    var graphics = Graphics.FromImage(image);
    graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
    graphics.PageUnit = GraphicsUnit.Pixel;
```
Här laddar vi in bilden från den angivna filsökvägen och initialiserar grafikobjektet för vidare bearbetning.
## Steg 2: Ställ in textegenskaper
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Definiera textegenskaper som färg, teckensnitt och utfyllnad. Justera dessa parametrar enligt dina önskemål.
## Steg 3: Mät textstorlek
```csharp
string text = "Happy Birthday!";
var words = text.Split(' ');
int extentWidth = 0;
int extentHeight = 0;
words.ToList().ForEach(word =>
{
    var stringSize = graphics.MeasureString(word, font);
    extentWidth = Math.Max(extentWidth, (int)stringSize.Width + padding);
    extentHeight += (int)stringSize.Height;
});
```
Beräkna önskad storlek för texten genom att mäta varje ord individuellt. Detta säkerställer korrekt placering och undviker överlappning av text.
## Steg 4: Rita text på bild
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Placera nu texten på bilden baserat på den beräknade storleken och rita den med det angivna teckensnittet och färgen.
## Steg 5: Spara bilden
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Spara den ändrade bilden i önskad katalog.
Denna steg-för-steg-guide visar en enkel process för att lägga till text till bilder med Aspose.Drawing för .NET. Experimentera med olika typsnitt, färger och textinnehåll för att uppnå önskad visuell effekt.
## Slutsats
Aspose.Drawing förenklar bildmanipuleringsuppgifter i .NET, vilket ger utvecklare en robust verktygslåda. Att lägga till text i bilder är bara ett exempel på dess möjligheter, som visar upp bibliotekets mångsidighet när det gäller att hantera grafiska element.
## Vanliga frågor
### Är Aspose.Drawing kompatibel med alla bildformat?
 Aspose.Drawing stöder ett brett utbud av bildformat, inklusive populära som JPEG, PNG och GIF. Referera till[dokumentation](https://reference.aspose.com/drawing/net/) för en komplett lista.
### Kan jag använda Aspose.Drawing för kommersiella projekt?
Ja, Aspose.Drawing lämpar sig för både personliga och kommersiella projekt. För licensinformation, besök[köpsidan](https://purchase.aspose.com/buy).
### Finns tillfälliga licenser tillgängliga för teständamål?
 Ja, du kan få en tillfällig licens för testning genom att besöka[Tillfällig licens](https://purchase.aspose.com/temporary-license/).
### Var kan jag hitta gemenskapsstöd för Aspose.Drawing?
 Engagera dig i samhället och få stöd på[Aspose.Drawing forum](https://forum.aspose.com/c/drawing/44).
### Hur kommer jag igång med Aspose.Drawing?
 Börja med att ladda ner biblioteket från[här](https://releases.aspose.com/drawing/net/) och utforska det omfattande[dokumentation](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
