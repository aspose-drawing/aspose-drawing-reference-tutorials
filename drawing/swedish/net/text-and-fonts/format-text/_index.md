---
date: 2026-07-17
description: Lär dig hur du förhindrar text overflow genom att ställa in text alignment
  i Aspose.Drawing för .NET och lägger till text på bilder. Steg‑för‑steg guide med
  exempel.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Ställ in text alignment med Aspose.Drawing för .NET
og_description: Förhindra text overflow genom att ställa in text alignment i Aspose.Drawing
  för .NET. Lär dig att draw string på image, center text i rectangle och ersätta
  System.Drawing.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Förhindra text overflow – Ställ in text alignment med Aspose.Drawing för
  .NET
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  headline: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to prevent text overflow by setting text alignment in Aspose.Drawing
    for .NET and add text to images. Step‑by‑step guide with examples.
  name: Prevent Text Overflow – Set Text Alignment with Aspose.Drawing for .NET
  steps:
  - name: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
    text: '**Aspose.Drawing Library** – download it [here](https://releases.aspose.com/drawing/net/).'
  - name: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
    text: '**Development Environment** – Visual Studio 2022 (or any C# IDE).'
  - name: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
    text: '**Basic .NET knowledge** – you should be comfortable with C# projects and
      NuGet packages.'
  - name: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
    text: '**Resize the rectangle** – increase `rectangle.Width` or `rectangle.Height`.'
  - name: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
    text: '**Split the text** – break the string into lines that fit, then call `DrawString`
      for each line with adjusted Y‑coordinates.'
  type: HowTo
- questions:
  - answer: Omit the `DrawRectangle` call and pass the desired `PointF` location to
      `Graphics.DrawString`.
    question: How do I draw a string without a surrounding rectangle?
  - answer: Yes—apply a `Matrix` transformation to the `Graphics` object before drawing,
      then reset it afterwards.
    question: Can I rotate the text while keeping alignment?
  - answer: Simply change the file extension in `bitmap.Save` and optionally specify
      `ImageFormat.Jpeg`.
    question: Is it possible to export the image as JPEG instead of PNG?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- prevent text overflow
- Aspose.Drawing
- .NET graphics
- text alignment
title: Förhindra text overflow – Ställ in text alignment med Aspose.Drawing för .NET
url: /sv/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Förhindra textöversvämning – Ställ in textjustering med Aspose.Drawing

## Introduktion

När du behöver **förhindra textöversvämning** när du renderar grafik i .NET, ger Aspose.Drawing dig finjusterad kontroll över textplacering, justering och radbrytning. Oavsett om du bygger en märkesgenerator, en dynamisk rapport eller någon bildbaserad utdata, säkerställer behärskning av textjustering att din text förblir inom den avsedda rektangeln och ser polerad ut. I den här guiden går vi igenom hur du skapar en bitmap‑duk, konfigurerar `StringFormat`, ritar en rektangel med centrerad text, hanterar översvämning och slutligen sparar bilden.

## Snabba svar
- **Vad betyder “set text alignment”?** Det definierar hur text positioneras horisontellt och vertikalt inom en ritningsrektangel.  
- **Vilken klass styr justering?** `StringFormat` låter dig sätta `Alignment` och `LineAlignment`.  
- **Kan jag rita en sträng och en rektangel tillsammans?** Ja—använd `Graphics.DrawRectangle` följt av `Graphics.DrawString`.  
- **Hur förhindrar jag textöversvämning?** Justera rektangelns storlek eller dela upp texten i flera rader manuellt.  
- **Behöver jag en licens för produktion?** En kommersiell Aspose.Drawing‑licens krävs för icke‑utvärderingsbruk.

## Vad är **set text alignment** i Aspose.Drawing?

`set text alignment` konfigurerar horisontell (`StringAlignment`) och vertikal (`LineAlignment`) placering av text inom en `Rectangle` eller ritningsområde. Genom att justera dessa egenskaper styr du om texten visas vänsterjusterad, centrerad, högerjusterad, toppjusterad, mittjusterad eller bottenjusterad, vilket möjliggör exakt layout i grafik, märken och rapporter som genereras med Aspose.Drawing.

