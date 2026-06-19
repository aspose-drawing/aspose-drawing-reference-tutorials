---
date: 2026-04-22
description: Naučte se, jak uložit bitmapu jako PNG pomocí Aspose.Drawing pro .NET
  s příkladem transformační matice. Průvodce krok za krokem s ukázkami kódu.
keywords:
- save bitmap as png
- transformation matrix example
- draw rotated ellipse
- convert graphics to png
- high-quality png output
linktitle: Lokální transformace v Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Uložte bitmapu jako PNG pomocí transformace v Aspose.Drawing
url: /cs/net/coordinate-transformations/local-transformation/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Uložení bitmapy jako PNG pomocí transformace v Aspose.Drawing

## Úvod

Pokud potřebujete **uložit bitmapu jako PNG** a zároveň aplikovat lokální transformaci na grafiku v .NET aplikaci, Aspose.Drawing proces zjednodušuje a je spolehlivý. V tomto tutoriálu uvidíte přesně, jak použít transformační matici na tvar, vykreslit výsledek a nakonec **převést grafiku na PNG** pro uložení nebo další zpracování. Na konci budete mít znovupoužitelný kódový vzor, který můžete přizpůsobit libovolnému scénáři lokální transformace.

## Rychlé odpovědi
- **Co je lokální transformace?** Jedná se o operaci založenou na matici (rotace, škálování, posunutí, zkosení) aplikovanou na konkrétní kreslicí prvek, aniž by ovlivnila celé plátno.  
- **Která knihovna to podporuje v .NET?** Aspose.Drawing pro .NET poskytuje plnohodnotné API, které funguje na všech podporovaných verzích .NET.  
- **Mohu výsledek uložit jako PNG?** Ano – stačí zavolat `Bitmap.Save` s názvem souboru končícím na “.png” a Aspose.Drawing se postará o konverzi.  
- **Potřebuji licenci pro vývoj?** Bezplatná zkušební verze funguje pro testování; pro produkční použití je vyžadována komerční licence.  
- **Jak dlouho trvá implementace?** Přibližně 10‑15 minut pro základní příklad.

## Jak uložit bitmapu jako PNG

Níže najdete kompletní, krok za krokem průvodce, který ukazuje **příklad transformační matice** a končí výstupem PNG vysoké kvality.

## Co znamená „jak aplikovat transformaci“ v programování grafiky?

Aplikace transformace znamená úpravu souřadnicového systému kreslicího objektu pomocí **Matrix**. Matice určuje, jak jsou body otáčeny, škálovány nebo posouvány, což vám umožňuje vytvářet sofistikované vizuální efekty s minimálním množstvím kódu.

## Proč použít Aspose.Drawing k **převodu grafiky na PNG**?

- **Cross‑platform**: Funguje na .NET Framework, .NET Core a .NET 5/6+.  
- **Žádné závislosti na GDI+**: Vyhýbá se problémům `System.Drawing.Common` na ne‑Windows platformách.  
- **Vysoká kvalita výstupu PNG**: Anti‑aliasing a pixel‑dokonalé vykreslování pro soubory PNG.  
- **Bohaté API**: Plná podpora pro cesty, pera, štětce a transformační matice.

## Požadavky

Než začnete, ujistěte se, že máte:

1. **Aspose.Drawing pro .NET** – stáhněte a nainstalujte z [odkaz ke stažení](https://releases.aspose.com/drawing/net/).  
2. Složku ve vašem počítači, kam bude uložena výstupní obrázek (např. `C:\MyImages\`).  
3. Základní znalost C# a nastavení .NET projektu.

## Import jmenných prostorů

First, bring the required namespaces into your C# file:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

Tyto jmenné prostory vám poskytují přístup ke třídám `Bitmap`, `Graphics`, `GraphicsPath` a `Matrix`, které jsou potřebné pro workflow transformace.

## Průvodce krok za krokem

### Krok 1: Vytvořit bitmapu

Začínáme s prázdným plátnem. Velikost bitmapy a formát pixelů jsou zvoleny tak, aby poskytovaly vysoce kvalitní 32‑bitový obrázek podporující alfa průhlednost.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Tip:** Použití `Format32bppPArgb` zajišťuje, že obrázek zachová přednásobenou alfu, což je ideální pro výstup PNG.

### Krok 2: Vytvořit objekt Graphics

Objekt `Graphics` poskytuje kreslicí metody, které pracují s bitmapou. Vyčistíme pozadí na neutrální šedou, aby se transformovaný tvar výrazněji zobrazil.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### Krok 3: Vytvořit GraphicsPath

Objekt `GraphicsPath` vám umožňuje definovat složité tvary. Zde přidáváme elipsu umístěnou na (300, 300) s šířkou 400 a výškou 200 – efektivně **kreslíme otočenou elipsu** po transformaci.

```csharp
GraphicsPath path = new GraphicsPath();
path.AddEllipse(300, 300, 400, 200);
```

### Krok 4: Aplikovat lokální transformaci (příklad transformační matice)

Nyní odpovídáme na hlavní otázku: **jak aplikovat transformaci**. Vytvoříme `Matrix`, otočíme ji o 45° kolem středu elipsy (500, 400) a aplikujeme matici na cestu.

```csharp
Matrix matrix = new Matrix();
matrix.RotateAt(45, new Point(500, 400));
path.Transform(matrix);
```

> **Proč otáčet kolem středu?** Otáčení kolem středu tvaru zabraňuje tomu, aby obíhalo kolem počátku, a poskytuje přirozený vzhled.

### Krok 5: Vykreslit transformovanou cestu

S transformací na místě vykreslíme cestu pomocí modrého pera o tloušťce 2. Tento krok efektivně **kreslí otočenou elipsu** na plátno.

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawPath(pen, path);
```

### Krok 6: Uložit transformovaný obrázek (převést grafiku na PNG)

Nakonec uložíme bitmapu jako soubor PNG. Cesta kombinuje vámi zvolený adresář s podsložkou pro příklady transformací.

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\LocalTransformation_out.png");
```

> **Poznámka:** Přípona `.png` automaticky spustí PNG enkodér Aspose.Drawing, čímž splňuje požadavek **uložit bitmapu jako png**.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **Prázdný výstupní obrázek** | Grafika není vymazána nebo barva pera odpovídá pozadí | Zavolejte `graphics.Clear` s kontrastní barvou a ujistěte se, že barva pera je viditelná. |
| **Deformovaná rotace** | Použití `Rotate` místo `RotateAt` | Použijte `RotateAt` a specifikujte středový bod tvaru. |
| **Soubor nebyl uložen** | Neplatná cesta adresáře nebo chybějící oprávnění k zápisu | Ověřte, že adresář existuje a aplikace má oprávnění k zápisu. |
| **PNG vypadá rozmazaně** | Nízké nastavení DPI bitmapy | Vytvořte bitmapu s vyšším rozlišením nebo nastavte `graphics.SmoothingMode = SmoothingMode.AntiAlias`. |

## Často kladené otázky

**Q: Mohu řetězit více transformací (např. škálování a pak rotaci)?**  
A: Ano. Vytvořte jedinou `Matrix` a zavolejte metody jako `Scale`, `RotateAt` a `Translate` ve požadovaném pořadí, poté ji aplikujte pomocí `path.Transform(matrix);`.

**Q: Je Aspose.Drawing vhodný pro vysokovýkonné renderování?**  
A: Rozhodně. Knihovna je optimalizována jak pro rychlost, tak pro kvalitu a vyhýbá se omezením GDI+ na ne‑Windows platformách.

**Q: Jaké další typy transformací jsou podporovány?**  
A: Kromě rotace můžete provádět posunutí, škálování a zkosení pomocí stejné třídy `Matrix`.

**Q: Jak zacházet s výjimkami během procesu transformace?**  
A: Zabalte kreslicí kód do bloku `try‑catch` a prozkoumejte výjimky `System.Drawing.Drawing2D`. Podívejte se na oficiální [dokumentaci Aspose.Drawing](https://reference.aspose.com/drawing/net/) pro podrobné pokyny k ošetření chyb.

**Q: Můžu vyzkoušet Aspose.Drawing před zakoupením?**  
A: Ano, plně funkční bezplatná zkušební verze je k dispozici přes [odkaz ke stažení](https://releases.aspose.com/drawing/net/).

## Závěr

Díky tomuto průvodci nyní víte **jak uložit bitmapu jako PNG** po aplikaci lokální transformace pomocí Aspose.Drawing pro .NET. Stejný vzor lze znovu použít pro škálování, posunutí nebo zkosení libovolného tvaru, což vám umožní vytvářet bohaté, interaktivní vizuální komponenty ve vašich aplikacích a zároveň poskytovat výstup PNG vysoké kvality.

---

**Last Updated:** 2026-04-22  
**Tested With:** Aspose.Drawing 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}