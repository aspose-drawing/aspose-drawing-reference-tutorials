---
date: 2025-11-29
description: 學習如何使用 Aspose.Drawing 建立點陣圖、套用全域變換，並將圖形轉換為 PNG。適用於 .NET 開發人員的逐步指南。
linktitle: World Transformation in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 使用 Aspose.Drawing 建立位圖 – 世界變換指南
url: /zh-hant/net/coordinate-transformations/world-transformation/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.Drawing 建立位圖 – 世界變換

## 介紹

歡迎！在本教學中，您將 **create bitmap with Aspose.Drawing** 並探索世界變換，讓您輕鬆平移、旋轉或縮放圖形。無論您需要 **graphics translate example**、想要 **convert graphics to PNG**，或是計畫 **multiple graphics transformations**，本指南都會以清晰、對話式的方式帶您逐步完成。

## 快速解答
- **What does “world transformation” mean?** 它將您的繪圖邏輯（世界）座標映射到頁面（裝置）座標。  
- **Can I export the result as PNG?** 可以 – 繪圖完成後，只需呼叫 `bitmap.Save(...)` 並使用 `.png` 副檔名。  
- **Do I need a license for Aspose.Drawing?** 免費試用版可用於開發；商業授權則需於正式環境使用。  
- **Is this compatible with .NET 6/7?** 完全相容 – Aspose.Drawing 支援 .NET Framework 4.5+ 以及 .NET Core/5/6/7。  
- **How many transformations can I chain?** 您可以依序套用 **multiple graphics transformations**（平移、旋轉、縮放等）。

## 什麼是 Aspose.Drawing 中的世界變換？

世界變換會改變繪圖指令所使用的座標系統。預設情況下，(0,0) 為位圖的左上角。透過 `TranslateTransform`、`RotateTransform` 或 `ScaleTransform`，您可以重新定位原點、旋轉形狀或調整大小，而不必改變原始幾何形狀。

## 為何使用 Graphics Translate 範例？

- **Simplifies positioning** – 在不重新計算每個點的情況下移動物件。  
- **Keeps code clean** – 單一變換呼叫即可取代多次手動座標調整。  
- **Boosts performance** – 圖形引擎在內部處理數學運算，提升效能。  

## 前置條件

在開始之前，請確保您已具備以下項目：

- **Aspose.Drawing library** 已整合至您的 .NET 專案（從官方 [Aspose.Drawing release page](https://releases.aspose.com/drawing/net/) 下載）。  
- 用於儲存輸出影像的 **document directory**。  
- 具備 **C#** 語法的基本認識，以及 Visual Studio 或您偏好的 IDE。  

現在，讓我們深入程式碼！

## 匯入命名空間

首先，匯入所需的命名空間：

```csharp
using System.Drawing;
using Aspose.Drawing;
```

這些讓您可以存取 `Bitmap`、`Graphics` 以及 Aspose 繪圖工具。

## 步驟說明

### 步驟 1：建立位圖

我們先建立一個空白畫布，用於放置繪圖內容。

```csharp
//ExStart: WorldTransformation
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

- **Why 32bppPArgb?** 此像素格式支援 Alpha 透明度與高品質色彩渲染，非常適合 PNG 輸出。  
- **Pro tip:** 調整寬度/高度以符合目標影像尺寸。  

### 步驟 2：設定世界變換（Graphics Translate 範例）

此處將原點移至位圖中心，使繪圖指令相對於該點執行。

```csharp
// Set the transformation that maps world coordinates to page coordinates:
graphics.TranslateTransform(500, 400);
```

- 此操作將 (0,0) 點移至 (500, 400) —— 1000 × 800 畫布的中心。  
- 您可以串接其他變換（例如 `RotateTransform`、`ScaleTransform`）以實現 **multiple graphics transformations**。  

### 步驟 3：使用變換後的座標繪製矩形

現在，任何繪製的形狀都會相對於新原點定位。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawRectangle(pen, 0, 0, 300, 200);
```

- 矩形的左上角起始於變換後的原點（影像中心）。  
- 歡迎嘗試其他形狀——橢圓、線條或自訂路徑。  

### 步驟 4：儲存結果 – Convert Graphics to PNG

最後，將位圖保存為 PNG 檔案。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\WorldTransformation_out.png");
//ExEnd: WorldTransformation
```

- PNG 能保留先前設定的精確色彩與透明度。  
- 將 `"Your Document Directory"` 替換為您機器上的實際路徑。  

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方式 |
|-------|----------------|-----|
| **File not found error** when saving | 目標資料夾不存在。 | 在呼叫 `Save` 前，以程式方式建立資料夾 (`Directory.CreateDirectory`)。 |
| **Blank image** after transformation | `TranslateTransform` 在繪圖之後才被呼叫。 | 確保變換在任何繪圖指令 **之前** 設定。 |
| **Distorted colors** | 使用不相容的像素格式。 | 堅持使用 `Format32bppPArgb` 以獲得 PNG 輸出。 |

## 常見問答

**Q: 我可以套用多於一個變換嗎？**  
A: 可以 – 您可以串接 `TranslateTransform`、`RotateTransform` 與 `ScaleTransform` 以實現複雜效果。

**Q: Aspose.Drawing 在商業專案中免費嗎？**  
A: 提供免費試用供評估使用，但正式環境需購買商業授權。

**Q: 這在 .NET Core 以及 .NET 5/6/7 上可用嗎？**  
A: 完全支援。Aspose.Drawing 支援所有現代 .NET 執行環境。

**Q: 我在哪裡可以找到完整的 API 參考文件？**  
A: 完整文件可於 [here](https://reference.aspose.com/drawing/net/) 取得。

**Q: 如何排除輸出檔案遺失的問題？**  
A: 檢查路徑字串、確認寫入權限，並在呼叫 `Save` 前確保目錄已存在。

## 結論

您現在已學會如何 **create bitmap with Aspose.Drawing**、套用 **world transformation**，以及 **convert graphics to PNG**。掌握這些基礎後，您可以打造更豐富的圖形、產生動態影像，並將精緻的視覺效果整合至任何 .NET 應用程式中。

---

**最後更新：** 2025-11-29  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  
**相關資源：** [Aspose.Drawing API Reference](https://reference.aspose.com/drawing/net/) | [Download Free Trial](https://releases.aspose.com/drawing/net/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}