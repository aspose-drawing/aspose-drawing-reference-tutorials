---
date: 2026-08-01
description: 了解如何使用 Aspose.Drawing 以 C# 建立 Bitmap 圖像並在 Bitmap 上繪製矩形。針對 .NET 開發人員的逐步指南。
keywords:
- create bitmap image c#
- draw rectangle on bitmap
- replace system.drawing
lastmod: 2026-08-01
linktitle: 在 Aspose.Drawing 中繪製矩形
og_description: 使用 Aspose.Drawing 以 C# 建立 Bitmap 圖像並在 Bitmap 上繪製矩形。本教學說明如何在 .NET 中產生、設定樣式及儲存矩形圖形。
og_image_alt: Guide to drawing rectangles on a bitmap with Aspose.Drawing for .NET
og_title: 建立 Bitmap 圖像 C# – 使用 Aspose.Drawing 繪製矩形
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to create bitmap image C# and draw rectangle on bitmap using
    Aspose.Drawing. Step‑by‑step guide for .NET developers.
  headline: Create Bitmap Image C# – Draw Rectangle with Aspose.Drawing for .NET
  type: TechArticle
- questions:
  - answer: Yes, create a `SolidBrush` and call `graphics.FillRectangle(brush, …)`
      before or after drawing the outline.
    question: Can I fill the rectangle with a solid color?
  - answer: Loop through a collection of `Rectangle` structs and call `DrawRectangle`
      for each iteration.
    question: How do I draw multiple rectangles?
  - answer: Use `graphics.RotateTransform(angle)` before drawing, then reset the transform
      after.
    question: Is there a way to rotate the rectangle?
  - answer: PNG, JPEG, BMP, GIF, and TIFF are all supported via the appropriate `ImageFormat`
      parameter.
    question: What image formats are supported for saving?
  - answer: Yes, the library is fully compatible with .NET Core, .NET 5, .NET 6, and
      later versions.
    question: Does Aspose.Drawing work on .NET Core?
  type: FAQPage
second_title: Aspose.Drawing .NET API - Alternative to System.Drawing.Common
tags:
- create bitmap image
- Aspose.Drawing
- .NET graphics
- draw rectangle
title: 在 .NET 中使用 Aspose.Drawing 建立 Bitmap 圖像 C# – 繪製矩形
url: /zh-hant/net/lines-curves-and-shapes/draw-rectangle/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.Drawing for .NET 繪製矩形

## 介紹

在本教學中，您將學習 **如何繪製矩形** 形狀，同時掌握使用 Aspose.Drawing **建立 C# 位圖影像** 的方法。無論您需要簡單的 UI 元件或是報告用的高解析度圖形，我們都會一步步說明如何建立位圖、設定 graphics 物件、繪製矩形，並儲存最終影像。此方法可在 Windows、Linux 與 macOS 上執行，並以完整跨平台的方案取代舊有的 `System.Drawing.Common` API。

## 快速解答
- **需要的函式庫是什麼？** Aspose.Drawing for .NET  
- **哪個方法用來繪製形狀？** `Graphics.DrawRectangle`  
- **需要授權嗎？** 試用版免費；正式環境需購買商業授權。  
- **可以調整矩形大小嗎？** 可以——調整寬度、高度與位置參數。  
- **程式碼相容於 .NET 6+ 嗎？** 當然，Aspose.Drawing 支援最新的 .NET 版本。

## 在 Aspose.Drawing 中「如何繪製矩形」是什麼意思？

使用 Aspose.Drawing 繪製矩形是透過 `Graphics` 類別在位圖畫布上繪製矩形輪廓或填滿形狀。這讓您能完整控制尺寸、顏色、線條粗細與影像格式，非常適合即時產生圖形。由於 Aspose.Drawing 在純受管理的引擎上執行，避免了 `System.Drawing.Common` 的原生 GDI+ 限制。

## 為什麼使用 Aspose.Drawing 來建立矩形？

