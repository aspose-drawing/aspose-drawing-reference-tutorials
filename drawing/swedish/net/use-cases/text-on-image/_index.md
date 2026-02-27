---
date: 2026-02-27
description: Lär dig hur du skapar en födelsedagskortbild med Aspose.Drawing för .NET.
  Denna guide visar hur du ritar en sträng på en bild, överlagrar text på en bild
  och snabbt lägger till en bildtext på fotot.
linktitle: Adding Text on Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hur man skapar en födelsedagskortbild med Aspose.Drawing
url: /sv/net/use-cases/text-on-image/
weight: 12
---

 produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Så skapar du födelsedagskortbild med Aspose.Drawing

## Introduktion
I den dynamiska världen av .NET‑utveckling står Aspose.Drawing ut som ett kraftfullt verktyg för att enkelt manipulera bilder. Oavsett om du behöver **skapa födelsedagskortbild**, lägga till ett vattenstämpel, eller helt enkelt överlagra text på en bild, går den här handledningen igenom exakt hur du ritar en sträng på bild med C#. I slutet av guiden har du ett personligt födelsedagskort redo att dela.

## Snabba svar
- **Vilket bibliotek ska jag använda?** Aspose.Drawing för .NET  
- **Kan jag lägga till en bildtext till foto?** Ja – använd `Graphics.DrawString` med anpassade typsnitt.  
- **Krävs en licens för produktion?** Ja, en kommersiell licens behövs.  
- **Vilka .NET‑versioner stöds?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Hur lång tid tar implementeringen?** Vanligtvis under 10 minuter för ett enkelt kort.

## Vad är en födelsedagskortbild?
En födelsedagskortbild är en personlig bild som kombinerar ett bakgrundsfoto med anpassad text – såsom en hälsning, mottagarens namn eller ett firande meddelande. Med Aspose.Drawing kan du programatiskt generera dessa kort utan manuella grafiska designverktyg.

## Varför använda Aspose.Drawing för att överlagra text på bild?
- **Cross‑platform support:** Fungerar på Windows, Linux och macOS.  
- **Rich drawing API:** Full kontroll över typsnitt, färger och layout.  
- **Inga externa beroenden:** Ersätter `System.Drawing.Common` med ett helt hanterat bibliotek.  
- **Hög prestanda:** Optimerad för massbearbetning av bilder.

## Förutsättningar
Innan du dyker ner i handledningen, se till att du har följande på plats:

1. Aspose.Drawing‑biblioteket: Ladda ner och installera Aspose.Drawing‑biblioteket från [Aspose.Drawing för .NET‑dokumentation](https://reference.aspose.com/drawing/net/).  
2. Utvecklingsmiljö: En fungerande .NET‑utvecklingsmiljö, såsom Visual Studio eller Visual Studio Code, med .NET 6 SDK eller senare installerad.

Nu går vi igenom steg‑för‑steg‑guiden för att lägga till text på en bild och spara den som ett födelsedagskort.

## Importera namnrymder
Börja med att importera de nödvändiga namnrymderna i ditt C#‑projekt:

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
Här laddar vi bilden från den angivna filsökvägen och initierar grafikobjektet för vidare bearbetning.

## Steg 2: Ställ in textegenskaper
```csharp
SolidBrush brush = new SolidBrush(Color.Navy);
Font font = new Font("Calibri", 20, FontStyle.Italic);
int padding = 5;
```
Definiera textegenskaper som färg, typsnitt och marginal. Justera dessa parametrar enligt dina designpreferenser.

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
Beräkna den nödvändiga storleken för texten genom att mäta varje ord individuellt. Detta säkerställer korrekt placering och undviker överlappning av text.

## Steg 4: Rita text på bilden
```csharp
Rectangle rectangle = new Rectangle(image.Width - padding - extentWidth, image.Height - padding - extentHeight, extentWidth, extentHeight);
graphics.DrawString(text, font, brush, rectangle);
```
Nu positionerar vi texten på bilden baserat på den beräknade storleken och ritar den med angivet typsnitt och färg.

## Steg 5: Spara bilden
```csharp
image.Save(Path.Combine("Your Document Directory", "UseCases", "girl_card_out.jpg"));
}
```
Spara den modifierade bilden till önskad katalog. Den resulterande filen är en färdig‑att‑skicka födelsedagskortbild.

## Vanliga användningsområden & tips
- **Lägg till bildtext till foto:** Ersätt `text` med vilken bildtext du behöver, till exempel “Celebrating 30 Years!”.  
- **Rita text på bitmap:** Samma metod fungerar för `Bitmap`‑objekt som skapas från början.  
- **Överlagra flera rader:** Loopa igenom en array av strängar och justera `Rectangle` Y‑koordinaten för varje rad.  
- **Proffstips:** Använd `Graphics.SmoothingMode = SmoothingMode.AntiAlias` för ännu mjukare textrendering.

## Slutsats
Aspose.Drawing förenklar bildmanipuleringsuppgifter i .NET och ger utvecklare ett robust verktygssats. Att lägga till text på bilder – oavsett om du **skapar födelsedagskortbild**, **draw string on image** eller **add caption to photo** – är bara ett exempel på dess mångsidighet när det gäller grafiska element.

## Vanliga frågor
### Är Aspose.Drawing kompatibel med alla bildformat?
Aspose.Drawing stöder ett brett spektrum av bildformat, inklusive populära som JPEG, PNG och GIF. Se [dokumentationen](https://reference.aspose.com/drawing/net/) för en komplett lista.

### Kan jag använda Aspose.Drawing i kommersiella projekt?
Ja, Aspose.Drawing är lämplig för både personliga och kommersiella projekt. För licensinformation, besök [köpsidan](https://purchase.aspose.com/buy).

### Finns tillfälliga licenser för teständamål?
Ja, du kan få en tillfällig licens för testning genom att besöka [Temporary License](https://purchase.aspose.com/temporary-license/).

### Var kan jag hitta community‑support för Aspose.Drawing?
Engagera dig i communityn och få support på [Aspose.Drawing‑forumet](https://forum.aspose.com/c/drawing/44).

### Hur kommer jag igång med Aspose.Drawing?
Börja med att ladda ner biblioteket från [här](https://releases.aspose.com/drawing/net/) och utforska den omfattande [dokumentationen](https://reference.aspose.com/drawing/net/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-02-27  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose