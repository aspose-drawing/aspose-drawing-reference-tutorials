---
date: 2025-12-04
description: Behärska bildladdning, batchkonvertering av bilder och formatändringar
  i .NET med Aspose.Drawing. Lär dig konvertera BMP till PNG och mer.
linktitle: Loading and Saving Images in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Konvertera BMP till PNG och andra format med Aspose.Drawing
url: /sv/net/image-editing/load-save/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konvertera BMP till PNG och andra format med Aspose.Drawing

## Introduktion

Välkommen till vår steg‑för‑steg‑guide om hur du **konverterar BMP till PNG** (och många andra bildformat) med Aspose.Drawing för .NET. Oavsett om du behöver **ändra bildformat** för en enskild fil eller köra en **batch‑bildkonvertering** på dussintals bilder, visar den här handledningen exakt hur du laddar, omvandlar och sparar bilder med ren, underhållbar kod.

## Snabba svar
- **Kan Aspose.Drawing konvertera BMP till PNG?** Ja – ladda bara BMP-filen och anropa `Save` med en .png‑ändelse.  
- **Stöds batch‑konvertering?** Absolut; loopa igenom filer och återanvänd samma `LoadAndSave`‑metod.  
- **Behöver jag en licens för produktion?** En licens krävs för produktionsanvändning; en tillfällig licens finns tillgänglig för utvärdering.  
- **Vilka .NET‑versioner är kompatibla?** Fungerar med .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **Var kan jag ladda ner biblioteket?** Hämta det senaste Aspose.Drawing‑paketet från den officiella nedladdningssidan.

## Vad är bildformatkonvertering i C# med Aspose.Drawing?

Aspose.Drawing är ett högpresterande, helt hanterat .NET‑bibliotek som ersätter den äldre `System.Drawing.Common`. Det ger dig full kontroll över **ladda bild ASP.NET**‑scenarier, stödjer över 100 bildformat och eliminerar plattforms‑specifika begränsningar.

## Varför använda Aspose.Drawing för batch‑bildkonvertering?

- **Plattformsoberoende pålitlighet** – inga GDI+‑beroenden.  
- **Rikt formatstöd** – BMP, GIF, JPG, PNG, TIFF och många fler.  
- **Konsekvent API** – samma kod fungerar på Windows, Linux och macOS.  
- **Prestanda** – optimerad för storskaliga bildbehandlingspipeline.

## Förutsättningar

Innan vi dyker ner, se till att du har:

- **Aspose.Drawing för .NET** – ladda ner det [här](https://releases.aspose.com/drawing/net/).  
- En fungerande **.NET‑utvecklingsmiljö** (Visual Studio, VS Code eller Rider).

Nu när vi är klara, låt oss importera de nödvändiga namnutrymmena och börja koda.

## Importera namnrymder

I ditt .NET‑projekt, börja med att importera det nödvändiga namnrymmet:

```csharp
using System.Drawing;
```

Dessa klasser tillhandahåller kärnfunktionaliteten för att ladda och spara bilder.

## Steg 1: Ladda en bild

Det första steget är att ladda en bildfil. Exemplet nedan demonstrerar hur man laddar bilder i olika format, inklusive BMP, som vi senare kommer att konvertera till PNG.

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

## Hur man konverterar BMP till PNG med Aspose.Drawing

`LoadAndSave`‑metoden hanterar både inläsning av källfilen och sparande i önskat utdataformat. Genom att skicka `"bmp"` som argument kommer metoden automatiskt att producera en PNG‑fil när du ändrar filändelsen i `outputPath`.

### Steg 2.1: Ladda bild

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    Bitmap loadedImage = new Bitmap(inputPath);
}
```

### Steg 2.2: Spara bild (ändra bildformat)

```csharp
private static void LoadAndSave(string graphicsFileFormats)
{
    string inputPath = "Your Document Directory" + @"GraphicsFileFormats\image." + graphicsFileFormats;
    string outputPath = "Your Document Directory" + @"GraphicsFileFormats\image_out." + graphicsFileFormats;
    
    Bitmap loadedImage = new Bitmap(inputPath);
    
    // Save the image
    loadedImage.Save(outputPath);
}
```

Upprepa anropet till `LoadAndSave` för varje bildformat du vill bearbeta. Genom att justera `outputPath`‑ändelsen kan du **konvertera BMP till PNG**, **ändra bildformat** till GIF, JPG osv., allt med samma metod.

## Vanliga fallgropar och tips

- **Filvägsavgränsare** – Använd `Path.Combine` för plattformsoberoende säkerhet istället för manuell strängkonkatenering.  
- **Disposera Bitmaps** – Inslut `Bitmap` i ett `using`‑block för att snabbt frigöra inhemska resurser.  
- **Kvalitetsinställningar** – När du sparar JPEG‑filer, överväg att ange ett `EncoderParameters`‑objekt för att kontrollera komprimeringskvaliteten.  
- **Batch‑behandling** – Placera dina bildfiler i en mapp och iterera över `Directory.GetFiles` för att automatisera storskaliga konverteringar.

## Vanliga frågor

### Q1: Är Aspose.Drawing kompatibel med alla bildformat?

A1: Aspose.Drawing stödjer ett brett spektrum av format, inklusive BMP, GIF, JPG, PNG och TIFF.

### Q2: Var kan jag hitta detaljerad dokumentation för Aspose.Drawing?

A2: Se den officiella dokumentationen [här](https://reference.aspose.com/drawing/net/).

### Q3: Hur kan jag skaffa en tillfällig licens för Aspose.Drawing?

A3: Besök [här](https://purchase.aspose.com/temporary-license/) för detaljer om tillfällig licens.

### Q4: Vad gör jag om jag stöter på problem eller har frågor under implementeringen?

A4: Sök hjälp från Aspose.Drawing‑gemenskapen på [Aspose Forum](https://forum.aspose.com/c/drawing/44).

### Q5: Var kan jag köpa Aspose.Drawing‑biblioteket?

A5: Du kan köpa det [här](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Kan jag använda den här koden i en ASP.NET‑webbapplikation?**  
A: Ja – samma `LoadAndSave`‑logik fungerar i ASP.NET, MVC eller Razor Pages; se bara till att filvägarna är åtkomliga för webbprocessen.

**Q: Är det möjligt att bearbeta bilder parallellt för snabbare batch‑konvertering?**  
A: Absolut. Inslut anropen till `LoadAndSave` i en `Parallel.ForEach`‑loop, men kom ihåg att hantera trådsäker disponering av `Bitmap`‑objekt.

## Slutsats

Du har nu lärt dig hur du **konverterar BMP till PNG**, utför **batch‑bildkonvertering** och **ändrar bildformat** med Aspose.Drawing för .NET. Använd dessa mönster för att automatisera bildpipeline, generera miniatyrbilder eller förbereda resurser för webbdistribution. Experimentera med olika format, integrera koden i dina tjänster och njut av pålitligheten hos ett helt hanterat ritbibliotek.

---

**Senast uppdaterad:** 2025-12-04  
**Testat med:** Aspose.Drawing 24.12 för .NET  
**Författare:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}