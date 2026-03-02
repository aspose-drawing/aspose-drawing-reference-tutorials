---
date: 2026-03-02
description: Vylepšete ilustrace svých dokumentů pomocí Aspose.Drawing pro .NET! Naučte
  se krok za krokem, jak přidat vysvětlivky pro jasnější a informativnější vizuály.
linktitle: Making Callouts in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: Jak přidat popisky pomocí Aspose.Drawing pro .NET
url: /cs/net/use-cases/make-callout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytváření popisků v Aspose.Drawing

## Úvod
Pokud se ptáte, **jak přidat popisky** do svých obrázků nebo diagramů pomocí Aspose.Drawing pro .NET, jste na správném místě. V tomto tutoriálu vás provedeme celým procesem – od načtení obrázku po kreslení krásně stylizovaných popisků – abyste mohli své ilustrace učinit přehlednějšími a informativnějšími.

## Rychlé odpovědi
- **Jaká knihovna potřebuji?** Aspose.Drawing pro .NET (ke stažení z oficiálního webu).  
- **Které verze .NET jsou podporovány?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Potřebuji licenci?** Bezplatná zkušební verze funguje pro vývoj; pro produkci je vyžadována komerční licence.  
- **Jak dlouho trvá implementace?** Obvykle méně než 10 minut pro základní popisek.  
- **Mohu přizpůsobit barvy a písma?** Ano – vše je řízeno standardními objekty GDI+ (Pen, Font, Brush).

## Jak přidat popisky v Aspose.Drawing
Níže je stručný, krok za krokem průvodce, který přesně ukazuje, **jak přidat popisky** do obrázku. Klidně zkopírujte kód, experimentujte s pozicemi a přizpůsobte styl tak, aby odpovídal vaší značce.

## Předpoklady
Než se pustíte do práce, ujistěte se, že máte:

