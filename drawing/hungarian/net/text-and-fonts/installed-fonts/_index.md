---
date: 2025-12-06
description: Ismerje meg, hogyan menthet PNG képfájlokat, miközben felsorolja a telepített
  betűtípusokat, megjeleníti a betűcsaládokat, bitmapből hoz létre grafikákat, és
  betűtípusokkal szöveget rajzol az Aspose.Drawing for .NET segítségével.
linktitle: Save PNG Image and Work with Installed Fonts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: PNG kép mentése és a telepített betűtípusok használata az Aspose.Drawing‑ban
url: /hu/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG kép mentése és a telepített betűtípusok használata az Aspose.Drawing-ban

## Bevezetés

Ha **PNG képet** kell mentened, amely egyúttal információt is megjelenít a gépen telepített betűtípusokról, az Aspose.Drawing for .NET tiszta, platformfüggetlen módot biztosít ehhez. Ebben az útmutatóban végigvezetünk a telepített betűtípusok listázásán, a betűcsaládok megjelenítésén, a bitmapből történő grafika létrehozásán és a betűtípusokkal való szövegrajzoláson – végül a végeredményt PNG képként mentjük. A végére egy újrahasználható kódrészletet kapsz, amelyet bármely .NET projektbe beilleszthetsz.

## Gyors válaszok
- **Ez az útmutató mit hoz létre?** Egy PNG kép, amely felsorolja a telepített betűcsaládokat.  
- **Melyik könyvtár szükséges?** Aspose.Drawing for .NET (nem szükséges a System.Drawing.Common).  
- **Használhatok egyedi betűtípusokat?** Igen – egyszerűen töltsd be őket egy `InstalledFontCollection`-be.  
- **Állítható a kimeneti felbontás?** Teljesen – módosítsd a bitmap méretét vagy a pixel formátumot.  
- **Szükséges licenc a kód futtatásához?** Ideiglenes licenc elegendő értékeléshez; a teljes licenc a termeléshez kötelező.

## Mit jelent a „PNG kép mentése” az Aspose.Drawing kontextusában?
A PNG kép mentése azt jelenti, hogy a rajzfelületet (egy `Bitmap`) egy `.png` kiterjesztésű fájlba rendereljük. Az Aspose.Drawing elvégzi a kódolást, így csak a `bitmap.Save(...)` hívást kell megadnod a kívánt úttal.

## Miért listázzuk a telepített betűtípusokat és mutassuk a betűcsaládokat?
A rendelkezésre álló betűtípusok ismerete lehetővé teszi, hogy dinamikus grafikákat készíts, amelyek alkalmazkodnak a végfelhasználó környezetéhez. Különösen hasznos jelentések, bizonyítványok vagy bármely vizuális tartalom előállításához, amelynek meg kell egyeznie a vállalati arculattal betűtípusfájlok küldése nélkül.

## Előkövetelmények

- **Aspose.Drawing könyvtár** – töltsd le a legújabb verziót az [Aspose Drawing letöltési oldalról](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider vagy bármely .NET‑kompatibilis szerkesztő.  
- **Alap C# ismeretek** – ismerned kell az osztályokat, objektumokat és egyszerű ciklusokat.

## Névterek importálása
A betűtípusokkal és grafikákkal való munkához importáld ezeket a névtereket a C# fájlod tetején:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Lépésről‑lépésre útmutató

### 1. lépés: Bitmap létrehozása (a vászon)
Először létrehozunk egy bitmapet, amely a végső képet tárolja. A bitmap mérete és a pixel formátum határozza meg a mentett PNG minőségét.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 2. lépés: Grafika létrehozása a bitmapből
Ezután egy `Graphics` objektumot kapunk a bitmapből. Ez az objektum lehetővé teszi alakzatok, szöveg és képek rajzolását a vászonra.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### 3. lépés: Ecset és betűtípus beállítása (szöveg rajzolása betűtípusokkal)
Szükségünk van egy ecsetre a szöveg színéhez és egy `Font` objektumra, amely meghatározza a betűtípust, méretet és stílust.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### 4. lépés: Telepített betűtípusok listázása és betűcsaládok megjelenítése
Most a bitmapen jelenítjük meg a betűcsaládok számát és az első néhány nevet. Ez bemutatja a **telepített betűtípusok listázása** és **betűcsaládok megjelenítése** funkciókat.

```csharp
graphics.DrawString(fonts.Families.Length + " installed font families.", arial, brush, 100, 100);

for (int i = 0; i < 6 && i < fonts.Families.Length; ++i)
{
    graphics.DrawString(fonts.Families[i].Name, arial, brush, 100, (i + 2) * 100);
}
```

### 5. lépés: PNG kép mentése
Végül a bitmapet PNG fájlként írjuk a lemezre. Ez a **png kép mentése** művelet központi része.

```csharp
bitmap.Save("Your Document Directory" + @"TextFonts\InstalledFonts_out.png");
```

> **Pro tipp:** Használd a `Path.Combine`-t fájlutak összeállításához, hogy elkerüld a könyvtárelválasztók különböző operációs rendszereken való problémáit.

## Gyakori problémák és megoldások
| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Nincsenek betűtípusok megjelenítve** | `InstalledFontCollection` nincs feltöltve (pl. fej nélküli szerveren, ahol nincsenek betűtípusok). | Telepítsd a szükséges betűtípusokat a szerveren, vagy ágyazz be egyedi betűtípusokat az alkalmazásba. |
| **A mentett fájl sérült** | Helytelen pixel formátum vagy hiányzó írási jogosultság. | Győződj meg arról, hogy a célmappa létezik, és az alkalmazásnak van írási joga; tartsd meg a `Format32bppPArgb`-t. |
| **A szöveg elmosódott** | Alacsony DPI beállítások. | Növeld a bitmap méreteit vagy állítsd be a `graphics.SmoothingMode = SmoothingMode.AntiAlias`-t. |

## Gyakran ismételt kérdések

**K: Használhatok egyedi betűtípusokat, amelyek nincsenek telepítve a gépen?**  
A: Igen. Töltsd be a betűtípusfájlt egy `PrivateFontCollection`-be, és hozz létre egy `Font`-ot ebből a gyűjteményből.

**K: Hogyan kezelem a betűtípusokkal kapcsolatos kivételeket?**  
A: Tedd a betűtípus létrehozását egy `try/catch` blokkba, és vizsgáld meg az `ArgumentException`-t a hiányzó családok miatt.

**K: Alkalmas az Aspose.Drawing webalkalmazásokhoz?**  
A: Teljesen. A könyvtár működik ASP.NET Core-ban, Azure Functions-ben és más szerveroldali környezetekben.

**K: Megváltoztathatom a szöveg színét vagy stílusát?**  
A: Igen. Használj különböző `Brush` típusokat (pl. `LinearGradientBrush`) és módosítsd a `FontStyle` enumot.

**K: Hol szerezhetek ideiglenes licencet teszteléshez?**  
A: Tölts le egy próbaverzió licencet az [Aspose ideiglenes licenc oldalról](https://purchase.aspose.com/temporary-license/).

## Következtetés

Ezeket a lépéseket követve megtanultad, hogyan **PNG képeket** ments, amelyek dinamikusan **listázzák a telepített betűtípusokat**, **megmutatják a betűcsaládokat**, **grafikákat hoznak létre bitmapből**, és **szöveget rajzolnak betűtípusokkal** az Aspose.Drawing for .NET segítségével. Nyugodtan kísérletezz más betűtípusokkal, színekkel és bitmap méretekkel, hogy megfeleljenek a projekt vizuális igényeinek.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-06  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose