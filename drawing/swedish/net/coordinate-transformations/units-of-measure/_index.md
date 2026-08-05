---
date: 2026-05-24
description: Lär dig hur du ställer in enhet i Aspose.Drawing för .NET, konvertera
  graphics units enkelt och behärska precise measurements för graphics rendering.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Units of Measure i Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  headline: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  type: TechArticle
- description: Learn how to set unit in Aspose.Drawing for .NET, convert graphics
    units easily, and master precise measurements for graphics rendering.
  name: How to Set Unit in Aspose.Drawing for .NET – Units of Measure
  steps:
  - name: Create a Bitmap
    text: The `Bitmap` class represents an in‑memory image that serves as a drawing
      canvas.
  - name: Create a Graphics Object
    text: '`Graphics` provides drawing methods for rendering shapes and text onto
      a `Bitmap`.'
  - name: Set Page Unit to Points
    text: '`PageUnit` is an enumeration that specifies the unit of measure for page
      coordinates. `PageUnit.Point` defines points as the unit of measure (1 point
      = 1/72 inch). This setting applies to all subsequent drawing calls.'
  - name: Draw a Rectangle in Points
    text: When you draw a rectangle after setting the unit, the dimensions you specify
      are interpreted as points, ensuring precise sizing.
  - name: Set Page Unit to Millimeters
    text: Assign `PageUnit.Millimeter` to the `Graphics` object; all coordinates now
      map to the metric system.
  - name: Draw a Rectangle in Millimeters
    text: The rectangle’s width and height are now expressed in millimeters, making
      it easy to align with physical measurements and ensuring that printed output
      matches real‑world sizes.
  - name: Set Page Unit to Inches
    text: '`PageUnit.Inch` changes the coordinate system so that 1 unit equals 1 inch,
      providing a straightforward way to size elements for print‑oriented layouts.
      CODE_BLOCK_PLACEHOLDER_10_END'
  - name: Draw a Rectangle in Inches
    text: Now any shape you draw uses inches as its measurement base, which is ideal
      for print layouts and for communicating dimensions to stakeholders accustomed
      to imperial units. CODE_BLOCK_PLACEHOLDER_11_END
  type: HowTo
- questions:
  - answer: Call `graphics.PageUnit = PageUnit.Point` (or `.Millimeter`, `.Inch`)
      on the `Graphics` object.
    question: What is the primary way to change units?
  - answer: Points.
    question: Which unit equals 1/72 inch?
  - answer: 25.4 mm = 1 inch.
    question: How many millimeters are in an inch?
  - answer: No, the Aspose.Drawing core library provides all unit constants.
    question: Do I need extra libraries to use units?
  - answer: Set the unit once per `Graphics` instance; draw everything using that
      unit for consistency.
    question: Can I mix units in one image?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Hur man ställer in enhet i Aspose.Drawing för .NET – Units of Measure
url: /sv/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man anger enhet i Aspose.Drawing för .NET – Måttenheter

## Introduktion

Välkommen till världen av Aspose.Drawing för .NET, där precision och flexibilitet möts i grafisk manipulation. I den här handledningen kommer du att upptäcka **hur man anger enhet** för dina ritningar, lära dig att **konvertera grafikens enheter** mellan punkter, millimeter och tum, samt se verkliga exempel som gör dina bilder pixelperfekta. Oavsett om du bygger rapporter, miniatyrbilder eller anpassade diagram är det avgörande att behärska måttenheter för en konsekvent återgivning på alla enheter.

## Snabba svar
- **Vad är det primära sättet att ändra enheter?** Anropa `graphics.PageUnit = PageUnit.Point` (eller `.Millimeter`, `.Inch`) på `Graphics`‑objektet.  
- **Vilken enhet motsvarar 1/72 tum?** Punkter.  
- **Hur många millimeter är i en tum?** 25,4 mm = 1 tum.  
- **Behöver jag extra bibliotek för att använda enheter?** Nej, Aspose.Drawing‑kärnbiblioteket tillhandahåller alla enhetskonstanter.  
- **Kan jag blanda enheter i en bild?** Ställ in enheten en gång per `Graphics`‑instans; rita allt med den enheten för konsekvens.

## Förutsättningar

Innan vi dyker ner i handledningen, se till att du har följande förutsättningar på plats:

