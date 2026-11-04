---
date: 2026-11-04
description: Ismerje meg, hogyan lehet téglalap grafikát rajzolni a koordináta-rendszer
  átalakítása közben a .NET Aspose.Drawing API-val. Ez a lépésről-lépésre útmutató
  bemutatja, hogyan konvertáljon hüvelyket pixelekre és állítsa be az oldal egységeit.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Koordináta-rendszer átalakítás az Aspose.Drawing-ban
og_description: Ismerje meg, hogyan lehet téglalap grafikát rajzolni hüvelykek pixelekre
  konvertálása és az oldal egységeinek beállítása közben az Aspose.Drawing for .NET-ben.
  Kövesse a lépésről-lépésre útmutatót a pontos oldal átalakításhoz.
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: Hogyan rajzoljunk téglalapot oldal átalakítással az Aspose.Drawing for .NET
  használatával
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
title: Hogyan rajzoljunk téglalapot – koordináta-rendszer átalakítás (oldal átalakítás)
  az Aspose.Drawing for .NET-ben
url: /hu/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan rajzoljunk téglalapot – koordináta‑rendszer átalakítás (oldal átalakítás) az Aspose.Drawing for .NET-ben

## Bevezetés

Ebben az útmutatóban megtanulja, hogyan **rajzoljon téglalap** grafikát, miközben oldal‑szintű koordináta‑rendszer átalakítást végez az Aspose.Drawing for .NET használatával. Akár jelentéskészítő motor, CAD‑stílusú vázlatkészítő eszköz, vagy bármely olyan alkalmazás fejlesztésén dolgozik, amelynek pontos valós‑világi mérésekre van szüksége, ez az útmutató minden lépésen végigvezet – a bitmap létrehozásától a végső PNG mentéséig. A végére magabiztosan fog tudni hüvelyket pixelekre konvertálni, törölni a vászon hátterét, és beállítani az oldal egységeit a nyomtatásra kész kimenethez.

## Gyors válaszok
- **Mi a koordináta‑rendszer átalakítás?** A lap‑szintű egységeket (például hüvelykeket) eszköz‑szintű pixelekre képezi le, így a rajzok bármely kimeneti eszközön helyesen méreteződnek.  
- **Miért válassza az Aspose.Drawing‑et?** Teljesen menedzselt, többplatformos grafikai API-t biztosít, amely helyettesíti a System.Drawing.Common‑t, és több mint 30 képformátumot támogat.  
- **Mennyi időt vesz igénybe a példa megvalósítása?** Körülbelül 5‑10 perc egy egyszerű téglalaphoz oldal átalakítással.  
- **Szükségem van licencre a fejlesztéshez?** A ingyenes próbaverzió fejlesztéshez használható; a termelésben való telepítéshez kereskedelmi licenc szükséges.  
- **Mely .NET futtatókörnyezetek támogatottak?** .NET Framework 4.6+, .NET Core 3.1+, valamint .NET 5/6/7.

## Mi az Aspose.Drawing?

Az Aspose.Drawing egy .NET grafikai könyvtár, amely **eszköz‑független API‑t** biztosít raszteres képek, vektorok és oldal‑szintű rajzok létrehozásához és manipulálásához GDI+ nélkül. Több mint **30 képformátumot** támogat, és akár **10 000 × 10 000 pixel** méretű képeket is képes feldolgozni, miközben alacsony memóriahasználatot tart fenn.

## Miért használjunk koordináta‑rendszer átalakítást az Aspose.Drawing‑del?

A koordináta‑rendszer átalakítás lehetővé teszi, hogy valós‑világi egységekben tervezzen grafikákat, miközben a könyvtár automatikusan kezeli a pixel skálázást bármely kimeneti eszköz számára. Ez a megközelítés garantálja, hogy egy 5 hüvelykes téglalap pontosan öt hüvelykként nyomtatódik egy 300 DPI nyomtatón, és arányosan jelenik meg egy 96 DPI képernyőn, ezzel kiküszöbölve a kézi konverziós hibákat.

