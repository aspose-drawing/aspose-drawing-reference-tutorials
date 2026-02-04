---
date: 2026-02-04
description: 學習如何使用 Aspose.Drawing .NET 在 C# 中旋轉矩形，內容包括繪製旋轉矩形、C# 矩陣運算以及圖形矩陣教學。
linktitle: Matrix Transformations in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 旋轉矩形 C# – Aspose.Drawing for .NET 中的矩陣變換教學
url: /zh-hant/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Matrix Transformation 教學：Aspose.Drawing for .NET 中的矩陣變換

## 介紹

歡迎閱讀 Aspose.Drawing .NET 的 **矩陣變換教學**！本指南將教您如何 **rotate rectangle c#**、繪製旋轉的矩形形.Drawing API 執行矩、產生動態報表，或只是想玩幾何效果，掌握矩陣變換即可在幾行程式碼內建立精確且可重複使用的視覺變換。

## 快速回答
- **本教學涵蓋什麼內容？** 在 Aspose.Drawing 中對矩形執行旋轉、平移與縮放的矩陣變換。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買商業授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。  
- **實作大約需要多久？** 基本範例約 10‑15 分鐘即可完成。  
- **可以看到輸出圖檔嗎？** 可以——教學會儲存 PNG，直接開啟檢視。

## 什麼是矩陣變換教學？

矩陣變換教學說明如何使用 3 移、旋切圖形基元。於 Aspose` 或形進行矩陣變換？

- **跨平台相容性** – 可在 Windows、Linux、macOS 上執行，且不受 System.Drawing.Common 限制。  
- **高效能渲染** – 為大型影像與複雜向量運算進行最佳化。  
- **完整 .NET API 支援** – 與 GDI+ 概念相同，遷移毫無障礙。

## 前置條件

在開始之前，請確保您已具備：

- 基本的 C# 知識。  
- 已安裝 Aspose.Drawing for .NET 的開發環境。若尚未下載，請前往 [here](https://releases.aspose.com/drawing/net/) 取得。  
- 了解圖形概念，如位圖畫布與矩形。

## 匯入命名空間

首先，將所需的命名空間引入：

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

這些命名空間讓您可以使用 `Bitmap`、`Graphics` 與 `Matrix` 類別來執行變換。

## 如何使用 Aspose.Drawing 進行 rotate rectangle c#

以下提供逐步說明，示範如何 **rotate rectangle c#**、平移與縮放。每一步皆使用相同的輔助方法 `TransformPath`，讓您專注於矩陣邏輯，而不必重複繪圖程式碼。

### 步驟 1：設定畫布

建立一個位圖作為繪圖表面，並以中性灰色背景清除，讓變換後的圖形更為突出。

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **小技巧：** 使用 `Format32bppPArgb` 可確保在之後套用抗鋸齒時正確處理 Alpha 通道。

### 步驟 2：定義原始矩形

此矩形為我們將要變換的基礎形狀，座標設計在畫布內部留有足夠空間。

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### 步驟 3：旋轉矩形（draw rotated rectangle）

現在 **apply matrix rotation** 15 度，繞原點旋轉。輔助方法 `TransformPath`（稍後示範）接受一個 lambda，傳入 `Matrix` 實例。

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### 步驟 4：平移矩形

平移會在不改變大小或方向的前提下移動形狀。此處將其向左上方移動 250 像素。

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### 步驟 5：縮放矩形（matrix scaling C#）

縮放會改變矩形的尺寸。`0.3f` 的因子將寬高皆縮小至原始的 30 %。

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### 步驟 6：儲存結果

最後，將變換後的影像寫入磁碟。請自行調整路徑，以指向您機器上已存在的資料夾。

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **注意：** 上述步驟中使用的 `TransformPath` 方法會從矩形建立 `GraphicsPath`，套用傳入的矩陣，並繪製變換後的形狀。此方式可在每個變換中重複使用相同的繪圖邏輯，保持程式碼簡潔。

## 常見問題與解決方案

| 問題 | 解決方案 |
|------|----------|
| **影像顯示為空白** |入權換結果偏離中心**繞原點 (欲旋轉的樞紐點。 |
| **大型影像效能下降** | 僅在需要時使用 `釋放 `Graphics` 物件。 |

## 常見問答

**Q: 在哪裡可以找到 Aspose.Drawing 的文件？**  
A: 文件可於 [here](https://reference.aspose.com/drawing/net/) 取得。

**Q: 如何取得 Aspose.Drawing 的臨時授權？**  
A: 請前往 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 我可以在哪裡尋求支援或加入社群？**  
A: 請造訪 Aspose.Drawing 論壇 [here](https://forum.aspose.com/c/drawing/44)。

**Q: 可以下載 Aspose.Drawing for .NET 嗎？**  
A: 可以，請從 [this link](https://releases.aspose.com/drawing/net/) 下載。

**Q: 如何購買 Aspose.Drawing？**  
A: 請至 [here](https://purchase.aspose.com/buy) 購買授權。

## 結論

您已完成使用 Aspose.Drawing for .NET 的完整 **矩陣變換教學**。現在您知道如何 **draw rotated rectangle**、**apply matrix rotation**，以及在任意形狀上執行 **matrix scaling C#**。可嘗試串接多重變換或使用自訂樞紐點，開發出更具創意的圖形效果。

---

**最後更新：** 2026-02-04  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}