---
date: 2026-11-04
description: 了解如何在 .NET 中使用 Aspose.Drawing API 繪製矩形圖形，同時執行 coordinate system transformation。本分步指南說明如何將
  inches 轉換為 pixels 並設定 page units。
keywords:
- how to draw rectangle
- convert inches to pixels
- how to set units
- save bitmap as png
- clear canvas background
lastmod: 2026-11-04
linktitle: Aspose.Drawing 的 coordinate system transformation
og_description: 了解如何在 Aspose.Drawing for .NET 中繪製矩形圖形，同時將 inches 轉換為 pixels 並設定 page
  units。遵循本分步指南，以實現精確的 page transformation。
og_image_alt: Developer guide showing rectangle drawing with coordinate system transformation
  in Aspose.Drawing
og_title: 如何使用 Aspose.Drawing for .NET 進行 page transformation 繪製矩形
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  headline: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  type: TechArticle
- description: Learn how to draw rectangle graphics while performing coordinate system
    transformation in .NET with Aspose.Drawing. This step‑by‑step guide shows how
    to convert inches to pixels and set page units.
  name: How to draw rectangle – coordinate system transformation (page transformation)
    in Aspose.Drawing for .NET
  steps:
  - name: Import namespaces
    text: The `using` statements give you access to the core drawing classes.
  - name: Create a bitmap
    text: '`Bitmap` represents an image in memory that you can draw onto. We start
      by creating a blank bitmap that will serve as the drawing surface. The pixel
      format `Format32bppPArgb` gives us high‑quality, premultiplied alpha support.'
  - name: Create a graphics object
    text: A `Graphics` object provides the drawing API for the bitmap. It’s the bridge
      between your code and the pixel buffer.
  - name: Clear the canvas
    text: Give the canvas a neutral background so the drawn shapes stand out. Here
      we fill it with a light gray.
  - name: Set the transformation (how to set unit)
    text: '`Graphics.PageUnit` specifies the unit of measure used for page coordinates.
      To map page coordinates to device pixels, set the `PageUnit` property. In this
      example we choose inches, but you could also use `GraphicsUnit.Millimeter`,
      `GraphicsUnit.Point`, or `GraphicsUnit.Pixel`. Setting the unit to i'
  - name: Draw a rectangle – draw rectangle graphics
    text: '`Pen` defines the color, width, and style of lines drawn on a graphics
      surface. Now we draw a rectangle using a thin blue pen. Because we switched
      to inches, the rectangle’s size and position are expressed in inches, making
      the code more readable for print‑oriented layouts.'
  - name: Save the image
    text: Finally, write the bitmap to a PNG file in the folder you specified earlier.
  type: HowTo
- questions:
  - answer: Yes, a free trial is available [here](https://releases.aspose.com/) .
    question: Can I use Aspose.Drawing for free?
  - answer: The full API reference is located [here](https://reference.aspose.com/drawing/net/)
      .
    question: Where can I find detailed documentation for Aspose.Drawing?
  - answer: Visit the [Aspose.Drawing Forum](https://forum.aspose.com/c/drawing/44)
      for community help and official assistance.
    question: How do I get support for Aspose.Drawing?
  - answer: Absolutely—obtain one [here](https://purchase.aspose.com/temporary-license/)
      .
    question: Is a temporary license available for Aspose.Drawing?
  - answer: You can buy it [here](https://purchase.aspose.com/buy) .
    question: Where can I purchase a full Aspose.Drawing license?
  type: FAQPage
second_title: Aspose.Drawing .NET API – alternative to System.Drawing.Common
tags:
- Aspose.Drawing
- coordinate transformation
- .NET graphics
- rectangle drawing
title: 如何在 Aspose.Drawing for .NET 中繪製矩形 – coordinate system transformation (page
  transformation)
url: /zh-hant/net/coordinate-transformations/page-transformation/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.Drawing for .NET 中繪製矩形 – 坐標系統轉換（頁面轉換）

## 介紹

在本教學中，您將學習 **如何繪製矩形** 圖形，同時使用 Aspose.Drawing for .NET 執行頁面層級的坐標系統轉換。無論您是在構建報表引擎、CAD 風格的草圖工具，或任何需要精確實際測量的應用程式，本指南都會一步步帶您完成——從建立位圖到儲存最終的 PNG。完成後，您將能熟練地將英吋轉換為像素、清除畫布背景，並設定列印就緒的頁面單位。

## 快速回答
- **什麼是坐標系統轉換？** 它將頁面層級的單位（例如英吋）映射到裝置層級的像素，使圖形在任何輸出裝置上正確縮放。  
- **為什麼選擇 Aspose.Drawing？** 它提供完整受管理、跨平台的圖形 API，取代 System.Drawing.Common，並支援超過 30 種影像格式。  
- **實作此範例需要多長時間？** 基本的矩形加頁面轉換大約需要 5‑10 分鐘。  
- **開發時需要授權嗎？** 開發階段可使用免費試用版；正式上線則需商業授權。  
- **支援哪些 .NET 執行環境？** .NET Framework 4.6+、.NET Core 3.1+，以及 .NET 5/6/7。

## Aspose.Drawing 是什麼？

Aspose.Drawing 是一套 .NET 圖形函式庫，提供 **裝置無關的 API** 來建立與操作點陣圖、向量與頁面層級的繪圖，且不依賴 GDI+。它支援 **30+ 影像格式**，可處理最高 **10,000 × 10,000 像素** 的圖像，同時保持低記憶體使用量。

## 為什麼在 Aspose.Drawing 中使用坐標系統轉換？

坐標系統轉換讓您以實際單位設計圖形，函式庫會自動處理任何輸出裝置的像素縮放。此方式保證 5 英吋的矩形在 300 DPI 印表機上正好列印出 5 英吋，且在 96 DPI 螢幕上呈現比例相同，避免手動換算錯誤。

- **裝置無關的設計：** 程式碼只寫一次，Aspose.Drawing 會在螢幕、印表機或 PDF 上自動縮放。  
- **精確繪圖：** 適用於技術圖、工程圖或任何需要精確測量的情境。  
- **跨平台可靠性：** 在 Windows、Linux、macOS 上表現一致，無 System.Drawing 的 GDI+ 限制。  
- **效能：** 在一般 2.5 GHz CPU 上，繪製 5 英吋矩形（300 DPI）耗時低於 **15 ms**，且函式庫在即時預覽情境下可達 **每秒 50 幀**。

## 前置條件

- **Aspose.Drawing 函式庫：** 從官方網站 [此處](https://releases.aspose.com/drawing/net/) 下載最新版本。  
- **IDE：** Visual Studio、Rider 或任何相容 .NET 的編輯器。  
- **輸出資料夾：** 在範例程式碼中將 `"Your Document Directory"` 替換為您希望儲存 PNG 的資料夾路徑。  
- **可選的 ASP.NET 支援：** 您可以將 NuGet 套件加入 ASP.NET Core 專案，使用相同的 API；模式遵循 .NET 函式庫的 **how to use aspnet** 方式。

## 如何使用頁面轉換繪製矩形？

載入空白位圖、將頁面單位設定為英吋，並使用細藍筆繪製矩形——只需幾行程式碼即可完成。`Graphics.PageUnit` 屬性告訴引擎將所有座標解讀為英吋，您可以以實際測量而非原始像素思考，函式庫會根據位圖的 DPI **自動將英吋轉換為像素**。

### 步驟 1：匯入命名空間

`using` 陳述式讓您取得核心繪圖類別的存取權。

```csharp
using System.Drawing;
```

### 步驟 2：建立位圖

`Bitmap` 是您繪圖的記憶體影像容器。它保存像素緩衝區，並提供儲存檔案的方法。建立位圖即定義畫布大小與像素格式。

```csharp
Bitmap bitmap = new Bitmap(1000, 800, System.Drawing.Imaging.PixelFormat.Format32bppPArgb);
```

### 步驟 3：建立 Graphics 物件

`Graphics` 為位圖提供繪圖表面。它將高階繪圖指令（線條、形狀、文字）轉換為底層位圖的像素操作。

```csharp
Graphics graphics = Graphics.FromImage(bitmap);
```

### 步驟 4：清除畫布背景

以中性色填滿畫布可確保圖形更為突出。此範例使用淡灰色作為背景，同時示範 **clear canvas background** 技巧。

```csharp
graphics.Clear(Color.FromKnownColor(KnownColor.Gray));
```

### 步驟 5：設定轉換（如何設定單位）

`Graphics.PageUnit` 指定頁面座標使用的測量單位。將其設為 `GraphicsUnit.Inch` 後，Aspose.Drawing 會根據位圖的 DPI（預設 96 DPI，列印時可設定為 300 DPI） **自動將英吋轉換為像素**。您亦可根據需求選擇 `GraphicsUnit.Millimeter`、`GraphicsUnit.Point` 或 `GraphicsUnit.Pixel`。

```csharp
graphics.PageUnit = GraphicsUnit.Inch;
```

### 步驟 6：繪製矩形 – 繪製矩形圖形

`Pen` 定義在繪圖表面上畫線的顏色、寬度與樣式。使用細藍筆，我們以英吋為單位繪製矩形，使程式碼在列印導向的版面配置中更易讀。

```csharp
Pen pen = new Pen(Color.FromKnownColor(KnownColor.Blue), 0.1f);
graphics.DrawRectangle(pen, 1, 1, 1, 1);
```

### 步驟 7：將位圖儲存為 PNG

最後，將位圖寫入先前指定的資料夾內的 PNG 檔。以 PNG 儲存可保留無損品質，且在各平台上廣受支援。

```csharp
bitmap.Save("Your Document Directory" + @"CoordinateSystemsTransformations\PageTransformation_out.png");
```

## 如何為印表機縮放圖形？

在繪圖前先將位圖的 DPI 設為目標印表機的解析度（例如 300 DPI）。如此會自動 **scale graphics printer** 輸出，使程式碼中的一英吋等同於列印頁面上的一英吋，而矩形的邏輯尺寸保持不變。呼叫 `bitmap.SetResolution(300, 300)` 後，同一矩形在紙張上會顯得較大，但尺寸仍精確。

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方式 |
|------|----------|----------|
| **未建立輸出檔案** | 路徑不正確或資料夾不存在 | 確認目標目錄已存在，或在儲存前呼叫 `Directory.CreateDirectory`。 |
| **矩形變形** | `PageUnit` 或 DPI 設定不匹配 | 確認 `graphics.PageUnit` 與預期單位相符，且位圖 DPI 已正確設定（預設 96 DPI，列印時 300 DPI）。 |
| **授權例外** | 生產環境未使用有效授權 | 在建立圖形物件前套用臨時或正式的 Aspose.Drawing 授權。 |

## 常見問答

**問：我可以免費使用 Aspose.Drawing 嗎？**  
**答：** 可以，免費試用版可在 [此處](https://releases.aspose.com/) 取得。

**問：在哪裡可以找到 Aspose.Drawing 的詳細文件？**  
**答：** 完整的 API 參考位於 [此處](https://reference.aspose.com/drawing/net/)。

**問：如何取得 Aspose.Drawing 的支援？**  
**答：** 前往 [Aspose.Drawing 論壇](https://forum.aspose.com/c/drawing/44) 取得社群協助與官方支援。

**問：Aspose.Drawing 是否提供臨時授權？**  
**答：** 當然可以——請於 [此處](https://purchase.aspose.com/temporary-license/) 取得。

**問：在哪裡可以購買完整的 Aspose.Drawing 授權？**  
**答：** 您可於 [此處](https://purchase.aspose.com/buy) 購買。

## 結論

現在您已掌握 **如何繪製矩形** 圖形，並使用 Aspose.Drawing for .NET 進行頁面層級的坐標系統轉換。透過將頁面單位設為英吋、清除畫布背景，並將結果儲存為 PNG，您即可獲得精確、裝置無關的輸出，適用於螢幕顯示與高解析度列印。可進一步嘗試其他單位、旋轉或自訂坐標原點，以開啟更強大的繪圖情境。

---

**最後更新：** 2026-11-04  
**測試環境：** Aspose.Drawing 24.12 for .NET  
**作者：** Aspose

## 相關教學

- [如何在 Aspose.Drawing for .NET 中設定單位 – 測量單位](/drawing/net/coordinate-transformations/units-of-measure/)
- [全域轉換](/drawing/net/coordinate-transformations/global-transformation/)
- [逐步轉換 – 坐標系統轉換](/drawing/net/coordinate-transformations/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}