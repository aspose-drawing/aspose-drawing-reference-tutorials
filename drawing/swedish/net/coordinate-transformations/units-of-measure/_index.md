---
title: Måttenheter i Aspose.Drawing för .NET
linktitle: Måttenheter i Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternativ till System.Drawing.Common
description: Utforska mångsidigheten hos Aspose.Drawing för .NET i denna djupgående handledning, där du behärskar måttenheter för precisionsgrafik.
weight: 14
url: /sv/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Måttenheter i Aspose.Drawing för .NET

## Introduktion

Välkommen till Aspose.Drawings värld för .NET, där precision och flexibilitet möts i grafisk manipulation. I den här handledningen kommer vi att fördjupa oss i krångligheterna med måttenheter inom Aspose.Drawing, vilket ger dig en steg-för-steg-guide för att utnyttja kraften i detta enastående bibliotek.

## Förutsättningar

Innan vi dyker in i handledningen, se till att du har följande förutsättningar på plats:

-  Aspose.Drawing för .NET: Se till att du har biblioteket installerat. Du kan ladda ner den[här](https://releases.aspose.com/drawing/net/).

- Dokumentkatalog: Ha en utsedd katalog där du vill spara dina skapade dokument.

- Grundläggande C#-kunskap: En grundläggande förståelse för C# rekommenderas för att få ut det mesta av den här guiden.

## Importera namnområden

Innan vi börjar, låt oss importera de nödvändiga namnrymden för att använda Aspose.Drawing effektivt:

```csharp
using System.Drawing;
```

Låt oss nu dela upp varje exempel i flera steg:

## Poäng som måttenheter

1. Skapa en bitmapp: Initiera en bitmapp med en angiven bredd och höjd.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. Skapa grafik: Skapa ett grafikobjekt från bitmappen för att rita på det.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. Ställ in sidenhet till punkter: Definiera punkter som måttenhet (1 punkt = 1/72 tum).

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. Rita rektangel: Rita en rektangel med punkter som enhet.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## Millimeter som måttenheter

1. Ställ in sidenhet till millimeter: Ändra måttenheten till millimeter (1 mm = 1/25,4 tum).

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. Rita rektangel i millimeter: Rita en annan rektangel med millimeter som enhet.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## Inches som måttenheter

1. Ställ in sidenhet till tum: Ändra måttenheten till tum.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. Rita rektangel i tum: Rita en rektangel med tum som enhet.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Spara resultatet

När du har slutfört exemplen sparar du den resulterande bilden i din dokumentkatalog:

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

Nu har du framgångsrikt navigerat mellan de olika måttenheterna i Aspose.Drawing för .NET, och skapat en visuell representation av rektanglar med hjälp av punkter, millimeter och tum.

## Slutsats

I den här handledningen har vi utforskat hur Aspose.Drawing för .NET hanterar olika måttenheter. Genom att manipulera punkter, millimeter och tum kan du uppnå precision och anpassningsförmåga i dina grafiska skapelser. Experimentera med dessa koncept för att frigöra Aspose.Drawings fulla potential.

## FAQ's

### F1: Kan jag använda Aspose.Drawing för .NET med andra .NET-ramverk?

S1: Ja, Aspose.Drawing är kompatibel med olika .NET-ramverk, vilket ger flexibilitet i din utvecklingsmiljö.

### F2: Finns det en gratis provperiod?

 S2: Ja, du kan utforska Aspose.Drawing med en gratis provperiod[här](https://releases.aspose.com/).

### F3: Hur får jag support för Aspose.Drawing för .NET?

 A3: Besök[Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) för samhällsstöd och diskussioner.

### F4: Kan jag köpa en tillfällig licens för kortsiktiga projekt?

 A4: Ja, du kan få en tillfällig licens[här](https://purchase.aspose.com/temporary-license/).

### F5: Var kan jag hitta detaljerad dokumentation för Aspose.Drawing?

 S5: Den omfattande dokumentationen finns tillgänglig[här](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
