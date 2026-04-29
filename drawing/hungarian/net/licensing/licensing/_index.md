---
date: 2026-02-09
description: Ismerje meg, hogyan állíthatja be az Aspose.Drawing licencet .NET-ben,
  és sajátítsa el a licencelési módszereket a teljes funkciók vízjel nélküli feloldásához.
linktitle: Licensing in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Aspose.Drawing licenc beállítása – Hogyan állítsuk be az Aspose.Drawing licencet
url: /hu/net/licensing/licensing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing licenc beállítása

## Introduction

Ha .NET alkalmazásokat építesz, amelyek erőteljes grafikai és képfeldolgozási funkciókra támaszkodnak, az **Aspose.Drawing licenc beállítása** az első lépés a kiértékelési korlátozások eltávolításához és a teljes funkciók eléréséhez. Ebben az útmutatóban három gyakorlati módot tanulhatsz meg az Aspose.Drawing licenc beállítására – fájlból betöltés, stream‑ből betöltés és a mérés‑alapú modell használata – hogy magabiztosan integrálhasd a könyvtárat.

## Quick Answers
- **Mi a fő módja az Aspose.Drawing aktiválásának?** Licencfájl betöltése a `License.SetLicense("Aspose.Drawing.lic")` használatával.  
- **Alkalmazhatok licencet futásidőben?** Igen, betöltheted a licencet egy `Stream`‑ből dinamikus helyzetekhez.  
- **Támogatott a mérés‑alapú licenc?** Teljesen; használd a `Metered.SetMeteredKey(publicKey, privateKey)`‑t a fogyasztás‑alapú számlázás engedélyezéséhez.  
- **Szükség van licencre a fejlesztői build-ekhez?** A próbaverzió teszteléshez működik, de egy érvényes licenc eltávolítja a vízjeleket és feloldja az összes API‑t.  
- **Mely .NET verziók kompatibilisek?** Az Aspose.Drawing támogatja a .NET Framework 4.x, .NET Core 3.1+ és a .NET 5/6+ verziókat.

## Prerequisites

Mielőtt elkezdenéd, győződj meg róla, hogy rendelkezel:

