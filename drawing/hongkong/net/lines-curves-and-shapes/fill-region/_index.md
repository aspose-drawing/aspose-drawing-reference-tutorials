---
title: Aspose.Drawing 中的填充區域
linktitle: Aspose.Drawing 中的填充區域
second_title: Aspose.Drawing .NET API - System.Drawing.Common 的替代方案
description: 透過此逐步教學，了解如何在 Aspose.Drawing for .NET 中填滿區域。輕鬆提升您的圖形設計技能。
weight: 20
url: /zh-hant/net/lines-curves-and-shapes/fill-region/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Drawing 中的填充區域

## 介紹

創建具有視覺吸引力的圖形通常涉及用顏色、圖案或漸變填充區域。 Aspose.Drawing for .NET 提供了強大的工具來有效地實現這一目標。在本教程中，我們將深入研究使用 Aspose.Drawing 填充區域的過程，Aspose.Drawing 是一個通用函式庫，可簡化 .NET 應用程式中的圖形操作。

## 先決條件

在我們開始之前，請確保您具備以下先決條件：

1.  Aspose.Drawing 函式庫：下載並安裝 Aspose.Drawing 函式庫。您可以找到該庫及其文檔[這裡](https://reference.aspose.com/drawing/net/).

2. 開發環境：設定 .NET 開發環境，例如 Visual Studio，將 Aspose.Drawing 整合到您的專案中。

## 導入命名空間

首先將必要的命名空間匯入到您的專案中。這些命名空間提供對使用 Aspose.Drawing 所需的類別和方法的存取。

```csharp
using System.Drawing;
using System.Drawing.Drawing2D;
```


現在，讓我們將範例程式碼分解為多個步驟，以便清楚、全面地理解。

## 第 1 步：建立點陣圖和圖形對象

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
```

在此步驟中，我們初始化一個新的點陣圖和一個要在其上繪製的圖形物件。

## 第 2 步：定義 GraphicsPath 並建立區域

```csharp
GraphicsPath path = new GraphicsPath();
path.AddPolygon(new Point[] { new Point(100, 400), new Point(500, 100), new Point(900, 400), new Point(500, 700) });
Region region = new Region(path);
```

透過指定具有一組點的多邊形來定義圖形路徑。使用此路徑建立一個區域。

## 步驟 3：排除內部區域

```csharp
GraphicsPath innerPath = new GraphicsPath();
innerPath.AddRectangle(new Rectangle(300, 300, 400, 200));
region.Exclude(innerPath);
```

建立另一個表示內部矩形的圖形路徑並將其從主區域中排除。

## 第四步：選擇畫筆並填滿區域

```csharp
Brush brush = new SolidBrush(Color.FromKnownColor(KnownColor.Blue));
graphics.FillRegion(brush, region);
```

選擇一個畫筆（在本例中為純藍色）並使用所選畫筆填滿先前定義的區域。

## 第 5 步：儲存結果影像

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\FillRegion_out.png");
```

將最終影像儲存到您所需的目錄。

## 結論

在 Aspose.Drawing for .NET 中填滿區域是一個簡單的過程，可讓您靈活地創建複雜且具有視覺吸引力的圖形。嘗試不同的形狀、顏色和圖案來釋放您的創造力。

## 常見問題解答

### Q1：我可以將Aspose.Drawing用於商業項目嗎？

 A1：是的，Aspose.Drawing 可用於個人和商業項目。有關許可詳細信息，請訪問[這裡](https://purchase.aspose.com/buy).

### Q2: 有免費試用嗎？

A2：是的，您可以免費試用[這裡](https://releases.aspose.com/).

### Q3：如何獲得 Aspose.Drawing 的支援？

 A3：訪問[Aspose.Drawing 論壇](https://forum.aspose.com/c/diagram/17)獲得社區和專家的幫助。

### Q4：我可以使用Aspose.Drawing產生動態影像嗎？

A4：當然。 Aspose.Drawing 可讓您在 .NET 應用程式中動態建立和操作影像。

### Q5：有臨時許可證嗎？

 A5：是的，可以取得臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
