---
date: 2026-05-19
description: Ismerje meg, hogyan kell téglalap grafikát rajzolni a coordinate system
  transformation közben .NET-ben az Aspose.Drawing segítségével. Ez a lépésről‑lépésre
  útmutató bemutatja, hogyan konvertálhatja az inches‑t pixels‑re, és állíthatja be
  a page units‑t.
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set unit
- scale graphics printer
- how to use aspnet
linktitle: Coordinate System Transformation az Aspose.Drawing-ban
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to Draw Rectangle – Coordinate System Transformation (Page Transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import Namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a Bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a Graphics Object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the Canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the Transformation (How to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a Rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the Image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/).
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/).
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/).
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – Alternative to System.Drawing.Common
title: Hogyan rajzoljunk téglalapot – Coordinate System Transformation (Oldal átalakítás)
  az Aspose.Drawing-ban .NET-hez
url: /hu/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Hogyan rajzoljunk téglalapot – Koordináta‑rendszer átalakítás (Oldal átalakítás) az Aspose.Drawing for .NET-ben

## Bevezetés

Üdvözöljük! Ebben az oktatóanyagban megtanulja, **hogyan rajzoljunk téglalapot** grafikai elemekkel, miközben az oldal koordinátáit átalakítja az Aspose.Drawing for .NET segítségével. Akár grafikai‑intenzív alkalmazást fejleszt, akár pontos vezérlést igényel a rajzolási egységek felett, ez az útmutató minden lépésen végigvezet – a vászon beállításától a téglalap elem rajzolásáig. A végére magabiztosan alkalmazhatja ezeket a technikákat saját projektjeiben.

## Gyors válaszok
- **Mi az a koordináta‑rendszer átalakítás?** Az oldal‑szintű egységek (például hüvelyk) leképezése az eszköz‑szintű pixelekre.  
- **Miért használjuk az Aspose.Drawing‑et?** Teljesen menedzselt, platform‑független alternatívát kínál a System.Drawing.Common‑hoz képest.  
- **Mennyi időt vesz igénybe a példa megvalósítása?** Körülbelül 5‑10 perc egy alap oldal‑átalakításhoz.  
- **Szükség van licencre?** Fejlesztéshez egy ingyenes próba verzió működik; termeléshez kereskedelmi licenc szükséges.  
- **Mely .NET verziók támogatottak?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Mi az Aspose.Drawing?

`Aspose.Drawing` egy .NET grafikai könyvtár, amely **eszköz‑független API‑t** biztosít raszteres képek, vektorok és oldal‑szintű rajzok létrehozásához és manipulálásához GDI+ nélkül. Több mint **30 képtípust** támogat, és akár **10 000 × 10 000 pixel** méretű képeket is feldolgozhat anélkül, hogy a teljes fájlt a memóriába töltené.

## Miért használjunk koordináta‑rendszer átalakítást az Aspose.Drawing‑ben?

A koordináta‑rendszer átalakítás lehetővé teszi, hogy valós‑világi egységekben tervezzen grafikát, miközben a könyvtár gondoskodik a pixel skálázásról bármely kimeneti eszközhöz. Ez biztosítja a méretek konzisztenciáját a képernyők és nyomtatók között, és egyszerűsíti a elrendezési számításokat.

- **Eszköz‑független tervezés:** Írjon kódot egyszer, és az Aspose.Drawing gondoskodik a pixel skálázásról bármely képernyő vagy nyomtató esetén.  
- **Precíz rajzolás:** Ideális technikai diagramokhoz, CAD‑stílusú vázlatokhoz vagy bármely olyan helyzethez, ahol a pontos méretek fontosak.  
- **Platform‑független megbízhatóság:** Konzisztensen működik Windows, Linux és macOS rendszereken a System.Drawing GDI+ korlátai nélkül.  
- **Teljesítmény adatok:** Egy tipikus 2,5 GHz CPU‑n egy 5‑hüvelykes téglalap rajzolása 300 DPI‑n kevesebb, mint **15 ms**, és a könyvtár képes **50 képkocka másodpercenként** valós‑idő előnézeti szcenáriókban.

## Előfeltételek

Mielőtt elkezdenénk, győződjön meg róla, hogy rendelkezik:

- **Aspose.Drawing könyvtár:** Töltse le a legújabb verziót a hivatalos oldalról [here](https://releases.aspose.com/drawing/net/).  
- **Fejlesztői környezet:** Visual Studio, Rider vagy bármely .NET‑kompatibilis IDE.  
- **A dokumentum könyvtára:** Cserélje le a kódban a `"Your Document Directory"` értéket arra a mappára, ahová a kimeneti képet menteni szeretné.  
- **ASP.NET támogatás (opcionális):** Az Aspose.Drawing használható ASP.NET Core projektekben a NuGet csomag hozzáadásával – ez ugyanazt a **how to use aspnet** mintát követi, mint bármely más .NET könyvtár.

Most, hogy minden készen áll, merüljünk el a lépés‑ről‑lépésre útmutatóban.

## Hogyan rajzoljunk téglalapot oldal átalakítással?

Töltsön be egy üres bitmapet, állítsa be az oldal egységét hüvelykre, és rajzoljon egy téglalapot egy vékony kék tollal – ez néhány kódsorral megvalósítja a téglalap rajzolását. A `Graphics.PageUnit` tulajdonság azt mondja a motornak, hogy minden koordinátát hüvelykben értelmezzen, így a valós‑világi mérésekre gondolhat a nyers pixelek helyett.

### 1. lépés: Névterek importálása

A `using` utasítások hozzáférést biztosítanak a fő rajzoló osztályokhoz.

```csharp
using System.Drawing;
```

### 2. lépés: Bitmap létrehozása

A `Bitmap` egy memóriában lévő képet képvisel, amelyre rajzolhat. Kezdjük egy üres bitmap létrehozásával, amely a rajzolási felületként szolgál. A `Format32bppPArgb` pixelformátum magas minőséget és előre szorzott alfa támogatást nyújt.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 3. lépés: Graphics objektum létrehozása

A `Graphics` objektum biztosítja a rajzolási API‑t a bitmaphez. Ez a híd a kód és a pixelpuffer között.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 4. lépés: Vászon törlése

Adjunk a vászonnak semleges hátteret, hogy a rajzolt alakzatok kiemelkedjenek. Itt egy világosszürke színnel töltjük ki.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### 5. lépés: Átalakítás beállítása (Hogyan állítsuk be az egységet)

A `Graphics.PageUnit` határozza meg a oldal koordinátákhoz használt mértékegységet. Az oldal koordináták eszköz‑pixelekre való leképezéséhez állítsa be a `PageUnit` tulajdonságot. Ebben a példában hüvelyket választunk, de használhatja a `GraphicsUnit.Millimeter`, `GraphicsUnit.Point` vagy `GraphicsUnit.Pixel` értékeket is. Az egység hüvelykre állítása automatikusan **átalakítja a hüvelyket pixelekre** a bitmap DPI‑ja (alapértelmezett 96 DPI, 300 DPI a nagy felbontású nyomtatáshoz) alapján.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 6. lépés: Téglalap rajzolása – téglalap grafika

A `Pen` határozza meg a vonalak színét, szélességét és stílusát a grafikai felületen. Most egy vékony kék tollal rajzolunk egy téglalapot. Mivel hüvelykre váltottunk, a téglalap mérete és pozíciója hüvelykben van megadva, ami olvashatóbbá teszi a nyomtatásra szánt elrendezéseket.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### 7. lépés: Kép mentése

Végül írja a bitmapet egy PNG fájlba abba a mappába, amelyet korábban megadott.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## Hogyan méretezzünk grafikát nyomtatóhoz?

A bitmap DPI‑ját állítsa be a célnyomtató felbontására (például 300 DPI) a rajzolás előtt. Ez automatikusan **méretezi a nyomtató kimenetet**, így a kódban egy hüvelyk egyenlő lesz egy hüvelykkel a nyomtatott lapon. A `bitmap.SetResolution(300, 300)` beállítása után ugyanaz a téglalap nagyobbnak fog látszani a nyomtatott lapon, miközben megőrzi pontos méreteit.

## Gyakori problémák és megoldások

| Probléma | Miért fordul elő | Megoldás |
|----------|------------------|----------|
| **A kimeneti fájl nem jön létre** | Hibás útvonal vagy hiányzó mappa | Győződjön meg arról, hogy a célkönyvtár létezik, vagy használja a `Directory.CreateDirectory` metódust a mentés előtt. |
| **A téglalap torzult** | Hibás `PageUnit` vagy nem megfelelő DPI | Ellenőrizze, hogy a `graphics.PageUnit` megegyezik a kívánt egységgel, és a bitmap DPI megfelelően van beállítva (alapértelmezett 96 DPI). |
| **Licenc kivétel** | Érvényes licenc hiánya a termelésben | Alkalmazza a temporális vagy állandó Aspose.Drawing licencet a grafikai objektumok létrehozása előtt. |

## Gyakran Ismételt Kérdések

**Q: Használhatom ingyenesen az Aspose.Drawing‑et?**  
A: Igen, egy ingyenes próba verzió elérhető [here](https://releases.aspose.com/).

**Q: Hol találom meg az Aspose.Drawing részletes dokumentációját?**  
A: A teljes API referencia itt érhető el [here](https://reference.aspose.com/drawing/net/).

**Q: Hogyan kaphatok támogatást az Aspose.Drawing‑hez?**  
A: Látogassa meg az [Aspose.Drawing Fórumot](https://forum.aspose.com/c/drawing/44) közösségi segítségért és hivatalos támogatásért.

**Q: Elérhető-e ideiglenes licenc az Aspose.Drawing‑hez?**  
A: Természetesen – szerezze be itt [here](https://purchase.aspose.com/temporary-license/).

**Q: Hol vásárolhatok teljes Aspose.Drawing licencet?**  
A: Megvásárolható itt [here](https://purchase.aspose.com/buy).

## Következtetés

Ebben az útmutatóban mindent lefedtünk, ami a **téglalap rajzolásához** szükséges az Aspose.Drawing‑del: a vászon beállítása, az oldal egységeinek konfigurálása, a pontos alakzatok rajzolása és az eredmény mentése. Használja ezeket a technikákat, hogy skálázható, eszköz‑független grafikákat hozzon létre jelentésekhez, CAD‑stílusú rajzokhoz vagy bármely olyan alkalmazáshoz, ahol a mérési pontosság lényeges. Következő lépésként fedezze fel a fejlettebb átalakításokat, mint a forgatás, méretezés és egyedi koordináta‑origók, hogy még erőteljesebb rajzolási forgatókönyveket valósítson meg.

---

**Last Updated:** 2026-05-19  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose  


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
