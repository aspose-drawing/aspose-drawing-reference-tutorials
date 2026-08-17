---
date: 2026-07-17
description: Leer hoe u tekstoverloop kunt voorkomen door tekstuitlijning in te stellen
  in Aspose.Drawing for .NET en tekst aan images toe te voegen. Stapsgewijze handleiding
  met voorbeelden.
keywords:
- prevent text overflow
- draw string on image
- center text in rectangle
- vertical text alignment
- replace system drawing
lastmod: 2026-07-17
linktitle: Stel tekstuitlijning in met Aspose.Drawing for .NET
og_description: Voorkom tekstoverloop door tekstuitlijning in te stellen in Aspose.Drawing
  for .NET. Leer hoe u draw string op image toepast, tekst centreert in rectangle,
  en System.Drawing vervangt.
og_image_alt: 'Developer guide: Prevent text overflow by aligning text in Aspose.Drawing
  for .NET'
og_title: Voorkom tekstoverloop – Stel tekstuitlijning in met Aspose.Drawing for .NET
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
title: Voorkom tekstoverloop – Stel tekstuitlijning in met Aspose.Drawing for .NET
url: /nl/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Voorkom tekstoverloop – Stel tekstuitlijning in met Aspose.Drawing

## Inleiding

Wanneer je **tekstoverloop moet voorkomen** tijdens het renderen van graphics in .NET, biedt Aspose.Drawing je fijnmazige controle over tekstplaatsing, uitlijning en afbreking. Of je nu een badge‑generator, een dynamisch rapport of een andere op afbeeldingen gebaseerde output bouwt, het beheersen van tekstuitlijning zorgt ervoor dat je tekst binnen het beoogde rechthoek blijft en er gepolijst uitziet. In deze gids lopen we door het maken van een bitmap‑canvas, het configureren van `StringFormat`, het tekenen van een rechthoek met gecentreerde tekst, het afhandelen van overloop, en tenslotte het opslaan van de afbeelding.

## Snelle Antwoorden
- **Wat betekent “tekstuitlijning instellen”?** Het definieert hoe tekst horizontaal en verticaal wordt gepositioneerd binnen een tekenrechthoek.  
- **Welke klasse regelt de uitlijning?** `StringFormat` laat je `Alignment` en `LineAlignment` instellen.  
- **Kan ik een string en een rechthoek samen tekenen?** Ja—gebruik `Graphics.DrawRectangle` gevolgd door `Graphics.DrawString`.  
- **Hoe voorkom ik tekstoverloop?** Pas de grootte van de rechthoek aan of splits de tekst handmatig in meerdere regels.  
- **Heb ik een licentie nodig voor productie?** Een commerciële Aspose.Drawing‑licentie is vereist voor niet‑evaluatiegebruik.

## Wat is **tekstuitlijning instellen** in Aspose.Drawing?

`tekstuitlijning instellen` configureert horizontale (`StringAlignment`) en verticale (`LineAlignment`) plaatsing van tekst binnen een `Rectangle` of tekengebied. Door deze eigenschappen aan te passen, bepaal je of tekst links‑uitgelijnd, gecentreerd, rechts‑uitgelijnd, boven‑uitgelijnd, midden‑uitgelijnd of onder‑uitgelijnd verschijnt, waardoor precieze lay‑out mogelijk is in graphics, badges en rapporten die met Aspose.Drawing worden gegenereerd.

## Waarom Aspose.Drawing gebruiken voor tekstuitlijning?

Aspose.Drawing elimineert de GDI+‑beperkingen die `System.Drawing.Common` teisteren. Het ondersteunt **5 belangrijke .NET‑runtime‑omgevingen** – .NET Framework 4.6+, .NET Core 2.0+, .NET 5, .NET 6 en .NET 7 – en kan afbeeldingen renderen tot **4000 × 4000 px** (≈ 100 MB) zonder het geheugen uit te putten. Anti‑aliasing, high‑DPI‑schaling en volledige Linux‑containercompatibiliteit stellen je in staat om pixel‑perfecte graphics te genereren in elke implementatiescenario.

## Vereisten

