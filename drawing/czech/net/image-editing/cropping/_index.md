---
date: 2025-12-02
description: Naučte se oříznout obrázek v .NET pomocí Aspose.Drawing. Tento tutoriál
  o ořezávání obrázků ukazuje krok za krokem, jak uložit oříznutý obrázek, pracovat
  s bitmapou a provádět hromadné ořezávání obrázků.
language: cs
linktitle: How to Crop Image .NET Using Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak oříznout obrázek v .NET pomocí Aspose.Drawing
url: /net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Jak oříznout obrázek v .NET pomocí Aspose.Drawing

## Úvod

Pokud vytváříte aplikaci .NET, která vyžaduje přesnou manipulaci s obrázky, je nezbytné se naučit **jak oříznout obrázek**. Aspose.Drawing poskytuje bohaté, plně spravované API, které vám umožní **oříznout obrázek v .NET** projektech bez nutnosti spoléhat se na starší knihovnu System.Drawing.Common. V tomto tutoriálu uvidíte kompletní, end‑to‑end příklad, který vás provede načtením bitmapy, definováním oblasti ořezu, provedením operace a nakonec **uložením oříznutého obrázku**. Na konci budete připraveni integrovat ořezávání obrázků do libovolného .NET řešení – ať už jde o jeden obrázek nebo **dávkové ořezávání obrázků**.

## Rychlé odpovědi
- **Jaká knihovna by měla být použita?** Aspose.Drawing pro .NET  
- **Mohu oříznout libovolný formát obrázku?** Ano – jsou podporovány nejčastější formáty (PNG, JPEG, BMP atd.).  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; licence je vyžadována pro produkci.  
- **Je možné dávkové zpracování?** Rozhodně – můžete opakovat stejný kód pro kolekci souborů.  
- **Jaké verze .NET jsou podporovány?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Co je “crop image .net”?

Ořezání obrázku znamená vyříznutí obdélníkové oblasti z většího obrázku. V .NET se tato operace typicky provádí na objektu `Bitmap`. Aspose.Drawing proces zjednodušuje tím, že poskytuje vysoce výkonné grafické primitivy, které fungují konzistentně napříč platformami.

## Proč použít Aspose.Drawing pro ořezávání obrázků?

- **Spolehlivost napříč platformami** – Žádné nativní závislosti, funguje na Windows, Linuxu i macOS.  
- **Bohatá podpora pixelových formátů** – Zpracovává 32‑bit ARGB, PArgb a mnoho dalších formátů.  
- **Optimalizovaný výkon** – Optimalizované kreslení a interpolace pro velké obrázky.  
- **Bezproblémová integrace** – Spolupracuje s ostatními produkty Aspose (PDF, Slides atd.).

## Předpoklady

Než začnete, ujistěte se, že máte:

- **Aspose.Drawing Library** – Přidejte NuGet balíček `Aspose.Drawing` do svého projektu nebo jej stáhněte z [oficiálního webu](https://releases.aspose.com/drawing/net/).  
- **Složku s obrázky** – Adresář, který obsahuje zdrojové obrázky, jež chcete oříznout. Nahraďte `"Your Document Directory"` v ukázkách kódu skutečnou cestou na vašem počítači.

## Import Namespaces

Nejprve importujte jmenný prostor, který obsahuje třídy pro kreslení:

```csharp
using System.Drawing;
```

Tím získáte přístup k `Bitmap`, `Graphics`, `Rectangle` a dalším nezbytným typům.

## Průvodce krok za krokem

### Krok 1: Vytvoření bitmapového plátna (crop image bitmap)

Začneme vytvořením prázdné bitmapy, která bude obsahovat výsledek ořezu. Nastavte šířku, výšku a pixelový formát tak, aby odpovídaly velikosti oblasti, kterou chcete vyříznout.

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **Tip:** Formát `Format32bppPArgb` zachovává alfa průhlednost a poskytuje vysoce kvalitní vykreslování.

### Krok 2: Vytvoření objektu Graphics

Objekt `Graphics` nám umožní kreslit na bitmapové plátno. Nastavení `InterpolationMode` ovlivňuje, jak bude obrázek při ořezu přeškálován.

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

> **Profesionální tip:** Pro hladší výsledky u škálovaných obrázků zvažte `InterpolationMode.HighQualityBicubic`.

### Krok 3: Načtení zdrojového obrázku

Načtěte obrázek, který chcete oříznout. Cesta kombinuje váš adresář dokumentů s názvem souboru.

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

> **Poznámka:** Aspose.Drawing dokáže přímo číst PNG, JPEG, BMP, GIF, TIFF a mnoho dalších formátů.

### Krok 4: Definování zdrojových a cílových obdélníků

`sourceRectangle` vybírá část původního obrázku, kterou chcete zachovat. Zde vybíráme oblast 50 × 40 pixelů v levém horním rohu. `destinationRectangle` určuje, kam grafický engine umístí oříznutou oblast na novou bitmapu.

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

> **Proč oba obdélníky?** Použití identických obdélníků provádí jednoduchý ořez. `destinationRectangle` můžete změnit, pokud chcete oříznutý fragment přesunout nebo změnit jeho měřítko.

### Krok 5: Provedení operace ořezu

Metoda `DrawImage` zkopíruje vybranou oblast ze zdrojového obrázku do cílové bitmapy.

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

> **Častý úskalí:** Zapomenutí uvolnit `Graphics` může zamknout soubor bitmapy. Uvolnění provedeme automaticky při ukončení metody.

### Krok 6: Uložení oříznutého obrázku (save cropped image)

Nakonec výsledek zapíšeme na disk. Změňte název souboru a cestu podle potřeby.

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

> **Výsledek:** Nyní máte nový PNG soubor, který obsahuje pouze oblast 50 × 40 pixelů, kterou jste určili.

## Časté problémy a řešení

| Problém | Příčina | Řešení |
|-------|-------|-----|
| **Prázdný výstupní soubor** | Zdrojový obdélník mimo hranice obrázku | Ověřte souřadnice a velikost `sourceRectangle`. |
| **Výjimka Out‑of‑memory** | Velmi velké zdrojové obrázky | Zpracovávejte obrázky po částech nebo použijte `using` bloky pro okamžité uvolnění prostředků. |
| **Nesprávné barvy** | Nesoulad pixelového formátu | Zajistěte shodu pixelového formátu zdrojové bitmapy nebo jej konvertujte pomocí `Bitmap.Clone`. |

## Často kladené otázky

**Q: Mohu oříznout obrázky libovolného formátu pomocí Aspose.Drawing?**  
A: Ano, Aspose.Drawing podporuje PNG, JPEG, BMP, GIF, TIFF a mnoho dalších formátů, takže můžete **jak oříznout obrázek** bez ohledu na původní typ souboru.

**Q: Existují pokročilé možnosti ořezu?**  
A: Rozhodně. Můžete kombinovat `GraphicsPath` pro neobdélníkové ořezy, aplikovat rotaci nebo použít `ImageAttributes` pro úpravu barev.

**Q: Můžu na jednom obrázku provést více ořezů?**  
A: Ano – stačí opakovat volání `DrawImage` s různými zdrojovými obdélníky nebo je řetězit v cyklu pro složitější transformace.

**Q: Je Aspose.Drawing vhodný pro dávkové ořezávání obrázků?**  
A: Ano. Zabalte výše uvedené kroky do `foreach` smyčky přes kolekci cest k souborům a automaticky zpracujte desítky či stovky obrázků.

**Q: Kde získám podporu pro dotazy týkající se Aspose.Drawing?**  
A: Navštivte [Aspose.Drawing Forum](https://forum.aspose.com/c/diagram/17), kde můžete klást otázky, sdílet kód a získat pomoc od komunity i produktových inženýrů.

## Závěr

V tomto tutoriálu jsme ukázali kompletní **crop image .net** workflow pomocí Aspose.Drawing. Nyní víte, **jak oříznout obrázek**, jak definovat přesné zdrojové obdélníky a **uložit oříznutý obrázek**. S těmito základy můžete rozšířit kód o **dávkové ořezávání obrázků**, aplikovat vlastní transformace nebo integrovat logiku do větších pipeline pro zpracování obrázků.

---  

**Poslední aktualizace:** 2025-12-02  
**Testováno s:** Aspose.Drawing 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}