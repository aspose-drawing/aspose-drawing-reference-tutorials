---
date: 2026-02-25
description: Tanulja meg, hogyan hozhat létre bitmap grafikákat C#‑ban, és menthet
  PNG képeket, miközben felsorolja a telepített betűtípusokat, betűtípusokkal szöveget
  rajzol, és a bitmap felbontását állítja be az Aspose.Drawing for .NET használatával.
linktitle: Create Bitmap Graphics C# – Save PNG Image and Work with Installed Fonts
  in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Bitmap grafika létrehozása C#-ban – PNG kép mentése és a telepített betűtípusokkal
  való munka az Aspose.Drawing-ben
url: /hu/net/text-and-fonts/installed-fonts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PNG kép mentése és telepített betűtípusok használata az Aspose.Drawing-ban

## Bevezetés

Ha **PNG képet** kell mentened, miközben **bitmap grafikai képeket hozol létre C#‑ban**, az Aspose.Drawing for .NET tiszta, platform‑független megoldást kínál. Ebben a bemutatóban végigvezetünk a telepített betűtípusok listázásán, a betűtípuscsaládok megjelenítésén, a bitmapből történő grafika létrehozásán és a betűtípusokkal való szövegrajzoláson – végül elmentjük az eredményt PNG képként. A végére egy újrahasználható kódrészletet kapsz, amelyet bármely .NET projektbe beilleszthetsz.

## Gyors válaszok
- **Mit hoz létre ez a bemutató?** Egy PNG kép, amely felsorolja a telepített betűtípuscsaládokat.  
- **Melyik könyvtár szükséges?** Aspose.Drawing for .NET (nem szükséges a System.Drawing.Common).  
- **Használhatok egyéni betűtípusokat?** Igen – egyszerűen töltsd be őket egy `InstalledFontCollection`‑be.  
- **Állítható a kimeneti felbontás?** Természetesen – módosítsd a bitmap méretét vagy a pixel formátumot a **bitmap felbontás C#‑ban** történő beállításhoz.  
- **Szükség van licencre a kód futtatásához?** Ideiglenes licenc elegendő értékeléshez; a teljes licenc szükséges a termeléshez.

## Mi az a „PNG kép mentése” az Aspose.Drawing kontextusában?
A PNG kép mentése azt jelenti, hogy a rajzfelületedet (egy `Bitmap`‑et) egy `.png` kiterjesztésű fájlba kódolod. Az Aspose.Drawing elvégzi a kódolást, így csak a `bitmap.Save(...)` hívást kell megadnod a kívánt úttal.

## Miért listázzuk a telepített betűtípusokat és mutassuk meg a betűtípuscsaládokat?
Az elérhető betűtípusok ismerete lehetővé teszi, hogy dinamikus grafikákat készíts, amelyek alkalmazkodnak a végfelhasználó környezetéhez. Különösen hasznos jelentések, bizonyítványok vagy bármilyen vizuális tartalom generálásához, amelynek meg kell felelnie a vállalati arculatnak anélkül, hogy betűtípusfájlokat kellene szállítani.

## Hogyan hozhatunk létre bitmap grafikai képeket C#‑ban az Aspose.Drawing segítségével?
Az alábbiakban egy gyakorlati, lépésről‑lépésre útmutatót találsz, amely pontosan bemutatja, hogyan **hozz létre bitmap grafikai képeket C#‑ban**, rajzolj szöveget betűtípusokkal, és állítsd be a bitmap felbontását, ha szükséges.

## Előfeltételek

- **Aspose.Drawing könyvtár** – töltsd le a legújabb verziót az [Aspose Drawing letöltési oldalról](https://releases.aspose.com/drawing/net/).  
- **IDE** – Visual Studio, Rider vagy bármely .NET‑kompatibilis szerkesztő.  
- **Alap C# ismeretek** – ismerned kell az osztályokat, objektumokat és egyszerű ciklusokat.

## Névterek importálása
A betűtípusok és grafika kezeléséhez importáld ezeket a névtereket a C# fájlod tetején:

```csharp
using System.Drawing;
using System.Drawing.Text;
```

## Lépésről‑lépésre útmutató

### 1. lépés: Bitmap létrehozása (a vászon)
Először létrehozunk egy bitmapet, amely a végső képet fogja tartalmazni. A bitmap mérete és pixel formátuma határozza meg a mentett PNG minőségét, és lehetővé teszi a **bitmap felbontás C#‑ban** történő beállítását.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 2. lépés: Grafika létrehozása bitmapből
Ezután egy `Graphics` objektumot kapunk a bitmapből. Ez az objektum lehetővé teszi alakzatok, szöveg és képek rajzolását a vászonra.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.Clear(Color.FromKnownColor(KnownColor.White));
```

### 3. lépés: Ecset és betűtípus beállítása (szöveg rajzolása betűtípusokkal)
Szükségünk van egy ecsetre a szöveg színéhez és egy `Font` objektumra, amely meghatározza a betűtípust, méretet és stílust. Itt történik a **szöveg rajzolása betűtípusokkal**.

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Black));
InstalledFontCollection fonts = new InstalledFontCollection();
Font arial = new Font("Arial", 20, FontStyle.Regular);
```

### 4. lépés: Telepített betűtípusok listázása és betűtípuscsaládok megjelenítése
Most megjelenítjük a betűtípuscsaládok számát és az első néhány nevet közvetlenül a bitmapen. Ez demonstrálja a **telepített betűtípusok listázása** és **betűtípuscsaládok megjelenítése** képességeket.

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

> **Pro tipp:** Használd a `Path.Combine`‑t az elérési utak összeállításához, hogy elkerüld a különböző operációs rendszerek könyvtárelválasztóival kapcsolatos problémákat.

## Gyakori problémák és megoldások
| Probléma | Ok | Megoldás |
|----------|----|----------|
| **Nincsenek megjelenített betűtípusok** | `InstalledFontCollection` nincs feltöltve (pl. fej nélküli szerveren, ahol nincsenek betűtípusok). | Telepítsd a szükséges betűtípusokat a szerverre, vagy ágyazz be egyéni betűtípusokat az alkalmazásba. |
| **A mentett fájl sérült** | Hibás pixel formátum vagy hiányzó írási jogosultság. | Győződj meg arról, hogy a célmappa létezik, és az alkalmazásnak van írási joga; tartsd meg a `Format32bppPArgb` beállítást. |
| **A szöveg elmosódott** | Alacsony DPI beállítások. | Növeld a bitmap méreteit, vagy állítsd be a `graphics.SmoothingMode = SmoothingMode.AntiAlias` értéket. |

## Gyakran ismételt kérdések

**K: Használhatok egyéni betűtípusokat, amelyek nincsenek telepítve a gépen?**  
V: Igen. Töltsd be a betűtípusfájlt egy `PrivateFontCollection`‑be, és hozz létre egy `Font`‑ot ebből a gyűjteményből.

**K: Hogyan kezeljem a betűtípusokkal kapcsolatos kivételeket?**  
V: Tekerd a betűtípus létrehozását egy `try/catch` blokkba, és vizsgáld meg az `ArgumentException`‑t a hiányzó családok miatt.

**K: Az Aspose.Drawing alkalmas webalkalmazásokhoz?**  
V: Teljesen. A könyvtár működik ASP.NET Core‑ban, Azure Functions‑ben és más szerver‑oldali környezetekben.

**K: Megváltoztathatom a szöveg színét vagy stílusát?**  
V: Igen. Használj különböző `Brush` típusokat (pl. `LinearGradientBrush`) és módosítsd a `FontStyle` enum‑ot.

**K: Hol szerezhetek ideiglenes licencet teszteléshez?**  
V: Tölts le egy próbaverzió licencet az [Aspose ideiglenes licenc oldaláról](https://purchase.aspose.com/temporary-license/).

## Következtetés

Ezekkel a lépésekkel megtanultad, hogyan **menthetsz PNG képeket**, amelyek dinamikusan **listázzák a telepített betűtípusokat**, **megmutatják a betűtípuscsaládokat**, **bitmapből hoznak létre grafikát**, és **betűtípusokkal szöveget rajzolnak** az Aspose.Drawing for .NET segítségével. Most már tudod, hogyan **hozz létre bitmap grafikai képeket C#‑ban**, állítsd be a bitmap felbontását, és szükség esetén használj egyéni betűtípusokat. Nyugodtan kísérletezz más betűtípusokkal, színekkel és bitmap méretekkel, hogy megfeleljenek projekted vizuális igényeinek.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Utoljára frissítve:** 2026-02-25  
**Tesztelve:** Aspose.Drawing 24.11 for .NET  
**Szerző:** Aspose