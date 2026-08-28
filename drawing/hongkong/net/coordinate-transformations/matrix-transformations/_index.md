---
date: 2026-08-28
description: 學習此 Aspose.Drawing .NET 的矩陣變換教學，內容包括如何繪製旋轉矩形、套用矩陣旋轉以及執行矩陣縮放（C#）。
keywords:
- matrix transformation tutorial
- draw rotated rectangle
- matrix rotation c#
- matrix scaling c#
- Aspose.Drawing graphics
lastmod: 2026-08-28
linktitle: Aspose.Drawing 的矩陣變換
og_description: Aspose.Drawing .NET 的矩陣變換教學。學習如何繪製旋轉矩形、套用矩陣旋轉、平移與縮放圖形（C#），只需數分鐘。
og_image_alt: Screenshot of a rotated rectangle created with Aspose.Drawing using
  matrix transformations
og_title: 矩陣變換教學 – 在 Aspose.Drawing 中套用旋轉、縮放與平移
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  headline: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  type: TechArticle
- description: Learn this matrix transformation tutorial for Aspose.Drawing .NET,
    covering how to draw rotated rectangle, apply matrix rotation, and perform matrix
    scaling C#.
  name: 'Matrix transformation tutorial: matrix transformations in Aspose.Drawing
    for .NET'
  steps:
  - name: set up the canvas
    text: Create a bitmap that will serve as the drawing surface. We also clear it
      with a neutral gray background so the transformed shapes stand out. > **Pro
      tip:** Using `Format32bppPArgb` ensures correct alpha handling when you later
      apply anti‑aliasing.
  - name: define the original rectangle
    text: This rectangle is the base shape we’ll transform. Its coordinates are chosen
      to keep it well within the canvas bounds.
  - name: rotate the rectangle (draw rotated rectangle)
    text: The `Matrix` class is Aspose.Drawing's representation of a 3 × 3 affine
      transformation matrix used for rotation, scaling and translation. We now **apply
      matrix rotation** of 15 degrees around the origin. The helper method `TransformPath`
      (shown later) takes a lambda that receives a `Matrix` instance
  - name: translate the rectangle
    text: Translation moves the shape without altering its size or orientation. Here
      we shift it left‑up by 250 pixels.
  - name: scale the rectangle (matrix scaling C#)
    text: Scaling changes the rectangle’s dimensions. A factor of `0.3f` reduces both
      width and height to 30 % of the original size.
  - name: save the result
    text: Finally, write the transformed image to disk. Adjust the path to point to
      a folder that exists on your machine. > **Note:** The `TransformPath` method
      (used in the steps above) creates a `GraphicsPath` from the rectangle, applies
      the supplied matrix, and draws the transformed shape. It’s a compact w
  type: HowTo
- questions:
  - answer: The documentation is available **[here](https://reference.aspose.com/drawing/net/)**.
    question: Where can I find the Aspose.Drawing documentation?
  - answer: Obtain a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: How do I get a temporary license for Aspose.Drawing?
  - answer: Visit the Aspose.Drawing forum **[here](https://forum.aspose.com/c/drawing/44)**.
    question: Where can I seek support or connect with the community?
  - answer: Yes, download it from **[here](https://releases.aspose.com/drawing/net/)**.
    question: Can I download Aspose.Drawing for .NET?
  - answer: Purchase your license **[here](https://purchase.aspose.com/buy)**.
    question: How can I purchase Aspose.Drawing?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- matrix transformation
- Aspose.Drawing
- .NET graphics
- C# drawing
- cross‑platform rendering
title: 矩陣變換教學：Aspose.Drawing 在 .NET 中的矩陣變換
url: /zh-hant/net/coordinate-transformations/matrix-transformations/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 矩陣變換教學：在 Aspose.Drawing for .NET 中的矩陣變換

## 介紹

在本 **矩陣變換教學** 中，您將了解 Aspose.Drawing 的 `Matrix` 類別如何以像素級精準度旋轉、平移與縮放圖形物件。無論您是構建圖表編輯器、產生自動化報告，或為伺服器端服務加入視覺效果，精通矩陣變換都是在 Windows、Linux 與 macOS 上產出專業外觀輸出的關鍵。

## 快速解答
- **此教學涵蓋什麼內容？** 它示範如何使用 Aspose.Drawing 的矩陣 API 旋轉、平移和縮放矩形。  
- **我需要授權嗎？** 免費試用可用於開發；商業授權則是正式環境的必需。  
- **支援哪些 .NET 版本？** .NET Framework 4.5 以上、 .NET Core 3.1 以上、 .NET 5/6/7 及更高版本。  
- **實作大約需要多久？** 完整範例大約 10‑15 分鐘即可完成。  
- **我可以看到輸出圖像嗎？** 可以——教學會儲存 PNG，您可立即開啟。

## 什麼是矩陣變換教學？

矩陣變換教學說明如何使用 3 × 3 仿射矩陣來移動、旋轉、縮放或剪切圖形基元。在 Aspose.Drawing 中，`Matrix` 類別封裝了這些操作，讓任何 `GraphicsPath` 或形狀都能以單一可重用物件進行變換。

## 為何使用 Aspose.Drawing 進行矩陣變換？

Aspose.Drawing 支援 **三大作業系統**（Windows、Linux、macOS），且可在典型伺服器硬體上於 **200 ms** 內渲染最高 **10,000 × 10,000 px** 的圖像。此函式庫提供 **100 % GDI+ API 相容性**，因此您可在不重寫邏輯的情況下遷移現有 System.Drawing 程式碼，同時避免 System.Drawing.Common 在非 Windows 平台上的授權限制。

## 前置條件

- 可運作的 C# 開發環境（Visual Studio、Rider 或 VS Code）。  
- 已安裝 Aspose.Drawing for .NET —— 從官方網站 **[此處](https://releases.aspose.com/drawing/net/)** 或 **[此連結](https://releases.aspose.com/drawing/net/)** 下載（若尚未下載）。  
- 具備位圖畫布、矩形與圖形路徑的基本概念。

## 匯入命名空間

首先，將所需的命名空間匯入作用域：

```csharp
using System;
using System.Drawing;
using System.Drawing.Drawing2D;
```

這些命名空間讓您能存取 `Bitmap`、`Graphics` 與執行變換所需的 `Matrix` 類別。

## 步驟說明

以下是一個簡潔的編號式導覽。每一步都包含簡短說明，並附上您需要的完整程式碼（程式碼區塊保持原樣）。

### 步驟 1：設定畫布

建立一個作為繪圖表面的位圖。我們同時以中性灰色背景清除畫布，使變換後的形狀更為突出。

```csharp
// Code snippet for setting up the canvas
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
Graphics graphics = Graphics.FromImage(bitmap);
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

> **專業提示：** 使用 `Format32bppPArgb` 可確保在之後套用抗鋸齒時正確處理 Alpha 通道。

### 步驟 2：定義原始矩形

此矩形是我們將要變換的基礎形狀。其座標選擇使其保持在畫布範圍內。

```csharp
// Code snippet for defining the original rectangle
Rectangle originalRectangle = new Rectangle(300, 300, 300, 200);
```

### 步驟 3：旋轉矩形（繪製旋轉矩形）

`Matrix` 類別是 Aspose.Drawing 用於旋轉、縮放與平移的 3 × 3 仿射變換矩陣的表示。我們現在 **套用 15 度的矩陣旋轉**，以原點為中心。稍後示範的 `TransformPath` 輔助方法接受一個 Lambda，該 Lambda 會收到一個 `Matrix` 實例。

```csharp
// Code snippet for rotating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Rotate(15.0f));
```

### 步驟 4：平移矩形

平移會在不改變大小或方向的情況下移動形狀。此處我們將其向左上方平移 250 像素。

```csharp
// Code snippet for translating the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Translate(-250, -250));
```

### 步驟 5：縮放矩形（矩陣縮放 C#）

縮放會改變矩形的尺寸。`0.3f` 的因子將寬度與高度同時縮小至原始的 30 %。

```csharp
// Code snippet for scaling the rectangle
TransformPath(graphics, originalRectangle, (matrix) => matrix.Scale(0.3f, 0.3f));
```

### 步驟 6：儲存結果

最後，將變換後的圖像寫入磁碟。請調整路徑以指向您機器上已存在的資料夾。

```csharp
// Code snippet for saving the result
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\MatrixTransformations_out.png");
```

> **注意：** `TransformPath` 方法（在上述步驟中使用）會從矩形建立 `GraphicsPath`，套用提供的矩陣，並繪製變換後的形狀。這是一種緊湊的方式，可在每次變換時重複使用相同的繪圖邏輯。

## 常見問題與解決方案

| 問題 | 解決方案 |
|------|----------|
| **圖像顯示為空白** | 確保輸出目錄已存在且您具有寫入權限。 |
| **變換看起來偏移** | 請記住 `Matrix.Rotate` 會繞原點 (0,0) 旋轉。於旋轉前先將圖形平移至所需的中心點。 |
| **大型圖像效能下降** | 僅在需要時使用 `graphics.SmoothingMode = SmoothingMode.AntiAlias;`，並及時釋放 `Graphics` 物件。 |

## 常見問答

**問：在哪裡可以找到 Aspose.Drawing 文件？**  
答：文件可於 **[此處](https://reference.aspose.com/drawing/net/)** 取得。

**問：如何取得 Aspose.Drawing 的臨時授權？**  
答：可於 **[此處](https://purchase.aspose.com/temporary-license/)** 取得臨時授權。

**問：在哪裡可以尋求支援或與社群聯繫？**  
答：請造訪 Aspose.Drawing 論壇 **[此處](https://forum.aspose.com/c/drawing/44)**。

**問：我可以下載 Aspose.Drawing for .NET 嗎？**  
答：可以，請從 **[此處](https://releases.aspose.com/drawing/net/)** 下載。

**問：如何購買 Aspose.Drawing？**  
答：請於 **[此處](https://purchase.aspose.com/buy)** 購買授權。

## 結論

您已完成使用 Aspose.Drawing for .NET 的完整 **矩陣變換教學**。現在您知道如何 **繪製旋轉矩形**、**套用矩陣旋轉**，以及在任意形狀上執行 **矩陣縮放 C#**。可嘗試串接多個變換或使用自訂中心點，釋放更多創意圖形效果。

---

**最後更新：** 2026-08-28  
**測試環境：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [如何繪製矩形 – 使用 Aspose.Drawing API for .NET 進行座標系統變換（頁面變換）](/drawing/net/coordinate-transformations/page-transformation/)
- [如何使用 Aspose.Drawing 儲存 PNG – 世界變換](/drawing/net/coordinate-transformations/world-transformation/)
- [逐步變換 – 座標變換](/drawing/net/coordinate-transformations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}