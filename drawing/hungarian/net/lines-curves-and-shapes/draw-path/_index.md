---
date: 2026-07-22
description: Ismerje meg, hogyan menthet bitmapet PNG‑ként, és exportálhatja a képet
  JPEG‑be az Aspose.Drawing segítségével. A lépésről‑lépésre útmutató bemutatja az
  útvonalak rajzolását, képek létrehozását és a formátumok exportálását.
keywords:
- save bitmap as png
- export image to jpeg
- Aspose.Drawing graphicspath
- .NET image processing
lastmod: 2026-07-22
linktitle: Útvonalak rajzolása az Aspose.Drawing‑ban
og_description: Mentse a bitmapet PNG‑ként, és exportálja a képet JPEG‑be az Aspose.Drawing
  for .NET használatával. Kövesse ezt az útmutatót a komplex útvonalak rajzolásához,
  magas minőségű képek létrehozásához és több formátum kimenetéhez.
og_image_alt: 'Guide: Save bitmap as PNG and export JPEG using Aspose.Drawing'
og_title: Bitmap mentése PNG‑ként – Útvonalak rajzolása az Aspose.Drawing‑al
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save bitmap as PNG and export image to JPEG with Aspose.Drawing.
    Step‑by‑step guide shows drawing paths, creating images, and exporting formats.
  headline: Save Bitmap as PNG – Using GraphicsPath in Aspose.Drawing
  type: TechArticle
- questions:
  - answer: Absolutely – use `path.AddBezier(...)` to define smooth curves.
    question: Can I draw custom Bezier curves with GraphicsPath?
  - answer: Call `path.Reset()` to remove all figures and start fresh.
    question: How do I clear a GraphicsPath before reusing it?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- save bitmap as png
- Aspose.Drawing
- .NET graphics
- image export
title: Bitmap mentése PNG‑ként – GraphicsPath használata az Aspose.Drawing‑ban
url: /hu/net/lines-curves-and-shapes/draw-path/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Útvonalak rajzolása az Aspose.Drawing-ban

## A GraphicsPath használata – Bevezetés

**Save bitmap as PNG** gyakran az első lépés, amikor veszteségmentes képre van szükség további feldolgozáshoz vagy közzétételhez. Ebben az útmutatóban megtanulja, hogyan rajzoljon kifinomult vektoros útvonalakat a `GraphicsPath` segítségével, hogyan jelenítse meg őket egy bitmapre, majd hogyan **save bitmap as PNG** vagy akár **export image to JPEG**. Akár jelentéskészítő motor, egy egyedi diagramkönyvtár építésén dolgozik, vagy egyszerűen dinamikus grafikákat kell generálnia, az Aspose.Drawing egy teljesen kezelt, cross‑platform API-t biztosít, amely helyettesíti a System.Drawing.Common‑t.

## Gyors válaszok
- **Mit tudok rajzolni a GraphicsPath segítségével?** Lines, rectangles, ellipses, curves, and custom shapes.  
- **Szükségem van licencre?** A próba ingyenes; a kereskedelmi licenc szükséges a termeléshez.  
- **Mely .NET verziók támogatottak?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6+.  
- **Szükséges a System.Drawing.Common?** Nem, az Aspose.Drawing önállóan működik.  
- **Menthetek különböző formátumokba?** Igen – PNG, JPEG, BMP, GIF és továbbiak.

## Mi az a GraphicsPath?
`GraphicsPath` az Aspose.Drawing vektoros tárolója, amely egy sor rajzolási primitívet, például vonalakat, íveket és görbéket tárol egyetlen objektumban. Ezeknek a primitíveknek a csoportosításával egységesen alkalmazhat transzformációkat, kitöltési szabályokat és vonalbeállításokat, ami egyszerűsíti a komplex grafikák létrehozását és biztosítja a következetes megjelenítést a különböző kimeneti formátumok között.

