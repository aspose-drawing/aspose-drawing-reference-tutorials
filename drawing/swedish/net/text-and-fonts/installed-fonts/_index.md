---
date: 2025-12-06
description: Lär dig hur du sparar PNG‑bildfiler samtidigt som du listar installerade
  teckensnitt, visar teckensnittsfamiljer, skapar grafik från bitmap och ritar text
  med teckensnitt med Aspose.Drawing för .NET.
language: sv
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Spara PNG‑bild och arbeta med installerade typsnitt i Aspose.Drawing
url: /net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spara PNG‑bild och arbeta med installerade teckensnitt i Aspose.Drawing

## Introduktion

Om du behöver **spara PNG‑bild**‑filer som också visar information om de teckensnitt som är installerade på en maskin, ger Aspose.Drawing för .NET dig ett rent, plattformsoberoende sätt att göra det. I den här handledningen går vi igenom hur man listar installerade teckensnitt, visar teckensnittsfamiljer, skapar grafik från en bitmap, och ritar text med teckensnitt – allt medan vi slutligen sparar resultatet som en PNG‑bild. I slutet har du ett återanvändbart kodsnutt som du kan lägga in i vilket .NET‑projekt som helst.

## Snabba svar
- **Vad skapar den här handledningen?** En PNG‑bild som listar installerade teckensnittsfamiljer.  
- **Vilket bibliotek krävs?** Aspose.Drawing för .NET (ingen System.Drawing.Common behövs).  
- **Kan jag använda egna teckensnitt?** Ja – ladda bara dem i en `InstalledFontCollection`.  
- **Kan upplösningen justeras?** Absolut – ändra bitmap‑storlek eller pixelformat.  
- **Behöver jag en licens för att köra koden?** En tillfällig licens fungerar för utvärdering; en full licens krävs för produktion.

## Vad betyder “spara PNG‑bild” i Aspose.Drawing‑sammanhang?

Att spara en PNG‑bild innebär att rendera din rityta (en `Bitmap`) till en fil med filändelsen `.png`. Aspose.Drawing sköter kodningen åt dig, så du behöver bara anropa `bitmap.Save(...)` med den önskade sökvägen.

## Varför lista installerade teckensnitt och visa teckensnittsfamiljer?

Att veta vilka teckensnitt som finns tillgängliga låter dig skapa dynamisk grafik som anpassar sig till slutanvändarens miljö. Det är särskilt praktiskt för att generera rapporter, certifikat eller annat visuellt innehåll som måste matcha företagets varumärke utan att distribuera teckensnittsfiler.

## Förutsättningar

- **Aspose.Drawing‑bibliotek** – ladda ner den senaste versionen från [Aspose Drawing‑nedladdningssidan](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider eller någon .NET‑kompatibel editor.  
- **Grundläggande C#‑kunskaper** – du bör vara bekväm med klasser, objekt och enkla loopar.

## Importera namnrymder
För att arbeta med teckensnitt och grafik, importera dessa namnrymder högst upp i din C#‑fil:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Steg‑för‑steg‑guide

### Steg 1: Skapa en bitmap (duken)
Först skapar vi en bitmap som kommer att hålla den slutgiltiga bilden. Bitmap‑storleken och pixelformatet bestämmer kvaliteten på den sparade PNG‑filen.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Steg 2: Skapa grafik från bitmap
Därefter får vi ett `Graphics`‑objekt från bitmap. Detta objekt låter oss rita former, text och bilder på duken.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### Steg 3: Ställ in pensel och teckensnitt (rita text med teckensnitt)
Vi behöver en pensel för textfärgen och ett `Font`‑objekt som definierar teckensnitt, storlek och stil.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### Steg 4: Lista installerade teckensnitt och visa teckensnittsfamiljer
Nu visar vi antalet teckensnittsfamiljer och de första namnen direkt på bitmap. Detta demonstrerar funktionerna **list installed fonts** och **show font families**.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### Steg 5: Spara PNG‑bild
Till sist skriver vi bitmap till disk som en PNG‑fil. Detta är den centrala **save png image**‑operationen.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Proffstips:** Använd `Path.Combine` för att bygga filsökvägar och undvika problem med katalogseparatorer på olika operativsystem.

## Vanliga problem och lösningar
| Problem | Orsak | Lösning |
|-------|-------|-----|
| **Inga teckensnitt visas** | `InstalledFontCollection` inte fylld (t.ex. körs på en huvudlös server utan teckensnitt). | Installera de nödvändiga teckensnitten på servern eller bädda in egna teckensnitt i din applikation. |
| **Sparad fil är korrupt** | Felaktigt pixelformat eller saknade skrivrättigheter. | Säkerställ att målmappen finns och att appen har skrivbehörighet; behåll `Format32bppPArgb`. |
| **Texten ser suddig ut** | Låga DPI‑inställningar. | Öka bitmap‑dimensionerna eller sätt `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Vanliga frågor

**Q: Kan jag använda egna teckensnitt som inte är installerade på maskinen?**  
A: Ja. Ladda teckensnittsfilen i en `PrivateFontCollection` och skapa ett `Font` från den samlingen.

**Q: Hur hanterar jag teckensnittrelaterade undantag?**  
A: Omge teckensnitts skapande med ett `try/catch`‑block och inspektera `ArgumentException` för saknade familjer.

**Q: Är Aspose.Drawing lämpligt för webbapplikationer?**  
A: Absolut. Biblioteket fungerar i ASP.NET Core, Azure Functions och andra server‑sidiga miljöer.

**Q: Kan jag ändra textfärg eller stil?**  
A: Ja. Använd olika `Brush`‑typer (t.ex. `LinearGradientBrush`) och ändra `FontStyle`‑enum.

**Q: Var kan jag få en tillfällig licens för testning?**  
A: Ladda ner en provlicens från [Aspose temporär‑licenssida](https://purchase.aspose.com/temporary-license/).

## Slutsats

Genom att följa dessa steg har du lärt dig hur du **sparar PNG‑bild**‑filer som dynamiskt **listar installerade teckensnitt**, **visar teckensnittsfamiljer**, **skapar grafik från bitmap** och **ritar text med teckensnitt** med Aspose.Drawing för .NET. Känn dig fri att experimentera med andra teckensnitt, färger och bitmap‑storlekar för att matcha ditt projekts visuella krav.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose