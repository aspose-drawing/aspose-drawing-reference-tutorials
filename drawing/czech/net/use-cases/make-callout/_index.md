---
title: Vytváření popisků v Aspose.Drawing
linktitle: Vytváření popisků v Aspose.Drawing
second_title: Aspose.Drawing .NET API – alternativa k System.Drawing.Common
description: Vylepšete své ilustrace dokumentů pomocí Aspose.Drawing pro .NET! Naučte se krok za krokem přidávat popisky pro jasnější a informativní vizuály.
weight: 10
url: /cs/net/use-cases/make-callout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vytváření popisků v Aspose.Drawing

## Úvod
Vítejte v našem podrobném průvodci vytvářením popisků v Aspose.Drawing pro .NET! Pokud chcete vylepšit své ilustrace dokumentů popisky, jste na správném místě. V tomto tutoriálu rozdělíme proces na zvládnutelné kroky pomocí knihovny Aspose.Drawing.
## Předpoklady
Než se pustíte do výukového programu, ujistěte se, že máte následující předpoklady:
- Základní znalost programovacího jazyka C#.
-  Knihovna Aspose.Drawing nainstalována. Můžete si jej stáhnout[tady](https://releases.aspose.com/drawing/net/).
- Dokument nebo obrázek, kam chcete přidat popisky.
## Importovat jmenné prostory
Ujistěte se, že máte ve svém projektu zahrnuty potřebné jmenné prostory:
```csharp
using System.Text;
using System.Threading.Tasks;
using System;
using System.Drawing;
using System.Drawing.Text;
using System.IO;
```
## Krok 1: Načtěte obrázek
 Začněte načtením obrázku, kam chcete přidat popisky. Nahradit`"Your Document Directory"` a`"gears.png"` s vaším skutečným adresářem a názvem souboru obrázku.
```csharp
using (var image = Image.FromFile(Path.Combine("Your Document Directory", "gears.png")))
{
    // Váš kód zde
}
```
## Krok 2: Vytvořte grafický objekt
 Vytvořit`Graphics` objekt z obrázku pro provedení operací kreslení.
```csharp
var graphics = Graphics.FromImage(image);
graphics.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;
graphics.PageUnit = GraphicsUnit.Pixel;
```
## Krok 3: Definujte pozice popisků
Definujte počáteční a koncový bod pro každý popis spolu s hodnotou a jednotkou popisku.
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
## Krok 4: Nakreslete popisky
 Implementujte`DrawCallOut` způsob kreslení popisků na obrázek.
```csharp
DrawCallOut(graphics, startAnchor1, endAnchor1, value1, unit1);
DrawCallOut(graphics, startAnchor2, endAnchor2, value2, unit2);
```
## Krok 5: Uložte obrázek
Uložte obrázek s popisky do požadovaného adresáře.
```csharp
image.Save(Path.Combine("Your Document Directory", "gears_with_callout_out.png"));
```
## Nakreslete zdrojový kód popisku
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
## Závěr

Gratulujeme! Úspěšně jste přidali popisky k obrázku pomocí Aspose.Drawing for .NET. Nebojte se experimentovat s různými pozicemi a hodnotami, abyste si popisky dále přizpůsobili.

## Nejčastější dotazy

### Mohu použít Aspose.Drawing pro jiné typy ilustrací?

Ano, Aspose.Drawing podporuje širokou škálu kreslicích operací pro různé typy ilustrací.

### Je Aspose.Drawing kompatibilní s různými formáty obrázků?

Absolutně! Aspose.Drawing podporuje oblíbené obrazové formáty jako PNG, JPEG, GIF a další.

### Kde najdu další příklady a dokumentaci?

 Prozkoumejte komplexní dokumentaci[tady](https://reference.aspose.com/drawing/net/).

### Jak získám podporu, pokud narazím na problémy?

 Navštivte[Aspose. Kreslící fórum](https://forum.aspose.com/c/diagram/17) za podporu komunity.

### Mohu Aspose.Drawing před nákupem vyzkoušet?

 Rozhodně! Začněte s bezplatnou zkušební verzí[tady](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
