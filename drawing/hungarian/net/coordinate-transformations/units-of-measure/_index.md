---
date: 2026-05-24
description: Tanulja meg, hogyan állíthatja be az egységet az Aspose.Drawing for .NET-ben,
  könnyedén konvertálhatja a grafikai egységeket, és mesteri pontosságú méréseket
  érhet el a grafikai megjelenítéshez.
keywords:
- how to set unit
- convert graphics units
- Aspose.Drawing units of measure
linktitle: Units of Measure az Aspose.Drawing-ben
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
title: Hogyan állítsuk be az egységet az Aspose.Drawing for .NET-ben – Units of Measure
url: /hu/net/coordinate-transformations/units-of-measure/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan állítsuk be a mértékegységet az Aspose.Drawing for .NET‑ben – Mértékegységek

## Bevezetés

Üdvözöljük az Aspose.Drawing for .NET világában, ahol a pontosság és a rugalmasság találkozik a grafikai manipulációban. Ebben az oktatóanyagról megtudja, **hogyan állítsa be a mértékegységet** a rajzokhoz, megtanulja a **grafikai egységek átalakítását** pontok, milliméter és hüvelyk között, és valós példákat láthat, amelyek pixel‑tökéletes képeket eredményeznek. Akár jelentéseket, bélyegképeket vagy egyedi diagramokat készít, a mértékegységek elsajátítása elengedhetetlen a konzisztens megjelenítéshez különböző eszközökön.

## Gyors válaszok
- **Mi a legfőbb módja az egységek módosításának?** Hívja a `graphics.PageUnit = PageUnit.Point` (vagy `.Millimeter`, `.Inch`) metódust a `Graphics` objektumon.  
- **Melyik egység egyenlő 1/72 hüvelykkel?** Pontok.  
- **Hány milliméter van egy hüvelykben?** 25,4 mm = 1 hüvelyk.  
- **Szükség van extra könyvtárakra az egységek használatához?** Nem, az Aspose.Drawing alapkönyvtára tartalmazza az összes egységkonstansot.  
- **Keverhetem-e az egységeket egy képen?** Állítsa be az egységet egyszer a `Graphics` példányra; minden rajzolást az adott egységgel végezzen a konzisztencia érdekében.

## Előfeltételek

Mielőtt belemerülnénk az oktatóanyagba, győződjön meg róla, hogy a következő előfeltételek rendelkezésre állnak:

- Aspose.Drawing for .NET: Győződjön meg róla, hogy a könyvtár telepítve van. Letöltheti [itt](https://releases.aspose.com/drawing/net/).
- Dokumentumkönyvtár: Legyen egy kijelölt könyvtár, ahová a létrehozott dokumentumokat menti.
- Alapvető C# ismeretek: Ajánlott a C# alapjainak ismerete a leírás teljes kihasználásához.

## Névterek importálása

Mielőtt elkezdenénk, importáljuk a szükséges névtereket az Aspose.Drawing hatékony használatához:

```csharp
using System.Drawing;
```

Most bontsuk le minden példát több lépésre:

## Hogyan állítsuk be az egységet Pontokra?

A `Bitmap` osztály egy memóriában lévő képet képvisel, amely rajzoló vászonként szolgál. Töltse be a bitmapet, hozzon létre egy `Graphics` objektumot, és állítsa be az oldal egységét pontokra – ez azt mondja az Aspose.Drawing‑nek, hogy minden koordinátát 1/72 hüvelyk értékként értelmezzen. A pontok használata finomhangolt vezérlést biztosít nyomtatásra kész grafikákhoz, és lehetővé teszi a vonalvastagság pontos megadását.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 1. lépés: Bitmap létrehozása  
A `Bitmap` osztály egy memóriában lévő képet képvisel, amely rajzoló vászonként szolgál.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 2. lépés: Graphics objektum létrehozása  
A `Graphics` rajzoló metódusokat biztosít alakzatok és szöveg megjelenítéséhez egy `Bitmap`‑en.

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

### 3. lépés: Oldal egységének beállítása Pontokra  
A `PageUnit` egy felsorolás, amely meghatározza az oldal koordinátáinak mértékegységét. A `PageUnit.Point` pontokat definiál mértékegységként (1 pont = 1/72 hüvelyk). Ez a beállítás minden későbbi rajzolási hívásra érvényes.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

### 4. lépés: Téglalap rajzolása Pontokban  
Amikor az egységet beállítva téglalapot rajzol, a megadott méretek pontként értelmeződnek, biztosítva a pontos méretezést.

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

## Hogyan állítsuk be az egységet Milliméterben?

A `PageUnit` egy felsorolás, amely meghatározza az oldal koordinátáinak mértékegységét. A milliméterre váltás akkor hasznos, ha metrikus méretekre van szükség, például mérnöki diagramok generálásakor. Az Aspose.Drawing 1 mm‑t 1/25,4 hüvelyknek tekint, lehetővé téve a grafikák összehangolását a gyártásban és a műszaki dokumentációban használt fizikai méretekkel.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

### 1. lépés: Oldal egységének beállítása Milliméterre  
Rendelje a `PageUnit.Millimeter` értéket a `Graphics` objektumhoz; minden koordináta most a metrikus rendszerhez igazodik.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 2. lépés: Téglalap rajzolása Milliméterben  
A téglalap szélessége és magassága most milliméterben van kifejezve, ami megkönnyíti a fizikai méretekkel való összehangolást, és biztosítja, hogy a nyomtatott kimenet a valós méretekkel egyezzen.

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## Hogyan állítsuk be az egységet Hüvelykben?

A `Graphics` rajzoló metódusokat biztosít alakzatok és szöveg megjelenítéséhez egy `Bitmap`‑en. A hüvelyk az alapértelmezett egység sok amerikai tervezőeszköz számára. Az egység hüvelykre állítása lehetővé teszi, hogy ismerős mértékegységekben gondolkodjon a UI elemek elrendezésekor, és egyszerűsíti a képernyőtervezésről a nyomtatásra való átmenetet, ahol a hüvelyk gyakran használt.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

### 1. lépés: Oldal egységének beállítása Hüvelykben  
A `PageUnit.Inch` úgy módosítja a koordináta rendszert, hogy 1 egység = 1 hüvelyk, egyszerű módot biztosítva az elemek méretezésére nyomtatási elrendezésekhez.

CODE_BLOCK_PLACEHOLDER_10_END

### 2. lépés: Téglalap rajzolása Hüvelykben  
Most minden alakzat hüvelykben mérve kerül rajzolásra, ami ideális nyomtatási elrendezésekhez és az imperial egységekkel dolgozó érintettek számára.

CODE_BLOCK_PLACEHOLDER_11_END

## Az eredmény mentése

A példák befejezése után mentse a kapott képet a dokumentumkönyvtárba. A `Bitmap.Save` metódus a megadott formátumban (PNG, JPEG stb.) írja ki a fájlt.

CODE_BLOCK_PLACEHOLDER_12_END

Most sikeresen megtanulta az Aspose.Drawing for .NET különböző mértékegységeit, és pontok, milliméter és hüvelyk használatával hozott létre téglalapokat.

## Miért használjuk az Aspose.Drawing egységrendszerét?

Az Aspose.Drawing **30+ képformátumot** támogat, és akár **5000 × 5000 pixel** méretű képeket is képes feldolgozni anélkül, hogy a teljes fájlt a memóriába töltené, így nagy‑léptékű grafikai generálás esetén is magas teljesítményt nyújt. Az egység kifejezett beállításával kiküszöbölheti a találgatást, csökkentheti a konverziós hibákat, és biztosíthatja, hogy a kimenet pontos fizikai méretekkel egyezzen minden platformon.

## Gyakori problémák és megoldások

- **Váratlan méret mentés után** – Ellenőrizze, hogy a `graphics.PageUnit`‑ot **a rajzolási hívások előtt** állította be; az egység későbbi módosítása nem méretezi át a már létező alakzatokat.  
- **Homályos kimenet magas DPI‑jú képernyőkön** – Növelje a bitmap felbontását (pl. `new Bitmap(width, height, 300)`) a cél DPI‑hoz igazítva.  
- **Keveredő egységek egy képen** – Hozzon létre külön `Graphics` példányokat minden egységhez, vagy végezze el a manuális konverziót a rajzolás előtt.

## Gyakran feltett kérdések

### Q1: Használhatom az Aspose.Drawing for .NET‑et más .NET keretrendszerekkel?
A1: Igen, az Aspose.Drawing kompatibilis különböző .NET keretrendszerekkel, így rugalmasan alkalmazható fejlesztési környezetében.

### Q2: Van ingyenes próbaverzió?
A2: Igen, az Aspose.Drawing ingyenes próbaverzióját [itt](https://releases.aspose.com/) tekintheti meg.

### Q3: Hogyan kaphatok támogatást az Aspose.Drawing for .NET‑hez?
A3: Látogassa meg az [Aspose.Drawing Fórumot](https://forum.aspose.com/c/drawing/44) a közösségi támogatás és megbeszélések érdekében.

### Q4: Vásárolhatok ideiglenes licencet rövid távú projektekhez?
A4: Igen, ideiglenes licencet [itt](https://purchase.aspose.com/temporary-license/) szerezhet be.

### Q5: Hol találok részletes dokumentációt az Aspose.Drawing‑hez?
A5: A teljes körű dokumentáció [itt](https://reference.aspose.com/drawing/net/) érhető el.

---

**Utoljára frissítve:** 2026-05-24  
**Tesztelt verzió:** Aspose.Drawing 24.11 for .NET  
**Szerző:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Kapcsolódó oktatóanyagok

- [Coordinate System Transformation – Page Transformation in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/page-transformation/)
- [Matrix Transformation Tutorial: Matrix Transformations in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/matrix-transformations/)
- [How to Apply Transformation: Local Transformation in Aspose.Drawing for .NET](/drawing/net/coordinate-transformations/local-transformation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}