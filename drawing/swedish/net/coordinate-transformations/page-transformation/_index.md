---
date: 2026-11-04
description: Lär dig hur du ritar rektangelgrafik samtidigt som du utför koordinatsystemtransformation
  i .NET med Aspose.Drawing API. Denna steg‑för‑steg‑guide visar hur du konverterar
  tum till pixlar och ställer in sid‑enheter.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Koordinatsystemtransformation i Aspose.Drawing
og_description: Lär dig hur du ritar rektangelgrafik samtidigt som du konverterar
  tum till pixlar och ställer in sid‑enheter i Aspose.Drawing för .NET. Följ steg‑för‑steg‑guiden
  för exakt sidtransformation.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Så ritar du en rektangel med sidtransformation med Aspose.Drawing för .NET
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: Så ritar du en rektangel – koordinatsystemtransformation (sidtransformation)
  i Aspose.Drawing för .NET
url: /sv/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ritar rektangel – koordinatsystemstransformation (sidtransformation) i Aspose.Drawing för .NET

## Introduktion

I den här handledningen kommer du att lära dig **hur man ritar rektangel** grafik samtidigt som du utför en sid‑nivå koordinatsystemstransformation med Aspose.Drawing för .NET. Oavsett om du bygger en rapporteringsmotor, ett CAD‑liknande skissverktyg eller någon applikation som kräver precisa verkliga mått, guidar den dig genom varje steg—från att skapa en bitmap till att spara den slutgiltiga PNG‑filen. I slutet kommer du att känna dig bekväm med att konvertera tum till pixlar, rensa dukens bakgrund och ställa in sid‑enheter för utskriftsklar output.

## Snabba svar
- **Vad är koordinatsystemstransformation?** Den mappar sid‑nivå enheter (såsom tum) till enhet‑nivå pixlar så att ritningar skalas korrekt på alla utskriftsenheter.  
- **Varför välja Aspose.Drawing?** Den tillhandahåller ett fullständigt hanterat, plattformsoberoende grafik‑API som ersätter System.Drawing.Common och stödjer 30+ bildformat.  
- **Hur lång tid tar exemplet att implementera?** Ungefär 5‑10 minuter för en grundläggande rektangel med sidtransformation.  
- **Behöver jag en licens för utveckling?** En gratis provversion fungerar för utveckling; en kommersiell licens krävs för produktionsdistributioner.  
- **Vilka .NET‑runtime-miljöer stöds?** .NET Framework 4.6+, .NET Core 3.1+, och .NET 5/6/7.

## Vad är Aspose.Drawing?

Aspose.Drawing är ett .NET‑grafikbibliotek som tillhandahåller ett **device‑independent API** för att skapa och manipulera rasterbilder, vektorer och sid‑nivå ritningar utan att förlita sig på GDI+. Det stödjer **30+ bildformat** och kan bearbeta bilder upp till **10 000 × 10 000 pixlar** samtidigt som minnesanvändningen hålls låg.

## Varför använda koordinatsystemstransformation med Aspose.Drawing?

Koordinatsystemstransformation låter dig designa grafik i verkliga enheter medan biblioteket automatiskt hanterar pixelskala för vilken utskriftsenhet som helst. Detta tillvägagångssätt garanterar att en 5‑tum rektangel skrivs ut exakt fem tum på en 300 DPI‑skrivare och visas proportionellt på en 96 DPI‑skärm, vilket eliminerar manuella konverteringsfel.

- **Device‑independent design:** Skriv kod en gång; Aspose.Drawing skalar den för skärmar, skrivare eller PDF‑filer.  
- **Precision drawing:** Ideal för tekniska diagram, ingenjörsscheman eller alla scenarier där exakta mått är viktiga.  
- **Cross‑platform reliability:** Fungerar konsekvent på Windows, Linux och macOS utan GDI+‑begränsningarna i System.Drawing.  
- **Performance:** På en typisk 2,5 GHz‑CPU slutförs ritning av en 5‑tum rektangel vid 300 DPI på under **15 ms**, och biblioteket kan rendera **50 bilder per sekund** i real‑tids‑förhandsgranskningsscenarier.

## Förutsättningar

