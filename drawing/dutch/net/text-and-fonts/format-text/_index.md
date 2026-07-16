---
date: 2026-02-25
description: Leer hoe u tekstuitlijning instelt in Aspose.Drawing voor .NET en tekst
  toevoegt aan afbeeldingen. Stapsgewijze handleiding met voorbeelden.
linktitle: Set Text Alignment with Aspose.Drawing for .NET
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Tekstuitlijning instellen met Aspose.Drawing voor .NET
url: /nl/net/text-and-fonts/format-text/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tekstuitlijning instellen in Aspose.Drawing

## Introductie

Als het gaat om **set tekstuitlijning** en het opmaken van tekst in uw .NET‑applicaties, is Aspose.Drawing de bibliotheek bij uitstek voor ontwikkelaars die precisie, prestaties en een rijke API‑omgeving nodig hebben. Of u nu een rapportage-engine, een dynamische badge-generator of een andere grafisch intensieve oplossing bouwt, de mogelijkheid om te bepalen hoe tekstvormen binnen worden uitgelijnd, zorgt ervoor dat uw output er gepolijst en professioneel uitziet. In deze tutorial lopen we het volledige proces door — van het maken van een bitmap‑canvas tot het tekenen van een rechthoekige met tekst, het afhandelen van overflow en uiteindelijk het opslaan van de afbeelding.

## Snelle antwoorden
- **Wat betekent “tekstuitlijning instellen”?** Het bepaalt hoe tekst horizontaal en verticaal binnen een tekenrechthoek wordt gepositioneerd.
- **Welke klasse regelt de uitlijning?** `StringFormat` laat u `Alignment` en `LineAlignment` instellen.
- **Kan ik een string en een rechthoekige samen tekenen?** Ja — gebruik `Graphics.DrawRectangle` gevolgd door `Graphics.DrawString`.
- **Hoe voorkom ik tekst‑overflow?** Pas de grootte van de rechthoek aan of splits de tekst handmatig in meerdere regels.
- **Heb ik een licentie nodig voor productie?** Een logische Aspose.Drawing‑licentie is vereist voor niet‑evaluatiegebruik.

## Wat is **tekstuitlijning instellen** in Aspose.Drawing?

`set tekstuitlijning` namelijk naar de configuratie van horizontale (`StringAlignment`) en verticale (`LineAlignment`) positionering van tekst binnen een `Rectangle` of een experimentele tekengebied. Door deze instellingen aan te passagiers, bepaalt u de tekst links‑uitgelijnd, gecentreerd, rechts‑uitgelijnd, boven‑uitgelijnd, midden‑uitgelijnd of onder‑uitgelijnd verschijnt.

## Waarom Aspose.Drawing gebruiken voor tekstuitlijning?

- **Volledige .NET‑compatibiliteit** – werkt met .NET Framework, .NET Core en .NET 5/6+.
- **Pixel‑perfecte weergave** – anti‑aliasing en hoge‑DPI‑ondersteuning direct beschikbaar.
- **Geen GDI+ beperkingen** – in afwachting tot `System.Drawing.Common` draait Aspose.Drawing op Linux‑containers zonder native afhankelijkheden.
- **Rijke styling** – combineer lettertypen, penselen, pennen en aangepaste `StringFormat`‑objecten voor hogere lay‑outs.

## Vereisten

