---
title: Aspose.Drawing for .NET 中的測量單位
linktitle: Aspose.Drawing 中的測量單位
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 在這個深入的教學中探索 Aspose.Drawing for .NET 的多功能性，掌握精確圖形的測量單位。
weight: 14
url: /zh-hant/net/coordinate-transformations/units-of-measure/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing for .NET 中的測量單位

## 介紹

歡迎來到 Aspose.Drawing for .NET 的世界，在這裡，圖形操作的精確性和靈活性得到了滿足。在本教程中，我們將深入研究 Aspose.Drawing 中測量單位的複雜性，為您提供逐步指南，以利用這個非凡庫的強大功能。

## 先決條件

在我們深入學習本教程之前，請確保您具備以下先決條件：

-  Aspose.Drawing for .NET：確保您已安裝程式庫。你可以下載它[這裡](https://releases.aspose.com/drawing/net/).

- 文檔目錄：有一個指定的目錄來保存您建立的文檔。

- 基本 C# 知識：建議對 C# 有基本了解，以便充分利用本指南。

## 導入命名空間

在開始之前，讓我們匯入必要的命名空間以有效地使用 Aspose.Drawing：

```csharp
using System.Drawing;
```

現在，讓我們將每個範例分解為多個步驟：

## 點作為測量單位

1. 建立點陣圖：初始化具有指定寬度和高度的位圖。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

2. 建立圖形：從點陣圖產生一個 Graphics 物件以在其上繪製。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

3. 將頁面單位設定為點：將點定義為測量單位（1 點 = 1/72 英吋）。

```csharp
graphics.PageUnit = GraphicsUnit.Point;
```

4. 繪製矩形：以點為單位繪製矩形。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Red), 36f), 72, 72, 72, 72);
```

## 毫米作為測量單位

1. 將頁面單位設定為毫米：將測量單位變更為毫米（1 毫米 = 1/25.4 英吋）。

```csharp
graphics.PageUnit = GraphicsUnit.Millimeter;
```

2. 以毫米為單位繪製矩形：以毫米為單位繪製另一個矩形。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Green), 6.35f), 25.4f, 25.4f, 25.4f, 25.4f);
```

## 英吋作為測量單位

1. 將頁面單位設定為英吋：將測量單位切換為英吋。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

2. 以英吋為單位繪製矩形：以英吋為單位繪製矩形。

```csharp
graphics.DrawRectangle(new Pen(Color.FromKnownColor(KnownColor.Blue), 0.125f), 1, 1, 1, 1);
```

## 保存結果

完成範例後，將產生的影像儲存到文件目錄：

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\UnitsOfMeasure_out.png");
```

現在，您已經成功地在 Aspose.Drawing for .NET 中導航了不同的測量單位，使用點、毫米和英吋建立了矩形的視覺化表示。

## 結論

在本教學中，我們探討了 Aspose.Drawing for .NET 如何處理不同的測量單位。透過操縱點、毫米和英寸，您可以在圖形創作中實現精度和適應性。試試這些概念來釋放 Aspose.Drawing 的全部潛力。

## 常見問題解答

### Q1：我可以將 Aspose.Drawing for .NET 與其他 .NET 框架一起使用嗎？

A1：是的，Aspose.Drawing 與各種 .NET 框架相容，為您的開發環境提供靈活性。

### Q2: 有免費試用嗎？

 A2：是的，您可以透過免費試用來探索 Aspose.Drawing[這裡](https://releases.aspose.com/).

### 問題 3：如何獲得 Aspose.Drawing for .NET 支援？

 A3：訪問[Aspose.繪圖論壇](https://forum.aspose.com/c/drawing/44)以獲得社區支持和討論。

### Q4：我可以為短期專案購買臨時許可證嗎？

 A4：是的，您可以獲得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

### Q5：在哪裡可以找到Aspose.Drawing的詳細文件？

 A5：提供全面的文檔[這裡](https://reference.aspose.com/drawing/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
