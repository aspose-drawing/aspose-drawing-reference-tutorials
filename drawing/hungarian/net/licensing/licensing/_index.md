---
date: 2026-05-29
description: Tanulja meg, hogyan állíthatja be az Aspose.Drawing licencet .NET-ben,
  és hogyan távolíthatja el az Aspose vízjelet. Ismerje meg a licencelési módszereket
  a teljes funkciók vízjel nélküli feloldásához.
keywords:
- remove aspose watermark
- how to activate aspose
- aspose drawing licensing
- aspose .net license
- metered aspose license
linktitle: Licencelés az Aspose.Drawing-ban
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  headline: Remove Aspose Watermark – Set Aspose.Drawing License
  type: TechArticle
- description: Learn how to set Aspose.Drawing license in .NET and remove Aspose watermark.
    Master licensing methods to unlock full features without watermarks.
  name: Remove Aspose Watermark – Set Aspose.Drawing License
  steps:
  - name: Confirm Success
    text: '> **Pro tip:** Place the `.lic` file in the same folder as your executable
      or provide an absolute path to avoid “file not found” errors.'
  - name: Confirm Success
    text: '> **Warning:** Remember to dispose the `FileStream` (or use a `using` block)
      to free file handles.'
  - name: Display the Consumption Details
    text: '> **Common pitfall:** If you forget to call `SetMeteredKey`, the API will
      fall back to trial mode and you’ll see watermarks in the output.'
  type: HowTo
- questions:
  - answer: Load a license file using `License.SetLicense("Aspose.Drawing.lic")`.
    question: What is the primary way to activate Aspose.Drawing?
  - answer: Yes, you can load the license from a `Stream` for dynamic scenarios.
    question: Can I apply a license at runtime?
  - answer: Absolutely; use `Metered.SetMeteredKey(publicKey, privateKey)` to enable
      consumption‑based billing.
    question: Is a metered license supported?
  - answer: A trial works for testing, but a valid license removes watermarks and
      unlocks all APIs.
    question: Do I need a license for development builds?
  - answer: Aspose.Drawing supports .NET Framework 4.x, .NET Core 3.1+, and .NET 5/6+.
    question: Which .NET versions are compatible?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose vízjel eltávolítása – Aspose.Drawing licenc beállítása
url: /hu/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing licenc beállítása

## Bevezetés

Ha .NET alkalmazásokat építesz, amelyek erőteljes grafika- és képfeldolgozási funkciókra támaszkodnak, **az Aspose.Drawing licenc beállítása** az első lépés az Aspose vízjel eltávolításához és a teljes funkciókészlet eléréséhez. Ebben az útmutatóban három gyakorlati módot tanulhatsz meg az Aspose.Drawing licenc beállítására – fájlból betöltés, stream‑ből betöltés és a mérő‑használati modell használata – hogy magabiztosan integráld a könyvtárat és tiszta kimenetet kapj.

## Gyors válaszok
- **Mi a fő módja az Aspose.Drawing aktiválásának?** Licencfájlt tölts be a `License.SetLicense("Aspose.Drawing.lic")` használatával.  
- **Alkalmazhatok licencet futásidőben?** Igen, a licencet betöltheted egy `Stream`‑ből dinamikus esetekben.  
- **Támogatott a mérő licenc?** Teljesen; használd a `Metered.SetMeteredKey(publicKey, privateKey)`‑t a fogyasztás‑alapú számlázás engedélyezéséhez.  
- **Szükségem van licencre a fejlesztői build-ekhez?** A próbaverzió tesztelésre használható, de egy érvényes licenc eltávolítja a vízjeleket és feloldja az összes API‑t.  
- **Mely .NET verziók kompatibilisek?** Az Aspose.Drawing támogatja a .NET Framework 4.x, a .NET Core 3.1+ és a .NET 5/6+ verziókat.

## Előfeltételek

Mielőtt elkezdenéd, győződj meg róla, hogy rendelkezel a következőkkel:

- **Aspose.Drawing Library** – töltsd le a legújabb csomagot innen: [here](https://releases.aspose.com/drawing/net/).  
- **License File** – szerezz be egy érvényes `.lic` fájlt a [Aspose](https://purchase.aspose.com/buy) oldalról.  
- **.NET Development Environment** – Visual Studio, Rider vagy bármely IDE, amely a .NET Framework/.NET Core célra van beállítva.

## Névterek importálása

Szükségünk van a szabványos .NET névterekre, valamint az Aspose.Drawing névtérre a licenceléshez. Add the following `using` statements at the top of your C# file:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Hogyan töltsünk be licencet fájlból?

`License` osztály az Aspose.Drawing licencelési komponensét képviseli, amely példányosításkor lehetővé teszi a licenc alkalmazását a könyvtárra. Licenc betöltése fájlból a legegyszerűbb megközelítés; egyszerűen a `SetLicense` metódust egy `.lic` fájlra mutatod, és a könyvtár eltávolítja az összes próbaverziós vízjelet az alkalmazás maradék futási idejére. Ez a módszer asztali és szerver környezetben egyaránt működik, és nem igényel további konfigurációt, csak hogy a fájl futásidőben elérhető legyen.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## Hogyan töltsünk be licencet stream‑ből?

Amikor a licencfájl erőforrásként van beágyazva vagy a hálózaton keresztül kerül lekérésre, a `Stream`‑ből történő betöltés rugalmasságot biztosít, miközben garantálja a vízjel eltávolítását. Ha egy `Stream` példányt adsz át a `SetLicense` metódusnak, a licencet a telepítési mappán kívül tartod, ami javíthatja a biztonságot és egyszerűsítheti a terjesztést konténeres vagy felhő környezetben. A folyamat megegyezik a fájl‑alapú betöltéssel, csak a stream életciklusát neked kell kezelni.

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

## Hogyan aktiváljunk Metered licencet?

`Metered` osztály kezeli az Aspose.Drawing mérő‑használati aktiválását, lehetővé téve a fogyasztás‑alapú számlázást. A mérő licenc lehetővé teszi, hogy csak a ténylegesen végrehajtott műveletekért fizess, ami ideális SaaS vagy felhasználás‑alapú modellekhez. Miután megadod a nyilvános és privát kulcsokat, minden képfeldolgozó hívás automatikusan nyomon követésre és számlázásra kerül, és a könyvtár teljes funkciómódban, vízjel nélkül működik a munkamenet időtartama alatt.

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

## Miért fontos helyesen beállítani az Aspose.Drawing licencet?

A licenc helyes beállítása biztosítja, hogy a könyvtár teljes‑funkciós módban fusson, eltávolítja a próbaverziós vízjeleket, és megfeleljen az Aspose licencfeltételeinek. A megfelelően alkalmazott licenc engedélyezi a prémium API‑kat, javítja a teljesítményt az értékelési ellenőrzések letiltásával, és lehetővé teszi a mérő számlázás használatát, ha szükséges. Ha a licencet nem töltöd be az első API‑hívás előtt, a könyvtár próbaverzióba lép, ami minden generált képen vízjelet eredményez.

- **Eltávolítja a vízjeleket**, amelyek a próbaverzióban jelennek meg.  
- **Feloldja a prémium API‑kat**, például fejlett képszűrőket és PDF konverziót.  
- **Biztosítja a megfelelőséget**, az Aspose licencfeltételeivel a kereskedelmi terjesztéshez.  
- **Lehetővé teszi a mérő számlázást**, így csak a felhasznált mennyiségért fizetsz.  

Az Aspose.Drawing **30+ képformátumot** támogat (beleértve a PNG, JPEG, BMP, TIFF és WebP formátumokat), és képes **több száz oldalas PDF dokumentumok feldolgozására a teljes fájl memóriába betöltése nélkül**, magas teljesítményű konverziót biztosítva közepes hardveren.

## Licenc betöltése fájlból

Licenc betöltése fájlból a legegyszerűbb megközelítés. Kövesd ezt a három lépést:

### 1. lépés: A License objektum inicializálása

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### 2. lépés: A licenc beállítása a `.lic` fájlból

```csharp
Console.WriteLine("License set successfully.");
```

### 3. lépés: Siker ellenőrzése

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro tip:** Helyezd a `.lic` fájlt ugyanabba a mappába, ahol az exe áll, vagy adj meg egy abszolút elérési utat a “file not found” hibák elkerülése érdekében.

## Licenc betöltése stream‑ből

Amikor a licencfájl erőforrásként van beágyazva vagy távoli helyről kerül lekérésre, a `Stream`‑ből történő betöltés rugalmasságot biztosít.

### 1. lépés: A License objektum inicializálása

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### 2. lépés: Licenc betöltése `FileStream` használatával

```csharp
Console.WriteLine("License set successfully.");
```

### 3. lépés: Siker ellenőrzése

```csharp
Console.WriteLine("License set successfully.");
```

> **Warning:** Ne felejtsd el eldobni a `FileStream`‑et (vagy használj `using` blokkot) a fájlkezelők felszabadításához.

## Metered licenc használata

A mérő licenc ideális SaaS vagy felhasználás‑alapú modellekhez. Nyomon követi a fogyasztást és a tényleges használat alapján számláz.

### 1. lépés: A Metered objektum inicializálása

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### 2. lépés: Nyilvános és privát kulcsok beállítása

```csharp
// Your image processing logic here
```

### 3. lépés: Képfeldolgozás végrehajtása

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### 4. lépés: Fogyasztási információ lekérése

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

### 5. lépés: Fogyasztási részletek megjelenítése

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Common pitfall:** Ha elfelejted meghívni a `SetMeteredKey`‑t, az API próbaverzióba lép, és a kimeneten vízjelek jelennek meg.

## Gyakori problémák és megoldások

| Probléma | Ok | Megoldás |
|----------|----|----------|
| “License file not found” hiba | Helytelen útvonal vagy hiányzó fájl a kimeneti mappában | Használj abszolút útvonalat, vagy állítsd be a fájl *Copy to Output Directory* tulajdonságát *Copy always*-ra. |
| A vízjel továbbra is megjelenik a licenc beállítása után | A licenc nincs betöltve az első API‑hívás előtt | Töltsd be a licencet **előtt**, bármely Aspose.Drawing művelet előtt. |
| A mérő fogyasztás mindig nulla | A kulcsok nincsenek beállítva vagy helytelen környezeti változók | Ellenőrizd a nyilvános/privát kulcsokat, és biztosíts internetkapcsolatot az Aspose mérő szerveréhez. |

## Gyakran feltett kérdések

**Q1: Használhatom az Aspose.Drawing‑t licenc nélkül?**  
A1: Igen, egy próbaverzió működik fejlesztéshez és értékeléshez, de vízjeleket ad hozzá és korlátozza egyes funkciókat.

**Q2: Milyen gyakran kell megújítanom az Aspose.Drawing licencet?**  
A2: A licencek örökösök a megvásárolt verzióra. A megújítás csak támogatás és frissítések esetén szükséges.

**Q3: Mi az a mérő licenc, és mikor kellene használni?**  
A3: A mérő licenc a használat (műveletek vagy feldolgozott adatok) alapján számláz. Ideális felhőszolgáltatásokhoz vagy felhasználás‑alapú modellekhez.

**Q4: Használhatom az Aspose.Drawing‑t kereskedelmi projektekben?**  
A4: Természetesen—miután rendelkezel érvényes licenccel, beágyazhatod az Aspose.Drawing‑t bármely kereskedelmi alkalmazásba.

**Q5: Hol találhatok közösségi támogatást az Aspose.Drawing‑hez?**  
A5: Látogasd meg a [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44) oldalt közösségi segítségért, példákért és megbeszélésekért.

## Következtetés

A **Aspose.Drawing licenc beállításának** (legyen szó fájlból, stream‑ből vagy mérő használatról) elsajátítása biztosítja, hogy a legjobbat hozd ki ebből a hatékony .NET grafikai könyvtárból, miközben teljesen **eltávolítod az Aspose vízjelet**. Kövesd a fenti lépéseket, figyelj a gyakori hibákra, és készen állsz robusztus képfeldolgozó megoldások építésére licencelési akadályok nélkül.

---

**Utoljára frissítve:** 2026-05-29  
**Tesztelve ezzel:** Aspose.Drawing 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