- **Aspose.Drawing könyvtár** – töltsd le a legújabb csomagot [innen](https://releases.aspose.com/drawing/net/).  
- **Licencfájl** – szerezz be egy érvényes `.lic` fájlt a [Aspose](https://purchase.aspose.com/buy) oldalról.  
- **.NET fejlesztői környezet** – Visual Studio, Rider vagy bármely IDE, amely a .NET Framework/.NET Core célplatformra épül.

## Import Namespaces

Szükségünk van a szabványos .NET névterekre, valamint az Aspose.Drawing névtérre a licenceléshez. Add hozzá a következő `using` utasításokat a C# fájlod tetejéhez:

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Loading License from a File

A licenc fájlból történő betöltése a legegyszerűbb megközelítés. Kövesd a három lépést:

### Step 1: Initialize the License Object

1. lépés: A License objektum inicializálása

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Step 2: Set the License from the `.lic` File

2. lépés: Licenc beállítása a `.lic` fájlból

```csharp
license.SetLicense("Aspose.Drawing.lic");
```

### Step 3: Confirm Success

3. lépés: Siker megerősítése

```csharp
Console.WriteLine("License set successfully.");
```

> **Pro tip:** Helyezd a `.lic` fájlt ugyanabba a mappába, ahol az exe található, vagy adj meg egy abszolút elérési utat a „file not found” hibák elkerülése érdekében.

## Loading License from a Stream

Ha a licencfájl erőforrásként van beágyazva vagy távoli helyről kerül lekérésre, a `Stream`‑ből történő betöltés rugalmasságot biztosít.

### Step 1: Initialize the License Object

1. lépés: A License objektum inicializálása

```csharp
System.Drawing.AsposeDrawing.License license = new System.Drawing.AsposeDrawing.License();
```

### Step 2: Load the License Using a `FileStream`

2. lépés: Licenc betöltése `FileStream` használatával

```csharp
FileStream myStream = new FileStream("Aspose.Drawing.lic", FileMode.Open);
license.SetLicense(myStream);
```

### Step 3: Confirm Success

3. lépés: Siker megerősítése

```csharp
Console.WriteLine("License set successfully.");
```

> **Figyelmeztetés:** Ne felejtsd el felszabadítani a `FileStream`‑et (vagy használj `using` blokkot) a fájlkezelők felszabadításához.

## Using Metered License

A mérés‑alapú licencelés ideális SaaS vagy felhasználás‑alapú fizetési esetekhez. Nyomon követi a fogyasztást és a tényleges használat alapján számláz.

### Step 1: Initialize the Metered Object

1. lépés: A Metered objektum inicializálása

```csharp
System.Drawing.AsposeDrawing.Metered metered = new System.Drawing.AsposeDrawing.Metered();
```

### Step 2: Set Public and Private Keys

2. lépés: Publikus és privát kulcsok beállítása

```csharp
metered.SetMeteredKey("your_public_key", "your_private_key");
```

### Step 3: Perform Your Image Processing

3. lépés: Képfeldolgozás végrehajtása

```csharp
// Your image processing logic here
```

### Step 4: Retrieve Consumption Information

4. lépés: Fogyasztási információ lekérése

```csharp
decimal amount = System.Drawing.AsposeDrawing.Metered.GetConsumptionQuantity();
decimal credits = System.Drawing.AsposeDrawing.Metered.GetConsumptionCredit();
```

### Step 5: Display the Consumption Details

5. lépés: A fogyasztási részletek megjelenítése

```csharp
Console.WriteLine("Amount Consumed: " + amount.ToString());
Console.WriteLine("Credits Consumed: " + credits.ToString());
```

> **Gyakori hibaforrás:** Ha elfelejted meghívni a `SetMeteredKey`‑t, az API visszatér a próbaverzió módba, és vízjeleket látsz a kimenetben.

## Why Set the Aspose.Drawing License Correctly?

- **Eltávolítja a vízjeleket**, amelyek a próbaverzióban jelennek meg.  
- **Feloldja a prémium API‑kat**, például a fejlett képszűrőket és PDF konverziót.  
- **Biztosítja a megfelelőséget** az Aspose licencfeltételeivel a kereskedelmi terjesztéshez.  
- **Lehetővé teszi a mérés‑alapú számlázást**, így csak a felhasznált mennyiségért fizetsz.

## Common Issues and Solutions

| Probléma | Ok | Megoldás |
|----------|----|----------|
| “License file not found” hiba | Helytelen útvonal vagy hiányzó fájl a kimeneti mappában | Használj abszolút útvonalat, vagy állítsd be a fájl *Copy to Output Directory* tulajdonságát *Copy always*-ra. |
| A vízjel továbbra is megjelenik a licenc beállítása után | A licenc nincs betöltve az első API hívás előtt | Töltsd be a licencet **előtt**, mielőtt bármilyen Aspose.Drawing műveletet végrehajtanál. |
| A mérés‑alapú fogyasztás mindig nulla | A kulcsok nincsenek beállítva vagy hibás környezeti változók | Ellenőrizd a publikus/privát kulcsokat, és biztosíts internetkapcsolatot az Aspose mérés‑szerveréhez. |

## Frequently Asked Questions

**Q1: Használhatom az Aspose.Drawing‑ot licenc nélkül?**  
A1: Igen, a próbaverzió licenc fejlesztéshez és kiértékeléshez működik, de vízjeleket ad hozzá és korlátozza egyes funkciókat.

**Q2: Milyen gyakran kell megújítanom az Aspose.Drawing licencet?**  
A2: A licencek örökösök a megvásárolt verzióra. A megújítás csak támogatás és frissítések esetén szükséges.

**Q3: Mi az a mérés‑alapú licencelés, és mikor kell használni?**  
A3: A mérés‑alapú licencelés a használat (műveletek vagy feldolgozott adatok) alapján számít fel díjat. Tökéletes felhőszolgáltatásokhoz vagy felhasználás‑alapú fizetési modellekhez.

**Q4: Használhatom az Aspose.Drawing‑ot kereskedelmi projektekben?**  
A4: Teljesen—miután rendelkezel egy érvényes licenccel, beágyazhatod az Aspose.Drawing‑ot bármely kereskedelmi alkalmazásba.

**Q5: Hol találok közösségi támogatást az Aspose.Drawing‑hoz?**  
A5: Látogasd meg az [Aspose.Drawing Fórumot](https://forum.aspose.com/c/drawing/44) közösségi segítség, példák és megbeszélések céljából.

## Conclusion

Az **Aspose.Drawing licenc beállításának** elsajátítása—legyen szó fájlból, stream‑ből vagy mérés‑alapú használatról—biztosítja, hogy a legtöbbet hozd ki ebből a hatékony .NET grafikai könyvtárból. Kövesd a fenti lépéseket, figyelj a gyakori hibákra, és készen állsz robusztus képfeldolgozó megoldások építésére licencelési akadályok nélkül.

---

**Utolsó frissítés:** 2026-02-09  
**Tesztelve ezzel:** Aspose.Drawing 24.11 for .NET  
**Szerző:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}