1. **Aspose.Drawing Library** – download het [hier](https://releases.aspose.com/drawing/net/).  
2. **Development Environment** – Visual Studio 2022 (of een andere C#‑IDE).  
3. **Basic .NET knowledge** – je moet vertrouwd zijn met C#‑projecten en NuGet‑pakketten.

## Namespaces Importeren

Om te beginnen, breng je de benodigde namespaces in scope. Deze geven je toegang tot graphics, tekstrendering en tekenprimitieven.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Hoe tekstoverloop voorkomen met Aspose.Drawing?

Bitmap is een klasse die een in het geheugen opgeslagen afbeelding vertegenwoordigt, terwijl `RectangleF` een zwevend‑kommagetal rechthoekig gebied voor tekenen definieert. Door een `StringFormat` te gebruiken met `Trimming` ingesteld op `StringTrimming.EllipsisCharacter`, worden overtollige tekens automatisch vervangen door een ellipsis, waardoor de tekst nooit de grenzen van de rechthoek overschrijdt. Het eerst meten van de string laat je bepalen of je de rechthoek moet verkleinen of de tekst in meerdere regels moet splitsen, waardoor een nette lay‑out zonder overlopen wordt gegarandeerd.

Laad je bitmap, definieer een passend formaat `RectangleF`, en gebruik een `StringFormat` met `Trimming` ingesteld op `StringTrimming.EllipsisCharacter` om overtollige tekens automatisch af te kappen. Voor volledige controle meet je de string met `Graphics.MeasureString` en verklein je de rechthoek of splits je de tekst in regels vóór het tekenen. Deze aanpak garandeert dat er geen tekens buiten de visuele grenzen vallen.

## Stap 1: Bitmap‑ en Graphics‑objecten Maken  

Bitmap vertegenwoordigt een afbeelding in het geheugen, terwijl Graphics tekenmethoden voor die bitmap biedt. Het maken van een bitmap levert een canvas waarop je kunt tekenen. Het `Graphics`‑object is het tekenoppervlak, en we schakelen hoogwaardige tekstrendering in met `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Stap 2: **StringFormat** en Styling Definiëren  

StringFormat specificeert tekstlay‑outopties zoals uitlijning, regelafstand en trimmen. Hier **stellen we tekstuitlijning in** door een `StringFormat`‑instantie te configureren. We bereiden ook penselen, pennen en een lettertype voor die gebruikt zullen worden bij het tekenen van de string.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Stap 3: Tekst Maken en Formatteren – **hoe een string te tekenen** en **rechthoek met tekst te tekenen**

Graphics.DrawString rendert tekst op het canvas, en Graphics.DrawRectangle tekent een rechthoekvorm. We stellen de tekst samen, definiëren de rechthoek die deze zal bevatten, en tekenen vervolgens zowel de rechthoekrand als de string zelf.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Hoe tekstoverloop afhandelen

Als de opgegeven `text` de grenzen van de rechthoek overschrijdt, heb je twee veelvoorkomende opties:

1. **De rechthoek vergroten** – vergroot `rectangle.Width` of `rectangle.Height`.  
2. **De tekst splitsen** – breek de string op in regels die passen, roep vervolgens `DrawString` aan voor elke regel met aangepaste Y‑coördinaten.

## Hoe een string op een afbeelding tekenen met Aspose.Drawing?

Graphics.DrawString tekent de opgegeven tekst met een lettertype en opmaakopties. Instantieer een `Graphics`‑object vanuit je bitmap, roep vervolgens `DrawString` aan met de voorbereide `StringFormat`. Deze enkele aanroep rendert de tekst precies op de gewenste plek, met respect voor uitlijning, trimmen en eventuele transformatie‑matrix die je hebt toegepast. Het toevoegen van een hoogwaardige rendering‑hint zorgt ervoor dat de output scherp blijft op high‑DPI‑schermen.

## Hoe tekst centreren in een rechthoek?

StringAlignment bepaalt de horizontale uitlijning van tekst binnen een lay‑out‑rechthoek. Stel `stringFormat.Alignment = StringAlignment.Center` en `stringFormat.LineAlignment = StringAlignment.Center` in. Dit centreert de tekst horizontaal en verticaal binnen de rechthoek, waardoor het ideaal is voor badges, knoppen of label‑overlays. De gecentreerde plaatsing werkt consistent over verschillende afbeeldingsgroottes en DPI‑instellingen, en biedt een evenwichtig visueel uiterlijk.

## Hoe verticale tekstuitlijning bereiken?

LineAlignment regelt de verticale plaatsing van tekst binnen de rechthoek. Gebruik `stringFormat.LineAlignment` met de waarden `StringAlignment.Near`, `Center` of `Far` om de tekst respectievelijk bovenaan, in het midden of onderaan de rechthoek te positioneren. Combineer dit met `Graphics.TranslateTransform` als je de tekst moet roteren terwijl je de verticale uitlijning behoudt. Het aanpassen van de regeluitlijning zorgt ervoor dat blokken met meerdere regels precies op de verwachte positie komen, zelfs na transformaties.

## Stap 4: Output Opslaan – **tekst aan afbeelding toevoegen**

Tot slot schrijf je de bitmap naar schijf. Deze stap demonstreert **tekst aan afbeelding toevoegen** in één enkele aanroep.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Veelvoorkomende Problemen en Oplossingen

| Issue | Solution |
|-------|----------|
| **Tekst verschijnt onscherp** | Zorg ervoor dat `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` is ingesteld. |
| **Tekst wordt afgesneden** | Vergroot de rechthoekgrootte of schakel woord‑wraplogica in door de stringgrootte te meten (`Graphics.MeasureString`). |
| **Lettertype niet gevonden** | Controleer of het lettertype op de hostmachine is geïnstalleerd of embed een privé‑lettertype met `PrivateFontCollection`. |
| **Onverwachte kleuren** | Controleer de kleuren van penselen en pennen; onthoud dat `Color.FromKnownColor` systeem‑gedefinieerde kleuren gebruikt. |

## Veelgestelde Vragen

**Q1: Is Aspose.Drawing compatibel met alle .NET‑versies?**  
A1: Ja, Aspose.Drawing is ontworpen om compatibel te zijn met een breed scala aan .NET‑versies, wat flexibiliteit voor ontwikkelaars garandeert.

**Q2: Kan ik de lettertype‑stijl verder aanpassen?**  
A2: Absoluut! Pas de parameters van het `Font`‑object aan om de gewenste lettergrootte, stijl en familie te bereiken.

**Q3: Hoe kan ik tekstoverloop binnen de gedefinieerde rechthoek afhandelen?**  
A3: Je kunt tekstoverloop beheren door de grootte van de rechthoek aan te passen of aangepaste logica te implementeren om lange tekst te verwerken.

**Q4: Zijn er andere opmaakopties beschikbaar in Aspose.Drawing?**  
A4: Ja, Aspose.Drawing biedt een uitgebreide set tools voor grafische manipulatie, inclusief diverse opmaakopties voor tekst, vormen en meer.

**Q5: Waar kan ik extra ondersteuning vinden voor Aspose.Drawing?**  
A5: Verken het Aspose.Drawing‑forum [hier](https://forum.aspose.com/c/drawing/44) voor community‑ondersteuning en discussies.

**Aanvullende Q&A**

**Q: Hoe teken ik een string zonder een omringende rechthoek?**  
A: Laat de `DrawRectangle`‑aanroep weg en geef de gewenste `PointF`‑locatie door aan `Graphics.DrawString`.

**Q: Kan ik de tekst roteren terwijl ik de uitlijning behoud?**  
A: Ja—pas een `Matrix`‑transformatie toe op het `Graphics`‑object vóór het tekenen, en reset het daarna.

**Q: Is het mogelijk om de afbeelding als JPEG in plaats van PNG te exporteren?**  
A: Verander simpelweg de bestandsextensie in `bitmap.Save` en specificeer eventueel `ImageFormat.Jpeg`.

---

**Laatst bijgewerkt:** 2026-07-17  
**Getest met:** Aspose.Drawing 24.11 for .NET  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Gerelateerde Tutorials

- [Hoe Tekst Tekenen met Aspose.Drawing voor .NET](/drawing/net/text-and-fonts/draw-text/)
- [Tekst Toevoegen aan Afbeeldingen in Aspose.Drawing](/drawing/net/use-cases/text-on-image/)
- [Hoe Tekst en Lettertypen Tekenen met Aspose.Drawing voor .NET](/drawing/net/text-and-fonts/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}