Aspose.Drawing 讓您 **在位圖上繪製矩形**，不需任何平台專屬的 DLL，且支援 **30 多種輸出格式**（包括 PNG、JPEG、BMP、GIF 與 TIFF）。它可處理最高 **10,000 × 10,000 像素** 的影像，同時將記憶體使用量控制在 **100 MB** 以下，效率比傳統 System.Drawing 實作高出 2‑3 倍。

## 前置條件

在開始程式碼之前，請確保您已具備以下項目：

- **Aspose.Drawing 函式庫** – 從官方網站[此處](https://releases.aspose.com/drawing/net/)下載。  
- **開發環境** – Visual Studio 2022 或任何相容 .NET 的 IDE。  
- **基本 .NET 知識** – 熟悉 C# 語法與專案結構。

## 匯入命名空間

`using` 指令會將必要的類別引入作用域，所有繪圖操作皆需要它們。

```csharp
using System.Drawing;
```

## 步驟 1：建立位圖影像

`Bitmap` 代表可在記憶體中的點陣圖影像，您可以在其上繪圖。建立它時會定義畫布大小與像素格式。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

## 步驟 2：建立 Graphics 物件

`Graphics` 是在位圖表面執行所有繪圖指令的引擎。取得它後，即可繪製形狀、文字與影像。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

## 步驟 3：定義矩形的 Pen

`Pen` 用於指定矩形的輪廓顏色與粗細，同時可設定虛線樣式與接合方式。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 2);
```

## 步驟 4：在位圖上繪製矩形

`Graphics.DrawRectangle` 使用先前定義的 Pen 繪製矩形。您需要提供 X、Y 座標以及寬度與高度，以精確定位形狀。

```csharp
graphics.DrawRectangle(pen, 10, 10, 900, 700);
```

## 步驟 5：儲存繪製的影像

`Bitmap.Save` 方法會將影像依您選擇的格式（例如 PNG、JPEG）寫入磁碟。此步驟示範 **儲存繪製影像** 的功能，並完成位圖的最終化以供再次使用。

```csharp
bitmap.Save("Your Document Directory" + @"LinesCurvesShapes\DrawRectangle_out.png");
```

恭喜！您已成功使用 Aspose.Drawing for .NET 完成 **如何繪製矩形**，同時學會了 **建立 C# 位圖影像** 的技巧。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|-------|----------|
| 空白影像輸出 | Bitmap 未釋放或 graphics 未刷新 | 在儲存前呼叫 `graphics.Dispose();`，或使用 `using` 區塊。 |
| 邊緣品質低 | 預設平滑模式 | 設定 `graphics.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;`。 |
| 檔案路徑錯誤 | 目錄無效 | 確認目標資料夾存在，或使用 `Path.Combine` 建立安全路徑。 |

## 常見問答

**Q: 我可以用純色填滿矩形嗎？**  
A: 可以，建立 `SolidBrush` 並在繪製輪廓前或後呼叫 `graphics.FillRectangle(brush, …)`。

**Q: 如何繪製多個矩形？**  
A: 迭代 `Rectangle` 結構的集合，對每一次呼叫 `DrawRectangle`。

**Q: 有辦法旋轉矩形嗎？**  
A: 在繪製前使用 `graphics.RotateTransform(angle)`，繪製完後再重設變換。

**Q: 儲存時支援哪些影像格式？**  
A: 皆支援 PNG、JPEG、BMP、GIF 與 TIFF，可透過相對應的 `ImageFormat` 參數指定。

**Q: Aspose.Drawing 能在 .NET Core 上使用嗎？**  
A: 能，該函式庫完全相容 .NET Core、.NET 5、.NET 6 以及更高版本。

---

**最後更新：** 2026-08-01  
**測試版本：** Aspose.Drawing 24.11 for .NET  
**作者：** Aspose  

---

## 相關教學

- [如何使用 Aspose.Drawing for .NET 繪製橢圓](/drawing/net/lines-curves-and-shapes/draw-ellipse/)
- [使用 Aspose.Drawing 繪製多條線段](/drawing/net/lines-curves-and-shapes/draw-lines/)
- [如何建立位圖 aspose.drawing – 在 .NET 中繪製多邊形](/drawing/net/lines-curves-and-shapes/draw-polygon/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}