1. **Aspose.Tekenbibliotheek** – download deze [hier](https://releases.aspose.com/drawing/net/).
2. **Ontwikkelomgeving** – Visual Studio 2022 (of een andere C#‑IDE).
3. **Basis .NET‑kennis** – u moet vertrouwd zijn met C#‑projecten en NuGet‑pakketten.

## Naamruimten importeren

Om te beginnen, brengt u de benodigde namespaces in scope. Deze geven u toegang tot graphics, tekstweergave en teken‑primitieven.

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Stap 1: Bitmap- en grafische objecten maken 

Het maken van een bitmap levert een canvas waarop u kunt tekenen. Het `Graphics`‑object is het tekenoppervlak, en we schakelen high‑quality tekstweergave in met `TextRenderingHint`.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

## Stap 2: **Tekstopmaak** en -stijl definiëren  

Hier **stellen we tekstuitlijning in** door een `StringFormat`‑instantie te configureren. We bereiden ook penselen, pennen en een lettertype voor die gebruikt zullen worden bij het tekenen van de string.

```csharp
StringFormat stringFormat = new StringFormat();
stringFormat.Alignment = StringAlignment.Center;          // Horizontal alignment
stringFormat.LineAlignment = StringAlignment.Center;      // Vertical alignment

Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 1);
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

## Stap 3: Tekst maken en opmaken – **tekenen** en **een rechthoek met tekst tekenen**

We stellen de tekst samen, definiëren de rechthoek die deze zal bevatten, en tekenen vervolgens zowel de rechthoekrand als de string zelf.

```csharp
string text = "Lorem ipsum ...";  // (Your lengthy text goes here)
Rectangle rectangle = new Rectangle(100, 100, 800, 600);
graphics.DrawRectangle(pen, rectangle);
graphics.DrawString(text, arial, brush, rectangle, stringFormat);
```

### Tekstoverloop afhandelen

Als de opgegeven `text` de grenzen van de rechthoek overschrijdt, heeft u twee veelvoorkomende opties:

1. **De rechthoek vergroten** – vergroot `rectangle.Width` of `rectangle.Height`.  
2. **De tekst splitsen** – splits de string in regels die passen, roep vervolgens `DrawString` aan voor elke regel met aangepaste Y‑coördinaten.

## Stap 4: De uitvoer opslaan – **tekst aan afbeelding toevoegen**

Tot slot schrijft u de bitmap naar schijf. Deze stap demonstreert **add text to image** in één enkele aanroep.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\FormatText_out.png");
```

## Veelvoorkomende problemen en oplossingen

| Probleem | Oplossing |
|----------|-----------|
| **Tekst is gratis** | Zorg ervoor dat `graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;` is ingesteld. |
| **Tekst wordt afgesneden** | Vergroot de grootte van de rechthoek of schakel woord‑wrap‑logica in door de stringgrootte te meten (`Graphics.MeasureString`). |
| **Lettertype niet gevonden** | Controleer of het lettertype is geïnstalleerd op de hostmachine of embed een privé-lettertype met `PrivateFontCollection`. |
| **Onverwachte kleuren** | Controleer de kleuren van penselen en pennen; onthoud dat `Color.FromKnownColor` systeem‑gedefinieerde gebruikte kleuren. |

## Veelgestelde vragen

### Q1: Is Aspose.Drawing compatibel met alle .NET‑versies?

A1: Ja, Aspose.Drawing is ontworpen om compatibel te zijn met een scala aan .NET‑versies, waardoor flexibiliteit voor ontwikkelaars onmogelijk wordt.

### Q2: Kan ik de lettertype‑stijl verder aanpassen?

A2: Absoluut! Pas de parameters van het `Font`-object aan om de uiteindelijke lettergrootte, stijl en familie te bereiken.

### Q3: Hoe kan ik tekst‑overflow binnen de gedefinieerde rechthoekige afhandelen?

A3: U kunt tekst‑overflow beheren door de grootte van de rechthoek aan te passen of aangepaste logica te implementeren om lange tekst te verwerken.

### Q4: Zijn er andere opmaakopties beschikbaar in Aspose.Drawing?

A4: Ja, Aspose.Drawing biedt een uitgebreide set tools voor grafische manipulatie, inclusief diverse opmaakopties voor tekst, vormen en meer.

### Q5: Waar kan ik extra ondersteuning voor Aspose.Drawing vinden?

A5: Verken het Aspose.Drawing‑forum [hier](https://forum.aspose.com/c/drawing/44) voor community‑ondersteuning en discussies.

**Aanvullende vragen en antwoorden**

**Q: Hoe teken ik een string zonder een horizontaal rechthoekig?**
A: Laat de `DrawRectangle`‑aanroep weg en deel de succesvolle `PointF`‑locatie door aan `Graphics.DrawString`.

**Q: Kan ik de tekst roteren terwijl ik de uitlijning behoud?**
A: Ja — pas een `Matrix`‑transformatie toe op het `Graphics`‑object vóór het tekenen, en reset het daarna.

**Q: Is het mogelijk om de afbeelding als JPEG in plaats van PNG te exporteren?**
A: Verander herhaaldelijk de bestandsextensie in `bitmap.Save` en specificeer `ImageFormat.Jpeg`.

---

**Laatst bijgewerkt:** 25-02-2026
**Getest met:** Aspose.Drawing 24.11 voor .NET
**Auteur:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}