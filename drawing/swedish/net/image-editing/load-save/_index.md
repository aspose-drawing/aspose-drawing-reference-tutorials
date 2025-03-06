---
title: Ladda och spara bilder i Aspose.Drawing
linktitle: Ladda och spara bilder i Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternativ till System.Drawing.Common
description: Master bild laddar och sparar i .NET med Aspose.Drawing. Utforska BMP, GIF, JPG, PNG, TIFF-format utan ansträngning.
weight: 13
url: /sv/net/image-editing/load-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ladda och spara bilder i Aspose.Drawing

## Introduktion

Välkommen till vår steg-för-steg-guide för att bemästra bildladdning och spara med Aspose.Drawing för .NET! Om du vill förbättra dina färdigheter i att manipulera olika bildformat utan ansträngning, är du på rätt plats. Aspose.Drawing för .NET är ett kraftfullt bibliotek som förenklar processen att arbeta med bilder, och i den här handledningen kommer vi att dyka ner i att ladda och spara bilder i olika format.

## Förutsättningar

Innan vi ger oss ut på denna inlärningsresa, se till att du har följande förutsättningar på plats:

-  Aspose.Drawing för .NET: Se till att du har biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/drawing/net/).

- .NET-miljö: Denna handledning förutsätter att du har praktiska kunskaper om .NET-utveckling.

Nu när vi är redo, låt oss utforska de väsentliga namnområdena och fördjupa oss i steg-för-steg-guiden.

## Importera namnområden

ditt .NET-projekt börjar du med att importera de nödvändiga namnrymden:

```csharp
using System.Drawing;
```

Dessa namnutrymmen tillhandahåller de grundläggande klasserna och metoderna som behövs för bildmanipulation.

## Steg 1: Ladda en bild

Låt oss börja med att ladda en bild. Det här exemplet laddar bilder i olika format som BMP, GIF, JPG, PNG och TIFF.

```csharp
public static void Run()
{
    LoadAndSave("bmp");
    LoadAndSave("gif");
    LoadAndSave("jpg");
    LoadAndSave("png");
    LoadAndSave("tiff");
}
```

## Steg 2: Implementera LoadAndSave-metoden

 Bryt nu ner`LoadAndSave` metod i flera steg:

### Steg 2.1: Ladda bild

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Steg 2.2: Spara bild

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Spara bilden
    loadedImage.Save(outputPath);
}
```

Upprepa dessa steg för varje bildformat du vill stödja.

## Slutsats

Grattis! Du har bemästrat konsten att ladda och spara bilder med Aspose.Drawing för .NET. Denna färdighet är ovärderlig för utvecklare som arbetar med olika bildformat. Experimentera, utforska och integrera denna kunskap i dina projekt.

## FAQ's

### F1: Är Aspose.Drawing kompatibel med alla bildformat?

S1: Aspose.Drawing stöder ett brett utbud av format, inklusive BMP, GIF, JPG, PNG och TIFF.

### F2: Var kan jag hitta detaljerad dokumentation för Aspose.Drawing?

S2: Kolla in den officiella dokumentationen[här](https://reference.aspose.com/drawing/net/).

### F3: Hur kan jag få en tillfällig licens för Aspose.Drawing?

 A3: Besök[här](https://purchase.aspose.com/temporary-license/) för tillfälliga licensdetaljer.

### F4: Vad händer om jag stöter på problem eller har frågor under implementeringen?

 S4: Sök hjälp från Aspose.Drawing-communityt på[Aspose Forum](https://forum.aspose.com/c/diagram/17).

### F5: Var kan jag köpa Aspose.Drawing-biblioteket?

 A5: Du kan köpa det[här](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
