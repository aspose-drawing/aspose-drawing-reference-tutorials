---
date: 2026-05-29
description: 了解如何在 .NET 中使用 Aspose.Drawing 儲存 PNG 並繪製 cardinal splines。將曲線儲存為 PNG，建立平滑圖形，並輕鬆產生
  bitmap 至檔案。
keywords:
- how to save png
- save bitmap to file
- create smooth curve
- draw curve c#
- generate png graphics
linktitle: 在 Aspose.Drawing 中繪製 Cardinal Splines
schemas:
- author: Aspose
  dateModified: '2026-05-29'
  description: Learn how to save PNG and draw cardinal splines in .NET with Aspose.Drawing.
    Save curve as PNG, create smooth graphics, and generate bitmap to file effortlessly.
  headline: How to Save PNG and Draw Cardinal Splines with Aspose.Drawing
  type: TechArticle
- questions:
  - answer: '`Graphics.DrawCurve` interpolates a series of points into a smooth cardinal
      spline.'
    question: What does the primary method do?
  - answer: PNG via `Bitmap.Save`.
    question: Which format is used to save the image?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license to save images?
  - answer: Yes, overloads of `DrawCurve` let you specify tension.
    question: Can I change the curve tension?
  - answer: Absolutely – it supports .NET Framework and .NET Core/5/6.
    question: Is Aspose.Drawing compatible with .NET 6+?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
title: 如何使用 Aspose.Drawing 儲存 PNG 並繪製 Cardinal Splines
url: /zh-hant/net/lines-curves-and-shapes/draw-cardinal-spline/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing 儲存 PNG 並繪製基數樣條曲線

## 介紹

在本教學中，您將學習如何使用 Aspose.Drawing for .NET 在繪製平滑基數樣條曲線的同時 **儲存 PNG** 檔案。無論您是要建立圖表元件、圖表編輯器，或僅需將自訂曲線匯出為 PNG，以下步驟將指導您建立位圖畫布、使用筆繪製樣條，並將結果保存至磁碟。您還會了解 Aspose.Drawing 為何是 System.Drawing.Common 的可靠跨平台替代方案。

## 快速解答
- **主要方法的功能是什麼？** `Graphics.DrawCurve` 將一系列點插值為平滑的基數樣條曲線。  
- **使用哪種格式儲存影像？** 透過 `Bitmap.Save` 使用 PNG。  
- **儲存影像是否需要授權？** 試用版可用於開發；正式環境需商業授權。  
- **可以調整曲線張力嗎？** 可以，`DrawCurve` 的多載允許您指定張力。  
- **Aspose.Drawing 是否相容於 .NET 6 以上？** 當然相容——支援 .NET Framework 以及 .NET Core/5/6。

## 在 Aspose.Drawing 中「儲存 PNG」是什麼意思？

儲存 PNG 代表將您在記憶體中繪製的位圖轉換為磁碟上的實體 PNG 檔案。此過程使用無損壓縮寫入像素資料，保留精確的顏色與任何 Alpha 通道資訊。Aspose.Drawing 的 `Bitmap.Save` 方法會自動處理 PNG 編碼，您無需自行管理格式細節。

## 為什麼要使用 Aspose.Drawing 繪製基數樣條曲線？

基數樣條曲線會產生平滑、流暢的曲線，緊貼一組控制點，非常適合用於資料視覺化、使用者介面圖形與自訂形狀。Aspose.Drawing 支援 **30 多種影像格式**，且能在不將整個檔案載入記憶體的情況下渲染數百頁的圖形，為您提供速度與彈性。

## 前置條件

