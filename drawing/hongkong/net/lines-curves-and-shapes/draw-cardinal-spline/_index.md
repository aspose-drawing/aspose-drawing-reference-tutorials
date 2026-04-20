---
date: 2026-02-12
description: 學習如何在 .NET 使用 Aspose.Drawing 儲存圖像並繪製 Cardinal 樣條曲線。將曲線儲存為 PNG，輕鬆打造平滑圖形。
linktitle: Drawing Cardinal Splines in Aspose.Drawing
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何在 Aspose.Drawing 中儲存圖像並繪製 Cardinal 樣條曲線
url: /zh-hant/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing 中儲存圖像與繪製 Cardinal 曲線

## 簡介

在本教學中，您將學習如何在使用 Aspose.Drawing for .NET 繪製平滑的 Cardinal 曲線時 **儲存影像** 檔案。無論您是在構建圖表元件、圖表編輯器，或僅需將自訂曲線匯出為 PNG，以下步驟將向您展示如何使用筆刷繪製曲線、客製化曲線，並將結果保存至磁碟。

## 快速解答
- **主要方法的功能是什麼？** `Graphics.DrawCurve` 會將一系列點插值為平滑的 Cardinal 曲線。  
- **使用哪種格式儲存影像？** 透過 `Bitmap.Save` 以 PNG 格式。  
- **儲存影像是否需要授權？** 開發階段可使用試用版；正式環境需購買商業授權。  
- **可以調整曲線張力嗎？** 可以，`DrawCurve` 的多載允許您指定張力。  
- **Aspose.Drawing 是否相容於 .NET 6 以上？** 完全相容——支援 .NET Framework 以及 .NET Core/5/6。

## 在 Aspose.Drawing 中「如何儲存影像」是什麼意思？

儲存影像是指將您在記憶體中繪製的位圖轉換為實體檔案（如 PNG、JPEG 或 BMP）。Aspose.Drawing 提供簡單的 `Bitmap.Save` 方法，為您處理編碼。

## 為什麼要使用 Aspose.Drawing 繪製 Cardinal 曲線？

Cardinal 曲線能產生平滑、流暢的曲線，貼近一組控制點，非常適合資料視覺化、使用者介面圖形及自訂形狀。使用 Aspose.Drawing 可避免 `System.Drawing.Common` 的限制，並獲得跨平台的一致性。

## 先決條件

- 已安裝 Visual Studio（任何較新版）。  
- Aspose.Drawing for .NET 程式庫。您可於[此處](https://releases.aspose.com/drawing/net/)下載。  
- 基本的 C# 程式設計知識。

## 匯入命名空間

在您的 C# 檔案中，首先匯入必要的命名空間：

```csharp
using System.Drawing;
```

## 步驟 1：建立 Bitmap（畫布）

首先，建立一個作為繪圖畫布的 bitmap。此 bitmap 會在您 **儲存影像** 之前渲染曲線。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 2：建立 Graphics 物件

接著，從 bitmap 取得 `Graphics` 物件。此物件提供繪圖表面。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 3：定義 Pen 並繪製曲線

使用所需的顏色與寬度定義 `Pen`，然後使用 `DrawCurve` 繪製 Cardinal 曲線。此範例示範 **使用 Pen 繪製曲線** 的技巧，亦作為 **Cardinal 曲線範例**。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
graphics.DrawCurve(pen, new Point[] {
    new Point(10, 700),
    new Point(250, 500),
    new Point(500, 10),
    new Point(750, 500),
    new Point(990, 700)
});
```

## 步驟 4：儲存影像（將曲線另存為 PNG）

最後，將 bitmap 持久化為 PNG 檔案。這即是本教學中 **如何儲存影像** 的核心。

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **專業提示：** 使用 `Path.Combine` 可在跨平台環境中安全組合檔案路徑。

恭喜！您已成功使用 Aspose.Drawing for .NET 繪製 Cardinal 曲線並將結果儲存為 PNG 影像。隨時嘗試不同的點陣列、Pen 顏色或線寬，以客製化您的曲線。

## 常見使用情境

- **資料視覺化** – 需要精確控制點的平滑折線圖。  
- **自訂 UI 元件** – 繪製旋鈕、滑桿或裝飾性邊框。  
- **可匯出圖形** – 即時產生 PNG 資產供報告或網頁內容使用。

## 故障排除與技巧

- **影像顯示空白？** 確認 bitmap 的像素格式支援 Alpha（`Format32bppPArgb`），並在需要時呼叫 `graphics.Clear(Color.Transparent)`。  
- **曲線形狀不如預期？** 使用多載 `DrawCurve(pen, points, tension)` 調整張力參數。  
- **檔案存取錯誤？** 確認目標目錄存在且應用程式具有寫入權限。

## 常見問題

### Q1：我可以在商業專案中使用 Aspose.Drawing 嗎？

A1：可以，Aspose.Drawing 適用於個人與商業專案。請於[購買頁面](https://purchase.aspose.com/buy)查看授權細節。

### Q2：如何取得測試用的臨時授權？

A2：可於[此處](https://purchase.aspose.com/temporary-license/)取得測試用臨時授權。

### Q3：在哪裡可以取得額外支援？

A3：請前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 獲取社群支援與討論。

### Q4：是否提供免費試用？

A4：有的，您可在購買前使用[免費試用](https://releases.aspose.com/)版體驗功能。

### Q5：如何取得文件說明？

A5：請參考完整的[文件說明](https://reference.aspose.com/drawing/net/)，內含詳細資訊與範例。

### Q6：我可以將輸出格式改為 JPEG 嗎？

A6：當然可以。將 `.png` 副檔名改為 `.jpg`，並在 `Save` 方法中指定 `ImageFormat.Jpeg`。

### Q7：能否在同一 bitmap 上繪製多條曲線？

A7：可以，只要使用不同的點陣列與 Pen，多次呼叫 `graphics.DrawCurve` 即可。

## 結論

本指南說明了在繪製 Cardinal 曲線後 **如何儲存影像** 檔案，示範了實用的 **使用 C# 繪製曲線** 方法，並強調此技術在常見情境中的優勢。您現在已具備將平滑曲線圖形整合至任何 .NET 應用程式的堅實基礎。

---

**最後更新：** 2026-02-12  
**測試版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}