## Miért használjuk a GraphicsPath‑t az Aspose.Drawing‑dal?
Az Aspose.Drawing‑del együtt használva a GraphicsPath pontos, rugalmas és nagy teljesítményű vektoros rajzolási képességeket biztosít. Lehetővé teszi összetett alakzatok építését, transzformációk alkalmazását és hatékony megjelenítését, miközben megőrzi a kereszt‑platform konzisztenciát és támogatja a nagyméretű képfeldolgozást. Emellett zökkenőmentesen integrálódik más .NET könyvtárakkal, lehetővé téve a raszter és vektor munkafolyamatok egyesítését egyetlen alkalmazásban.

- **Pontosság:** Kezel 50+ vektoros primitívet alpixel pontossággal, biztosítva, hogy amikor **save bitmap as PNG** a kimenet éles marad bármely felbontáson.  
- **Rugalmasság:** Kombináljon vonalakat, íveket és Bézier-görbéket egy útvonalba, majd egyetlen `Graphics.DrawPath` hívással jelenítse meg.  
- **Teljesítmény:** Az optimalizált renderelési csővezeték akár 400 MP képeket is feldolgozza a teljes fájl memóriába töltése nélkül, így a nagyméretű kötegelt feladatok is megvalósíthatók.  
- **Kereszt‑platform:** Azonos eredmények Windows, Linux és macOS futtatókörnyezetekben, kiküszöbölve a platform‑specifikus hibákat.

## Előfeltételek

Mielőtt belemerülne az útmutatóba, győződjön meg róla, hogy rendelkezik a következő előfeltételekkel:

- **Aspose.Drawing könyvtár:** Töltse le és telepítse az Aspose.Drawing könyvtárat. A könyvtárat megtalálja [itt](https://releases.aspose.com/drawing/net/).
- **Egyéb Aspose termékek:** Fedezze fel a további Aspose termékeket [itt](https://releases.aspose.com/).
- **Fejlesztői környezet:** Állítsa be a .NET fejlesztői környezetet a szükséges eszközökkel (Visual Studio, .NET SDK, stb.).

## Névterek importálása

Kezdje a szükséges névterek importálásával a projektben:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## 1. lépés: Bitmap és Graphics létrehozása

Bitmap egy memóriában tárolt képet jelent, míg a Graphics rajzolási metódusokat biztosít a képre való rendereléshez. Kezdje egy `Bitmap` és egy `Graphics` objektum létrehozásával. Ez a bitmap lesz a vászon, amelyre a `GraphicsPath` megjelenik, és később **save bitmap as PNG**.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

## 2. lépés: Pen és GraphicsPath definiálása

Pen meghatározza a vonal színét, vastagságát és stílusát; a GraphicsPath egyetlen vektoros objektumként tárolja a rajzolási primitívek gyűjteményét. Ezután definiáljon egy `Pen`‑t a rajzolási attribútumok megadásához, és hozza létre a `GraphicsPath`‑t. A `GraphicsPath` objektum a vektoradatokat tárolja, mielőtt megrajzolná őket:

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
GraphicsPath path = new GraphicsPath();
```

## 3. lépés: Vonalak és alakzatok hozzáadása

Az AddLine, AddRectangle és AddEllipse a megfelelő alakzatokat adja a GraphicsPath‑hez a későbbi rendereléshez. Vonalakat, téglalapokat és ellipsziseket adjon a `GraphicsPath`‑hez, hogy összetett útvonalat hozzon létre. Egyedi Bézier-görbéket is hozzáadhat a sima alakzatokhoz:

```csharp
path.AddLine(100, 100, 1000, 400);
path.AddLine(1000, 600, 300, 600);
path.AddRectangle(new Rectangle(500, 350, 200, 400));
path.AddEllipse(10, 250, 450, 300);
```

## 4. lépés: Útvonal rajzolása

A DrawPath a GraphicsPath‑ből származó vektoradatokat a Graphics felületre rendereli a megadott Pen segítségével. Rajzolja meg az útvonalat a `Graphics` objektumra a megadott `Pen`‑nel. Ez a művelet rasterizálja a vektoradatokat a bitmap vászonra:

```csharp
graphics.DrawPath(pen, path);
```

## 5. lépés: Kép mentése – Exportálás PNG vagy JPEG formátumba

A Bitmap.Save metódus a képet a lemezre írja a kiválasztott formátumban, például PNG vagy JPEG. Rajzolás után **save bitmap as PNG** használhatja veszteségmentes minőséghez, vagy **export image to JPEG** a kisebb fájlméret érdekében. Válassza ki a legmegfelelőbb formátumot a további felhasználáshoz:

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawPath_out.png");
```

Ismételje ezeket a lépéseket szükség szerint, hogy összetett és vizuálisan vonzó útvonalakat hozzon létre.

## Gyakori problémák és megoldások

| Probléma | Megoldás |
|----------|----------|
| **Az útvonal nem látható** | Győződjön meg róla, hogy a Pen színe kontrasztos a háttérrel, és hogy a bitmap helyesen van mentve. |
| **Váratlan képméret** | Ellenőrizze, hogy a bitmap méretei és a pixel formátum megfelelnek az igényeinek. |
| **Licenc kivétel** | Használjon próba licencet a teszteléshez; alkalmazzon érvényes licencet a termelésbe való bevezetés előtt. |

## Gyakran ismételt kérdések

### Q1: Használhatom az Aspose.Drawing‑ot más .NET könyvtárakkal?
A1: Igen, az Aspose.Drawing zökkenőmentesen integrálódik más .NET könyvtárakkal, így sokoldalú megoldást nyújt a fejlesztési projektekben.

### Q2: Elérhető próba verzió?
A2: Igen, a ingyenes próbát elérheti [itt](https://releases.aspose.com/).

### Q3: Hol találok támogatást az Aspose.Drawing‑hoz?
A3: Látogassa meg az Aspose.Drawing [fórumot](https://forum.aspose.com/c/drawing/44) segítségért és közösségi támogatásért.

### Q4: Hogyan szerezhetek ideiglenes licencet?
A4: Ideiglenes licencet szerezhet [itt](https://purchase.aspose.com/temporary-license/).

### Q5: Megvásárolhatom az Aspose.Drawing‑ot?
A5: Igen, az Aspose.Drawing‑ot megvásárolhatja [itt](https://purchase.aspose.com/buy).

**K: Rajzolhatok egyedi Bézier-görbéket a GraphicsPath‑szel?**  
A: Teljesen – használja a `path.AddBezier(...)`‑t a sima görbék definiálásához.

**K: Hogyan törölhetem a GraphicsPath‑t újrahasználat előtt?**  
A: Hívja a `path.Reset()`‑t az összes ábra eltávolításához és az újrakezdéshez.

## Összegzés

Gratulálunk! Sikeresen megtanulta, **hogyan használja a GraphicsPath‑t** útvonalak rajzolásához, majd **save bitmap as PNG** vagy **export image to JPEG** használatával az Aspose.Drawing .NET-hez. Ez az útmutató bemutatta a bitmap létrehozását, a pen definiálását, a `GraphicsPath` felépítését, különféle alakzatok renderelését, és a végső kép exportálását több formátumban. Kísérletezzen különböző koordinátákkal, színekkel és vonalvastagságokkal, hogy felszabadítsa az Aspose.Drawing teljes kreatív potenciálját.

---

**Last Updated:** 2026-07-22  
**Tested With:** Aspose.Drawing 24.12 for .NET  
**Author:** Aspose

## Kapcsolódó útmutatók

- [Bitmap mentése PNG‑ként és zárt görbék rajzolása az Aspose.Drawing‑dal](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [Bitmap mentése C# – Bézier-spline-ok rajzolása az Aspose.Drawing‑dal](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [Hogyan mentse a képet és rajzoljon kardinal spline‑okat az Aspose.Drawing‑ban](/drawing/net/lines-curves-and-shapes/draw-cardinal-spline/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}