- Aspose.Drawing för .NET: Säkerställ att du har biblioteket installerat. Du kan ladda ner det [here](https://releases.aspose.com/drawing/net/).
- Dokumentkatalog: Ha en avsedd katalog där du vill spara dina skapade dokument.
- Grundläggande C#‑kunskaper: En grundläggande förståelse för C# rekommenderas för att få ut det mesta av den här guiden.

## Importera namnrymder

Innan vi börjar, låt oss importera de nödvändiga namnrymderna för att använda Aspose.Drawing effektivt:

```csharp
using System.Drawing;
```

Nu ska vi bryta ner varje exempel i flera steg:

## Hur man anger enhet till punkter?

`Bitmap`‑klassen representerar en bild i minnet som fungerar som en ritningsyta. Ladda din bitmap, skapa ett `Graphics`‑objekt och sätt sidans enhet till punkter — detta talar om för Aspose.Drawing att tolka alla koordinater som 1/72 tum‑värden. Att använda punkter ger dig finjusterad kontroll för utskriftsklara grafik och låter dig specificera linjebredder med hög precision.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Steg 1: Skapa en Bitmap  
`Bitmap`‑klassen representerar en bild i minnet som fungerar som en ritningsyta.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Steg 2: Skapa ett Graphics‑objekt  
`Graphics` tillhandahåller ritmetoder för att rendera former och text på en `Bitmap`.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### Steg 3: Ställ in Page Unit till punkter  
`PageUnit` är en uppräkning som specificerar måttenheten för sidkoordinater. `PageUnit.Point` definierar punkter som måttenhet (1 punkt = 1/72 tum). Denna inställning gäller för alla efterföljande ritningsanrop.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### Steg 4: Rita en rektangel i punkter  
När du ritar en rektangel efter att ha ställt in enheten tolkas de dimensioner du anger som punkter, vilket säkerställer exakt storlek.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Hur man anger enhet till millimeter?

`PageUnit` är en uppräkning som specificerar måttenheten för sidkoordinater. Att byta till millimeter är praktiskt när du behöver metrisk dimensionering, till exempel vid generering av ingenjörsdiagram. Aspose.Drawing behandlar 1 mm som 1/25,4 tum, vilket låter dig anpassa grafik till fysiska mått som används i tillverkning och teknisk dokumentation.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### Steg 1: Ställ in Page Unit till millimeter  
Tilldela `PageUnit.Millimeter` till `Graphics`‑objektet; alla koordinater mappar nu till det metriska systemet.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Steg 2: Rita en rektangel i millimeter  
Rektangelns bredd och höjd uttrycks nu i millimeter, vilket gör det enkelt att anpassa till fysiska mått och säkerställer att utskriften matchar verkliga storlekar.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Hur man anger enhet till tum?

`Graphics` tillhandahåller ritmetoder för att rendera former och text på en `Bitmap`. Tum är standardenheten för många amerikanska designverktyg. Att ställa in enheten till tum låter dig tänka i bekanta termer när du lägger upp UI‑element, och förenklar övergången från skärmdesign till utskrift där tum ofta används.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### Steg 1: Ställ in Page Unit till tum  
`PageUnit.Inch` ändrar koordinatsystemet så att 1 enhet motsvarar 1 tum, vilket ger ett enkelt sätt att dimensionera element för utskriftsorienterade layouter.

CODE_BLOCK_PLACEHOLDER_10_END

### Steg 2: Rita en rektangel i tum  
Nu använder alla former du ritar tum som mätnorm, vilket är idealiskt för utskriftslayouter och för att kommunicera dimensioner till intressenter som är vana vid det imperiska systemet.

CODE_BLOCK_PLACEHOLDER_11_END

## Spara resultatet

Efter att ha slutfört exemplen, spara den resulterande bilden i din dokumentkatalog. `Bitmap.Save`‑metoden skriver filen i det format du specificerar (PNG, JPEG, osv.).

CODE_BLOCK_PLACEHOLDER_12_END

Nu har du framgångsrikt navigerat de olika måttenheterna i Aspose.Drawing för .NET och skapat en visuell representation av rektanglar med punkter, millimeter och tum.

## Varför använda Aspose.Drawing:s enhetssystem?

Aspose.Drawing stödjer **30+ bildformat** och kan bearbeta bilder upp till **5000 × 5000 pixlar** utan att ladda hela filen i minnet, vilket ger hög prestanda för storskalig grafikgenerering. Genom att explicit ange enheten eliminerar du gissningar, minskar konverteringsfel och säkerställer att ditt resultat matchar exakta fysiska dimensioner på alla plattformar.

## Vanliga problem och lösningar

- **Oväntad storlek efter sparande** – Verifiera att du har ställt in `graphics.PageUnit` **före** några ritningsanrop; att ändra enheten senare ändrar inte befintliga former retroaktivt.  
- **Suddig utskrift på hög‑DPI‑skärmar** – Öka bitmapens upplösning (t.ex. `new Bitmap(width, height, 300)`) för att matcha mål‑DPI.  
- **Blandade enheter i en bild** – Skapa separata `Graphics`‑instanser för varje enhet eller utför manuell konvertering innan ritning.

## Vanliga frågor

### Q1: Kan jag använda Aspose.Drawing för .NET med andra .NET‑ramverk?
A1: Ja, Aspose.Drawing är kompatibel med olika .NET‑ramverk, vilket ger flexibilitet i din utvecklingsmiljö.

### Q2: Finns en gratis provversion tillgänglig?
A2: Ja, du kan utforska Aspose.Drawing med en gratis provversion [here](https://releases.aspose.com/).

### Q3: Hur får jag support för Aspose.Drawing för .NET?
A3: Besök [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) för community‑support och diskussioner.

### Q4: Kan jag köpa en tillfällig licens för korttidsprojekt?
A4: Ja, du kan skaffa en tillfällig licens [here](https://purchase.aspose.com/temporary-license/).

### Q5: Var kan jag hitta detaljerad dokumentation för Aspose.Drawing?
A5: Den omfattande dokumentationen finns [here](https://reference.aspose.com/drawing/net/).

---

**Last Updated:** 2026-05-24  
**Tested With:** Aspose.Drawing 24.11 för .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