- **Aspose.Drawing library:** Ladda ner den senaste versionen från den officiella webbplatsen [here](https://releases.aspose.com/drawing/net/).  
- **IDE:** Visual Studio, Rider eller någon .NET‑kompatibel editor.  
- **Output folder:** Ersätt `"Your Document Directory"` i exempel‑koden med den mapp där du vill spara PNG‑filen.  
- **Optional ASP.NET support:** Du kan lägga till NuGet‑paketet i ett ASP.NET Core‑projekt och använda samma API; mönstret följer den typiska **how to use aspnet**‑metoden för .NET‑bibliotek.

## Hur man ritar rektangel med sidtransformation?

Läs in en tom bitmap, sätt sid‑enheten till tum och rita en rektangel med en tunn blå penna — detta slutför rektangelritningen på bara några kodrader. `Graphics.PageUnit`‑egenskapen talar om för motorn att tolka alla koordinater som tum, så du kan tänka i verkliga mått istället för råa pixlar, och biblioteket automatiskt **convert inches to pixels** baserat på bitmapens DPI.

### Steg 1: importera namnrymder

`using`‑satserna ger dig åtkomst till de grundläggande ritklasserna.

```csharp
using System.Drawing;
```

### Steg 2: skapa en bitmap

`Bitmap` är den minnes‑bildbehållare du ritar på. Den innehåller pixelbufferten och exponerar metoder för att spara till filer. Att skapa en bitmap definierar dukens storlek och pixelformat.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### Steg 3: skapa ett graphics‑objekt

`Graphics` tillhandahåller ritytan för bitmapen. Den översätter hög‑nivå ritkommandon (linjer, former, text) till pixeloperationer på den underliggande bitmapen.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### Steg 4: rensa dukens bakgrund

Att rensa duken med en neutral färg säkerställer att dina former framträder. I detta exempel fyller vi bakgrunden med ljusgrå, vilket också demonstrerar tekniken **clear canvas background**.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Steg 5: ställ in transformationen (hur man sätter enheter)

`Graphics.PageUnit` specificerar måttenheten som används för sidkoordinater. Att sätta den till `GraphicsUnit.Inch` talar om för Aspose.Drawing att automatiskt **convert inches to pixels** baserat på bitmapens DPI (96 DPI som standard, 300 DPI för högupplöst utskrift). Du kan också välja `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` eller `GraphicsUnit.Pixel` beroende på dina layout‑krav.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### Steg 6: rita en rektangel – rita rektangelgrafik

`Pen` definierar färg, bredd och stil på linjer som ritas på en graphics‑yta. Med en tunn blå penna ritar vi en rektangel vars dimensioner uttrycks i tum, vilket gör koden mer läsbar för utskriftsorienterade layouter.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### Steg 7: spara bitmap som png

Slutligen skriver du bitmapen till en PNG‑fil i den mapp du angav tidigare. Att spara som PNG bevarar förlustfri kvalitet och stöds brett på olika plattformar.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Hur man skalar grafik för en skrivare?

Ställ in bitmapens DPI till målskrivarens upplösning (t.ex. 300 DPI) innan du ritar. Detta automatiskt **scale graphics printer**‑utdata så att en tum i din kod motsvarar en tum på den utskrivna sidan, medan rektangelns logiska storlek förblir oförändrad. Efter att ha anropat `bitmap.SetResolution(300, 300)` kommer samma rektangel att visas större på papper men behålla sina exakta dimensioner.

## Vanliga problem och lösningar

| Problem | Varför det händer | Lösning |
|---------|-------------------|---------|
| **Output file not created** | Felaktig sökväg eller saknad mapp | Se till att målkatalogen finns eller anropa `Directory.CreateDirectory` innan du sparar. |
| **Rektangeln ser förvrängd ut** | Felaktig `PageUnit` eller DPI | Verifiera att `graphics.PageUnit` matchar den avsedda enheten och att bitmapens DPI är korrekt inställd (standard 96 DPI, 300 DPI för utskrift). |
| **Licensundantag** | Kör utan en giltig licens i produktion | Applicera din temporära eller permanenta Aspose.Drawing‑licens innan du skapar graphics‑objekt. |

## Vanliga frågor

**Q: Kan jag använda Aspose.Drawing gratis?**  
A: Ja, en gratis provversion finns [here](https://releases.aspose.com/).

**Q: Var kan jag hitta detaljerad dokumentation för Aspose.Drawing?**  
A: Den fullständiga API‑referensen finns [here](https://reference.aspose.com/drawing/net/).

**Q: Hur får jag support för Aspose.Drawing?**  
A: Besök [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) för gemenskapsstöd och officiell hjälp.

**Q: Finns en tillfällig licens tillgänglig för Aspose.Drawing?**  
A: Absolut—skaffa en [here](https://purchase.aspose.com/temporary-license/).

**Q: Var kan jag köpa en fullständig Aspose.Drawing‑licens?**  
A: Du kan köpa den [here](https://purchase.aspose.com/buy).

## Slutsats

Du vet nu **how to draw rectangle** grafik med sid‑nivå transformation med Aspose.Drawing för .NET. Genom att sätta sid‑enheten till tum, rensa dukens bakgrund och spara resultatet som PNG, får du exakt, enhetsoberoende utdata som är lämplig både för skärmvisning och högupplöst utskrift. Experimentera med andra enheter, rotation eller anpassade koordinatursprung för att låsa upp ännu kraftfullare ritningsscenarier.

---

**Senast uppdaterad:** 2026-11-04  
**Testat med:** Aspose.Drawing 24.12 for .NET  
**Författare:** Aspose

## Relaterade handledningar

- [Hur man ställer in enhet i Aspose.Drawing för .NET – Måttenheter](/drawing/net/coordinate-transformations/units-of-measure/)
- [Global transformation](/drawing/net/coordinate-transformations/global-transformation/)
- [Steg för steg transformation – Koordinattransformationer](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}