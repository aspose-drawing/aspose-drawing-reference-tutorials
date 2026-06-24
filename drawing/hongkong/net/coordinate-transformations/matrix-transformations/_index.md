---
date: 2026-05-03
description: 學習此 Aspose.Drawing .NET 矩陣變換教學，內容涵蓋如何繪製旋轉矩形、套用矩陣旋轉，以及執行矩陣縮放（C#）。
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- cross platform drawing
- matrix rotation c#
- c# graphics matrix
linktitle: Aspose.Drawing 中的矩陣變換
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 矩陣變換教學：Aspose.Drawing for .NET 中的矩陣變換
url: /zh-hant/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 矩陣變換教學：Aspose.Drawing for .NET 中的矩陣變換

## 簡介

歡迎閱讀本 **matrix transformation tutorial**，適用於 Aspose.Drawing .NET！無論您是構建圖形編輯器、產生動態報表，或僅在嘗試幾何效果，掌握矩陣變換即可讓您 **draw rotated rectangle** 圖形、**apply matrix rotation**，甚至執行 **matrix scaling C#** 操作，精確無誤。接下來的幾分鐘內，您將看到如何設定畫布、變換形狀並儲存結果——全部使用功能強大的 Aspose.Drawing API。

## 快速回答

- **What does this tutorial cover?** 在 Aspose.Drawing 中對矩形執行 rotate、translate 和 scale 矩陣變換。  
- **Do I need a license?** 免費試用可用於開發；商業授權在正式環境中必須使用。  
- **Which .NET versions are supported?** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。  
- **How long will implementation take?** 基本範例大約需要 10‑15 分鐘。  
- **Can I see the output image?** 可以——教學會儲存 PNG，您可直接開啟。

## 什麼是矩陣變換教學？

矩陣變換教學說明如何使用 3 × 3 變換矩陣來平移、旋轉、縮放或剪切圖形基元。在 Aspose.Drawing 中，`Matrix` 類別封裝了這些操作，讓您能以單一可重複使用的物件操作任何 `GraphicsPath` 或形狀。

## 為什麼在矩陣變換中使用 Aspose.Drawing？

- **Cross‑platform drawing** – 在 Windows、Linux、macOS 上皆可運作，且不受 System.Drawing.Common 限制。  
- **High‑performance rendering** – 為大型影像與複雜向量運算進行最佳化。  
- **Full .NET API coverage** – 與 GDI+ 概念相同，讓遷移變得毫無痛感。

## 先決條件

在開始之前，請確保您具備：

- 基本的 C# 知識。  
- 已安裝 Aspose.Drawing for .NET 的開發環境。若尚未下載，請前往 [here](https://releases.aspose.com/drawing/net/) 取得。  
- 熟悉圖形概念，例如位圖畫布與矩形。

## 匯入命名空間

首先，將所需的命名空間引入作用域：

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

這些命名空間讓您可以存取 `Bitmap`、`Graphics` 以及執行變換所需的 `Matrix` 類別。

## 逐步指南

以下是一個簡潔的編號步驟說明。每一步都包含簡短說明，並附上您需要的完整程式碼（程式碼區塊保持原樣）。

### 步驟 1：設定畫布

建立一個作為繪圖表面的位圖。我們同時以中性灰色背景清除它，使變換後的形狀更為突出。

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **Pro tip:** 使用 `Format32bppPArgb` 可確保在稍後套用抗鋸齒時正確處理 Alpha 通道。

### 步驟 2：定義原始矩形

此矩形是我們將要變換的基礎形狀。其座標選擇使其保持在畫布範圍內。

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### 步驟 3：旋轉矩形（draw rotated rectangle）

現在我們 **apply matrix rotation** 15 度，繞原點旋轉。輔助方法 `TransformPath`（稍後示範）接受一個傳入 `Matrix` 實例的 lambda。

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### 步驟 4：平移矩形

平移會在不改變尺寸或方向的情況下移動形狀。此處我們將其向左上移動 250 像素。

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### 步驟 5：縮放矩形（matrix scaling C#）

縮放會改變矩形的尺寸。`0.3f` 的比例將寬度與高度皆縮減至原始的 30 %。

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### 步驟 6：儲存結果

最後，將變換後的影像寫入磁碟。請調整路徑指向您機器上已存在的資料夾。

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **Note:** `TransformPath` 方法（在上述步驟中使用）會從矩形建立 `GraphicsPath`，套用提供的矩陣，並繪製變換後的形狀。這是一種簡潔的方式，可在每個變換中重複使用相同的繪圖邏輯。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **圖像顯示為空白** | 確保輸出目錄已存在且您具有寫入權限。 |
| **變換看起來偏離中心** | 請記得 `Matrix.Rotate` 會繞原點 (0,0) 旋轉。於旋轉前先將形狀平移至所需的旋轉中心點。 |
| **大型影像的效能延遲** | 僅在需要時使用 `graphics.SmoothingMode = SmoothingMode.AntiAlias;`，並及時釋放 `Graphics` 物件。 |

## 常見問答

**Q: 在哪裡可以找到 Aspose.Drawing 的文件說明？**  
A: 文件可於 [here](https://reference.aspose.com/drawing/net/) 取得。

**Q: 如何取得 Aspose.Drawing 的臨時授權？**  
A: 可於 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 在哪裡可以尋求支援或加入社群？**  
A: 請前往 Aspose.Drawing 論壇 [here](https://forum.aspose.com/c/drawing/44)。

**Q: 可以下載 Aspose.Drawing for .NET 嗎？**  
A: 可以，請從 [this link](https://releases.aspose.com/drawing/net/) 下載。

**Q: 如何購買 Aspose.Drawing？**  
A: 請於 [here](https://purchase.aspose.com/buy) 購買授權。

## 結論

您已完成使用 Aspose.Drawing for .NET 的完整 **matrix transformation tutorial**。您已了解如何 **draw rotated rectangle**、**apply matrix rotation**，以及對任意形狀執行 **matrix scaling C#**。可嘗試串接多個變換或使用自訂旋轉中心，以發掘更多創意圖形效果。

---

**最後更新：** 2026-05-03  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}