- Základní znalosti programovacího jazyka C#.  
- Knihovnu Aspose.Drawing nainstalovanou. Můžete si ji stáhnout [zde](https://releases.aspose.com/drawing/net/).  
- Dokument nebo obrázek, do kterého chcete přidat popisky.

## Importování jmenných prostorů
Ujistěte se, že máte ve svém projektu zahrnuty potřebné jmenné prostory:

```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```

## Krok 1: Načtení obrázku
Začněte načtením obrázku, do kterého chcete přidat popisky. Nahraďte `"Your Document Directory"` a `"gears.png"` skutečným adresářem a názvem souboru obrázku.

```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Your code here
}
```

## Krok 2: Vytvoření objektu Graphics
Vytvořte objekt `Graphics` z obrázku, abyste mohli provádět kreslicí operace.

```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```

## Krok 3: Definování pozic popisků
Definujte počáteční a koncové body pro každý popisek spolu s hodnotou a jednotkou popisku.

```csharp
PointF startAnchor1 = new PointF(107, 55);
PointF endAnchor1 = new PointF(179, 5);
int value1 = 74;
string unit1 = "mm";
PointF startAnchor2 = new PointF(111, 146);
PointF endAnchor2 = new PointF(29, 180);
int value2 = 28;
string unit2 = "mm";
```

## Krok 4: Kreslení popisků
Implementujte metodu `DrawCallOut`, která vykreslí popisky na obrázku.

```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```

## Krok 5: Uložení obrázku
Uložte obrázek s popisky do požadovaného adresáře.

```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```

## Zdrojový kód pro kreslení popisku
```csharp
void DrawCallOut(Graphics graphic, PointF startAnchor, PointF endAnchor, int value, string unit)
            {
                Pen pen = new Pen(Color.DarkGray, 1);
                Font font = new Font("Arial", 10, FontStyle.Bold);
                string outputValue = $"{value} {unit}";
                var textSize = graphic.MeasureString(outputValue, font);
                int diameterSymbolSize = 12;
                int spaceSize = 3;
                textSize.Width += diameterSymbolSize + spaceSize;
                float callOutMiddleX = endAnchor.X > startAnchor.X ? endAnchor.X - textSize.Width : endAnchor.X + textSize.Width;
                float callOutMiddleY = endAnchor.Y > startAnchor.Y ? endAnchor.Y - textSize.Height : endAnchor.Y + textSize.Height;
                graphic.DrawLine(pen, startAnchor.X, startAnchor.Y, callOutMiddleX, callOutMiddleY);
                float textAnchorX = Math.Min(callOutMiddleX, endAnchor.X);
                float textAnchorY = callOutMiddleY;
                graphic.DrawLine(pen, callOutMiddleX, callOutMiddleY, textAnchorX == callOutMiddleX ? textAnchorX + textSize.Width : textAnchorX, callOutMiddleY);
                graphic.DrawEllipse(pen, new Rectangle((int)textAnchorX + spaceSize, (int)(textAnchorY - textSize.Height) + spaceSize, 10, 10));
                graphic.DrawLine(pen, (int)textAnchorX + 1, (int)textAnchorY - 1, (int)textAnchorX + diameterSymbolSize + 2, (int)textAnchorY - diameterSymbolSize - 2);
                SolidBrush brush = new SolidBrush(Color.DarkGray);
                graphic.DrawString(outputValue, font, brush, (int)textAnchorX + diameterSymbolSize + spaceSize, (int)(textAnchorY - textSize.Height));
            }
```

## Časté problémy a tipy
- **Nesprávné souřadnice ukotvení** – ujistěte se, že počáteční a koncové body jsou v rámci rozměrů obrázku; jinak může být popisek oříznut.  
- **Překrývající se text** – upravte `spaceSize` nebo velikost písma, pokud se popisek střetává s jinou grafikou.  
- **Výkon** – u velmi velkých obrázků zvažte uvolnění objektů `Pen`, `Font` a `Brush` po použití, aby se uvolnily zdroje.

## Závěr
Gratulujeme! Nyní víte, **jak přidat popisky** do obrázku pomocí Aspose.Drawing pro .NET. Klidně experimentujte s různými pozicemi, barvami a písmy, aby odpovídaly vašemu vizuálnímu stylu.

## Často kladené otázky

### Mohu použít Aspose.Drawing pro jiné typy ilustrací?
Ano, Aspose.Drawing podporuje širokou škálu kreslicích operací pro různé typy ilustrací.

### Je Aspose.Drawing kompatibilní s různými formáty obrázků?
Rozhodně! Aspose.Drawing podporuje populární formáty obrázků jako PNG, JPEG, GIF a další.

### Kde najdu více příkladů a dokumentaci?
Prozkoumejte komplexní dokumentaci [zde](https://reference.aspose.com/drawing/net/).

### Jak získám podporu, pokud narazím na problémy?
Navštivte [forum Aspose.Drawing](https://forum.aspose.com/c/drawing/44) pro komunitní podporu.

### Můžu vyzkoušet Aspose.Drawing před zakoupením?
Samozřejmě! Začněte s bezplatnou zkušební verzí [zde](https://releases.aspose.com/).

**Další otázky a odpovědi**

**Q: Mohu změnit styl čáry popisku (čárkovaná, tečkovaná)?**  
**A:** Ano – stačí nastavit vlastnost `Pen.DashStyle` před vykreslením čáry.

**Q: Je možné přidat barvu pozadí k popisku?**  
**A:** Rozhodně. Vytvořte `SolidBrush` s požadovanou barvou a vyplňte obdélník za textem před voláním `DrawString`.

**Q: Jak zajistit, aby popisek vypadal stejně na displejích s vysokým DPI?**  
**A:** Nastavte `graphics.PageUnit = GraphicsUnit.Pixel` (jak je ukázáno) a používejte vektorová měření, aby měřítko zůstalo konzistentní.

---

**Poslední aktualizace:** 2026-03-02  
**Testováno s:** Aspose.Drawing 24.11 pro .NET  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}