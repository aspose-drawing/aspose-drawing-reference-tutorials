---
date: 2026-02-19
description: Naučte se kreslit cesty a spojovat je pomocí per v Aspose.Drawing a poté
  uložit obrázek jako PNG pomocí jednoduchého C# kódu.
linktitle: Joining Paths with Pens in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak kreslit cestu a spojovat cesty pomocí per v Aspose.Drawing
url: /cs/net/pens/join/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak kreslit cesty a spojovat cesty pomocí per v Aspose.Drawing

## Úvod

Vítejte ve světě **Aspose.Drawing pro .NET**! V tomto tutoriálu objevíte **jak kreslit cesty** objektů, spojíte je s různými styly spojení čar a nakonec **uložíte obrázek jako PNG**. Ať už vytváříte nástroj pro reportování, editor designu nebo jen potřebujete ostrou vektorovou grafiku, ovládnutí kreslení cest pomocí per vám poskytne detailní kontrolu nad vizuálním výstupem.

## Rychlé odpovědi
- **Co znamená „draw path“?** Vytváří definice čar nebo tvarů založené na vektorech, které může vykreslit objekt `Graphics`.  
- **Jaké typy spojení čar jsou k dispozici?** `Bevel`, `Miter`, `Round` a `BevelClipped`.  
- **Mohu výsledek exportovat jako PNG?** Ano — použijte `Bitmap.Save` s příponou `.png`.  
- **Potřebuji licenci?** Zkušební verze funguje pro hodnocení; pro produkční nasazení je vyžadována komerční licence.  
- **Jaké verze .NET jsou podporovány?** .NET Framework 4.6+, .NET Core 3.1+ a .NET 6+.

## Co je „jak kreslit cestu“ v Aspose.Drawing?

Kreslení cesty znamená vytvoření objektu `GraphicsPath`, který obsahuje sérii čar, křivek nebo tvarů. Jakmile je cesta vytvořena, namalujete ji na povrch `Graphics` pomocí `Pen`. Tento přístup je flexibilnější než kreslení jednotlivých čar, protože můžete na celý tvar použít transformace, ořezávání a různé styly spojení.

## Proč použít Aspose.Drawing pro spojování cest?

- **Plná kompatibilita s .NET** – funguje na Windows, Linuxu i macOS.  
- **Bohaté možnosti spojení čar** – vytvořte zkosené, zaoblené nebo šikmé rohy jednou vlastností.  
- **Vysoce kvalitní rastrový výstup** – uložte přímo do PNG, JPEG, BMP atd., bez dalších kroků převodu.  
- **Žádná omezení GDI+** – ideální pro serverové vykreslování, kde může být omezen `System.Drawing.Common`.

## Předpoklady

Než se ponoříme do kódu, ujistěte se, že máte:

1. **Knihovnu Aspose.Drawing** – stáhněte ji **[zde](https://releases.aspose.com/drawing/net/)**.  
2. **Vývojové prostředí .NET** – Visual Studio, VS Code nebo jakékoli IDE podporující C#.

Nyní, když je vše připraveno, projděme si jednotlivé kroky.

## Importujte jmenné prostory

Přidejte požadované jmenné prostory na začátek souboru, aby kompilátor věděl, kde najít třídy pro grafiku:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Krok 1: Vytvořte objekt Bitmap a Graphics

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

Začínáme s prázdným plátnem (`Bitmap`) o rozměrech 1000 × 800 pixelů a získáme objekt `Graphics`, který vykreslí naše příkazy.

## Krok 2: Definujte metodu DrawPath

```csharp
private static void DrawPath(Graphics graphics, LineJoin join, int y)
{
    Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 30);
    GraphicsPath path = new GraphicsPath();
    path.StartFigure();
    path.AddLine(100, y, 200, y);
    path.AddLine(200, y, 200, y + 100);
    pen.LineJoin = join;
    graphics.DrawPath(pen, path);
}
```

Tato pomocná metoda zapouzdřuje logiku kreslení:

- **Pen** – nastaví barvu a tloušťku (30 px).  
- **GraphicsPath** – definuje dvě spojené čáry tvořící tvar „L“.  
- **LineJoin** – určuje, jak je vykreslený roh mezi dvěma čarami (`Bevel`, `Round` atd.).  

Můžete tuto metodu zavolat s libovolnou hodnotou `LineJoin` a zobrazit vizuální rozdíl.

## Krok 3: Spojte cesty pomocí Bevel LineJoin

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

Použití `LineJoin.Bevel` vytvoří zploštělý roh tam, kde se dvě čáry setkají.

## Krok 4: Spojte cesty pomocí Round LineJoin

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

`LineJoin.Round` vytvoří hladký, zaoblený roh — ideální pro elegantnější vzhled.

## Krok 5: Uložte výsledek jako PNG

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

Volání `Save` zapíše bitmapu do souboru ve formátu PNG. Přizpůsobte cestu tak, aby odpovídala vašemu prostředí.

## Časté problémy a řešení

| Problém | Proč k tomu dochází | Řešení |
|-------|----------------|-----|
| **Obrázek je prázdný** | `Graphics` objekt nebyl vymazán nebo je bitmapa příliš malá. | Zavolejte `graphics.Clear(Color.White);` před kreslením nebo zvětšete rozměry bitmapy. |
| **Roh vypadá zubatě** | Použití bitmapy s nízkým rozlišením a silným perem. | Zvyšte DPI bitmapy (`new Bitmap(width, height, PixelFormat.Format32bppPArgb)`) nebo zmenšete šířku pera. |
| **Chyba: soubor nenalezen** | Neplatná cesta pro uložení. | Použijte `Path.Combine(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments), "Pens", "Join_out.png")`. |

## Často kladené otázky

### Q1: Mohu používat Aspose.Drawing zdarma?

A1: Aspose.Drawing je komerční produkt, ale můžete si jeho možnosti vyzkoušet pomocí **[bezplatné zkušební verze](https://releases.aspose.com/)**.

### Q2: Kde najdu dokumentaci k Aspose.Drawing?

A2: Podívejte se na **[dokumentaci](https://reference.aspose.com/drawing/net/)** pro podrobné pokyny.

### Q3: Jak mohu získat podporu pro Aspose.Drawing?

A3: Navštivte **[forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44)** pro komunitní pomoc a oficiální podporu.

### Q4: Jsou k dispozici dočasné licence pro Aspose.Drawing?

A4: Ano, můžete získat **[dočasnou licenci](https://purchase.aspose.com/temporary-license/)** pro krátkodobé použití.

### Q5: Kde si mohu zakoupit Aspose.Drawing?

A5: Zakupte Aspose.Drawing **[zde](https://purchase.aspose.com/buy)**.

## Závěr

V tomto průvodci jsme pokryli **jak kreslit cesty** objektů, použili různé styly `LineJoin` a uložili finální grafiku jako soubor PNG pomocí Aspose.Drawing pro .NET. Ovládnutím těchto kroků můžete vytvářet propracované vektorové grafiky, vlastní ikony nebo dynamické grafy přímo ze serverového kódu.

**Poslední aktualizace:** 2026-02-19  
**Testováno s:** Aspose.Drawing 24.11 for .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}