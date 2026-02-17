---
date: 2026-02-17
description: 學習如何在 .NET 使用 Aspose.Drawing 繪製矩形。本分步指南將向您展示如何建立位圖圖像、在位圖上繪製矩形，以及儲存繪製後的圖像。
linktitle: Drawing Rectangles in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing for .NET 繪製矩形
url: /zh-hant/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing for .NET 繪製矩形

## 介紹

在本教學中，您將學會 **如何在 .NET 應用程式中使用 Aspose.Drawing 套件繪製矩形**。無論是為 UI 元素產生簡單的矩形，或是為報表建立複雜的圖形，以下步驟將帶您完成建立位圖、設定 Graphics 物件、在位圖上繪製矩形，最後將繪製好的圖像儲存至磁碟的全過程。

## 快速回答
- **需要哪個套件？** Aspose.Drawing for .NET  
- **哪個方法負責繪製圖形？** `Graphics.DrawRectangle`  
- **需要授權嗎？** 試用版免費；正式環境需購買商業授權。  
- **可以調整矩形大小嗎？** 可以 – 調整寬度、高度與位置參數即可。  
- **程式碼支援 .NET 6+ 嗎？** 完全支援，Aspose.Drawing 相容於現代 .NET 版本。

## 在 Aspose.Drawing 中「繪製矩形」是什麼意思？
使用 Aspose.Drawing 繪製矩形即是透過 `Graphics` 類別在位圖畫布上繪製矩形輪廓（或填滿形狀）。此方式讓您能完整掌控尺寸、顏色、線條粗細與圖像格式，非常適合即時產生圖形。

## 為什麼選擇 Aspose.Drawing 來建立矩形？
- **跨平台支援** – 可在 Windows、Linux 與 macOS 上執行。  
- **無 GDI+ 依賴** – 避免 `System.Drawing.Common` 的限制。  
- **功能豐富** – 進階繪圖、抗鋸齒與高品質輸出格式。  
- **授權簡便** – 提供試用版，升級至商業授權亦相當順暢。

## 前置條件

在開始撰寫程式碼前，請確保您已具備以下項目：

- Aspose.Drawing 套件：請確定已安裝 Aspose.Drawing for .NET。您可以在此處下載 [here](https://releases.aspose.com/drawing/net/)。  
- 開發環境：在您的機器上配置好可使用的 .NET 開發環境，例如 Visual Studio。  
- 基本 .NET 知識：熟悉 .NET 程式設計的基礎概念。

## 匯入命名空間

先在專案中匯入必要的命名空間，這些命名空間是操作圖形與繪製所必需的：

```csharp
using System.Drawing;
```

## 步驟 1：建立位圖影像

首先，建立一個 `Bitmap` 物件作為繪圖表面。此位圖將用來 **產生矩形圖像** 的內容。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 2：建立 Graphics 物件

接著，從位圖取得 `Graphics` 物件。Graphics 物件是讓您 **建立圖形物件**（如繪製形狀、線條與文字）的引擎。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 3：為矩形定義 Pen

定義一個 `Pen` 物件，以指定矩形輪廓的顏色與粗細。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## 步驟 4：在位圖上繪製矩形

現在，使用 `Graphics` 物件 **在位圖上繪製矩形**。依需求調整 X、Y、寬度與高度的數值。

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## 步驟 5：儲存繪製好的影像

最後，將位圖寫入檔案，以便檢視結果。此步驟示範 **儲存繪製影像** 的功能。

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

恭喜！您已成功使用 Aspose.Drawing for .NET 完成 **繪製矩形** 的操作。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| 產生空白影像 | 位圖未釋放或 Graphics 未刷新 | 在儲存前呼叫 `graphics.Dispose();`，或使用 `using` 區塊。 |
| 邊緣品質低 | 預設平滑模式 | 設定 `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`。 |
| 檔案路徑錯誤 | 目錄不存在 | 確認目標資料夾已建立，或使用 `Path.Combine` 產生安全路徑。 |

## 常見問答

**Q: 可以用單色填滿矩形嗎？**  
A: 可以，建立 `SolidBrush` 後呼叫 `graphics.FillRectangle(brush, …)`，可在繪製輪廓前或後執行。

**Q: 如何一次繪製多個矩形？**  
A: 迭代 `Rectangle` 結構集合，對每個項目呼叫 `DrawRectangle`。

**Q: 有辦法旋轉矩形嗎？**  
A: 在繪製前使用 `graphics.RotateTransform(angle)`，繪製完畢後再重設變換。

**Q: 支援哪些影像格式儲存？**  
A: 透過對應的 `ImageFormat` 參數，可支援 PNG、JPEG、BMP、GIF 與 TIFF。

**Q: Aspose.Drawing 能在 .NET Core 上執行嗎？**  
A: 能，該套件完整相容於 .NET Core、.NET 5、.NET 6 以及更高版本。

## 其他資源

若您在使用過程中遇到問題或有任何疑問，歡迎前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 取得協助。

### 常見問答

#### Q1: 可以免費使用 Aspose.Drawing 嗎？

A1: Aspose.Drawing 為商業套件，但您可透過 [免費試用](https://releases.aspose.com/) 先行體驗功能。

#### Q2: 哪裡可以找到詳細文件？

A2: 請參考 [文件說明](https://reference.aspose.com/drawing/net/) 取得深入資訊。

#### Q3: 如何取得臨時授權？

A3: 前往取得 [臨時授權](https://purchase.aspose.com/temporary-license/) 以供測試使用。

#### Q4: Aspose.Drawing 適合用於複雜圖形任務嗎？

A4: 絕對適合！Aspose.Drawing 提供先進功能，能處理複雜的圖形操作。

#### Q5: 哪裡可以購買 Aspose.Drawing？

A5: 前往 [此處](https://purchase.aspose.com/buy) 購買授權。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-02-17  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

---