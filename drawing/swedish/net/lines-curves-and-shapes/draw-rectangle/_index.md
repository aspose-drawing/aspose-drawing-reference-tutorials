---
date: 2026-08-01
description: Lär dig hur du skapar bitmap-bild C# och ritar en rektangel på bitmap
  med Aspose.Drawing. Steg‑för‑steg‑guide för .NET‑utvecklare.
keywords:
- create bitmap image c#
- draw rectangle on bitmap
- replace system.drawing
lastmod: 2026-08-01
linktitle: Rita rektanglar i Aspose.Drawing
og_description: Skapa bitmap-bild C# och rita rektangel på bitmap med Aspose.Drawing.
  Denna handledning visar hur du generate, style och save rectangle graphics i .NET.
og_image_alt: Guide to drawing rectangles on a bitmap with Aspose.Drawing for .NET
og_title: Skapa bitmap-bild C# – Rita rektangel med Aspose.Drawing
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to create bitmap image C# and draw rectangle on bitmap using
    Aspose.Drawing. Step‑by‑step guide for .NET developers.
  headline: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)`
      before or after drawing the outline.
    question: Can I fill the rectangle with a solid color?
  - answer: Loop through a collection of `Rectangle` structs and call `DrawRectangle`
      for each iteration.
    question: How do I draw multiple rectangles?
  - answer: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform
      after.
    question: Is there a way to rotate the rectangle?
  - answer: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat`
      parameter.
    question: What image formats are supported for saving?
  - answer: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and
      later versions.
    question: Does Aspose.Drawing work on .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- create bitmap image
- Aspose.Drawing
- .NET graphics
- draw rectangle
title: Skapa bitmap-bild C# – Rita rektangel med Aspose.Drawing för .NET
url: /sv/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hur man ritar rektangel med Aspose.Drawing för .NET

## Introduktion

I den här handledningen kommer du att lära dig **hur man ritar rektangel** former samtidigt som du behärskar hur man **skapar bitmap-bild C#** med Aspose.Drawing. Oavsett om du behöver ett enkelt UI‑element eller en högupplöst grafik för en rapport, går vi igenom att skapa en bitmap, konfigurera ett graphics‑objekt, rita rektangeln och spara den slutliga bilden. Metoden fungerar på Windows, Linux och macOS, och den ersätter det äldre `System.Drawing.Common`‑API:et med en fullt plattformsoberoende lösning.

## Snabba svar
- **Vilket bibliotek krävs?** Aspose.Drawing for .NET  
- **Vilken metod ritar formen?** `Graphics.DrawRectangle`  
- **Behöver jag en licens?** En provversion är gratis; en kommersiell licens krävs för produktion.  
- **Kan jag ändra rektangelns storlek?** Ja – justera bredd, höjd och positionsparametrar.  
- **Är koden kompatibel med .NET 6+?** Absolut, Aspose.Drawing stödjer moderna .NET‑versioner.

## Vad betyder “how to draw rectangle” i sammanhanget av Aspose.Drawing?

Att rita en rektangel med Aspose.Drawing använder `Graphics`‑klassen för att rendera en rektangulär kontur eller fylld form på en bitmap‑canvas. Detta ger full kontroll över storlek, färg, linjetjocklek och bildformat, vilket gör det idealiskt för grafik i realtid. Eftersom Aspose.Drawing körs på en ren hanterad motor undviker den de inbyggda GDI+‑begränsningarna i `System.Drawing.Common`.

## Varför använda Aspose.Drawing för att skapa rektangel?

Aspose.Drawing låter dig **rita rektangel på bitmap** utan några plattforms‑specifika DLL‑filer, och det stödjer **30+ output‑format** (inklusive PNG, JPEG, BMP, GIF och TIFF). Det kan bearbeta bilder upp till **10 000 × 10 000 pixlar** samtidigt som minnesanvändningen hålls under **100 MB**, vilket är 2‑3× mer effektivt än den äldre System.Drawing‑implementeringen.