- 已安裝 Visual Studio（任何近期版本）。  
- Aspose.Drawing for .NET 函式庫。您可以在[此處](https://releases.aspose.com/drawing/net/)下載。  
- 具備基本的 C# 程式設計知識。

## 匯入命名空間

在您的 C# 檔案中，首先匯入必要的命名空間：

`Aspose.Drawing` 命名空間包含所有核心類型，例如 `Bitmap`、`Graphics` 與 `Pen`。  
```csharp
using Aspose.Drawing;
```
```csharp
using System.Drawing;
```

## 步驟 1：建立位圖（畫布）

首先，建立一個位圖作為繪圖的畫布。此位圖是樣條曲線在您 **儲存影像** 前渲染的地方。

Bitmap 代表具有特定像素格式與尺寸的記憶體內圖像。  
```csharp
int width = 800;
int height = 600;
Bitmap bitmap = new Bitmap(width, height, PixelFormat.Format32bppPArgb);
```
```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 2：建立 Graphics 物件

接著，從位圖取得 `Graphics` 物件。此物件提供繪圖表面。

Graphics 為在位圖上渲染形狀、文字與影像提供繪圖表面。  
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.Transparent);
```
```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 3：定義 Pen 並繪製曲線

使用所需的顏色與寬度定義 `Pen`，然後使用 `DrawCurve` 繪製基數樣條曲線。此示範 **使用 Pen 繪製曲線** 的技巧，亦作為 **基數樣條範例**。

Pen 封裝了繪製線條與曲線時使用的顏色、寬度與線條樣式。  
```csharp
Pen pen = new Pen(Color.Blue, 3);
PointF[] points = {
    new PointF(100, 400), new PointF(200, 100),
    new PointF(300, 300), new PointF(400, 150),
    new PointF(500, 350)
};
graphics.DrawCurve(pen, points, 0.5f); // tension = 0.5
```
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

## 步驟 4：儲存影像（將曲線儲存為 PNG）

最後，將位圖持久化為 PNG 檔案。這就是本教學中 **儲存 PNG** 的核心。

Bitmap.Save 會將影像寫入指定格式的檔案，例如 PNG。  
```csharp
string outputPath = Path.Combine(Environment.CurrentDirectory, "cardinal-spline.png");
bitmap.Save(outputPath, ImageFormat.Png);
```
```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawCardinalSpline_out.png");
```

> **專業提示：** 使用 `Path.Combine` 在跨平台時安全地組合檔案路徑。

恭喜！您已成功使用 Aspose.Drawing for .NET 繪製基數樣條曲線並將結果儲存為 PNG 影像。**隨意** 嘗試不同的點陣列、Pen 顏色或線寬，**自訂您的曲線**。

## 常見使用情境

- **資料視覺化** – 需要精確控制點的平滑折線圖。  
- **自訂 UI 元件** – 繪製旋鈕、滑桿或裝飾性邊框。  
- **可匯出圖形** – 即時產生 PNG 資產供報告或網頁內容使用。

## 疑難排解與技巧

- **影像顯示空白？** 確認位圖的像素格式支援 alpha（`Format32bppPArgb`），且必要時呼叫 `graphics.Clear(Color.Transparent)`。  
- **曲線形狀不如預期？** 使用多載 `DrawCurve(pen, points, tension)` 調整張力參數。  
- **檔案存取錯誤？** 確認目標目錄存在且您的應用程式具備寫入權限。

## 常見問題

**Q1：我可以在商業專案中使用 Aspose.Drawing 嗎？**  
A1：可以，Aspose.Drawing 適用於個人與商業專案。請於[購買頁面](https://purchase.aspose.com/buy)查看授權細節。

**Q2：如何取得測試用的臨時授權？**  
A2：可於[此處](https://purchase.aspose.com/temporary-license/)取得測試用臨時授權。

**Q3：在哪裡可以取得其他支援？**  
A3：請前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44)取得社群支援與討論。

**Q4：是否提供免費試用？**  
A4：是的，您可在購買前使用[免費試用](https://releases.aspose.com/)版探索功能。

**Q5：如何取得文件說明？**  
A5：請參考完整的[文件說明](https://reference.aspose.com/drawing/net/)以取得詳細資訊與範例。

---

**最後更新：** 2026-05-29  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [將位圖儲存為 PNG 並使用 Aspose.Drawing 繪製封閉曲線](/drawing/net/lines-curves-and-shapes/draw-closed-curve/)
- [C# 儲存位圖 – 使用 Aspose.Drawing 繪製貝塞爾樣條](/drawing/net/lines-curves-and-shapes/draw-bezier-spline/)
- [使用實心筆刷在 Aspose.Drawing 中將位圖儲存為 PNG](/drawing/net/lines-curves-and-shapes/solid-brushes/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}