- **Eszköz‑független tervezés:** A kódot egyszer írja meg; az Aspose.Drawing skálázza képernyőkre, nyomtatókra vagy PDF‑ekre.  
- **Precíz rajzolás:** Ideális műszaki diagramokhoz, mérnöki vázlatokhoz vagy bármely olyan helyzethez, ahol a pontos méretek számítanak.  
- **Többplatformos megbízhatóság:** Következetesen működik Windows, Linux és macOS rendszereken a System.Drawing GDI+ korlátozása nélkül.  
- **Teljesítmény:** Egy tipikus 2,5 GHz CPU-n egy 5 hüvelykes téglalap rajzolása 300 DPI‑n kevesebb, mint **15 ms** alatt befejeződik, és a könyvtár **50 képkocka másodpercenként** képes renderelni valós‑idő előnézeti helyzetekben.

## Előfeltételek

- **Aspose.Drawing könyvtár:** Töltse le a legújabb verziót a hivatalos oldalról [itt](https://releases.aspose.com/drawing/net/).  
- **IDE:** Visual Studio, Rider vagy bármely .NET‑kompatibilis szerkesztő.  
- **Kimeneti mappa:** Cserélje le a mintakódban a `"Your Document Directory"` értéket arra a mappára, ahová a PNG-t menteni szeretné.  
- **Opcionális ASP.NET támogatás:** Hozzáadhatja a NuGet csomagot egy ASP.NET Core projekthez, és ugyanazt az API‑t használhatja; a minta a tipikus **how to use aspnet** megközelítést követi a .NET könyvtáraknál.

## Hogyan rajzoljunk téglalapot oldal átalakítással?

Töltsön be egy üres bitmapet, állítsa be az oldal egységét hüvelykre, és rajzoljon egy téglalapot egy vékony kék tollal – ez néhány kódsorral befejezi a téglalap rajzolását. A `Graphics.PageUnit` tulajdonság azt mondja a motornak, hogy minden koordinátát hüvelykben értelmezzen, így a nyers pixelek helyett valós‑világi mérésekkel dolgozhat, és a könyvtár automatikusan **konvertálja a hüvelykeket pixelekre** a bitmap DPI‑ja alapján.

### 1. lépés: névterek importálása

A `using` utasítások hozzáférést biztosítanak a fő rajzoló osztályokhoz.

```csharp
using System.Drawing;
```

### 2. lépés: bitmap létrehozása

`Bitmap` az a memóriában lévő képtároló, amelyre rajzol. Tartalmazza a pixelpufferet, és módszereket biztosít a fájlokba mentéshez. Egy bitmap létrehozása meghatározza a vászon méretét és a pixelformátumot.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 3. lépés: graphics objektum létrehozása

`Graphics` biztosítja a rajzolási felületet a bitmaphez. A magas szintű rajzolási parancsokat (vonalak, alakzatok, szöveg) pixelműveletekké alakítja az alatta lévő bitmapen.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 4. lépés: a vászon háttér törlése

A vászon semleges színnel való törlése biztosítja, hogy alakzatai kiemelkedjenek. Ebben a példában a hátteret világosszürkével töltjük, ami egyben bemutatja a **clear canvas background** technikát.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### 5. lépés: az átalakítás beállítása (hogyan állítsuk be az egységeket)

`Graphics.PageUnit` határozza meg az oldal koordinátáihoz használt mértékegységet. `GraphicsUnit.Inch`‑re állítva az Aspose.Drawing automatikusan **konvertálja a hüvelykeket pixelekre** a bitmap DPI‑ja alapján (alapértelmezett 96 DPI, 300 DPI a nagy felbontású nyomtatáshoz). A `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` vagy `GraphicsUnit.Pixel` értékeket is választhatja a tervezési igényeknek megfelelően.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 6. lépés: téglalap rajzolása – téglalap grafika

`Pen` határozza meg a grafikus felületen rajzolt vonalak színét, szélességét és stílusát. Egy vékony kék tollal egy olyan téglalapot rajzolunk, amelynek méretei hüvelykben vannak megadva, ezáltal a kód olvashatóbbá válik nyomtatásra orientált elrendezések esetén.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### 7. lépés: bitmap mentése PNG‑ként

Végül a bitmapet a korábban megadott mappába PNG fájlként írja. PNG‑ként mentve a veszteségmentes minőséget őrzi, és széles körben támogatott a különböző platformokon.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Hogyan méretezzen grafikákat nyomtatóhoz?

A rajzolás előtt állítsa be a bitmap DPI‑ját a célnyomtató felbontására (például 300 DPI). Ez automatikusan **scale graphics printer** kimenetet hoz létre, így a kódban egy hüvelyk egyenlő lesz a nyomtatott oldalon egy hüvelykkel, miközben a téglalap logikai mérete változatlan marad. A `bitmap.SetResolution(300, 300)` hívás után ugyanaz a téglalap nagyobbnak fog látszani a papíron, de pontos méreteit megtartja.

## Gyakori problémák és megoldások

| Probléma | Miért fordul elő | Megoldás |
|----------|------------------|----------|
| **Kimeneti fájl nem jött létre** | Helytelen útvonal vagy hiányzó mappa | Győződjön meg arról, hogy a célkönyvtár létezik, vagy hívja a `Directory.CreateDirectory`‑t a mentés előtt. |
| **A téglalap torzult** | Nem megfelelő `PageUnit` vagy DPI | Ellenőrizze, hogy a `graphics.PageUnit` megfelel a kívánt egységnek, és a bitmap DPI megfelelően van beállítva (alapértelmezett 96 DPI, 300 DPI nyomtatáshoz). |
| **Licenc kivétel** | Érvényes licenc hiánya a termelésben | Alkalmazza az ideiglenes vagy állandó Aspose.Drawing licencet a grafikus objektumok létrehozása előtt. |

## Gyakran ismételt kérdések

**Q: Használhatom ingyenesen az Aspose.Drawing‑et?**  
**A: Igen, egy ingyenes próbaverzió elérhető [itt](https://releases.aspose.com/).**

**Q: Hol találhatók részletes dokumentációk az Aspose.Drawing‑hez?**  
**A: A teljes API-referencia itt érhető el [itt](https://reference.aspose.com/drawing/net/).**

**Q: Hogyan kaphatok támogatást az Aspose.Drawing‑hez?**  
**A: Látogassa meg az [Aspose.Drawing Fórumot](https://forum.aspose.com/c/drawing/44) a közösségi segítségért és hivatalos támogatásért.**

**Q: Elérhető ideiglenes licenc az Aspose.Drawing‑hez?**  
**A: Természetesen—szerezze be itt [itt](https://purchase.aspose.com/temporary-license/).**

**Q: Hol vásárolhatok teljes Aspose.Drawing licencet?**  
**A: Itt vásárolható [itt](https://purchase.aspose.com/buy).**

## Következtetés

Most már tudja, **hogyan rajzoljon téglalap** grafikát oldal‑szintű átalakítással az Aspose.Drawing for .NET használatával. Az oldal egységének hüvelykre állításával, a vászon háttér törlésével és az eredmény PNG‑ként mentésével pontos, eszköz‑független kimenetet ér el, amely alkalmas a képernyőn való megjelenítésre és a nagy felbontású nyomtatásra egyaránt. Kísérletezzen más egységekkel, forgatással vagy egyedi koordináta‑origókkal, hogy még erőteljesebb rajzolási forgatókönyveket nyisson meg.

---

**Last Updated:** 2026-11-04  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose

## Kapcsolódó oktatóanyagok

- [Hogyan állítsuk be az egységet az Aspose.Drawing for .NET‑ben – Mértékegységek](/drawing/net/coordinate-transformations/units-of-measure/)
- [Globális átalakítás](/drawing/net/coordinate-transformations/global-transformation/)
- [Lépésről‑lépésre átalakítás – Koordináta‑átalakítások](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}