## Varför använda Aspose.Drawing för textjustering?

Aspose.Drawing eliminerar GDI+‑begränsningarna som plågar `System.Drawing.Common`. Det stödjer **5 stora .NET‑runtime‑miljöer** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 och .NET 7 – och kan rendera bilder upp till **4000 × 4000 px** (≈ 100 MB) utan att tömma minnet. Anti‑aliasing, hög‑DPI‑skalning och full Linux‑container‑kompatibilitet låter dig skapa pixelperfekt grafik i alla distributionsscenarier.

## Förutsättningar

1. **Aspose.Drawing Library** – ladda ner den [här](https://releases.aspose.com/drawing/net/).  
2. **Development Environment** – Visual Studio 2022 (eller någon C#‑IDE).  
3. **Basic .NET knowledge** – du bör vara bekväm med C#‑projekt och NuGet‑paket.

## Importera namnrymder

För att börja, importera de nödvändiga namnrymderna till scopet. Dessa ger dig åtkomst till grafik, textrendering och ritningsprimitiver.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Hur förhindrar man textöversvämning med Aspose.Drawing?

`Bitmap` är en klass som representerar en bild lagrad i minnet, medan `RectangleF` definierar ett flyttalsrektangelområde för ritning. Genom att använda ett `StringFormat` med `Trimming` satt till `StringTrimming.EllipsisCharacter` ersätts överflödiga tecken automatiskt med en ellipsis, vilket säkerställer att texten aldrig överskrider rektangelns gränser. Att mäta strängen först låter dig avgöra om du ska krympa rektangeln eller dela upp texten i flera rader, vilket garanterar en ren layout utan spill‑over.

Läs in din bitmap, definiera en lämpligt stor `RectangleF`, och använd ett `StringFormat` med `Trimming` satt till `StringTrimming.EllipsisCharacter` för att automatiskt kapa överflödiga tecken. För full kontroll, mät strängen med `Graphics.MeasureString` och krymp rektangeln eller dela upp texten i rader innan du ritar. Detta tillvägagångssätt garanterar att inga tecken spill utanför de visuella gränserna.

## Steg 1: Skapa Bitmap‑ och Graphics‑objekt  

`Bitmap` representerar en bild i minnet, medan `Graphics` tillhandahåller ritningsmetoder för den bitmappen. Att skapa en bitmap ger en duk du kan rita på. `Graphics`‑objektet är ritningsytan, och vi aktiverar högkvalitativ textrendering med `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Steg 2: Definiera **StringFormat** och stil  

`StringFormat` specificerar alternativ för textlayout såsom justering, radavstånd och trimning. Här **sätter vi textjustering** genom att konfigurera en `StringFormat`‑instans. Vi förbereder också penslar, pennor och ett teckensnitt som kommer att användas när strängen ritas.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Steg 3: Skapa och formatera text – **how to draw string** och **draw rectangle with text**

`Graphics.DrawString` renderar text på duken, och `Graphics.DrawRectangle` ritar en rektangelform. Vi sammansätter texten, definierar rektangeln som ska innehålla den, och ritar sedan både rektangelns kant och själva strängen.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Hur hanterar man textöversvämning

Om den angivna `text` överskrider rektangelns gränser, har du två vanliga alternativ:

1. **Resize the rectangle** – öka `rectangle.Width` eller `rectangle.Height`.  
2. **Split the text** – dela upp strängen i rader som får plats, och anropa sedan `DrawString` för varje rad med justerade Y‑koordinater.

## Hur ritar man en sträng på en bild med Aspose.Drawing?

`Graphics.DrawString` ritar den angivna texten med ett teckensnitt och formateringsalternativ. Instansiera ett `Graphics`‑objekt från din bitmap, och anropa sedan `DrawString` med det förberedda `StringFormat`. Detta enkla anrop renderar texten exakt där du vill ha den, med respekt för justering, trimning och eventuell transformationsmatris du har tillämpat. Att lägga till ett högkvalitativt renderingshint säkerställer att resultatet förblir skarpt på hög‑DPI‑skärmar.

## Hur centrerar man text i en rektangel?

`StringAlignment` bestämmer horisontell justering av text inom en layout‑rektangel. Sätt `stringFormat.Alignment = StringAlignment.Center` och `stringFormat.LineAlignment = StringAlignment.Center`. Detta centrerar texten horisontellt och vertikalt inne i rektangeln, vilket gör den idealisk för märken, knappar eller etikett‑överlappningar. Den centrerade placeringen fungerar konsekvent över olika bildstorlekar och DPI‑inställningar, vilket ger ett balanserat visuellt intryck.

## Hur uppnår man vertikal textjustering?

`LineAlignment` styr vertikal placering av text i rektangeln. Använd `stringFormat.LineAlignment` med värdena `StringAlignment.Near`, `Center` eller `Far` för att placera texten högst upp, i mitten eller längst ner i rektangeln. Kombinera detta med `Graphics.TranslateTransform` om du behöver rotera texten samtidigt som du bevarar vertikal justering. Justering av radjusteringen säkerställer att flerradiga block linjerar exakt där du förväntar dig, även efter transformationer.

## Steg 4: Spara resultatet – **add text to image**

Till sist, skriv bitmapen till disk. Detta steg demonstrerar **add text to image** i ett enda anrop.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Vanliga problem och lösningar

| Problem | Lösning |
|-------|----------|
| **Text visas suddigt** | Ensure `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` is set. |
| **Text klipps** | Increase the rectangle size or enable word‑wrap logic by measuring string size (`Graphics.MeasureString`). |
| **Typsnitt ej hittat** | Verify the font is installed on the host machine or embed a private font using `PrivateFontCollection`. |
| **Oväntade färger** | Double‑check brush and pen colors; remember that `Color.FromKnownColor` uses system‑defined colors. |

## Vanliga frågor

**Q1: Är Aspose.Drawing kompatibel med alla .NET‑versioner?**  
A1: Ja, Aspose.Drawing är designat för att vara kompatibelt med ett brett spektrum av .NET‑versioner, vilket säkerställer flexibilitet för utvecklare.

**Q2: Kan jag anpassa typsnittsstilen ytterligare?**  
A2: Absolut! Justera `Font`‑objektets parametrar för att uppnå önskad teckenstorlek, stil och familj.

**Q3: Hur kan jag hantera textöversvämning inom den definierade rektangeln?**  
A3: Du kan hantera textöversvämning genom att justera rektangelns storlek eller implementera anpassad logik för att hantera lång text.

**Q4: Finns det andra formateringsalternativ tillgängliga i Aspose.Drawing?**  
A4: Ja, Aspose.Drawing erbjuder ett omfattande verktygssats för grafisk manipulation, inklusive olika formateringsalternativ för text, former och mer.

**Q5: Var kan jag hitta ytterligare support för Aspose.Drawing?**  
A5: Utforska Aspose.Drawing‑forumet [här](https://forum.aspose.com/c/drawing/44) för community‑support och diskussioner.

**Additional Q&A**

**Q: Hur ritar jag en sträng utan en omgivande rektangel?**  
A: Utelämna `DrawRectangle`‑anropet och skicka den önskade `PointF`‑platsen till `Graphics.DrawString`.

**Q: Kan jag rotera texten samtidigt som jag behåller justeringen?**  
A: Ja—applicera en `Matrix`‑transformation på `Graphics`‑objektet före ritning, och återställ den därefter.

**Q: Är det möjligt att exportera bilden som JPEG istället för PNG?**  
A: Ändra helt enkelt filändelsen i `bitmap.Save` och ange eventuellt `ImageFormat.Jpeg`.

---

**Senast uppdaterad:** 2026-07-17  
**Testad med:** Aspose.Drawing 24.11 for .NET  
**Författare:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Relaterade handledningar

- [Hur man ritar text med Aspose.Drawing för .NET](/drawing/net/text-and-fonts/draw-text/)
- [Lägga till text på bilder i Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [Hur man ritar text och typsnitt med Aspose.Drawing för .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}