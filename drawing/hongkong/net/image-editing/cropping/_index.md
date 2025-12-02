---
date: 2025-12-02
description: 學習如何使用 Aspose.Drawing 在 .NET 中裁剪圖像。此圖像裁剪教學逐步說明如何儲存裁剪後的圖像、操作位圖以及處理批次圖像裁剪。
language: zh-hant
linktitle: How to Crop Image .NET Using Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何在 .NET 中使用 Aspose.Drawing 裁剪圖像
url: /net/image-editing/cropping/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing 在 .NET 中裁剪圖像

## 簡介

如果您正在開發需要精確圖像處理的 .NET 應用程式，學習 **如何裁剪圖像** 檔案是必備技能。Aspose.Drawing 提供功能豐富、全託管的 API，讓您在 **crop image .net** 專案中不必依賴舊版的 System.Drawing.Common 函式庫。本教學示範完整的端對端範例，說明如何載入位圖、定義裁剪區域、執行裁剪，最後 **儲存裁剪後的圖像**。完成後，您即可將圖像裁剪整合至任何 .NET 解決方案——無論是單張圖片或 **批次圖像裁剪** 工作流程。

## 快速回答
- **應該使用哪個函式庫？** Aspose.Drawing for .NET  
- **可以裁剪任何圖像格式嗎？** 可以——支援大多數常見格式（PNG、JPEG、BMP 等）。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式上線需購買授權。  
- **支援批次處理嗎？** 完全支援——可將相同程式碼迴圈套用於多個檔案。  
- **支援哪些 .NET 版本？** .NET Framework 4.6 以上、.NET Core 3.1 以上、.NET 5/6/7。

## 什麼是「crop image .net」？

裁剪圖像是指從較大的圖片中擷取矩形區域。在 .NET 中，這項操作通常在 `Bitmap` 物件上執行。Aspose.Drawing 透過高效能的圖形基元，讓此流程在各平台上保持一致且簡便。

## 為什麼使用 Aspose.Drawing 進行圖像裁剪？

- **跨平台可靠性** – 無需本機相依，支援 Windows、Linux 與 macOS。  
- **豐富的像素格式支援** – 處理 32‑bit ARGB、PArgb 等多種格式。  
- **效能優化** – 為大尺寸圖像優化繪製與插值。  
- **無縫整合** – 可與其他 Aspose 產品（PDF、Slides 等）協同使用。

## 先決條件

在開始之前，請確保您已具備：

- **Aspose.Drawing 函式庫** – 在專案中加入 NuGet 套件 `Aspose.Drawing`，或從[官方網站](https://releases.aspose.com/drawing/net/)下載。  
- **圖像資料夾** – 放置欲裁剪的來源圖像。請將程式碼片段中的 `"Your Document Directory"` 替換為您機器上的實際路徑。

## 匯入命名空間

首先，匯入包含繪圖類別的命名空間：

```csharp
using System.Drawing;
```

這樣即可使用 `Bitmap`、`Graphics`、`Rectangle` 等必要型別。

## 逐步指南

### 步驟 1：建立 Bitmap 畫布（crop image bitmap）

我們先建立一個空白的 bitmap，用來存放裁剪後的結果。請依照欲擷取區域的寬、高與像素格式進行調整。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

> **提示：** `Format32bppPArgb` 格式可保留 alpha 透明度，並提供高品質的渲染效果。

### 步驟 2：建立 Graphics 物件

`Graphics` 物件讓我們可以在 bitmap 畫布上繪圖。設定 `InterpolationMode` 會影響裁剪時的重新取樣方式。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.InterpolationMode = InterpolationMode.NearestNeighbor;
```

> **專業提示：** 若要在縮放圖像時取得更平滑的結果，可考慮使用 `InterpolationMode.HighQualityBicubic`。

### 步驟 3：載入來源圖像

載入欲裁剪的圖像。路徑會將文件目錄與檔名組合起來。

```csharp
Bitmap image = new Bitmap("Your Document Directory" + @"Images\aspose_logo.png");
```

> **注意：** Aspose.Drawing 能直接讀取 PNG、JPEG、BMP、GIF、TIFF 等多種格式。

### 步驟 4：定義來源與目標矩形

`sourceRectangle` 用來選取原圖中要保留的區塊。此處我們取左上角 50 × 40 像素的區域。`destinationRectangle` 則告訴圖形引擎在新 bitmap 上放置裁剪區塊的位置。

```csharp
Rectangle sourceRectangle = new Rectangle(0, 0, 50, 40);
Rectangle destinationRectangle = sourceRectangle;
```

> **為什麼需要兩個矩形？** 使用相同的矩形即可完成簡單裁剪。若改變 `destinationRectangle`，則可重新定位或縮放裁剪後的圖像。

### 步驟 5：執行裁剪操作

`DrawImage` 方法會將來源圖像中選取的區域複製到目標 bitmap。

```csharp
graphics.DrawImage(image, destinationRectangle, sourceRectangle, GraphicsUnit.Pixel);
```

> **常見陷阱：** 忘記釋放 `Graphics` 會導致 bitmap 檔案被鎖定。結束方法時會自動處理釋放。

### 步驟 6：儲存裁剪後的圖像（save cropped image）

最後，將結果寫入磁碟。請依需求變更檔名與路徑。

```csharp
bitmap.Save("Your Document Directory" + @"Images\Cropping_out.png");
```

> **結果：** 您現在得到一個只包含指定 50 × 40 像素區域的 PNG 檔案。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **輸出檔案為空白** | `sourceRectangle` 超出圖像範圍 | 檢查 `sourceRectangle` 的座標與尺寸是否正確。 |
| **記憶體不足例外** | 圖像過大 | 分段處理圖像或使用 `using` 陳述式即時釋放資源。 |
| **顏色不正確** | 像素格式不匹配 | 使來源 bitmap 的像素格式相同，或使用 `Bitmap.Clone` 進行轉換。 |

## 常見問題

**Q: 可以使用 Aspose.Drawing 裁剪任何格式的圖像嗎？**  
A: 可以，Aspose.Drawing 支援 PNG、JPEG、BMP、GIF、TIFF 等多種格式，讓您 **how to crop image** 檔案時不受原始類型限制。

**Q: 有進階的裁剪選項嗎？**  
A: 當然。您可以結合 `GraphicsPath` 進行非矩形裁剪、套用旋轉，或使用 `ImageAttributes` 調整顏色。

**Q: 能對同一張圖像執行多次裁剪嗎？**  
A: 可以——只要重複呼叫 `DrawImage` 並提供不同的來源矩形，或在迴圈中串接多個操作即可完成複雜轉換。

**Q: Aspose.Drawing 適合批次圖像裁剪嗎？**  
A: 完全適合。將上述步驟包在 `foreach` 迴圈中，對一系列檔案路徑進行處理，即可自動批次處理數十或數百張圖像。

**Q: 如何取得 Aspose.Drawing 相關問題的支援？**  
A: 前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/diagram/17) 提問、分享程式碼，並向社群與產品工程師尋求協助。

## 結論

本教學示範了使用 Aspose.Drawing 完整的 **crop image .net** 工作流程。您已掌握 **how to crop image** 檔案的技巧、如何精確定義來源矩形，以及 **save cropped image** 的方法。憑藉這些基礎，您可以擴充程式碼以支援 **batch image cropping**、自訂轉換，或將此邏輯整合至更大型的圖像處理管線中。

---  

**最後更新：** 2025-12-02  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}