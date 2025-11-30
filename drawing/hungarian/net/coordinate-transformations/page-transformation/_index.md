---
date: 2025-11-30
description: Tanulja meg, hogyan alkalmazzon koordináta-rendszer-átalakítást, rajzoljon
  téglalap bitmapet, és alakítsa át az oldalakat az Aspose.Drawing for .NET használatával.
language: hu
linktitle: Page Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Koordináta-rendszer átalakítás (oldaltranszformáció) az Aspose.Drawing .NET-ben
url: /net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Coordinate System Transformation (Page Transformation) in Aspose.Drawing for .NET

## Introduction

Üdvözöljük! Ebben az útmutatóban megtudja, **how to perform a coordinate system transformation** egy oldalon az Aspose.Drawing .NET használatával. Akár **draw rectangle bitmap** objektumokat kell rajzolnia, ábrákat méretezni, vagy egyszerűen az oldal egységeit az eszköz egységeire leképezni, az alábbi lépések végigvezetik a teljes folyamaton – világosan, tömören, és készen állva a másolás‑beillesztésre a projektjébe.

## Quick Answers

- **Mi a fő osztály a rajzoláshoz?** `Graphics` from Aspose.Drawing.
- **Hogyan állíthatom be az oldal egységeit?** Use `graphics.PageUnit = GraphicsUnit.Inch;`.
- **Rajzolhatok-e egy téglalapot egy átalakított oldalon?** Yes—create a `Pen` and call `DrawRectangle`.
- **Hol kerül mentésre a kimenet?** To the folder you specify in `bitmap.Save`.
- **Szükség van licencre a termeléshez?** A valid Aspose.Drawing license is required for commercial use.

## What is coordinate system transformation?

A **coordinate system transformation** megváltoztatja, hogy a logikai oldalkoordináták (például hüvelyk vagy milliméter) hogyan képeződnek le a fizikai eszközkoordinátákra (pixel). A transzformáció beállításával szabályozhatja a méretezést, forgatást és eltolást minden rajzolási műveletnél, megkönnyítve a felbontás‑független grafikák tervezését.

## Why use Aspose.Drawing for page transformations?

- **Full .NET compatibility** – .NET Framework, .NET Core és .NET 5/6 támogatással működik.
- **Rich graphics API** – ugyanazt a funkcionalitást kínálja, mint a System.Drawing.Common platformkorlátozások nélkül.
- **Simple unit handling** – könnyedén válthat hüvelyk, milliméter, pont stb. között egyetlen tulajdonsággal.
- **High‑quality output** – PNG, JPEG, BMP és egyéb formátumok generálása pontos vezérléssel.

## Prerequisites

Mielőtt belemerülnénk, győződjön meg róla, hogy rendelkezik:

- **Aspose.Drawing Library** – töltse le a legújabb verziót a hivatalos oldalról [here](https://releases.aspose.com/drawing/net/).
- **Development Environment** – Visual Studio (bármely kiadás) vagy más .NET IDE.
- **Write Access** – egy mappa a gépén, ahol a transzformált kép mentésre kerül (cserélje le a `"Your Document Directory"`-t a kódban a tényleges útvonalra).

Most, hogy készen állunk, lépjünk át minden lépésen.

## Import Namespaces

Először hozza be a szükséges névteret a láthatóságba:

```csharp
using System.Drawing;
```

> *Miért fontos ez*: `System.Drawing` tartalmazza a `Bitmap`, `Graphics`, `Pen` és szín struktúrákat, amelyeket a teljes útmutató során használni fogunk.

## Step 1: Create a Bitmap

1. lépés: Bitmap létrehozása

Hozzon létre egy üres vásznat, amely a transzformált rajzot fogja tartalmazni. Méretként **1000 × 800 pixel**-t adunk meg, és egy alfa átlátszóságot támogató pixelformátumot használunk.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> Ez a bitmap a rajzfelületként szolgál. A választott pixelformátum (`Format32bppPArgb`) biztosítja a magas minőségű megjelenítést előszorozott alfával.

## Step 2: Create a Graphics Object

2. lépés: Graphics objektum létrehozása

Egy `Graphics` objektum biztosítja a rajzolási metódusokat (vonalak, alakzatok, szöveg). Ezt a bitmapből nyerjük ki, amelyet éppen létrehoztunk.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

> A `Graphics` objektum minden renderelési művelet központja; tiszteletben tartja a következő lépésben alkalmazott transzformációs beállításokat.

## Step 3: Clear the Canvas

3. lépés: Vászon törlése

Mielőtt bármit rajzolna, törölje a vásznat egy semleges háttérszínre (ebben a példában szürke). Ez a lépés azt is bemutatja, hogyan tölthető fel a teljes bitmap egy egységes színnel.

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

## Step 4: Set Transformation (Apply Page Transformation)

4. lépés: Transzformáció beállítása (Oldal transzformáció alkalmazása)

Itt **apply the page transformation** úgy állítjuk be a `PageUnit`-ot hüvelykre. Ez azt mondja a grafikai motornak, hogy az összes további koordinátát hüvelykben értelmezze, nem pixelekben.

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

> *Tip*: A `PageUnit` módosítása egyszerű módja annak, hogy **how to transform page** koordinátákat használjon anélkül, hogy kézzel számolná a pixelértékeket.

## Step 5: Draw a Rectangle (Draw rectangle bitmap)

5. lépés: Téglalap rajzolása (Draw rectangle bitmap)

Most egy olyan téglalapot rajzolunk, amely **1 hüvelyk × 1 hüvelyk** méretű a (1, 1) hüvelykes pozícióban. A `Pen` vastagsága `0.1f` hüvelyk, ami vékony, de látható vonalat eredményez.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

> Ez bemutatja a **draw rectangle bitmap** alkalmazását a transzformáció után – vegye észre, hogy a téglalap mérete hüvelykben van megadva, nem pixelekben.

## Step 6: Save the Image

6. lépés: Kép mentése

Végül a transzformált bitmapet lemezre mentjük. Cserélje le a `"Your Document Directory"`-t a gépén lévő tényleges mappára.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

> A kimeneti fájl (`PageTransformation_out.png`) tartalmazni fogja a koordináta-rendszer átalakítással rajzolt téglalapot, amelyet korábban beállítottunk.

## Common Issues and Solutions

Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|-------|-------|----------|
| **A kép üresnek jelenik meg** | A vászon nincs törölve vagy a rajzolás a látható területen kívül történik. | Ellenőrizze a `graphics.PageUnit` és a koordináta értékeket; győződjön meg róla, hogy a téglalap a bitmap határain belül van. |
| **Helytelen méretezés** | Rossz `GraphicsUnit` használata. | Ellenőrizze, hogy a `graphics.PageUnit` megfelel a kívánt egységnek (pl. `GraphicsUnit.Inch`). |
| **Fájlútvonal hibák** | Hiányzó könyvtár vagy érvénytelen karakterek. | Hozza létre a célkönyvtárat előre, vagy használja a `Path.Combine`-t az útvonal biztonságos összeállításához. |

## Frequently Asked Questions

Gyakran feltett kérdések

**Q: Használhatom ingyenesen az Aspose.Drawing-et?**  
A: Az Aspose.Drawing ingyenes próbaverziót kínál, amelyet [here](https://releases.aspose.com/) érhet el.

**Q: Hol találom az Aspose.Drawing részletes dokumentációját?**  
A: A dokumentáció [here](https://reference.aspose.com/drawing/net/) érhető el.

**Q: Hogyan kaphatok támogatást az Aspose.Drawing-hez?**  
A: Támogatásért látogasson el az [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17) oldalra.

**Q: Elérhető-e ideiglenes licenc az Aspose.Drawing-hez?**  
A: Igen, ideiglenes licencet szerezhet [here](https://purchase.aspose.com/temporary-license/).

**Q: Hol vásárolhatom meg az Aspose.Drawing-et?**  
A: Az Aspose.Drawing megvásárolható [here](https://purchase.aspose.com/buy).

## Conclusion

Összegzés

Most már megtanulta, hogyan **apply a coordinate system transformation**, **draw rectangle bitmap** objektumokat, és hogyan **save the result** az Aspose.Drawing .NET használatával. Ezek az építőelemek lehetővé teszik felbontás‑független grafikák létrehozását, amelyek tökéletesek jelentésekhez, UI elemekhez vagy bármilyen olyan helyzethez, ahol a pontos méretezés fontos. Kísérletezzen más `GraphicsUnit` értékekkel (például `Millimeter` vagy `Point`), hogy lássa, hogyan befolyásolják a rajzokat.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Utolsó frissítés:** 2025-11-30  
**Tesztelt verzió:** Aspose.Drawing 24.11 for .NET  
**Szerző:** Aspose