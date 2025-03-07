---
title: Spojení cest s pery v Aspose.Drawing
linktitle: Spojení cest s pery v Aspose.Drawing
second_title: Aspose.Drawing .NET API – alternativa k System.Drawing.Common
description: Prozkoumejte umění spojování cest pomocí per v Aspose.Drawing pro .NET. Vytvářejte úžasnou grafiku s možnostmi LineJoin.
weight: 11
url: /cs/net/pens/join/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Spojení cest s pery v Aspose.Drawing

## Úvod

Vítejte ve světě Aspose.Drawing pro .NET! V tomto tutoriálu se ponoříme do umění spojování cest pomocí per pomocí Aspose.Drawing, výkonné knihovny, která poskytuje rozsáhlé funkce pro práci s grafikou a obrázky v aplikacích .NET.

## Předpoklady

Než se ponoříme do vzrušujícího světa spojování cest, ujistěte se, že máte na místě následující:

1.  Knihovna Aspose.Drawing: Ujistěte se, že máte nainstalovanou knihovnu Aspose.Drawing for .NET. Můžete si jej stáhnout[tady](https://releases.aspose.com/drawing/net/).

2. Vývojové prostředí .NET: Mějte na svém počítači nastavené funkční vývojové prostředí .NET.

Nyní, když jsme vše připraveni, pojďme se vrhnout na kroky ke spojení cest pomocí per v Aspose.Drawing.

## Importovat jmenné prostory

Než začnete kódovat, ujistěte se, že jste importovali potřebné jmenné prostory pro přístup k požadovaným třídám a metodám. Na začátek kódu přidejte následující jmenné prostory:

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Krok 1: Vytvořte bitmapový a grafický objekt

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

 Zde inicializujeme nový`Bitmap` objekt se zadanými rozměry a vytvořte a`Graphics` objekt z této bitmapy.

## Krok 2: Definujte metodu DrawPath

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

 V tomto kroku definujeme metodu tzv`DrawPath` to trvá a`Graphics` objekt, a`LineJoin`výčet a vertikální poloha (`y` ) jako parametry. Uvnitř metody vytvoříme a`Pen` objekt se zadanou barvou a šířkou, a`GraphicsPath` objekt a přidejte k němu řádky.

## Krok 3: Spojte cesty pomocí Bevel LineJoin

```csharp
DrawPath(graphics, LineJoin.Bevel, 200);
```

 Zavolej`DrawPath` metoda s`LineJoin.Bevel` ke spojení cest spojením zkosené čáry.

## Krok 4: Spojte cesty pomocí Round LineJoin

```csharp
DrawPath(graphics, LineJoin.Round, 400);
```

 Nyní zavolejte`DrawPath` metoda s`LineJoin.Round` spojovat cesty kulatým spojem.

## Krok 5: Uložte výsledek

```csharp
bitmap.Save("Your Document Directory" + @"Pens\Join_out.png");
```

Uložte výsledný obrázek do požadovaného adresáře.

Nyní jste úspěšně vytvořili spojené cesty pomocí per v Aspose.Drawing! Experimentujte s různými styly spojování čar a začleňte je do své grafiky.

## Závěr

V tomto tutoriálu jsme prozkoumali proces spojování cest pomocí per v Aspose.Drawing pro .NET. Pomocí několika kroků můžete vylepšit grafiku a vytvořit vizuálně přitažlivé návrhy.

## FAQ

### Q1: Mohu používat Aspose.Drawing zdarma?

 A1: Aspose.Drawing je komerční produkt, ale jeho možnosti můžete prozkoumat pomocí a[zkušební verze zdarma](https://releases.aspose.com/).

### Q2: Kde najdu dokumentaci Aspose.Drawing?

 A2: Viz[dokumentace](https://reference.aspose.com/drawing/net/) za komplexní návod.

### Q3: Jak mohu získat podporu pro Aspose.Drawing?

 A3: Navštivte[Aspose. Kreslící fórum](https://forum.aspose.com/c/diagram/17) za komunitu a podporu.

### Q4: Jsou k dispozici dočasné licence pro Aspose.Drawing?

 A4: Ano, můžete získat a[dočasná licence](https://purchase.aspose.com/temporary-license/) pro krátkodobé použití.

### Q5: Kde mohu zakoupit Aspose.Drawing?

 A5: Nákup Aspose.Drawing[tady](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
