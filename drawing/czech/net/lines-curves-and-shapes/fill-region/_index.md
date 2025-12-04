---
title: Vyplnění oblastí v Aspose.Drawing
linktitle: Vyplnění oblastí v Aspose.Drawing
second_title: Aspose.Drawing .NET API – alternativa k System.Drawing.Common
description: Naučte se, jak vyplnit oblasti v Aspose.Drawing pro .NET pomocí tohoto podrobného návodu. Vylepšete své dovednosti v oblasti grafického designu bez námahy.
weight: 20
url: /cs/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Vyplnění oblastí v Aspose.Drawing

## Úvod

Vytváření vizuálně přitažlivé grafiky často zahrnuje vyplnění oblastí barvami, vzory nebo přechody. Aspose.Drawing for .NET poskytuje výkonné nástroje, jak toho dosáhnout efektivně. V tomto tutoriálu se ponoříme do procesu vyplňování oblastí pomocí Aspose.Drawing, všestranné knihovny, která zjednodušuje grafické operace v aplikacích .NET.

## Předpoklady

Než začneme, ujistěte se, že máte splněny následující předpoklady:

1.  Aspose.Drawing Library: Stáhněte a nainstalujte knihovnu Aspose.Drawing. Knihovnu a její dokumentaci najdete[tady](https://reference.aspose.com/drawing/net/).

2. Vývojové prostředí: Nastavte vývojové prostředí .NET, jako je Visual Studio, pro integraci Aspose.Drawing do vašich projektů.

## Importovat jmenné prostory

Začněte importováním potřebných jmenných prostorů do vašeho projektu. Tyto jmenné prostory poskytují přístup ke třídám a metodám potřebným pro práci s Aspose.Drawing.

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


Nyní si ukázkový kód rozdělíme do několika kroků pro jasné a komplexní pochopení.

## Krok 1: Vytvořte bitmapový a grafický objekt

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

V tomto kroku inicializujeme novou bitmapu a grafický objekt, na který se má kreslit.

## Krok 2: Definujte GraphicsPath a vytvořte oblast

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

Definujte grafickou cestu zadáním mnohoúhelníku se sadou bodů. Vytvořte oblast pomocí této cesty.

## Krok 3: Vyloučení vnitřní oblasti

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

Vytvořte další grafickou cestu představující vnitřní obdélník a vylučte ji z hlavní oblasti.

## Krok 4: Vyberte štětec a vyplňte oblast

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

Vyberte štětec (v tomto případě plnou modrou barvu) a vyplňte dříve definovanou oblast vybraným štětcem.

## Krok 5: Uložte výsledný obrázek

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

Uložte konečný obrázek do požadovaného adresáře.

## Závěr

Vyplňování oblastí v Aspose.Drawing for .NET je přímočarý proces, který vám poskytuje flexibilitu při vytváření komplexní a vizuálně přitažlivé grafiky. Experimentujte s různými tvary, barvami a vzory a popusťte uzdu své kreativitě.

## FAQ

### Q1: Mohu použít Aspose.Drawing pro komerční projekty?

 A1: Ano, Aspose.Drawing lze použít pro osobní i komerční projekty. Podrobnosti o licencích naleznete na adrese[tady](https://purchase.aspose.com/buy).

### Q2: Je k dispozici bezplatná zkušební verze?

 A2: Ano, máte přístup k bezplatné zkušební verzi[tady](https://releases.aspose.com/).

### Q3: Jak mohu získat podporu pro Aspose.Drawing?

 A3: Navštivte[Aspose. Kreslící fórum](https://forum.aspose.com/c/diagram/17) získat pomoc od komunity a odborníků.

### Q4: Mohu generovat dynamické obrázky pomocí Aspose.Drawing?

A4: Rozhodně. Aspose.Drawing vám umožňuje dynamicky vytvářet a manipulovat s obrázky ve vašich aplikacích .NET.

### Q5: Jsou k dispozici dočasné licence?

 A5: Ano, lze získat dočasné licence[tady](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