## Förutsättningar

Innan vi dyker ner i koden, se till att du har följande:

- **Aspose.Drawing Library** – ladda ner den från den officiella webbplatsen [here](https://releases.aspose.com/drawing/net/).  
- **Utvecklingsmiljö** – Visual Studio 2022 eller någon .NET‑kompatibel IDE.  
- **Grundläggande .NET‑kunskap** – bekantskap med C#‑syntax och projektstruktur.

## Importera namnrymder

`using`‑direktiven importerar de nödvändiga klasserna till scopet. De krävs för alla ritoperationer.

```csharp
using System.Drawing;
```

## Steg 1: Skapa en bitmap‑bild

`Bitmap` representerar en rasterbild i minnet som du kan rita på. Att skapa den definierar canvas‑storleken och pixelformatet.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## Steg 2: Skapa Graphics‑objekt

`Graphics` är motorn som utför alla ritkommandon på bitmap‑ytan. När du har den kan du rendera former, text och bilder.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## Steg 3: Definiera Pen för rektangel

`Pen` specificerar konturfärgen och tjockleken för rektangeln. Den styr även streckstilar och linjesömmar.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## Steg 4: Rita rektangel på bitmap

`Graphics.DrawRectangle` ritar rektangeln med den tidigare definierade pennan. Du anger X‑, Y‑koordinater samt bredd och höjd för att placera formen exakt där du vill ha den.

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## Steg 5: Spara den ritade bilden

`Bitmap.Save`‑metoden skriver bilden till disk i det format du väljer (t.ex. PNG, JPEG). Detta steg demonstrerar **save drawn image**‑funktionen och slutför bitmap‑filen för återanvändning.

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

Grattis! Du har framgångsrikt slutfört **how to draw rectangle** med Aspose.Drawing för .NET och lärt dig hur man **create bitmap image C#** under processen.

## Vanliga problem och lösningar

| Problem | Orsak | Lösning |
|-------|-------|----------|
| Tom bildutdata | Bitmap inte frigjord eller grafik inte spolas | Anropa `graphics.Dispose();` innan du sparar, eller använd ett `using`‑block. |
| Låga kantkvalitet | Standard smoothing‑läge | Sätt `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`. |
| Fel i filsökväg | Ogiltig katalog | Säkerställ att målmappen finns eller använd `Path.Combine` för att bygga en säker sökväg. |

## Vanliga frågor

**Q: Kan jag fylla rektangeln med en solid färg?**  
A: Ja, skapa en `SolidBrush` och anropa `graphics.FillRectangle(brush, …)` före eller efter att du ritat konturen.

**Q: Hur ritar jag flera rektanglar?**  
A: Loopa igenom en samling av `Rectangle`‑strukturer och anropa `DrawRectangle` för varje iteration.

**Q: Finns det ett sätt att rotera rektangeln?**  
A: Använd `graphics.RotateTransform(angle)` innan du ritar, återställ sedan transformen efteråt.

**Q: Vilka bildformat stöds för sparande?**  
A: PNG, JPEG, BMP, GIF och TIFF stöds alla via rätt `ImageFormat`‑parameter.

**Q: Fungerar Aspose.Drawing på .NET Core?**  
A: Ja, biblioteket är fullt kompatibelt med .NET Core, .NET 5, .NET 6 och senare versioner.

---

**Senast uppdaterad:** 2026-08-01  
**Testat med:** Aspose.Drawing 24.11 for .NET  
**Författare:** Aspose  

## Relaterade handledningar

- [Hur man ritar ellips med Aspose.Drawing för .NET](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [Rita flera linjer med Aspose.Drawing](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [Hur man skapar bitmap aspose.drawing – Rita polygoner i .NET](/drawing/net/lines-curves-and-shapes/draw-polygon/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}